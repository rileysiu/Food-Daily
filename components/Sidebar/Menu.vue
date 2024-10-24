<script setup>
const items = ref([
    {
        title: "儀表板",
        path: "/",
        icon: 'ri:dashboard-line'
    },
    {
        title: "日記",
        path: "/diet",
        icon: 'material-symbols:menu-book-outline'
    }
])
</script>

<template>
    <div>
        <header class="flex items-center gap-2 p-4 hover:scale-[101%] transition cursor-pointer">
            <Logo />
        </header>
        <div class="px-4 grow">
            <div class="grid gap-4">
                <NuxtLink :href="item.path"
                    v-for="(item, index) in items" :key="index"
                    class="flex items-center gap-2 px-2 py-1 transition rounded cursor-pointer hover:bg-neutral-100">
                    <Icon size="30" :name="item.icon" />
                    <span>{{ item.title }}</span>
                </NuxtLink>
            </div>
        </div>
    </div>
</template>
