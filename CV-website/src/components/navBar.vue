<template>
    <nav>
      <div>
        <ul>
          <li><a class="btn-primary" @click="scrollToRef('aboutMe')">
            <img class="avatar" src='../assets/img/avatar.svg'>
            <!-- 'test' text can be placed here if needed -->
          </a></li>
          
          <li><a class="btn-primary" @click="scrollToRef('myProjects')">
            <img class="avatar" src='../assets/img/projects.svg'>
          </a></li>
    
          <li><a class="btn-primary" @click="scrollToRef('publications')">
            <img class="avatar" src='../assets/img/publications.svg'>
          </a></li>
          <li><a class="btn-primary" @click="scrollToRef('certificate')">
            <img class="avatar" src='../assets/img/certificate.svg'>
          </a></li>
        </ul>
      </div>
    </nav>
    </template>
      
     
    <script>
    export default {
      name: 'navBar',
      methods: {
        scrollToRef(refName) {
          // Emit an event to notify the parent component with the refName
          this.$emit('scroll-to-ref', refName);
        }
      }
    }
    </script>