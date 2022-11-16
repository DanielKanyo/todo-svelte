<script lang="ts">
    import { todos } from "./TodoStore";

    const removeItem = (index: number) => {
        todos.update((todos) => {
            todos.splice(index, 1);

            return todos;
        });
    }
</script>

<div class="todo-list">
    {#each $todos as todo, i}
        <div class="todo-item">
            <div>{todo}</div>
            <button on:click={() => removeItem(i)}>X</button>
        </div>
    {/each}
</div>

<style>
    .todo-list {
        padding: 15px 0;
        text-align: left;
    }

    .todo-item {
        display: flex;
        justify-content: space-between;
        border: 1px solid grey;
        margin-bottom: 5px;
        padding: 5px 10px;
    }
</style>
