<template>
    <div class="badge">
        {{ label }}
    </div>
</template>

<script>
export default {
    props: ['label'],
};
</script>

<style>
.badge {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    font-weight: bold;
    color: #ffffff;
    font-size: 0.5rem;
    margin: 0 0.3rem;
    padding: 0.2rem 0.3rem;
    border-radius: 1rem;
    background-color: var(--DesaturatedDarkCyan);
}
</style>
