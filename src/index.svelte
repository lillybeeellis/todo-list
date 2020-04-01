<script>
let todos = [
    "wash the dog",
    "vaccume the carpet"

]
</script>


<h1 class="title">To-do list</h1>

<ul class="list">
{#each todos as todo}
 <li class="list-item">{todo}</li>
 {/each}
</ul>