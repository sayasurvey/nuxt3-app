<template>
  <div>
    <Field v-model="props.modelValue" :name="props.name" v-slot="{ field }">
      <p>{{ props.label }}</p>
      <input v-bind="field" :type="props.inputType" />
    </Field>
    <ErrorMessage :name="props.name" v-slot="{ message }">
      <p>Error: {{ message }}</p>
    </ErrorMessage>
  </div>
</template>

<script setup lang="ts">
import { ErrorMessage, Field } from 'vee-validate';
import { defineProps, withDefaults } from 'vue';

interface Props {
  modelValue: string,
  label: string,
  name: string,
  inputType?: string
};

const props = withDefaults(
  defineProps<Props>(), {
    inputType: "text"
  }
);
</script>