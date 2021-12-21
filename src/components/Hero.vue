<template>
    <div class="front" :style="{ backgroundImage: `url(${imagePath})` }" >

        <p class="lead">{{leadText}}</p>
        <p class="title">{{title}}</p>
        <p class="description">{{desciption}}</p>

    <div class="button">
        <button 
        class="sub-button"
        v-on:click="changeVisibleA"
        :disabled="!visibleA"
        >NEW ARRIVALS</button> 

        <button 
        class="sub-button"
        v-on:click="changeVisibleB"
         :disabled="!visibleB"
        >BEST SELLERS</button>
    </div>

    </div>

</template>

<script lang="ts">
import { defineComponent } from 'vue'
import diamond from '@/assets/images/diamond.jpg'

export default defineComponent({
    data() {
    return {
      imagePath: diamond,
      leadText: 'DISCOVER',
      title: 'YOUR STONE',
      desciption: 'Start your engagement ring journey here.Craft your own bespoke design or browse from our ready to wear collection',
      visibleA: true,
      visibleB: true,
    }
    },
    methods: {
     changeVisibleA() {
       this.$emit('update-visibleA')
       this.visibleA= false
           console.log('you clicked button A from child')

        },
        changeVisibleB() {
       this.$emit('update-visibleB')
       this.visibleB= false
           console.log('you clicked button B from child')

        } 
    } 
   
})
</script>

<style>

.front {
  text-align: center;
  background-repeat: no-repeat;
  background-size: cover;
  
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
