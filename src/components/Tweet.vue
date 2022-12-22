<template>
  <div class="tweet">
    <ProfileImage :image="tweet.user.image"></ProfileImage>
    <div class="body">
      <div class="top">
        <User :user="tweet.user" ></User>
        <Timestamp :timestamp="tweet.timestamp"></Timestamp>
      </div>
      <Message :message="tweet.message"></Message>
      <Actions></Actions>
    </div>
    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>
<script>

import ProfileImage from "./ProfileImage.vue";
import User from "./User.vue"
import Message from "./Message.vue"
import Actions from "./Actions.vue"
import Timestamp from "./Timestamp.vue"

export default{
  props: {
    tweet : {
      type: Object,
    },
    },
  components : {
    ProfileImage,
    User,
    Message,
    Actions,
    Timestamp

  }

  }

</script>
<style scoped>
a {
  color: #42b983;
}
</style>