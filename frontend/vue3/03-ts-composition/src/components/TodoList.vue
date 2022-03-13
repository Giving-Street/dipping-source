<script setup lang="ts">
// https://vuejs.org/guide/essentials/reactivity-fundamentals.html#declaring-methods
import { reactive } from 'vue';
import TodoItem from './TodoItem.vue';

export type TodoItem = {
    title: string
    description?: string
    isDone: boolean
}
const todoItems: TodoItem[] = reactive([
    {
        title: "foo",
        isDone: false
    },
    {
        title: "bar",
        isDone: false
    },
    {
        title: "baz",
        description: "description",
        isDone: false
    },
])
</script>

<template>
<div class="todo-items" v-for="(todoItem, todoItemKey) in todoItems" :key="todoItemKey">
    <TodoItem :title="todoItem.title" :is-done="todoItem.isDone"/>
</div>
</template>