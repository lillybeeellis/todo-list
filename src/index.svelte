<script>
let newTodo =""
let todos = [
    "wash the dog",
    "vaccume the carpet"

]

function addTodo(){
    //add the newTodo to the end of the todos array
    todos = [...todos, newTodo]
}

</script>


<h1 class="title">To-do list</h1>

<label>
Tdo:
<input type="text" bind:value={newTodo}> 
</label>


<button on:click={addTodo}>Add</button>


<ul class="list">
{#each todos as todo}
 <li class="list-item">{todo}</li>
 {/each}
</ul>