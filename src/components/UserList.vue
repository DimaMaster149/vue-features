<template>
  <div class="main" @click="deleteUser($event)">
    <user-list-item v-for="(user, index) in users" :user="user" :key="index"/>
  </div>
</template>

<script>
import UserListItem from "./UserListItem";
import axios from "axios"
export default {
  name: "UserList",
  components: {
    UserListItem
  },
  data() {
    return {
      users: []
    };
  },
  created() {
    axios.get('https://randomuser.me/api/').then(res => {
      this.users.push(res.data.results[0]);
      console.log(this.users)
    })
  },
  methods: {
    deleteUser($event) {
      console.log($event, "event");
      let attr = $event.target.getAttribute('data-id');
      console.log(attr, 'attr')
    }
  }
};
</script>

<style lang="scss" scoped>
</style>