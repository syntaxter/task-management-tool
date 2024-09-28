<script>
  import TaskItem from "./TaskItem.svelte";

</script>
<style>
  .container {
    margin: 10px 20px;
  }
  .lista-de-tareas {
    border: solid 2px #d6d6d6;
    margin-top: 10px;
    padding: 10px;
    border-radius: 10px;
    display:flex;
    align-items:center;
    gap: 10px;
  } 
</style>

<div class="container">
  <h2>
    Lista de tareas
  </h2>
  <div class="lista-de-tareas">
    {#each {length: 3} as _, i}
      <TaskItem />
  {/each}

  </div>
</div>


