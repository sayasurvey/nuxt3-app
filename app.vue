<template>
  <div>
    <Form :validationSchema="validationSchema" v-slot="{ meta: { valid } }">
      <TextField v-model="email" name="email" label="メールアドレス"/>
      <TextField v-model="password" name="password" label="パスワード" inputType="password"/>
      <button :disabled="!valid">ログイン</button>
    </Form>
  </div>
</template>

<script setup lang="ts">
import { Form } from 'vee-validate';
import * as yup from 'yup';
import { ref } from 'vue';

const email = ref("");
const password = ref("");

const validationSchema = yup.object().shape({
  email: yup.string().required().email().label("メールアドレス"),
  password: yup.string().required().min(8).label("パスワード")
})
</script>
