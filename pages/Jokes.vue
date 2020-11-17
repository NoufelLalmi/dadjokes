/* eslint-disable */
<template>
  <div class="container">
    <div v-for="joke in jokes" :key="joke.id">
      <Joke :id="joke.id" :joke="joke.joke"></Joke>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import Joke from '~/components/Joke.vue'
export default {
  components: { Joke },
  data() {
    return {
      jokes: [],
    }
  },

  async created() {
    const config = {
      headers: {
        Accept: 'application/json',
      },
    }
    try {
      const res = await axios.get('https://icanhazdadjoke.com/search', config)
      this.jokes = res.data.results
    } catch (error) {
      console.log(error)
    }
  },
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: block;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
