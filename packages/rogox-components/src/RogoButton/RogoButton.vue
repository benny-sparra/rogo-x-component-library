<template>
  <button class="btn btn-primary" v-on:click="clickHandler">{{ text }}</button>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  props: {
    text: String
  },
  methods: {
    clickHandler : function(){
      this.$emit('rogoButtonClicked', '');
    }
  }
});
</script>

<!-- <style scoped>
button {
  list-style: none;
  word-wrap: break-word;
  -webkit-text-size-adjust: none;
  border-spacing: 0;
  border-collapse: collapse;
  line-height: normal;
  display: inline-block;
  padding: 5px 13px;
  color: #FFF;
  background: #EF800C;
  border: 1px solid #EF800C;
  vertical-align: middle;
  border-radius: 0;
  overflow: visible;
  font-family: 'Lato', 'sans-serif';
  font-size: 12px;
  text-align: center;
  text-decoration: none;
  font-weight: 700;
  zoom: 1;
  direction: ltr;
  cursor: pointer;
  -webkit-appearance: button;
  margin: 0;
}
</style> -->
