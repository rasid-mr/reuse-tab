<template>
  <div>
    <label for="textInput">{{ label }}</label>
    <input type="text" :id="id" v-bind="$attrs" />
    <div class="color"></div>
    <p>{{ link }} hel</p>
  </div>
</template>

<script>
export default {
  inheritAttrs: false,
  props: ["label", "link", "id"],
};
</script>

<style>
.color {
  width: 20rem;
  padding-top: 20rem;
  background-color: red;
}
</style>
