<template>
    <div class="label">
        {{ label }}
    </div>
</template>

<script>
export default {
    props: ['label'],
};
</script>

<style scoped>
.label {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    font-weight: bold;
    color: var(--DesaturatedDarkCyan);
    font-size: 0.6rem;
    padding: 0.4rem;
    margin: 0 0.3rem;
    border-radius: 0.3rem;
    background-color: var(--LightGrayishCyan);
}

.label:hover {
    cursor: pointer;
    color: var(--LightGrayishCyan);
    background-color: var(--DesaturatedDarkCyan);
}
</style>
