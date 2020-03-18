<template>
  <div class="about">
    <h1>This is an about page</h1>
    <hello-about propMessge="Messge" />
  </div>
</template>

<script>
import HelloAbout from "@/components/HelloAbout.vue";
export default {
  name: "About",
  components: {
    HelloAbout
  }
};
</script>
