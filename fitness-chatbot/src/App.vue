<template>
  <div id="app">
    <div class="chat-side">
      <ChatBox />
    </div>
    <div class="notes-side">
      <LongTermMemory />
    </div>
  </div>
</template>

<script setup>
import ChatBox from './components/ChatBox.vue';
import LongTermMemory from './components/LongTermMemory.vue';
</script>

<style>
  html, body {
    height: 100%;
    width: 100%;
    margin: 0;
    padding: 0;
  }

  #app {
    display: flex;
    justify-content: center;
    gap: 2rem;
    min-width: 100%;
    min-height: 100%;
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  .chat-side {
    flex: 1;
  }
  .notes-side {
    flex: 1;
  }
</style>
