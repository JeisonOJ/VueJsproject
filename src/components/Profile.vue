<template>
    <div class="dashboard">
        <aside class="sidebar">
            <About />
            <Overview />
        </aside>
        <main class="main-content">
            <ActivityTimeline />
            <div class="connections-teams">
                <Connection />
                <Teams />
            </div>
            <ProjectList />
        </main>
    </div>
</template>
<script setup lang="ts">
import About from "./About.vue";
import Overview from "./Overview.vue";
import ActivityTimeline from "./ActivityTimeline.vue";
import Connection from "./Connection.vue";
import Teams from "./Teams.vue";
import ProjectList from "./ProjectList.vue";

</script>
<style scoped>
.dashboard {
    display: flex;
    padding: 20px;
    gap: 5%;
}

.sidebar {
    width: 25%;
    display: flex;
    flex-direction: column;
    gap: 20px;
}

.main-content {
    width: 75%;
    display: flex;
    flex-direction: column;
    gap: 20px;
}

.connections-teams {
    display: flex;
    gap: 20px;
    margin-top: 20px;
}
</style>
