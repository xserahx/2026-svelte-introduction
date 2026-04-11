<script>
    let todos = $state([
        { title: "Assignment 1", done: false },
        { title: "<i>Assignment 2</i>", done: false },
        { title: "Assignment 3", done: false }
    ]);

    let groceries = $state([
        { title: "Milk", done: false },
        { title: "<b>Bread</b>", done: false },
        { title: "Eggs", done: false }
    ]);
</script>

{#snippet todoItem(todo)}
    <li>
        <label>
            <input type="checkbox" bind:checked={todo.done}>
            {todo.title}
        </label>
    </li>
{/snippet}

<h3>Todo List</h3>

<ul>
    {#each todos as todo}
        {@render todoItem(todo)}
    {/each}
</ul>

<h3>Grocery List</h3>

<ul>
    {#each groceries as grocery}
        {@render todoItem(grocery)}
    {/each}
</ul>

<style>
    label :global {
       i { color: green; }
       b { color: blue;  }
    }
</style>