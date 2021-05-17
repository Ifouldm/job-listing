<template>
    <div class="list">
        <JobCard v-for="job in jobData" :key="job.id" :job="job" />
    </div>
</template>

<script>
import JobCard from './JobCard.vue';
import jobData from '../data/data.json';

export default {
    data() {
        return { jobData };
    },
    components: {
        JobCard,
    },
};
</script>

<style>
.list {
    background-color: var(--LightGrayishCyan);
}
</style>
