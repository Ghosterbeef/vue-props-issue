<template>
    <div class="content">
        <div class="content-group">
            <VInput label="Поле ввода 1" placeholder="Тут"/>
            <VInput label="Поле ввода 2" placeholder="Кроется"/>
            <VInput label="Поле ввода 3" placeholder="Какой-то"/>
            <VInput label="Нажми на меня" placeholder="Подвох" :messages="['Какие то странные поля ввода']"/>
        </div>
    </div>
</template>

<script setup lang="ts">
import VInput from "@/components/VInput.vue";
</script>

<style>
*,*::before,*::after {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background-color: #333;
    font-size: 16px;
    line-height: 20px;
    font-family: sans-serif;
}

.content {
    margin-inline: auto;
    width: min(85%, 750px);
}

.content-group {
    display: flex;
    flex-direction: column;
    gap: 20px;
}
</style>
