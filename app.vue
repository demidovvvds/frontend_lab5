<template>
  <div class="app-container">
    <h1>100 vue clickers</h1>
    <div class="clickers-grid">
      <Clicker 
        v-for="n in 100" 
        :key="n" 
        :amount="10" 
        @button-clicked="handleAlert(n)"
      >
        <button class="custom-button">tap on me (clicker {{ n }})</button>
      </Clicker>
    </div>
  </div>
</template>

<script setup>
import Clicker from './clicker.vue'

const handleAlert = (n) => {
  alert(`clicker ${n} clicked!`)
}
</script>

<style>
.app-container {
  font-family: Arial, sans-serif;
  padding: 20px;
}
.clickers-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}
.custom-button {
  background-color: #42b883;
  color: white;
  border: none;
  padding: 8px 12px;
  border-radius: 4px;
  font-size: 14px;
}
.custom-button:hover {
  background-color: #33a06f;
}
</style>