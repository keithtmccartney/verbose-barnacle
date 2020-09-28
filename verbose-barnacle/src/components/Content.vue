<template>
    <div>
        <p>The child components of Content.vue are:</p>
        <ul>
            <li v-for="child in childComponents">{{ child }}</li>
        </ul>
    </div>
</template>

<script>
export default {
    data() {
        return {
            childComponents: ['TempVarChart.vue', 'Highlights.vue']
        }
    },
    methods: {

    },
    computed: {

    },
}
</script>

<style>
    
</style>