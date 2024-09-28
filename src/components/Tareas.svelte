<script>

  import { count } from "../stores/tasks";

  function alerta(){
    count.update(n => n + 1);
  }

</script>

<button aria-label="Prueba" on:click={alerta}>Pruebas de clic</button>