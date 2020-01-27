<template>
  <!-- PART 4: Add your code here -->
  <div>
    {{name}}
    <Counter :initialCount= 'episodes_seen'/>
  </div>
</template>

<script>
// PART 4: Add your code here
import Counter from "./Counter.vue";
export default {
  props:['id','name','episodes_seen'],
  components:{
    Counter
  }
};
</script>

<style>
</style>
