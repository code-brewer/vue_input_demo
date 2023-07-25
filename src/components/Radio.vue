<template>
  <label>
    {{ label }}
    <input type="radio" :value="value" :checked="myChecked === value" @change="onchange">
  </label>
</template>

<script>
export default {
  name: "my-checkbox",
  model: {
    prop: "myChecked",
    event: "mychange"
  },
  props: {
    label: String,
    value: String,
    myChecked: {
      type: String
    }
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
