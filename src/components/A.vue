<template>
  <Page class="page" actionBarHidden="true" backgroundSpanUnderStatusBar="true">
    <StackLayout>
      <Nav selected="A" />
      <Label textWrap="true" text="Welcome to Page A. You should be able to click the B button on the Nav to navigate to Page B" />
    </StackLayout>
  </Page>
</template>

<script>
import Nav from "./Nav";
export default {
  components: {
    Nav
  }
};
</script>

<style scoped>
.hello-world {
  margin: 20;
}

label {
  color: red;
}
</style>
