<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import { Head } from '@inertiajs/vue3';

defineProps({
    user: Object,
});
</script>

<template>
    <AppLayout>
        <Head title="Mi Perfil" />

        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="bg-white overflow-hidden shadow-xl sm:rounded-lg p-6">
                    <h2 class="text-2xl font-bold mb-6">Información Personal</h2>
                    
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <div>
                            <h3 class="text-gray-600 font-semibold">Nombre</h3>
                            <p class="text-gray-900">{{ user.name }}</p>
                        </div>

                        <div>
                            <h3 class="text-gray-600 font-semibold">Apellido</h3>
                            <p class="text-gray-900">{{ user.lastname }}</p>
                        </div>

                        <div>
                            <h3 class="text-gray-600 font-semibold">Teléfono</h3>
                            <p class="text-gray-900">{{ user.phone }}</p>
                        </div>

                        <div>
                            <h3 class="text-gray-600 font-semibold">Email</h3>
                            <p class="text-gray-900">{{ user.email }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </AppLayout>
</template> 