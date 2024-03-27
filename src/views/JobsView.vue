<template>
    <div class="about">
      <h1>This is the jobs page</h1>
      <div v-for="job in jobs" v-bind:key="job.id">
        <router-link :to="{ name: 'JobDetails', params: { id: job.id, job: job } }">
            {{ job.title }}
        </router-link>
          
      </div>
    </div>
  </template>

  <script>
  export default {
    data() {
        return {
            jobs : [
            { 
                id: 1,
                title: 'Préparer test',
                details: 'lorem ipsum'
            },
            { 
                id: 2,
                title: 'Peindre la façade',
                details: 'lorem ipsum' 
            }
         ]
        }
    }  
  }
  </script>