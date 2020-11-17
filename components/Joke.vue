<template>
  <div>
    <div class="joke-container">
      <div class="joke-content">
        <h1>{{ this.id }}</h1>
        <span>{{ this.joke }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['joke', 'id'],
}
</script>

<style>
.joke-container {
  background-color: rgb(155, 224, 115);
  overflow: visible;
  color: aliceblue;
  text-align: center;
  align-content: center;
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
