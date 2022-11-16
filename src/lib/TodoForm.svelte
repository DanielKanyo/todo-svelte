<script lang="ts">
    import { todos } from "./TodoStore";

    let todo: string = "";

    const createTodoItem = (e: Event) => {
        e.preventDefault();

        todos.update((todos) => {
            return [todo, ...todos];
        });

        todo = "";
    };
</script>

<form>
    <div class="form">
        <input type="text" bind:value={todo} />
        <button on:click={createTodoItem}>Add Item</button>
    </div>
</form>

<style>
    .form {
        display: flex;
    }

    input {
        width: 100%;
    }

    button {
        min-width: 100px;
        margin-left: 10px;
    }
</style>
