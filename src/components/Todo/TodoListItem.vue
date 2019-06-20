<template>
  <div>
    <ul>
      <li v-for="(todo, index) in todos" :key="index">
        <slot name="todo" :todo="todo">
          {{index}}
        </slot>
      </li>
    </ul>
    <slot :todoObject="todoObject">
      {{todoObject.id}}
    </slot>
  </div>
</template>

<script>
export default {
  name: "TodoListItem",
  data() {
    return {
      todoObject: { name: "todo", id: 1 },
      todos: ["todo one", "todo two"]
    };
  }
};
</script>

<style lang="scss" scoped>
</style>