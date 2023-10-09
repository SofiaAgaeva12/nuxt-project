<template>
  <div v-if="timer">
    Processing navigation in 0.{{ timer }}s
    <p>Counter: {{ counter }}</p>
    <p>
      <button @click="counter--">-</button>
      <button @click="counter++">+</button>
    </p>
    <p>Same Counter: {{ sameCounter }}</p>
  </div>
  <external></external>
  <footer>

  </footer>
</template>

<script>
export default {
  name: "strange"
}
  import External from "/pages/external.vue";

  const counter = useState('counter', () => Math.round(Math.random() * 100))
  const sameCounter = useState('counter')
  const route = useRoute()
  const timer = useState('timer', () => 0)
</script>

<style scoped>
nav, footer {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1rem;
}
.layouts {
  padding: 1rem;
}
</style>