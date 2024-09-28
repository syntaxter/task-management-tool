<script>
    import {count} from '../stores/tasks.js';

    let contadorEstado = 0;

    count.subscribe(value => {
        contadorEstado = value;
    });
</script>

<h1>Prueba</h1>

<p>contador es igual a {contadorEstado}</p>