<script lang="ts">
export default {
  props: ['label', 'placeholder', 'inputValue']
}
</script>

<template>
  <div class="text-box">
    <label>{{ label }}</label>
    <input v-model="inputValue" :placeholder="placeholder" />
  </div>
</template>

<style scoped>
input {
  padding: 0 10px;
  width: var(--control-width);
}

label {
  width: var(--label-width);
}

.text-box {
  max-width: 70%;
  margin: 15px 0;
  display: flex;
  justify-content: space-between;
}
</style>