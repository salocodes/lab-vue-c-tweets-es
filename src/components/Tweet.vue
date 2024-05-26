<script setup>
import Profileimage from "./Profileimage.vue"
import User from "./User.vue"
import Timestamp from "./Timestamp.vue"
import Message from "./Message.vue"
import Actions from "./Actions.vue"

defineProps({
  tweet: Object,
})
</script>

<template>
  <div class="tweet">
    <Profileimage :image="tweet.user.image" />

    <div class="body">
      <div class="top">
        <User :userData="tweet.user" />
        <Timestamp :time="tweet.timestamp" />
      </div>

      <Message :message="tweet.message" />
      <Actions />
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>