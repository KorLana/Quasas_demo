<template padding>
  <q-layout viev: hHh lpR fFf>
    <q-header reveal elevated>

      <q-toolbar class="header_toolbar">
        <router-link to="/"> <q-img class="logo" src="src\image\Logo Light 1T Sprint Horizontal.png" />
        </router-link>

        <q-btn id="telegram_button" icon="lab la-telegram" label="Войти в Telegram" @click="onClick" />
        <q-btn class="univer_button" @click="onClick">
          <img src="src\image\buton_B.png">
        </q-btn>
        <div>
          <q-img class="logo1" src="src\image\Logo Tsifrovie Professii.png" />
        </div>

        <q-btn glossy icon="menu" label="Выбери свою роль" @click="toggleRightDrawer" />
        <q-drawer class="menu_conteiner" v-model="rightDrawerOpen" side="right" overlay>

          <q-list>
            <q-item clickable v-ripple>
              <router-link class="menu_link1" to="/"> МЕНЕДЖЕР </router-link>
            </q-item>
            <q-item clickable v-ripple>
              <router-link class="menu_link1" to="/page1"> СИСТЕМНЫЙ АНАЛИТИК </router-link>
            </q-item>
          </q-list>

        </q-drawer>
        <EssentialLink v-for="link in essentialLinks" :key="link.title" v-bind="link" />
      </q-toolbar>
    </q-header>
    <router-view />
  </q-layout>
</template>


<script>
import { defineComponent, ref } from 'vue'
import EssentialLink from 'components/EssentialLink.vue'

const linksList = [

]

export default defineComponent({
  name: 'MainLayout',

  components: {
    EssentialLink
  },

  setup() {
    const rightDrawerOpen = ref(false)

    return {
      essentialLinks: linksList,
      rightDrawerOpen,
      toggleRightDrawer() {
        rightDrawerOpen.value = !rightDrawerOpen.value
      }
    }
  }
})
</script>

<style>
.header_toolbar {
  height: 150px;
  justify-content: space-between;
}

.logo {
  min-width: 200px;
  margin: 10px;
}

.logo1 {
  min-width: 113px;
  margin: 10px;
}

.menu_conteiner {
  width: 200px;
  height: 200px;
  background-color: #1d1d1dc8;
}

.menu_link1 {
  margin: 10px 20px;
  color: white;
  text-decoration: none;
  display: block;
}

#telegram_button {
  max-width: 290px;
  border-radius: 5px;
  box-shadow: 0px 0px 20px 0px rgba(240, 0, 250, 1), 0px 0px 10px 0px rgba(0, 25, 240, 1);
  border: 2px solid;
  border-image-source: linear-gradient(90deg, #C800C8 0%, #9600FF 100%, #9600FF 100%);
}

.univer_button {
  width: 250px;
}

@media (max-width: 768px) {
  body.lock {
    overflow: hidden;
  }
}
</style>
