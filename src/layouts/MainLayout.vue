<template>
  <q-layout view="lHh Lpr lFf">
    <q-header style="background: transparent">
      <q-toolbar style=" padding: 0 5%" class="row justify-between">

        <div style="height: 100px; width: 100px;"> <q-img src="Homepage/logo.png" /> </div>

        <ul style="line-style: none; width: 50%" class="row justify-center q-mx-auto align-items">
          <li style="width: 20%; margin: 0 auto"> <router-link to="#"> BUY </router-link> </li>
          <li style="width: 20%; margin: 0 auto"> <router-link to="#"> SELL </router-link> </li>
          <li style="width: 20%; margin: 0 auto"> <router-link to="#"> AGENT FINDER </router-link> </li>
          <li style="width: 20%; margin: 0 auto"> <router-link to="#"> BLOG </router-link> </li>
        </ul>

        <div class="row justify-evenly" style="width:20%">
          <q-btn label="SIGN UP" class="bg-blue" style="margin: 0 3%; width: 40%" color="white" />
          <q-btn label="LOG IN" class="bg-white" style="margin: 0 3%; width: 40%" color="blue" />
        </div>
      </q-toolbar>
    </q-header>

    <!-- <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
    >
      <q-list>
        <q-item-label
          header
        >
          Essential Links
        </q-item-label>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer> -->

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'



export default defineComponent({
  name: 'MainLayout',

  components: {
    // EssentialLink
  },

  data () {
    // const leftDrawerOpen = ref(false)

    return {

    }
  }
})
</script>
