<script>
  let { id, text, done } = $props()
  
  const handleClick = e => {
    done = !done
    console.log("clicked:", e.target);
  }
</script>

<!-- svelte-ignore a11y_click_events_have_key_events -->
<!-- svelte-ignore a11y_no_static_element_interactions -->
 <div id="grandpa">
  <div id={id} onclick={handleClick} class="{done ? "done" : "not-done"} wrapper">
    <p>{text}</p>
  </div>
 </div>


<style>
  #grandpa {
    height: 100px;
    width: auto;
  }
  .wrapper {
    font-family: sans-serif;
    border: 1px solid black;
    border-radius: 1rem;
    padding: 1rem;
    position: absolute;
  }

  .done {
    margin-left: 5px;
    margin-top: 5px;
    text-decoration: line-through; 
  }
  .not-done {
    box-shadow: 5px 5px 0px 1px rgba(0,0,0,1);
  }
</style>