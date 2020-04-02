<script>
  let newTodo = "";
  let place = 0;
  let todos = ["wash the dog", "vaccume the carpet", "Do homework", "eat"];

  function addTodo() {
    //add the newTodo to the end of the todos array
    todos = [...todos, newTodo];
  }

  function removeTodo(index) {
    //remove the todo at index from the todos array
    todos = [...todos.slice(0, index), todos.slice(index + 1)];
  }
</script>

<h1 class="title">To-do list</h1>

<label>
  Tdo:
  <input type="text" bind:value={newTodo} />
</label>

<button on:click={addTodo}>Add</button>

<label>
  Remove:
  <input type="number" bind:value={place} />
</label>


<button
  on:click={() => {
    removeTodo(place);
  }}>
  Remove
</button>

<ul class="list">
  {#each todos as todo, index}
    <li class="list-item">{index}: {todo}</li>
  {/each}
</ul>
