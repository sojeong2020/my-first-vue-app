<template>
<div class="app">

  <hero 
  @update-visibleA="updateVisibleA"
  @update-visibleB="updateVisibleB" />
  
</div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Hero from './components/Hero.vue'

export default defineComponent({
  name: 'App',
  components: {Hero},
   methods: {
    updateVisibleA() {
     console.log('from A parent ')
    },
    updateVisibleB() {
    console.log('from B parent')
    }, 

    } 

});
</script>


<style>

</style>
