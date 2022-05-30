<template>
  <q-page>
    <Homepage />
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'
import Homepage from 'pages/Homepage.vue'

export default defineComponent({
  name: 'IndexPage',
  components:{
    Homepage
  }
})
</script>
