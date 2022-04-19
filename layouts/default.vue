<template>
  <n-layout style="height: 860px">
    <n-layout-header style="height: 64px" bordered>
      <n-space style="padding: 10px">
        <n-gradient-text type="info" style="padding-top: 10px">
          DentalDesk
        </n-gradient-text>
        <n-menu
          v-model:value="activeKey"
          mode="horizontal"
          :options="menuOptions"
        />
      </n-space>
    </n-layout-header>
    <n-layout
      position="absolute"
      :native-scrollbar="false"
      style="top: 64px; bottom: 64px"
      has-sider
    >
      <n-layout content-style="padding: 24px;" :native-scrollbar="false">
        <slot />
        <n-h2>Pingshan Road</n-h2>
        <n-h2>Pingshan Road</n-h2>
        <n-h2>Pingshan Road</n-h2>
        <n-h2>Pingshan Road</n-h2>
        <n-h2>Pingshan Road</n-h2>
        <n-h2>Pingshan Road</n-h2>
        <n-h2>Pingshan Road</n-h2>
        <n-h2>Pingshan Road</n-h2>
        <n-h2>Pingshan Road</n-h2>
        <n-h2>Pingshan Road</n-h2>
        <n-h2>Pingshan Road</n-h2>
        <n-h2>Pingshan Road</n-h2>
      </n-layout>
    </n-layout>
    <!-- <n-layout-footer
      position="absolute"
      style="height: 64px; padding: 24px"
      bordered
    >
      城府路
    </n-layout-footer> -->
  </n-layout>
</template>
<script>
import { defineComponent, h, ref } from "vue";
import { NIcon } from "naive-ui";
import {
  BookOutline as BookIcon,
  PersonOutline as PersonIcon,
  WineOutline as WineIcon,
} from "@vicons/ionicons5";

function renderIcon(icon) {
  return () => h(NIcon, null, { default: () => h(icon) });
}

const menuOptions = [
  {
    label: () =>
      h(
        "a",
        {
          href: "https://en.wikipedia.org/wiki/Hear_the_Wind_Sing",
          target: "_blank",
          rel: "noopenner noreferrer",
        },
        "Hear the Wind Sing"
      ),
    key: "hear-the-wind-sing",
  },
  {
    label: "Pinball 1973",
    key: "pinball-1973",

    children: [
      {
        label: "Rat",
        key: "rat",
      },
    ],
  },
  {
    label: "A Wild Sheep Chase",
    key: "a-wild-sheep-chase",
  },
  {
    label: "Dance Dance Dance",
    key: "Dance Dance Dance",
    children: [
      {
        type: "group",
        label: "People",
        key: "people",
        children: [
          {
            label: "Narrator",
            key: "narrator",
            icon: renderIcon(PersonIcon),
          },
          {
            label: "Sheep Man",
            key: "sheep-man",
            icon: renderIcon(PersonIcon),
          },
        ],
      },
      {
        label: "Beverage",
        key: "beverage",
        icon: renderIcon(WineIcon),
        children: [
          {
            label: "Whisky",
            key: "whisky",
          },
        ],
      },
      {
        label: "Food",
        key: "food",
        children: [
          {
            label: "Sandwich",
            key: "sandwich",
          },
        ],
      },
      {
        label: "The past increases. The future recedes.",
        key: "the-past-increases-the-future-recedes",
      },
    ],
  },
];

export default defineComponent({
  setup() {
    return {
      activeKey: ref(null),
      menuOptions,
    };
  },
});
</script>
