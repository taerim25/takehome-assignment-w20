<template>
  <div>
    <p>I'm a Counter!</p>
    <button v-on:click="count += 1">Add 1</button>
    <button v-on:click="count -= 1">Subtract 1</button>
    <p>Current count: {{count}}</p>
  </div>  
</template>

<script>
export default {
  props:{
    initialCount: {
      type:Number
    }
  },
  data() {
    return {
      count: this.initialCount
    };
  }
};
</script>

<style>
</style>

