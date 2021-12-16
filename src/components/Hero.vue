<template>
    <div class="front" >

        <img :src="image">
        <p class="lead">{{leadText}}</p>
        <p class="title">{{title}}</p>
        <p class="description">{{desciption}}</p>

    <div class="button">
        <button 
        class="sub-button"
        v-on:click="changeVisible"
        >NEW ARRIVALS</button>
        <button 
        class="sub-button"
        v-on:click="changeVisible"
        >BEST SELLERS</button>
    </div>

    </div>
    
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    /* props: {
     change: {
         type: Boolean,
         required: true
        }
    },  */
     data() {
    return {
      image: '../assets/images/diamond.jpg',
      leadText: 'DISCOVER',
      title: 'YOUR STONE',
      desciption: 'Start your engagement ring journey here.Craft your own bespoke design or browse from our ready to wear collection',
      visible: true 
      }
    },
    methods: {
     changeVisible() {
       this.$emit('change-visible')
        } 
    } 
   
})
</script>

<style>
.front {
  
  text-align: center;

    } 
.lead {
    font-size: 20px;
    }
.title {
    font-size: 28px;
    }
.description {
    font-size: 18px;
    }
.sub-button {
  margin: 20px;
  background-color: #39495c;
  border-radius: 5px;
  color: white;
  padding: 10px;
  text-align: center;
  cursor: pointer;
}
</style>
