<script>
    let clicked = false;
    let tiempo = 0;
    function iniciarTemporizador() {
        let tiempoTranscurrido = 0;
        const temporizador = setInterval(() => {
            tiempo += 1;
            tiempo.toFixed(1);
        }, 1000);
        return temporizador;
    }
</script>

<style>
      .tareas {
    padding: 10px;
    border: solid 1px #d6d6d6;
    border-radius: 5px;
    margin: 5px 0;
    width: 200px;
    height: 100px;
    position: relative;
  }
  button {
    width: 30px;
    height: 30px;
    display:flex;
    justify-content:center;
    align-items:center;
    position: absolute;
    border-radius: 50%;
    background-color: white;
    border: 2px solid #000;
    cursor: pointer;
    & i {
      font-size: 1.2rem;
      line-height: 0px;
      pointer-events: none;
    }
    &.finalizar {
      top: 2px;
      right: 2px;
      width: 20px;
      height: 20px;
      border-radius: 0px;
      border: none;
      & i {
        color: green;
        font-size: 1rem;
        opacity: 0.6;
      }
    }
    &.temporizador {
      width: 30px;
      height: 30px;
      border-radius: 50%;
      border: 1pz solid #fff;
      bottom: 0px;
      left: 0px;
      &.active {
        background-color: #000;
        color: white;
        animation: activeItem 1s infinite;
        & i {
            color: white;
        }
      }
      & i {
        color: blue;
        font-size: 1rem;
        opacity: 0.6;
      }
    }

  }
  .tiempo-transcurrido {
    font-size: 2rem;
    font-weight: bold;
    text-align: center;
    margin-top: 10px;
    position: absolute;
    right: 10px;
    bottom: 4px;
    display: none;
    &.active {
        display: block;
    }
  }

  @keyframes activeItem {
    0% {
      transform: scale(1);
    }
    50% {
      transform: scale(1.2);
    }
    100% {
      transform: scale(1);
    }
  }
</style>

<div class="tareas">
    <h3>Revisión de correo electrónico.</h3>
    <p class:active={ clicked } class="tiempo-transcurrido">{tiempo}</p>
    <button aria-label="Boton de finalizada" class="finalizar"><i class="fi fi-rr-progress-complete"></i></button>
    <button on:click|once={() => { clicked = true; iniciarTemporizador()}} class:active={ clicked } aria-label="Iniciar temporizador" class="temporizador"><i class="fi fi-rr-play"></i></button>
</div>