<template>
  <div id="app">
    <hello></hello>
    <div>
        <a href='javascript:void(0);' v-on:click='onShowModal'>Show Modal</a>
    </div>
    <modal
        :is-show='isShowModal' 
        title='Modal title'
        v-on:ok='onModalOk'
        v-on:cancel='onModalCancel'>
            <p>content text!</p>
        </modal>
  </div>
</template>

<script>
import Hello from './components/Hello'
import Modal from './components/Modal'

export default {
    name: 'app',
    data () {
        return {
            isShowModal: false
        };
    },
    components: {
        Hello,
        Modal
    },
    methods: {
        onShowModal () {
            this.isShowModal = true;
        },
        onModalOk () {
            this.isShowModal = false;
        },
        onModalCancel () {
            this.isShowModal = false;
        }
    }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
  max-width: 1200px;
  padding: 20px;
}
</style>
