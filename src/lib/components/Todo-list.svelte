<script>
  import { v4 as uuidv4 } from 'uuid';
  import Todo from "./Todo.svelte"
  let todos = $state([
    {
      id: uuidv4(),
      text: "todo1",
      done: false
    },
    {
      id: uuidv4(),
      text: "todo2",
      done: true
    }
  ])
</script>

{#each todos as {id, text, done}}
  <Todo {id} {text} {done}/>
{/each}


