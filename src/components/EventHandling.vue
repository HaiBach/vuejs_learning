<template>
  <div id="event-handling">
    <p>{{ message }}</p>
    <button v-on:click="reserveMessage">Reverse message</button>
  </div>
</template>


<script setup>
  const EventHandling = {
    data() {
      return {
        message: 'Xin chào mọi người!'
      }
    },
    methods: {
      reserveMessage() {
        this.message = this.message
          .split('')
          .reverse()
          .join('')
      }
    }
  }

  // Vue.createApp(EventHandling).moute('#event-handling') 
</script>