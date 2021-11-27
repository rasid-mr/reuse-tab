<template>
  <div class="about">
    <tab-wrapper>
      <one-tab title="Tab 1">This is the 1st tab</one-tab>
      <one-tab title="Tab 2">This is the 2st tab</one-tab>
      <one-tab title="Tab 3">This is the 3rd tab</one-tab>
      <one-tab title="Tab 4">This is the 4th tab</one-tab>
    </tab-wrapper>
  </div>
</template>

<script>
import TabWrapper from "../components/About/TabWrapper";
import OneTab from "../components/About/Tab";
export default {
  components: {
    TabWrapper,
    OneTab,
  },
};
</script>
