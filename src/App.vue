<template>
  <!-- <router-view /> -->
  <pre>isAbsolute: {{ isAbsolute }}</pre>
  <pre>isSupported: {{ isSupported }}</pre>
  <pre>alpha: {{ alpha?.toFixed(3) }}</pre>
  <pre>beta: {{ beta?.toFixed(3) }}</pre>
  <pre>gamma: {{ gamma?.toFixed(3) }}</pre>

  <pre>acceleration: {{ JSON.stringify(acceleration) }}</pre>
  <pre>accelerationIncludingGravity: {{ JSON.stringify(accelerationIncludingGravity) }}</pre>
  <pre>rotationRate: {{ JSON.stringify(rotationRate) }}</pre>
  <pre>interval: {{ interval?.toFixed(3) }}</pre>
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
  margin-left: 1em;
  color: greenyellow;
  background-color: black;
  font-size: larger;
}
</style>