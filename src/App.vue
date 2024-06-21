<template>
  <v-app>
    <SysBar/>
    <v-main>
      <FixTabs/>
    </v-main>
  </v-app>
</template>

<script>
import SysBar from '/src/components/SysBar.vue'
import FixTabs from '/src/components/FixTabs.vue'
export default {
  name: 'App',

  components: {
    FixTabs,
    SysBar,
  },

  data: () => ({
    //
  }),
}
</script> 