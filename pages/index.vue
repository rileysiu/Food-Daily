<script setup>
import { Tabs, TabsContent, TabsList, TabsTrigger } from '@/components/ui/tabs'
const response = await $fetch('/api/hello')
console.log(response)
const list = [
    {
        displayName: '早餐',
        title: 'Breakfast'
    },
    {
        displayName: '午餐',
        title: 'Lunch'
    },
    {
        displayName: '晚餐',
        title: 'Dinner'
    },
    {
        displayName: '小Food',
        title: 'Snacks'
    },
]

</script>

<template>
    <div class="grid w-full gap-4">
        <header class="flex items-start justify-between">
            <div class="grow">
                <p>Hi, welcome back !</p>
                <h1>Dashboard</h1>
            </div>
            <div class="w-[120px] h-[36px] bg-neutral-200"></div>
        </header>
        <main class="grid gap-4">
            <Tabs default-value="Breakfast" class="w-full">
                <TabsList class="w-full">
                    <TabsTrigger v-for="(item, index) in list" :key="index " :value="item.title" class="w-full">
                        {{ item.displayName }}
                    </TabsTrigger>
                </TabsList>
                <TabsContent v-for="(item, index) in list" :key="index " :value="item.title">
                    {{ item.title }}
                </TabsContent>
            </Tabs>
            <div class="flex items-center gap-4">
                <div v-for="(item, index) in 3" :key="index" class="w-full h-[260px] bg-neutral-200"></div>
            </div>
        </main>
        <footer>
            <div class="flex items-center gap-4">
                <div v-for="(item, index) in 3" :key="index" class="w-full h-[260px] bg-neutral-200"></div>
            </div>
        </footer>
    </div>
</template>
