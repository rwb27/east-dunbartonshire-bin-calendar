<script setup>
import { onMounted, ref } from 'vue'

import Calendar from 'js-year-calendar'
import 'js-year-calendar/dist/js-year-calendar.css'

defineProps({
  greenBinFirstDay: {
    type: String,
    required: true,
  },
  /*grayBinFirstDay: {
    type: String,
    required: true,
  },
  recyclingBinFirstDay: {
    type: String,
    required: true,
  },
  foodBinFirstDay: {
    type: String,
    required: true,
  }*/
})

const calendar = ref(null)

onMounted(() => {
  console.log('cal', calendar)
  new Calendar(calendar.value)
})
</script>

<template>
  <div class="calendarContainer">
    <h2>Calendar</h2>
    <div ref="calendar"></div>
  </div>
</template>

<style scoped></style>
