<template>
  <div>
    <todo-list-item >
      <template v-slot:todo="todoSlotProps">
        {{todoSlotProps.todo}}
      </template>

      <template v-slot="slotProps">
        {{slotProps.todoObject.name}}
      </template>
      
    </todo-list-item>
  </div>
</template>

<script>
import TodoListItem from "./TodoListItem";

export default {
  name: "TodoList",
  components: { TodoListItem }
};
</script>

<style lang="scss" scoped>
</style>