<script lang="ts">
export default {
  props: ['label', 'buttonValues'],
  data() {
    return {
      isDisabledButton: false,
      isButtonPrimary: true,
      buttonValues: ['Yes', 'No']
    }
  },
  methods: {
    notify(value: string) {
      alert('Choosen value: ' + value)
    }
  }
}
</script>

<template>
  <div class="option-button">
    <label class="label">{{ label }}</label>
    <div class="button-wrapper">
      <button v-for="buttonValue of buttonValues"
              @click="notify(buttonValue)" 
              :disabled="isDisabledButton" 
              :class="{ button__primary: isButtonPrimary }">{{ buttonValue }}
      </button>
    </div>
  </div>
</template>

<style scoped>
.option-button {
  max-width: 70%;
  margin: 15px 0;
  display: flex;
}

button {
  min-width: var(--button-min-width);
  border-radius: var(--button-radius);
}

.button__primary {
  color: #000066;
  background-color: white;
  border-color: #000066;
}

.label {
  width: var(--label-width);
}

.button-wrapper {
  width: var(--control-width);
  display: flex;
  justify-content: space-between;
}
</style>