<template>
  <div>
    <h1>{{ title }}</h1>
    <div v-if="showModal">
      <Modal
        :header="header"
        :text="content"
        theme="sale"
        @close="toggleModal"
      />
    </div>
    <button @click="toggleModal">open modal</button>
  </div>
</template>

<script>
import Modal from "./components/Modal.vue";

export default {
  name: "App",
  data() {
    return {
      title: "My first Vue App",
      header: "hey",
      content: "content...",
      showModal: false,
    };
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    },
  },
  components: {
    Modal,
  },
};
</script>

<style >
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1 {
  color: navy;
}
</style>
