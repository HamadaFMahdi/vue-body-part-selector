<script>
import Vue from 'vue';
import VueBodyPartSelector from '@/vue-body-part-selector.vue';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    VueBodyPartSelector
  },
  data() {
    return {
      selection: '',
      disabled: false,
      multiple: false,
      bodyColour: "#FF0000",
      selectionColour: "#0000FF"
    };
  },
  methods: {
    handleClick(newVal) {
      console.log(newVal)
    }
  }
});
</script>

<template>
  <div id="app">
    <div class="human-body">
      <vue-body-part-selector 
        :selection.sync="selection"
        @click="handleClick"
        :disabled="disabled"
        :multiple="multiple"
        :body-colour="bodyColour"
        :selection-colour="selectionColour"
        :showParts="{
          'head': true,
          'face': true,
          'neck': true,
          'shoulder-left': true,
          'shoulder-right': true,
          'arm-left': true,
          'forearm-left': true,
          'arm-right': true,
          'forearm-right': true,
          'chest-left': true,
          'chest-right': true,
          'belly-left': true,
          'ribs-left': true,
          'belly-right': true,
          'belly': true,
          'ribs-right': true,
          'thigh-left': true,
          'innerthigh-left': true,
          'feet-left': true,
          'calf-left': true,
          'knee-left': true,
          'thigh-right': true,
          'genitalia': true,
          'innerthigh-right': true,
          'right-feet': true,
          'calf-right': true,
          'knee-right': true,
          'elbow-right': true,
          'hand-right': true,
          'elbow-left': true,
          'hands-left': true,
          'armback-left': true,
          'leg-left': true,
          'buttock': true,
          'loin': true,
          'column': true,
          'head-back': true,
          'nape': true,
          'armback-right': true,
          'leg-right': true,
          'back-right': true,
          'clavicule-right': true,
          'back-left': true,
          'clavicule-left': true,
        }"
      />
    </div>
    <br>
    Selection: {{selection}}
    <br>
    <br>
    <strong>Options:</strong>
    <br>
    <input type="radio" v-model="disabled" :value="true">Disabled
    <input type="radio" v-model="disabled" :value="false">Not Disabled
    <br>
    <input type="radio" v-model="multiple" :value="true">Multiple
    <input type="radio" v-model="multiple" :value="false">Single
    <br>
    <label for="bodyColour"> Body Colour: </label>
    <input id="bodyColour" type="text" v-model="bodyColour">
    <br>
    <label for="selectionColour"> Selection Colour: </label>
    <input id="selectionColour" type="text" v-model="selectionColour">

  </div>
</template>

<style scoped>

  .human-body {
    width: 300px;
    height: 420px;
  }

</style>
