<script>
  import { data } from '../data.js'
  import Todo from "$lib/components/Todo.svelte"
  let todos = $state(data)
</script>

<div id="list-wrapper">
  {#each todos as {id, text, done}}
    <Todo {id} {text} {done}/>
  {/each}
</div>

<style>
  #list-wrapper {
    display: flex;
    flex-direction: column;
    margin: auto;
    width: 70%;
  }
</style>



