<template>
  <div>
    <form
      @submit.prevent="submitForm"
      class="flex flex-col w-1/5 m-auto border-4 rounded-xl shadow-lg p-4 mt-2"
    >
      <h1 class="text-xl font-extrabold mb-4">Login</h1>

      <label class="font-bold" for="email">Enter your email address</label>

      <input
        class="mb-2 p-2 border-2 rounded-lg"
        placeholder="Email"
        type="text"
        v-model="email"
      />
      <span v-if="v$.email.$error" class="text-red-500">
		  {{ v$.email.$errors[0].$message }}</span>

      <label class="font-bold" for="password"> Enter your password </label>
      <input
        class="mb-2 p-2 border-2 rounded-lg"
        type="password"
        placeholder="Password"
        v-model="password"
      />
      <span v-if="v$.password.$error" class="text-red-500">{{
        v$.password.$errors[0].$message
      }}</span>
      <button
        @click="submitForm"
        class="mt-4 mb-4px-4 py-2 bg-blue-500 text-slate-300 rounded-xl hover:bg-blue-900"
      >
        Login
      </button>
      <p class="text-center mt-4">Not registered?</p>
      <button
        class="mb-4px-4 py-2 bg-green-500 text-slate-300 rounded-xl hover:bg-green-900"
      >
        Register
      </button>
    </form>
  </div>
</template>
<script>
import useValidate from "@vuelidate/core";
import { required, email, minLength } from "@vuelidate/validators";
export default {
  name: "LoginPage",
  data() {
    return {
      v$: useValidate(),
      email: "",
      password: "",
    };
  },
  validations() {
    return {
      email: { required, email },
      password: { required, minLength: minLength(8) },
    };
  },
  methods: {
    submitForm() {
      this.v$.$validate();
      if (!this.v$.$error) {
        alert("The form has been submitted");
      } else {
        alert("Form Failed Validation");
      }
    },
    toRegister() {
      navigator.to("/");
    },
  },
};
</script>

<style></style>
