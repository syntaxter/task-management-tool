<script>
    import {count} from '../stores/tasks.js';

    let contadorEstado = 0;

    count.subscribe(value => {
        contadorEstado = value;
    });
</script>

<style>
    * {margin: 0px;padding: 0px;box-sizing: border-box;}
    .main-title {
        color: #333;
        font-size: 1rem;
        text-align: center;
        font-weight: 500;
        background-color: #d6d6d6;
        display: inline-block;
        color: #000000;
        padding: 5px 10px;
        border-bottom-right-radius: 10px;
        margin-right: 20px;
    }
    a {
        text-decoration: none;
        display: inline-flex;
        align-items: center;
    }
</style>

<h1 class="main-title">
    Administrador de tareas
</h1>

<a href="https://paypal.me/syntaxter">
    Donar para mantener el proyecto Por Paypal
    <img width="20px" src="https://www.paypalobjects.com/marketing/web/logos/paypal-mark-color_new.svg" alt="">
</a>