<template>
    <div class="card">
        <div class="col">
            <img :src="job.logo" alt="Company logo" />
        </div>
        <div class="col">
            <div class="row">
                <span class="company">{{ job.company }}</span
                ><span class="badges"
                    ><Badge label="NEW!" v-if="job.new"/><Badge
                        label="FEATURED"
                        v-if="job.featured"
                /></span>
            </div>
            <div class="row">
                <span class="position">{{ job.position }}</span>
                <span class="labels">
                    <Label
                        v-for="label in labels"
                        :key="label"
                        :label="label"
                    />
                </span>
            </div>
            <div class="row details">
                <span class="timeAgo">{{ job.postedAt }}</span>
                <span class="contract">{{ job.contract }}</span>
                <span class="location">{{ job.location }}</span>
            </div>
        </div>
    </div>
</template>

<script>
import Badge from './Badge.vue';
import Label from './Label.vue';
export default {
    props: {
        job: {},
    },
    computed: {
        labels() {
            return [
                this.job.level,
                this.job.role,
                ...this.job.languages,
                ...this.job.tools,
            ];
        },
    },
    components: {
        Badge,
        Label,
    },
};
</script>

<style>
.card {
    padding: 2rem;
    margin: 2rem;
    border-radius: 0.3rem;
    background-color: #ffffff;
    box-shadow: 0.5rem 0.5rem 0.5rem hsla(180, 29%, 50%, 0.2);
    display: flex;
}

.card .selected {
    border-left: var(--DesaturatedDarkCyan);
}

.company {
    font-size: 0.8rem;
    font-weight: bold;
    color: var(--DesaturatedDarkCyan);
}

.position {
    cursor: pointer;
    font-weight: bold;
}

.position:hover {
    color: var(--DesaturatedDarkCyan);
}

.row {
    display: flex;
}

.timeAgo,
.contract,
.location {
    font-size: 0.6rem;
    color: var(--DarkGrayishCyan);
}

.details > span:not(:last-child):after {
    content: '·';
    margin: 0 0.5rem;
}
</style>
