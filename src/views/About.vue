<template>
  <div class="about">
    <h1>This is an about page</h1>
    <user-list/>
  </div>
</template>

<script>
import UserList from "../components/UserList"
export default {
  name: "About",
  components: {
    UserList
  }
}
</script>
