<template>
  <q-layout view="lHh Lpr lFf">
    <q-header>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />


      </q-toolbar>
      <div class="q-px-lg q-px-xl q-mb-md">
        <div class="text-h3">Ali Test</div>
        <div class="text-subtitle1">{{todaysDate}}</div>
      </div>
      <q-img src="src/assets/wallpaper.jpg" class="header-image absolute-top"></q-img>
    </q-header>

    <q-drawer
        v-model="leftDrawerOpen"
        show-if-above
        :width="250"
        :breakpoint="600"
      >
        <q-scroll-area style="height: calc(100% - 144px); margin-top: 144px; border-right: 1px solid #ddd">
          <q-list padding>
            <q-item
              to="/todo"
              exact
              clickable v-ripple>
              <q-item-section avatar>
                <q-icon name="list" />
              </q-item-section>
              <q-item-section>
                Todo
              </q-item-section>
            </q-item>

            <q-item
              to="/content"
              exact
              clickable v-ripple>
              <q-item-section avatar>
                <q-icon name="eco" />
              </q-item-section>
              <q-item-section>
                Files
              </q-item-section>
            </q-item>

            <q-item
              to="/weather"
              exact
              clickable v-ripple>
              <q-item-section avatar>
                <q-icon name="map" />
              </q-item-section>
              <q-item-section>
                Weather
              </q-item-section>
            </q-item>

            <q-item
              to="/help"
              exact
              clickable v-ripple>
                <q-item-section avatar>
                  <q-icon name="help" />
                </q-item-section>
                <q-item-section>
                  Help
                </q-item-section>
            </q-item>
          </q-list>
        </q-scroll-area>

        <q-img class="absolute-top" src="src/assets/profile-wall.jpg" style="height: 144px">
          <div class="absolute-bottom bg-transparent">
            <q-avatar size="56px" class="q-mb-sm">
              <img src="src/assets/profile.jpg">
            </q-avatar>
            <div class="text-weight-bold">Alice</div>
            <div>@alicecrudele</div>
          </div>
        </q-img>
      </q-drawer>

    <q-page-container>
      <keep-alive>
        <router-view />
      </keep-alive>
    </q-page-container>
  </q-layout>
</template>

<script>

import { defineComponent, ref } from 'vue'

import { date } from 'quasar'

export default defineComponent({
  name: 'MainLayout',

  components: {

  },

  setup () {
    const leftDrawerOpen = ref(false)

    return {
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  },

  computed: {
    todaysDate() {
      const timeStamp = Date.now()
      return date.formatDate(timeStamp, 'dddd D MMMM')
    }
  }


})
</script>

<style lang="scss">

.header-image{
  height: 100%;
  z-index: -1;
  opacity: 0.5 white;
}

</style>
