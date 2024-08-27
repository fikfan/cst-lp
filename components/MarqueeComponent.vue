<template>
  <Vue3Marquee 
  :clone="true" 
  :duration="5" 
  :gradient="true" 
  :gradient-color="[248, 248, 248]" 
  gradient-length="50%">
    <img :src="Logo" width="200" height="200" alt="">
  </Vue3Marquee>
</template>

<script setup>

import Logo from '@/assets/images/logo.png'
</script>