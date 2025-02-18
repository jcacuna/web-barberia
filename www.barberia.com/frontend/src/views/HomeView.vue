<script setup>
const authRoutes = [
    { name: 'register', text: 'Crear una cuenta' },
    { name: 'login', text: 'Iniciar Sesión' }
];
</script>

<template>
    <div class="flex flex-col items-center justify-center min-h-screen bg-gradient-to-b from-gray-900 to-gray-800 px-5">
        <div class="max-w-3xl text-center">
            <h1 class="text-5xl font-extrabold text-white mb-5">Bienvenidos a AppSalon</h1>
            <p class="text-lg text-gray-300 leading-relaxed">
                Si deseas cambiar tu look, mejorar tu apariencia y lucir mejor, has venido al lugar indicado.
                Crea una cuenta y comienza a agendar tus sesiones de belleza.
            </p>
        </div>

        <div class="p-8 mt-10 rounded-lg w-full max-w-2xl">
            <RouterView />
            <nav class="mt-8 flex flex-col space-y-4 sm:flex-row sm:justify-center sm:space-x-4 sm:space-y-0">
                <RouterLink v-for="route in authRoutes" :key="route.name"
                    class="w-full sm:w-1/2 text-center bg-blue-500 text-white font-bold py-3 rounded-lg transition duration-300 hover:bg-blue-600"
                    :to="{ name: route.name }">
                    {{ route.text }}
                </RouterLink>
            </nav>
        </div>
    </div>
</template>
