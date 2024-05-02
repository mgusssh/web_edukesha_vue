<script setup>
import VHeader from "@/components/VHeader.vue"
import VFooter from "@/components/VFooter.vue"
import VServis from "@/components/VServis.vue"
import VTutorials from "@/components/VTutorials.vue"
import VHistory from "@/components/VHistory.vue"
import VPossibility from "@/components/VPossibility.vue"
import VWork from "@/components/VWork.vue"
import VDistance from "@/components/VDistance.vue"

</script>



<template>
    <v-header />
    <main>
        <v-servis />
        <v-tutorials />
        <v-history />
        <v-possibility />
        <v-work />
        <v-distance />
    </main>
    <v-footer />
</template>

<style scoped>

</style>

