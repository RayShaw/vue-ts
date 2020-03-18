<template>
  <div class="hello-about">
    <input v-model="msg" />
    <p>prop: {{propMessge}}</p>
    <p>msg: {{msg}}</p>
    <p>helloMsg: {{helloMsg}}}</p>
    <p>computed msg: {{computedMsg}}}</p>
    <button @click="greet">greet</button>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class About extends Vue {
  @Prop() propMessge!: string;

  //initial data
  msg = 123;

  // use prop values for initial data
  helloMsg = "Hello, " + this.propMessge;

  // lifecycle hook
  mounted() {
    this.greet();
  }

  // couputed
  get computedMsg(): string {
    return "computed " + this.msg;
  }

  //method
  greet(): void {
    console.log("greeting: ", this.msg);
  }
}
</script>
