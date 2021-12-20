<template>
  <h1>Events For Good</h1>
  <div class="events">
    <EventCard v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from "@/components/EventCard.vue";

export default {
  name: "EventList",
  components: {
    EventCard,
  },
  data() {
    return {
      events: [
        {
          id: 5928101,
          category: "animal welfare",
          title: "Cat Adoption Day",
          description: "Find your new feline friend at this event.",
          location: "Meow Town",
          date: "January 28, 2022",
          time: "12:00",
          petsAllowed: true,
        },
        {
          id: 4582797,
          category: "food",
          title: "Community Gardening",
          description: "Join us as we tend to the community edible plants.",
          location: "Flora City",
          date: "March 14, 2022",
          time: "10:00",
          petsAllowed: true,
          organizer: "Fern Pollin",
        },
        {
          id: 8419988,
          category: "sustainability",
          title: "Beach Cleanup",
          description: "Help pick up trash along the shore.",
          location: "Playa Del Carmen",
          date: "July 22, 2022",
          time: "11:00",
          petsAllowed: false,
          organizer: "Carey Wales",
        },
        {
          id: 1234567,
          category: "stream",
          title: "Live Presidente Bolinho",
          description: "3 horas de code e bate papo",
          location: "Twitch.tv",
          date: "Nixian 17, 12021",
          time: "09:00",
          petsAllowed: true,
          organizer: "Presidente bolinho",
        },
        {
          id: 7654321,
          category: "Birthday",
          title: "Aniversário do Tairritadotio",
          description: "Dia de comemorar menos um ano de vida",
          location: "Internet",
          date: "Nixian 17, 12021",
          time: "09:00",
          petsAllowed: true,
          organizer: "Tairritadotio",
        },
      ],
    };
  },
};
</script>

<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
