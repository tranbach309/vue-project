<script setup lang="ts">
import Header from '../components/Header.vue'
import Footer from '../components/Footer.vue'
import TextBox from '../components/TextBox.vue'
import OptionButton from '../components/OptionButton.vue'
</script>

<template>
  <main>
    <Header/>

    <TextBox label="Your registration number" placeholder="REG"/>
    <TextBox label="Surname" inputValue="Bach"/>
    <TextBox label="Lastname"/>
    <OptionButton label="Gender" buttonValues="['Men', 'Women']"/>

    <Footer/>
  </main>
</template>
