<template>
  <Page class="page" actionBarHidden="true" backgroundSpanUnderStatusBar="true">
    <StackLayout>
      <Nav selected="A" />
      <Label textWrap="true" text="Welcome to Page A. You should be able to click the B button on the Nav to navigate to Page B. However it does not work." />
    </StackLayout>
  </Page>
</template>

<script>
import Nav from "./Nav";

console.log("In A");
console.dir(Nav);

export default {
  components: {
    Nav
  }
};
</script>

<style scoped>
label {
  color: white;
  margin: 10;
}
</style>
