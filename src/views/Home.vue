<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <wrapper-component
      label="Home"
      placeholder="search"
      class="kira"
      link="null"
      @keydown="getTarget"
      id="1"
    ></wrapper-component>
    <wrapper-component
      placeholder="search"
      link
      id="2"
      class="kira"
    ></wrapper-component>
    <select-option
      v-model="selected"
      :choices="choices"
      @change="getChange"
      class="vModel"
    ></select-option>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import WrapperComponent from "../components/WrapperComponent";
import SelectOption from "../components/SelectOption";

export default {
  data() {
    return {
      selected: null,
      choices: [
        {
          value: 1,
          id: 1,
        },
        {
          value: 2,
          id: 2,
        },
      ],
    };
  },
  name: "Home",
  components: {
    HelloWorld,
    WrapperComponent,
    SelectOption,
  },
  methods: {
    getTarget(event) {
      console.log(event.target.value);
    },
    getChange(event) {
      console.log(event.target.value);
    },
  },
};
</script>

<style lang="scss">
.kira {
  padding: 1rem 1.5rem;
}
</style>
