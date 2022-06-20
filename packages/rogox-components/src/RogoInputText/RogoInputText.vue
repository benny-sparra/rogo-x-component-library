<script setup lang="ts">
import { defineComponent } from "vue";
import moment from 'moment'
import { Form, Field } from 'vee-validate';

const props = defineProps({
  modelValue: {
    type: String,
    default: '',
    required: true
  }
})

const emit = defineEmits(['update'])
//@input="$emit(update:modelValue, $event.target.value)"
</script>

<template>
  {{ moment(new Date).format("dddd MM YYYY") }}

  <Field name="email" class="form-control" type="email" />
  <input class="form-control" type="text" :value="modelValue" />
</template>