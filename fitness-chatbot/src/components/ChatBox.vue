<template>
  <div class="chat-container">
    <div class="chat-history">
      <p v-for="(message, index) in chatHistory" :key="index" class="chat-message">
        {{message}}
      </p>
    </div>
    <div class="chat-footer">
      <input class="chat-input" v-model="userInput" placeholder="Enter your message..." />
      <button class="chat-submit" @click="handleSubmit">Submit</button>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const chatHistory = ref([]);
const userInput = ref('');

const handleSubmit = () => {
  chatHistory.value.push(userInput.value);
  userInput.value = '';
}
</script>

<style scoped>
.chat-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 1em;
  height: 80%;
  box-sizing: border-box;
  border: solid #5B6DCD 10px;
}

.chat-history {
  overflow-y: auto;
  flex-grow: 1;
}

.chat-message {
  background-color: #e5e5e5;
  padding: 0.5em;
  border-radius: 8px;
  margin-bottom: 1em;
}

.chat-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.chat-input {
  flex-grow: 1;
  padding: 0.5em;
  border-radius: 8px;
  border: none;
  margin-right: 1em;
}

.chat-submit {
  padding: 0.5em 1em;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 8px;
  cursor: pointer;
}

.chat-submit:hover {
  background-color: #45a049;
}

</style>