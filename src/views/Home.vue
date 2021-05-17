<template>
    <Filters />
    <JobList />
    <Attribution />
</template>

<script>
import Attribution from '../components/Attribution.vue';
import Filters from '../components/Filters.vue';
import JobList from '../components/JobList.vue';
export default {
    components: {
        Filters,
        JobList,
        Attribution,
    },
};
</script>

<style></style>
