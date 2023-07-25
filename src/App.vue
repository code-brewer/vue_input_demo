<template>
  <div id="app">
    <section>
      <my-checkbox v-model="mycheckbox" value="mycheckbox1" label="mycheckbox1"/>
      {{mycheckbox}}
    </section>
    <section>
      <my-radio v-model="myradio" value="myradio1" label="myradio1"/>
      <my-radio v-model="myradio" value="myradio2" label="myradio2"/>
      {{myradio}}
    </section>
    <section>
      <my-text v-model="mytext"/>
      {{mytext}}
    </section>
  </div>
</template>

<script>
import MyCheckbox from "./components/Checkbox";
import MyRadio from "./components/Radio";
import MyText from "./components/Text";

export default {
  name: "App",
  components: {
    MyCheckbox,
    MyRadio,
    MyText
  },
  data() {
    return {
      mycheckbox: false,
      myradio: "",
      mytext: "hello world"
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
