<template>
    <Page class="page" actionBarHidden="true" backgroundSpanUnderStatusBar="true">
        <Nav selected="B" />
        <Label textWrap="true" text="Welcome to Page B. You should be able to click the A button in the Nav to navigate to Page A. However it does not work." />
    </Page>
</template>

<script>
import Nav from "./Nav";

console.log("In B");
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