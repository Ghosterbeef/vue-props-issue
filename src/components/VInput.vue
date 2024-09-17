<template>
    <div class="field">
        <label v-if="label" class="field__label" :for="id">{{label}}</label>
        <input :id="id" class="field__input" :placeholder="placeholder" :type="type">
        <span v-for="hint in messages" :key="hint" class="field__hint">{{hint}}</span>
    </div>
</template>

<script setup lang="ts">
interface Props {
    id?: string;
    label?: string;
    placeholder?: string;
    type?: string;
    messages?: string[];
}

withDefaults(defineProps<Props>(), {id: Math.random(), type: 'text', messages: []})
</script>

<style scoped>
.field {
    display: flex;
    flex-direction: column;
    gap: 4px;
}

.field__input {
    display: block;
    font-size: 20px;
    line-height: 24px;
    padding: 8px;
    border: none;
    border-radius: 4px;
    outline: none;
}

.field__label {
    color: #fff;
}

.field__hint {
    color: #d5d5d5;
}
</style>
