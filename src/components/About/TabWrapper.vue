<template>
  <div>
    <ul class="title">
      <li
        v-for="title in tabTitles"
        :key="title"
        @click="selectedTitle = title"
        :class="{ selected: title == selectedTitle }"
      >
        {{ title }}
      </li>
    </ul>
    <slot />
  </div>
</template>

<script>
import { ref, provide } from "vue";
export default {
  setup(props, { slots }) {
    const tabTitles = ref(slots.default().map((tab) => tab.props.title));
    console.log(tabTitles);
    const selectedTitle = ref(tabTitles.value[0]);

    provide("selectedTitle", selectedTitle);
    return {
      selectedTitle,
      tabTitles,
    };
  },
};
</script>

<style>
.title {
  display: flex;
  justify-content: center;
  align-items: center;
  list-style: none;
}
.title li {
  color: rgb(251, 255, 0);
  background-color: rgb(0, 135, 193);
  display: block;
  width: 5rem;
  height: 2rem;
  border-radius: 0.5rem;
  margin-left: 2rem;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}
.title li.selected {
  background-color: rgb(186, 0, 0);
  color: blanchedalmond;
}
</style>
