# Human Body Parts Selector (Vue JS)

This is a library for those who want to be able to allow users to select body parts.

## Example

https://vue-body-part-selector.netlify.app/

[source code for the example above](https://github.com/HamadaFMahdi/body-part-selector-test/blob/master/src/App.vue)

## Intallation

`yarn add vue-body-part-selector`

or 

`npm i vue-body-part-selector`

## Usage

Import component & register it e.g.

```
<script>
import Vue from 'vue';
import VueBodyPartSelector from 'vue-body-part-selector';

export default Vue.extend({
  name: 'App',
  components: {
    VueBodyPartSelector
  },
  data() {  
  ... // etc.
```

Use it e.g.

```
      <vue-body-part-selector 
        :selection.sync="selection" // make sure to define selection in data
        @click="handleClick"
        :disabled="false"
        :multiple="true"
        body-colour="green"
        selection-colour="yellow"
        :show-parts="{ // won't show head, face and neck
          'head': false,
          'face': false,
          'neck': false,
        }"
      />
```

## Props

| Name             | Type   | Desc                                                                                                                                      | Default                         |
|------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| disabled         | bool   | If true, you can't select anything.                                                                                                       | false                           |
| multiple         | bool   | If true allows you to select multiple body parts.                                                                                         | false                           |
| body-colour      | string | Determines colour of the body.                                                                                                            | black                           |
| selection-colour | string | Determines colour of selection when clicked.                                                                                              | black                           |
| show-parts       | object | Allows you to hide body parts. Useful if you only want e.g. the front or the back or half of the front. (Please see below for structure). | object where all parts are true |

## show-parts object structure

Note: `true` means show, `false` means hide.

```
{
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
}
```

## License: MIT

## Credits

Credits go to [Carlos Fuentes](https://stackoverflow.com/users/1566111/carlos-fuentes) who did a great job making the base for this.
[Check source here](https://stackoverflow.com/a/65485328/9301008).
