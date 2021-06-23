<template>
  <div class="home">
    <tweet v-for="tweet in tweets" 
    :key="tweet._id"
    :tweet="tweet"
    />
  </div>
</template>

<script>
// @ is an alias to /src
import {ref} from 'vue'
import vtweets from '@/vtweets.js'
import Tweet from '../components/Tweet.vue'
export default {
  components: { Tweet },
  setup() {
    const tweets = ref(vtweets)

    return {
      tweets
    }
  }
}
</script>
