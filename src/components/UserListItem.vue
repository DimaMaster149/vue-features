<template>
  <div>
    {{user.name}}
    <button :data-id="user.id.name"> delete </button>
  </div>
</template>

<script>
export default {
  name: "UserListItem",
  props: {
    user: {
      type: Object,
      required: true
    }
  }
};
</script>
