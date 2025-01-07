<script setup lang="ts">

const message = "test"
const rawHtml = `<span style="color: red">This should be red.</span>`
const num = 3
const items = [
  {id: 1, name: "john"},
  {id: 2, name: "test"},
]

</script>

<template>
  <div class="about">
    <h1>This is an about page</h1>
    <div v-text="message"></div>
    <button v-tooltip='"This is a button"'>Hover Me</button>
    <p>Using text interpolation: {{ rawHtml }}</p>
    <p>Using v-html directive: <span v-html="rawHtml"></span></p>
    <p v-if="num === 1">Number is 1</p>
    <p v-else-if="num === 2">Number is 2</p>
    <p v-else>Number is neither 1 nor 2</p>

    <ul>
      <p>for loop</p>
      <li v-for="item in items" :key="item.id">{{ item.name }}</li>
    </ul>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
    flex-direction: column;
  }
}
</style>
