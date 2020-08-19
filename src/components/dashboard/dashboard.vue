<template>
  <div>
    <vue-countdown v-on:time-expire="handleTimeExpire" :seconds="3600" :start="start"></vue-countdown>

    <button v-on:click="startTimer">Start timer</button>
  </div>
</template>

<script>
import VueCountdown from '@dmaksimovic/vue-countdown';

export default {
  name: 'my-component',
  data () {
    return {
      start: false
    };
  },
  components: {
    'vue-countdown': VueCountdown
  },
  methods: {
    handleTimeExpire () {
      alert('Time is up!')
    },
    startTimer () {
      this.start = true
    }
  }
}

</script>
