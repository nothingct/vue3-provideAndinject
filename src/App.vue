<template>
  <button @click="message='Be alive, Take it.'">
    Click!
  </button>
  <h1> App: {{ message }}</h1>
  <Parent />
</template>

<script>
import Parent from '~/components/Parent'
import { computed } from 'vue'
export default {
  components :{
    Parent
  },
  data() {
    return {
      message : 'here comes the life'
    }
  },
  provide(){
    return{
      msg : computed(()=> this.message)
    }
  }
}
</script>