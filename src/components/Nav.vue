<template>
  <FlexboxLayout class="header-nav" alignItems="center">
    <FlexboxLayout @tap="toA()" :class="{selected: selected === 'A', 'nav-item': true }">
      <Label text="A" />
    </FlexboxLayout>
    <FlexboxLayout @tap="toB()" :class="{selected: selected === 'B', 'nav-item': true}">
      <Label text="B" />
    </FlexboxLayout>
    <!-- <FlexboxLayout @tap="toFindContent()" :class="{selected: selected === 'C', 'nav-item': true}">
      <Label text="C" />
    </FlexboxLayout>
    <FlexboxLayout :class="{selected: selected === 'D', 'nav-item': true}">
      <Label text="D" />
    </FlexboxLayout> -->
  </FlexboxLayout>
</template>

<script>
import A from "./A.vue";
import B from "./B.vue";

export default {
  // possible values for selected
  // queue, calendar, findcontent, smartpost
  props: ["selected"],
  methods: {
    toA() {
      if (this.selected === "A") {
        return;
      }
      this.$navigateTo(A, {
        transition: {},
        transitionIOS: {},
        transitionAndroid: {},
        context: {}
      });
    },
    toB() {
      if (this.selected === "B") {
        return;
      }
      this.$navigateTo(B, {
        transition: {},
        transitionIOS: {},
        transitionAndroid: {},
        context: {}
      });
    }
  }
};
</script>

<style scoped>
.header-nav .nav-item {
  justify-content: center;
  align-items: center;
  align-self: stretch;
  flex-grow: 1;
  flex-shrink: 1;
  padding: 10;
  font-weight: 800;
}
label {
  color: white;
  font-size: 25;
}
.header-nav {
  background-color: #222;
  padding: 0;
}
.selected {
  background-color: #0c0c0c;
}
</style>
