<template>
  <v-app>
      <v-layout class="rounded rounded-md">
        <v-app-bar color="surface-variant" title="X-Logger">
          <v-icon icon="mdi-numeric-4-circle"></v-icon>
          <v-spacer></v-spacer>

          <v-icon icon="mdi-battery" class="ms-2 col"></v-icon>
          <v-icon icon="mdi-connection" class="ms-2"></v-icon>
          <v-icon icon="mdi-lan-connect" class="ms-2"></v-icon>
          <span class="ms-2">11:00PM</span>
          <v-spacer></v-spacer>
          <DropMenu></DropMenu>
        </v-app-bar>

        <v-navigation-drawer>
          <v-list>
          <v-list-item title="Drawer left"></v-list-item>
          </v-list>
          </v-navigation-drawer>
    
        <v-navigation-drawer location="right">
          <v-list>
          <v-list-item style="border: 1px solid black;"><p>'Selected Device'</p></v-list-item>
          <v-list-item> <FixTabs></FixTabs></v-list-item>
          </v-list>
        </v-navigation-drawer>
    
        <v-main class="d-flex align-center justify-center" style="min-height: 300px;">
          <GraphArea></GraphArea>
          
        </v-main>
      </v-layout>
  </v-app>
</template>

<script>
//import SysBar from '/src/components/SysBar.vue'
import DropMenu from './components/DropMenu.vue'
import FixTabs from '/src/components/FixTabs.vue'
import GraphArea from './components/GraphArea.vue';
export default {
  name: 'App',

  components: {
    GraphArea,
    DropMenu,
    FixTabs,
    //SysBar,
  },
  data: () => ({
      items: [
        { title: 'Device0' },
        { title: 'Device1' },
        { title: 'Device2' },
        { title: 'Device3' },
      ],
    }),
}
</script> 