<script>
import Vue from 'vue';
import VueBodyPartSelector from '@/vue-body-part-selector.vue';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    VueBodyPartSelector
  }
});
</script>

<template>
  <div id="app">
    <vue-body-part-selector />
  </div>
</template>
