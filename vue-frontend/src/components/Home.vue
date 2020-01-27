<template>
  <div>
    <!-- PART 1: Pass in a "complete" prop here -->
    <Instructions complete=true />
    <!-- PART 4: Modify the Show component to accept all of these props -->
    <Show
      v-for="show in shows"
      :key="show.id"
      :id="show.id"
      :name="show.name"
      :episodes_seen="show.episodes_seen"
    />
    <input type="text" v-model="newShowName" />
    <button type="button" @click="submit">submit </button>
  </div>
</template>

<script>
import Instructions from "./Instructions.vue";
import Show from "./Show.vue";

export default {
  components: {
    Instructions,
    Show
  },
  data() {
    return {
      newShowName:'',
      shows: [
        { id: 1, name: "Game of Thrones", episodes_seen: 0 },
        { id: 2, name: "Naruto", episodes_seen: 220 },
        { id: 3, name: "Black Mirror", episodes_seen: 3 }
      ]
    };
  },
  //couldn't finish bonus for front end part, following function fails to add show to shows
  methods:{
    submit: function() { 
      id = this.shows[this.shows.length-1].id+1
      show = {id:id,name:this.newShowName, episodes_seen:0} 
      this.shows.push( show  )
    }
  }
};
</script>

<style>
</style>


