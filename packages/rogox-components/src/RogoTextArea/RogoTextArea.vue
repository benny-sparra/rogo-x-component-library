<template>
<label>{{ labelText }}</label>
  <textarea class="form-control" ></textarea>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  props: {
    labelText: String
  }
});
</script>