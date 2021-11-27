<template>
  <div>
    <select>
      <option disabled></option>
      <option v-for="choice in choices" :key="choice.id">
        {{ choice.value }}
      </option>
    </select>
  </div>
</template>

<script>
export default {
  props: ["choices"],
};
</script>

<style></style>
