<template>
  <div class="hello">
    <b-form-checkbox v-model="checkBoxValue">
      Checkbox Test
    </b-form-checkbox>

    <b-form-group label="Individual radios">
      <b-form-radio v-model="radioValue" name="some-radios" value="A">Option A</b-form-radio>
      <b-form-radio v-model="radioValue" name="some-radios" value="B">Option B</b-form-radio>
    </b-form-group>

    <b-form-input v-model="textValue" placeholder="Enter your name"></b-form-input>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: ['props'],
   computed: {
      checkBoxValue: { 
         get: function () { return this.props.checkBoxValue; },
         set: function (val) {
            console.log('Checkbox Setter Triggered!', val)
         }
      },
      radioValue: { 
         get: function () { return this.props.radioValue; },
         set: function (val) {
            console.log('Radio Setter Triggered!', val)
         }
      },
      textValue: { 
         get: function () { return this.props.editValue; },
         set: function (val) {
            console.log('Text Setter Triggered!', val)
         }
      }
   }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
