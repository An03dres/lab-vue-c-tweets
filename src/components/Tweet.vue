<template>
  <div class="tweet">
    <ProfileImage :image="tweet.user.image" />
    <div class="body">
      <div class="top">
        <User :userData="tweet.user" />
        <Timestamp :time="tweet.timestamp" />
        <span class="more"><i class="fas fa-ellipsis-h"></i></span>
      </div>
      <Message :message="tweet.message" />
      <Actions />
    </div>
  </div>
</template>

<script setup>
import ProfileImage from './ProfileImage.vue'
import User from './User.vue'
import Timestamp from './Timestamp.vue'
import Message from './Message.vue'
import Actions from './Actions.vue'

defineProps({
  tweet: Object
});
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
