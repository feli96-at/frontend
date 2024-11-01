<template>
    <div class="flex justify-center items-center h-screen bg-gray-100">
        <div class="w-full max-w-md bg-white shadow-md rounded-lg p-6">
            <h2 class="text-2xl font-semibold text-center mb-6">Register</h2>

            <form @submit.prevent="submitForm">
                <div class="mb-4">
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="username">Username</label>
                    <input v-model="form.username" type="text" id="username"
                        class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none focus:ring focus:ring-indigo-200"
                        placeholder="Enter your username" required />
                </div>

                <div class="mb-4">
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="password">Password</label>
                    <input v-model="form.password" type="password" id="password"
                        class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none focus:ring focus:ring-indigo-200"
                        placeholder="Enter your password" required />
                </div>

                <div class="mb-6">
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="repassword">Re-enter Password</label>
                    <input v-model="form.repassword" type="password" id="repassword"
                        class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none focus:ring focus:ring-indigo-200"
                        placeholder="Re-enter your password" required />
                    <p v-if="errorMessage" class="text-red-500 text-sm mt-1">{{ errorMessage }}</p>
                </div>

                <button type="submit"
                    class="w-full bg-indigo-500 text-white font-bold py-2 px-4 rounded hover:bg-indigo-600 focus:outline-none focus:ring focus:ring-indigo-200">
                    Register
                </button>
            </form>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            form: {
                username: '',
                password: '',
                repassword: ''
            },
            errorMessage: ''
        };
    },
    methods: {
        submitForm() {
            if (this.form.password !== this.form.repassword) {
                this.errorMessage = "Passwords do not match!";
            } else {
                this.errorMessage = '';
                // Proceed with form submission (e.g., API call)
                console.log("Form submitted:", this.form);
            }
        }
    }
};
</script>

<style scoped>
/* Add any additional styling if needed */
</style>