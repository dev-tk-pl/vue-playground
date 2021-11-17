<template>
  <img alt="Vue logo" src="./assets/logo.png" />
</template>

<script>
import { useCookies } from "vue3-cookies";
export default {
  name: "App",
  components: {},
  setup() {
    const { cookies } = useCookies();
    return { cookies };
  },
  mounted() {
    let my_cookie_value = this.cookies.get("myCoookie");
    console.log(my_cookie_value);
    this.cookies.set("myCoookie", "abcdefg");
  },
};
</script>

<style lang="scss"></style>
