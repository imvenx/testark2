<template>
  <!-- <router-view /> -->
  <div>isAbsolute: {{ isAbsolute }}</div>
  <div>isSupported: {{ isSupported }}</div>
  <div>alpha: {{ alpha }}</div>
  <div>beta: {{ beta }}</div>
  <div>gamma: {{ gamma }}</div>
</template>

<script setup lang="ts">
import { useDeviceOrientation } from '@vueuse/core'

const {
  isAbsolute,
  isSupported,
  alpha,
  beta,
  gamma,
} = useDeviceOrientation()
</script>

<style>
* {
  text-align: center;
  color: greenyellow;
  background-color: black;
  font-size: larger;
}
</style>