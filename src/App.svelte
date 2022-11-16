<script lang="ts">
    import TodoForm from "./lib/TodoForm.svelte";
    import TodoList from "./lib/TodoList.svelte";
</script>

<div class="todo-list-container">
    <h1>Todo List</h1>
    <TodoForm />
    <TodoList />
</div>

<style>
    .todo-list-container {
        margin: 0 auto;
        width: 500px;
        padding: 15px 0;
        text-align: center;
    }
</style>
