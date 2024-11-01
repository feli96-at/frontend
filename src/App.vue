<template>
    <div class="h-screen flex justify-center items-center">
        <div class="max-w-md w-full bg-blue-200 p-6 rounded shadow">
            <h2 class="text-center text-2xl">Register</h2>
            <form action="">
                <div class="mt-4">
                    <label for="username" class="block">Username</label>
                    <input type="text" class="border w-full rounded">
                </div>
                <div class="mt-4">
                    <label for="password" class="block">Password</label>
                    <input type="password" class="border w-full rounded">
                </div>
                <div class="mt-4">
                    <label for="repassword" class="block">Re-enter password</label>
                    <input type="password" class="border w-full rounded">
                </div>
                <button type="submit" class="bg-blue-400 w-full mt-4 rounded">Submit</button>
            </form>
        </div>
    </div>
</template>