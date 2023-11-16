<script setup>
import { ref } from 'vue';

const email = ref('');
const password = ref('');
</script>

<template>
    <main>
        <header>
            <h1 class="logo">SECRET APP</h1>
            <h2>Login</h2>
            <p>Login or create an account to start using the super secret app</p>
        </header>

        <form @submit.prevent="">
            <label>
                <span>Enter your email</span>
                <input type="email" v-model="email" placeholder="test@test.com" />
            </label>

            <label>
                <span>Enter your password</span>
                <input type="password" v-model="password" placeholder="***********" />
            </label>

            <input type="submit" value="Login" />
        </form>

        <footer>
            <p>Don't have an account? <router-link to="/register">Register</router-link></p>
        </footer>
    </main>
</template>