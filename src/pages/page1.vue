<template>
  <q-page>
    <div class="container">
      <img class="image" src="src\image\kot.jpeg" alt="Кот">

    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage'
})
</script>
<style>
.container {
  max-width: 300px;
  border: 2px brown;
  max-height: 300px;
  margin: 0 auto;
}

.image {
  width: 300px;
  height: 300px;
  object-fit: cover;
}
</style>
