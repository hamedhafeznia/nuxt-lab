<template>
  <div>
    <EventCard 
        v-for="(event, index) in events"
        :key="index"
        :event="event"
        :data-index="index"
    />
  </div>
</template>

<script>
import EventCard from "../../components/EventCard.vue"
    export default {
    
    async asyncData({ $axios, error }) {
        try {
        const response = await $axios.get('https://jsonplaceholder.typicode.com/todos');
        return {
            events: response.data
        }
        } catch(e) {
            console.log(e)
        }
    },


    components: { EventCard }
}
</script>