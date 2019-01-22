<template>
  <div id="online-friends">
    <h2>Online Friends</h2>
    <div v-for="(friend, index) in friends" :key="index">
      <span @click="unfriend(friend.name)" v-if="friend.online">{{ friend.name }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'OnlineFriends',
  props: ['friends'],
  data() {
    return {
      
    }
  },
  methods: {
    unfriend(name) {
      this.$emit('delete', { name })
    }
  }
}
</script>

<style>

</style>
