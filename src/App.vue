<template>
  <h1>{{ title }}</h1>
  <p>Welcome...</p>
  <div v-if="showModal">
    <Modal theme="none" @close="toggleModal">
      <h1>Ninja Giveaway!</h1>
      <p>Grab your ninja swag for half price</p>
      <template v-slot:links>
        <a href="#">Signup now</a>
        <a href="#">More info</a>
      </template>
    </Modal>
  </div>

  <div v-if="showModalTwo">
    <Modal theme="none" @close="toggleModalTwo">
      <h1>Modal Two</h1>
      <p>Modal Two sdfha fsdjkhf </p>
      <template v-slot:links>
        <a href="#">Signup now</a>
        <a href="#">More info</a>
      </template>
    </Modal>
  </div>

  <button @click="toggleModal">Open Modal</button>
  <button @click="toggleModalTwo">Open Modal Two</button>


</template>

<script>
import Modal from './components/Modal';

export default {
  name: 'App',
  components: {
    Modal
  },
  data() {
    return{
      title: 'My first Vue App :)',
      showModal: false,
      showModalTwo: false,
    }
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    },
    toggleModalTwo() {
      this.showModalTwo = !this.showModalTwo;
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
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}

</style>
