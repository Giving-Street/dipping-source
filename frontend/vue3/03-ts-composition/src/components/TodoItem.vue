<script setup lang="ts">
// https://vuejs.org/guide/components/props.html#prop-validation
const props = defineProps({
    title: String,
    description: {
        type: String,
        required: false
    },
    isDone: Boolean
})

</script>

<template>
  <div class="todo-item">
    <div class="todo-item-title">
        {{ props.title }}
    </div>
    <div class="todo-item-description">
        {{props.description}}
    </div>
    <div class="todo-item-checkbox">
        <div class="todo-item-checked" v-if="props.isDone">
            done
        </div>
        <div class="todo-item-checked" v-else>
            not done
        </div>
    </div>
  </div>
</template>