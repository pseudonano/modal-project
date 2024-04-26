<template>
  <h1>{{  title }}</h1>
  <p>Welcome to the best site in the world..</p>
  <div v-if="showModal">
    <Modal @close="toggleModal">
      <!-- <template v-slot:accessLinks>
        <a href="www.google.com" target="_blank">Sign Up</a>
      </template>
      <template v-slot:infoLinks>
        <a href="a" target="_blank" rel="noreferrer noopener">more info</a>
      </template> -->
      <template />
      <h1>HI</h1>
      <p>this is example of using slots instead of props</p>
    </Modal>
  </div>
  <button @click="toggleModal">Open Modal</button>
  <div>
    <ScrollableContent>
    </ScrollableContent>
  </div>
  <!-- <BoxContent /> -->
</template>

<script>
import Modal from './components/Modal.vue'
import ScrollableContent from './components/ScrollableContent.vue'
import BoxContent from './components/BoxContent.vue'

export default {
  name: 'App',
  components: {Modal,ScrollableContent,BoxContent},
  data(){
    return {
      title: `Teguh's cool websites`,
      header: 'Sign up for giveaway!',
      text: 'Grab your chance ASAP by visiting this ',
      textLink: 'link',
      showModal: false
    }
  },
  methods:{
    toggleModal(){
      this.showModal = !this.showModal
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
h1 {
  border-bottom: 1px solid #e1e443;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
