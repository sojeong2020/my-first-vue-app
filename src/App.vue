<template>
<div class="app">
  
 <Hero />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Hero from './components/Hero.vue'

export default defineComponent({
  name: 'App',
  components: {Hero},
  data() {
    return {
      visible:  true
      }
    },
   methods: {
     updateVisible() {
      this.visible=true
      
        } 
    } 
  
  
});
</script>


<style>

</style>
