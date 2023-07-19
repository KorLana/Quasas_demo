<template>
  <q-page-container style="background-color: #0a0a12">
    <div class="person_container">
      <q-img class="person_image" src="src\image\Персонажи.png" />
    </div>
    <div>
      <q-img ratio class="title_image" src="src\image\НАЙтИ СЕБЯ В АЙТИ.png" />
    </div>
    <router-view />
    <div class="title_container">
      <p class="title_text"> Самый недушный курс профориентации для тех, кто вместо того, чтобы читать про
        IT-профессии, готов попробовать их
        все на практике</p>
    </div>
  </q-page-container>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage'
})
</script>
<style>
.person_container {
  max-width: 1440px;
  margin: 0 auto;
  padding-top: 30px;
  background-color: #0a0a12;
  position: relative;
  z-index: 15;
  opacity: 0.7;
}

.person_image {
  width: 100%;
  object-fit: cover;

}

.title_image {
  max-width: 1200px;
  object-fit: cover;
  margin-top: -75%;
  left: 10%;
  z-index: 1;


}

.title_container {
  max-width: 1440px;
  margin: 0 auto;
  background-color: #0a0a12;

}

.title_text {
  max-width: 1400px;
  padding: 10px;
  color: white;
  font-size: 26px;
  text-align: center;
}
</style>
