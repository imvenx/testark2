<template>
  <!-- <router-view /> -->
  <div>isAbsolute: {{ isAbsolute }}</div>
  <div>isSupported: {{ isSupported }}</div>
  <div>alpha: {{ alpha?.toFixed(3) }}</div>
  <div>beta: {{ beta?.toFixed(3) }}</div>
  <div>gamma: {{ gamma?.toFixed(3) }}</div>

  <div>acceleration: {{ acceleration }}</div>
  <div>accelerationIncludingGravity: {{ accelerationIncludingGravity }}</div>
  <div>rotationRate: {{ rotationRate }}</div>
  <div>interval: {{ interval?.toFixed(3) }}</div>
</template>

<script setup lang="ts">
import { useDeviceOrientation } from '@vueuse/core'
import { useDeviceMotion } from '@vueuse/core'

const {
  isAbsolute,
  isSupported,
  alpha,
  beta,
  gamma,
} = useDeviceOrientation()


const {
  acceleration,
  accelerationIncludingGravity,
  rotationRate,
  interval,
} = useDeviceMotion()
</script>

<style>
* {
  text-align: center;
  color: greenyellow;
  background-color: black;
  font-size: larger;
}
</style>