<template>
<h1>{{title}} text</h1>
<modal :header="header" :text="text" theme="sale"/>
<input type="text" ref="name">
<button @click="handleEvent">click</button>
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: {Modal},
  data(){
    return{
     header : "Sign up for a Giveaway",
     text : "Grab the course for the half price"
    }
  },
  methods: {
    handleEvent(){
      console.log('event')
      console.log(this.$refs.name)
      this.$refs.name.classList.add('mahdi')
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1{
  border-bottom: solid 1px #ccc ;
  display: inline-block ;
  padding-bottom: 10px ;  
}
</style>
