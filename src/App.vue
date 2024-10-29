<template>
  <div id="app">
    <FormModel />
  </div>
</template>

<script>
import Vue from 'vue';
import FormModel from './components/FormModel.vue';

export default Vue.extend ({
  name: 'App',
  components: {
    FormModel
  }
});
</script>

<style>

</style>
