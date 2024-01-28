<template>
    <Head title="Dashboard" />

    <AuthenticatedLayout>
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">Dashboard</h2>
        </template>

        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                    <!-- Cards with image, text, and "Add to Cart" button -->
                    <div v-for="item in cardData" :key="item.id" class="bg-white overflow-hidden shadow-sm sm:rounded-lg flex flex-col">
                        <img :src="item.imageUrl" alt="Item Image" class="w-full h-48 object-cover">
                        <div class="p-6 text-gray-900 flex-grow">
                            <h3 class="font-semibold text-xl mb-2">{{ item.itemName }}</h3>
                            <button @click="() => addToCart(item)" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded self-end">
                                Add to Cart
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Long horizontal card with Checkout button and total price -->
                <div class="bg-white overflow-hidden shadow-sm sm:rounded-lg mt-4">
                    <div class="p-6 bg-gray-800 text-white">
                        <h2 class="text-2xl font-semibold">Order Summary</h2>
                    </div>
                    <div class="p-6 text-gray-900">
                        <!-- Content for order summary, total price, etc. -->
                        <p>Total Price: ${{ totalPrice }}</p>
                        <button @click="checkoutButtonClicked" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded self-end">
                            Checkout
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </AuthenticatedLayout>
</template>

<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head } from '@inertiajs/vue3';
import { ref } from 'vue'; // Import ref from Vue for reactive data

const addToCart = (item) => {
    // Add your "Add to Cart" logic here
    console.log(`Item ${item.id} added to cart!`);
};

const checkoutButtonClicked = () => {
    // Add your checkout logic here
    console.log('Checkout button clicked!');
};

// Sample data for the cards
const cardData = [
    { id: 1, itemName: 'Burnham Park Tour Package', imageUrl: 'http://1.bp.blogspot.com/-JTisht9di10/T3UNA9Kyy7I/AAAAAAAADhs/CJYGLsQ_6F8/s1600/DSC_1836.jpg' },
    { id: 2, itemName: 'Riverview Water Park Package', imageUrl: 'https://th.bing.com/th/id/OLC.btGLEwlGfs5HoA480x360?&rs=1&pid=ImgDetMain' },
    { id: 3, itemName: 'The Manor at Camp John Hay', imageUrl: 'https://pix8.agoda.net/hotelImages/2563055/-1/8be27b955c83c8e4608d4f011fbecc89.jpg?ca=14&ce=1&s=1024x' },
];

// Sample total price
const totalPrice = ref(100); // Set your initial total price value
</script>
