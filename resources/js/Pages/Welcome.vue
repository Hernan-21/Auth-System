<script setup>
import { Head, Link } from '@inertiajs/vue3';

defineProps({
    canLogin: {
        type: Boolean,
    },
    canRegister: {
        type: Boolean,
    },
});
</script>

<template>
    <Head title="Welcome" />

    <div class="min-h-screen flex flex-col items-center justify-center bg-gray-100">
        <div class="text-center mb-8">
            <h1 class="text-4xl font-bold text-gray-900 mb-2">
                Bienvenido
            </h1>
            <p class="text-gray-600">
                Por favor, inicia sesión o regístrate para continuar
            </p>
        </div>

        <div class="space-x-4">
            <Link 
                :href="route('login')"
                class="inline-block px-6 py-3 bg-indigo-600 text-white font-semibold rounded-lg hover:bg-indigo-700 transition duration-150"
            >
                Iniciar Sesión
            </Link>

            <Link 
                v-if="canRegister"
                :href="route('register')"
                class="inline-block px-6 py-3 bg-white text-indigo-600 font-semibold rounded-lg border border-indigo-600 hover:bg-indigo-50 transition duration-150"
            >
                Registrarse
            </Link>
        </div>
    </div>
</template>
