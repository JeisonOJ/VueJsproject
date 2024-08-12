<script setup lang="ts">

import { ref } from 'vue';
import Profile from './Profile.vue';
import Team from './Team.vue';
import Projects from './Projects.vue';
import Connections from './Connections.vue';

const page = ref('profile');
const changePage = (newPage: string) => {
    page.value = newPage;
}

const classActive = (currentPage: string) => {
    return {
        active: page.value === currentPage
    }
}
</script>
<template>

    <div class="header">
        <input type="text" placeholder="Search" class="search-bar">
        <div class="header-icons">
            <i class='bx bx-world' ></i>
            <i class='bx bx-sun'></i>
            <i class='bx bxs-bell-ring' ></i>
            <img src="/userProfile.png" alt="Profile" class="profile-icon">
        </div>
    </div>

    <div class="profile-header">
        <img src="/backProfile.png" alt="Background" class="background-image">
        <div class="profile-details">
            <img src="/userProfile.png" alt="John Doe" class="profile-pic">
            <div>
                <h1>John Doe</h1>
                <div class="info">
                    <p class="title"><i class='bx bx-palette' ></i>  UX Designer</p>
                    <p class="location"><i class='bx bx-current-location' ></i>   Vatican City</p>
                    <p class="joined-date"><i class='bx bx-calendar' ></i>  Joined April 2021</p>
                </div>
            </div>
            <button class="connected-button">Connected</button>
        </div>
    </div>

    <div class="menu">
        <button @click="changePage('profile')" :class="classActive('profile')"><i class='bx bx-user-pin'></i>  Profile</button>
        <button @click="changePage('team')" :class="classActive('team')"><i class='bx bxs-universal-access' ></i>  Team</button>
        <button @click="changePage('projects')" :class="classActive('projects')"><i class='bx bxs-briefcase'></i>  Projects</button>
        <button @click="changePage('connections')" :class="classActive('connections')"><i class='bx bx-cog' ></i>  Connections</button>
    </div>

    <div class="content">
        <div v-if="page === 'profile'">
            <Profile />
        </div>
        <div v-if="page === 'team'">
            <Team />
        </div>
        <div v-if="page === 'projects'">
            <Projects />
        </div>
        <div v-if="page === 'connections'">
            <Connections />
        </div>
    </div>

</template>
<style scoped>
.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 20px;
    background-color: #fff;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);


}

i{
    color: #222;
}



.search-bar {
    padding: 5px 10px;
    font-size: 16px;
    border: 1px solid #ddd;
    border-radius: 5px;
}

.header-icons {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 18%;
}

.header-icons span,
.header-icons .profile-icon {
    margin-left: 15px;
    font-size: 20px;
    cursor: pointer;
}

.profile-icon {
    width: 30px;
    height: 30px;
    border-radius: 50%;
}

.profile-header {
    position: relative;
    text-align: center;
}

.background-image {
    width: 100%;
    height: 150px;
    object-fit: cover;
}

.profile-details {

    display: flex;
    text-align: center;
    justify-content: space-around;
    background-color: #fff;


}

.profile-pic {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    border: 5px solid #fff;
    position: relative;
    top: -20px;
    
}

.profile-details h1 {
    margin: 10px 0 5px 0;
    font-size: 24px;
    color: #222;
    text-align: start;
}

.info{
    display: flex;
    gap: 36px;
}

.profile-details .title,
.profile-details .location,
.profile-details .joined-date {
    font-size: 14px;
    color: #888;
    margin: 2px 0;
}

.connected-button {
    padding: 8px 20px;
    font-size: 16px;
    background-color: #6c5ce7;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    margin-top: 10px;
    height: 40px;
    align-self: center;
    color: #f0f0f0;
}

.connected-button:hover {
    background-color: #5245cc;
}

.menu {
    display: flex;
    justify-content: center;
    background-color: #fff;
    padding: 10px 0;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.menu button {
    background: none;
    border: none;
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    color: #6c5ce7;
    border-radius: 5px;
}

.menu button:hover {
    background-color: #f0f0f0;
    
}

.active {
    background-color: #6c5ce7 !important;
    color:#f0f0f0 !important;
    
}
</style>