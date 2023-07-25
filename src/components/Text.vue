<template>
  <label>
    <input type="text" :value="myChecked" @input="onchange">
  </label>
</template>

<script>
export default {
  name: "my-text",
  model: {
    prop: "myChecked",
    event: "mychange"
  },
  props: {
    myChecked: String
  },
  methods: {
    onchange(e) {
      let value = e.target.value;
      this.$emit("mychange", value);
    }
  }
};
</script>

<style scoped>
</style>
