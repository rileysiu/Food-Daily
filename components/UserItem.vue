<script setup>
const loading = ref(false)
const name = ref('Riley')
const description = ref('Frontend Engineer')
</script>

<template>
    <div class="p-2 m-2 border rounded flex items-center justify-start gap-2 cursor-pointer hover:bg-neutral-50 transition">
        <div class="rounded-full w-10 h-10 bg-green-500 flex items-center justify-center font-bold text-white">
            {{ name[0] }}
        </div>
        <div>
            <p class="font-bold text-black m-0 leading-1 text-sm">{{ name }}</p>
            <p class="m-0 text-xs">{{ description }}</p>
        </div>
    </div>
</template>