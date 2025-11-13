<script setup>
import {ref} from 'vue'

const message = ref("Hello, World!")

function reverseMessage() {
  message.value = message.value.split('').reverse().join('')
}
</script>

<template>
  <h1>{{ message }}</h1>

  <button @click="reverseMessage">Reverse Message</button>
  <button @click="message += '!'">Append !</button>
  <button @click="message = 'Hello, World!'">Reset</button>

  <a href="https://baxter.com" target = "_blank">Baxter</a>
</template>

<style>
body {
  background-color: coral;
}

button, a {
  display: block;
  margin-bottom: 1em;
}
</style>