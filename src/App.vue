<template>
  <n-config-provider :theme-overrides="themeOverrides">
    <router-view></router-view>
  </n-config-provider>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { NConfigProvider } from "naive-ui";
/**
 * @type import('naive-ui').GlobalThemeOverrides
 */
const themeOverrides = {
  common: {
    primaryColor: "#2080f0",
    primaryColorHover: "#4098fc",
    primaryColorPressed: "#1060c9",
    primaryColorSuppl: "#4098fc",
    infoColor: "#C0C4CC",
    infoColorHover: "#8c8c8c",
    infoColorPressed: "#8c8c8c",
    infoColorSuppl: "#C0C4CC",
    fontWeightStrong: "400",
    textColorBase: "#4c4948",
  },
  Menu: {
    itemTextColor: "#4c4948",
    itemIconColor: "#4c4948",
  },
};
export default defineComponent({
  components: {
    NConfigProvider,
  },
  setup() {
    return {
      themeOverrides,
    };
  },
});
</script>
