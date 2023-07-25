<template>
  <label>
    {{ label }}
    <input type="checkbox" :checked="myChecked" @change="onchange">
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
    myChecked: {
      type: Boolean,
      default: false
    }
  },
  methods: {
    onchange(e) {
      this.$emit("mychange", e.target.checked);
    }
  }
};
</script>

<style scoped>
</style>
