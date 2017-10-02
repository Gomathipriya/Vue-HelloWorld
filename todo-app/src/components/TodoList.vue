<template>
    <div>
        <p> Completed Tasks: {{todos.filter(todo =>{return todo.done === true}).length}}</p>
    </div>
</template>

<script type="text/javascript>
    export default{
        props: ['todos'],
    };
</script>

<style>
</style>