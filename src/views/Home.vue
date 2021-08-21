<template>
  <div class="events-form">
    <h1>Next Transmitions</h1>
    <EventCard v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from "@/components/EventCard.vue";

export default {
  name: "Home",
  components: {
    EventCard,
  },
  data() {
    return {
      events: [
        {
          id: 123456,
          category: "survival horror",
          title: "Play Resident Evil 7",
          description: "Watch me play this awesome horror game!",
          location: "Twitch Channel",
          date: "12/05/2021",
          time: "22:00",
          player: "Urmatawil",
        },
        {
          id: 123457,
          category: "survival horror",
          title: "Play Outlast 2",
          description: "Watch me play this scary game!",
          location: "Twitch Channel",
          date: "17/05/2021",
          time: "23:00",
          player: "Urmatawil",
        },
        {
          id: 123458,
          category: "FPS",
          title: "Play Battlefield 2424",
          description: "Watch me play the new game from this franchise",
          location: "Twitch Channel",
          date: "24/08/2021",
          time: "16:00",
          player: "Urmatawil",
        },
      ],
    };
  },
};
</script>

<style scoped>
.events-form {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
