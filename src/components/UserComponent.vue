<template>
    <div id="UserComponent">
        <img
            @click="openMenu = !openMenu"
            src="https://picsum.photos/id/237/200"
            alt="User Profile Icon"
            data-tooltip-target="tooltip-no-arrow-user"
            data-tooltip-placement="bottom"
            class="w-8 cursor-pointer rounded-full"
        />

        <div
            id="tooltip-no-arrow-user"
            role="tooltip"
            class="tooltip invisible absolute z-10 inline-block rounded-sm px-2 py-1 text-xs font-medium text-white opacity-0 shadow-sm delay-150 dark:bg-gray-600"
        >
            <span>Google Account</span>
            <span class="block text-gray-300">Muhamad Hafs</span>
            <span class="block text-gray-300">muhamadhaspin@gmail.com</span>
        </div>

        <div
            v-if="openMenu"
            class="absolute right-2 top-14 z-10 w-80 rounded-lg bg-white"
        >
            <div class="flex w-full justify-center">
                <img
                    src="https://picsum.photos/id/237/200"
                    alt="User Profile Icon"
                    class="mt-4 w-20 rounded-full"
                />
            </div>

            <div class="mt-2 flex w-full justify-center text-lg text-gray-700">
                Muhamad Hafs
            </div>
            <div
                class="mt-2 flex w-full justify-center border-b pb-4 text-sm text-gray-700"
            >
                muhamadhaspin@gmail.com
            </div>

            <div class="my-5 flex justify-center">
                <button
                    class="rounded border border-gray-300 bg-transparent px-4 py-2 text-xs font-semibold text-gray-600 hover:bg-gray-100"
                >
                    Sign out of Gmail
                </button>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const openMenu = ref(false)
</script>
