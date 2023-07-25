<script setup>
const bgOrange = 'background-color: rgb(251 146 60)'
const bgBlue = 'background-color: rgb(96 165 250)'
const bgGreen = 'background-color: rgb(74 222 128)'

const bgGreen2 = 'background-color: rgb(20 83 45)'
const bgRed = 'background-color: rgb(127 29 29)'

const weekday = true

const colors = {
  backgroundColor: 'rgb(254 202 202)',
  borderColor: 'rgb(185 28 28)',
  color: 'color: rgb(127 29 29)'
}

const messageType = "success"

if('success' === messageType) {
  colors.backgroundColor = 'rgba(204, 251, 241, 1)',
  colors.color = 'rgba(19, 78, 74, 1)',
  colors.borderColor= 'rgba(20, 184, 166, 1)'
}
</script>

<template>
  <section class="max-width: 1280px mx-auto">
    <h1 class="text-center text-2xl py-10">Class & Style Binding</h1>
    <section class="flex space-x-10">
      <div class="w-1/3 h-16" :style="bgOrange"></div>
      <div class="w-1/3 h-16" :style="bgBlue"></div>
      <div class="w-1/3 h-16" :style="bgGreen"></div>
    </section>

    <section class="mt-10">
      <div class="h-16 flex justify-center text-white items-center" :style="weekday===true ? bgGreen2 : bgRed">
      {{ weekday===true ? "It's Weekday Day" : "It's Weekend Day" }}
      </div>
    </section>

    <section class="mt-10">
      <div class=" border-t-4 px-4  h-16 rounded-b shadow-md" :style="colors">
        <p class="font-bold">Our privacy policy has changed</p>
        <p class="text-sm">Make sure you know how these changes affect you.</p>
      </div>
    </section>
  </section>
</template>

<style scoped></style>
