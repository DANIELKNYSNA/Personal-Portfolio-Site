<template>
    <div >
    <v-form class="flex flex-col w-1/5 m-auto border-4 rounded-xl shadow-lg p-4 mt-2" >
        <h1 class="text-xl font-extrabold mb-4">Login</h1>
        <label class="font-bold" for="email">Enter your email address</label>
        <input class="mb-2 p-2 border-2 rounded-lg"  type="text" placeholder="Email" v-model="email">
        <label class="font-bold" for="password">Enter your password</label>
        <input class="mb-2 p-2 border-2 rounded-lg" type="password" placeholder="Password" v-model="password">
        <button @click="onSubmit"
                class="mt-4 mb-4px-4 py-2 bg-blue-500 text-slate-300 rounded-xl hover:bg-blue-900">Login</button>
        <p class="text-center mt-4">Not registered?</p>
        <button @click="toregister"
                class="mb-4px-4 py-2 bg-green-500 text-slate-300 rounded-xl hover:bg-green-900">Register</button>

    </v-form>
        
    </div>
	<v-card width="400" class="mx-auto mt-5">
		<v-card-title>
			<h1 class="display-1">Login</h1>
		</v-card-title>
		<v-card-text>
			<v-form>
				<v-text-field label="Username" prepend-icon="mdi-account-circle" />
				<v-text-field
					:type="showPassword ? 'text' : 'password'"
					label="Password"
					prepend-icon="mdi-lock"
					:append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
					@click:append="showPassword = !showPassword"
				/>
			</v-form>
		</v-card-text>
		<v-divider></v-divider>
		<v-card-actions>
			<v-btn color="success">Register</v-btn>
			<v-spacer></v-spacer>
			<v-btn color="info">Login</v-btn>
		</v-card-actions>
	</v-card>
</template>




<script>
export default {
	name: 'LoginPage',
	data() {
		return {
			showPassword: false
		}        
	},
    methods: {
      onSubmit() {
          //write the function for post request
      }
  }
}
</script>

<style></style>





