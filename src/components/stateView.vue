<script setup>
import { ref } from 'vue';

const navItems = [
    { label: 'Stage 1', stage: false },
    { label: 'Stage 2', stage: false },
    { label: 'Stage 3', stage: false },
    { label: 'Stage 4', stage: false },
    { label: 'Stage 5', stage: false },
    { label: 'Stage 6', stage: false },
];

const activeIndex = ref(0); // Always start at index 0

function setActive(index) {
    navItems[index].stage = true; // Toggle the stage state
    activeIndex.value = index < navItems.length - 1 ? index + 1 : index; // Move to the next stage
}

function setUnActive(index) {
    navItems[index].stage = false;
    activeIndex.value = index > 0 ? index - 1 : 0; // Move to the previous stage
}

</script>

<template>
    <div class="container">
        <ul class="nav nav-pills nav-fill mb-3">
            <li class="nav-item" v-for="(item, index) in navItems" :key="index">
                <a class="nav-link" :class="{ active: activeIndex === index, pass: item.stage === true }">
                    {{ item.label }}
                </a>
            </li>
        </ul>
        <div class="tab-content">
            <div class="tab-pane fade show active">
                <div class="container d-flex justify-content-center align-items-center"
                    style="height: 650px; width: 100%;">
                    <p>Stage Content</p>
                </div>
            </div>
        </div>
        <div class="d-flex justify-content-between mt-3">
            <button class="btn btn-primary" @click="setUnActive(activeIndex)" :disabled="activeIndex === 0">
                Previous
            </button>
            <button class="btn btn-primary" @click="setActive(activeIndex)" :disabled="activeIndex === navItems.length">
                Next
            </button>
        </div>
    </div>
</template>

<style scoped>
.pass {
    pointer-events: none;
    opacity: 0.6;
    color: white;
    background-color: green;
}
</style>
