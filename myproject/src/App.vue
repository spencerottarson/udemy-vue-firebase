<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <Navbar />
    <Blogs />
  </div>
</template>

<script>
import Navbar from './Navbar'
import AllFriends from './AllFriends'
import OnlineFriends from './OnlineFriends'
import Blogs from './Blogs'

export default {
  name: 'app',
  components: {
    Navbar,
    OnlineFriends,
    AllFriends,
    Blogs
  },
  data () {
    return {
      title: 'My first Vue app, Wooo :)',
      friends: [
        { name: 'Spencer', online: true },
        { name: 'Amber', online: true },
        { name: 'Parker', online: true },
        { name: 'Diane', online: false },
        { name: 'Jack', online: false }
      ]
    }
  },
  methods: {
    deleteFriend(payload) {
      this.friends = this.friends.filter(friend => {
        return friend.name != payload.name
      })
    }
  }
}
</script>

<style>
h1{
  color: #444;
  font-weight: normal;
  text-align: center;
}
</style>
