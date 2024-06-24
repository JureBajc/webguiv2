<template>
  <v-app>
      <v-layout class="rounded rounded-md">
        <v-app-bar color="surface-variant" title="Application bar">
          <v-spacer></v-spacer>
          <div class="text-center">
            <v-menu
              open-on-click
            >
              <template v-slot:activator="{ props }">
                <v-btn
                  color="white"
                  v-bind="props"
                >
                  Dropdown
                </v-btn>
              </template>
        
              <v-list>
                <v-list-item
                  v-for="(item, index) in items"
                  :key="index"
                >
                  <v-list-item-title>{{ item.title }}</v-list-item-title>
                </v-list-item>
              </v-list>
            </v-menu>
          </div>
        </v-app-bar>


        <v-navigation-drawer>
          <v-list>
            <v-list-item title="Drawer left"></v-list-item>
          </v-list>
        </v-navigation-drawer>
    
        <v-navigation-drawer location="right">
          <v-list>
            <v-list-item> <FixTabs></FixTabs></v-list-item>
          </v-list>
        </v-navigation-drawer>
    
        <v-main class="d-flex align-center justify-center" style="min-height: 300px;">
          Main Content
        </v-main>
      </v-layout>
  </v-app>
</template>

<script>
//import SysBar from '/src/components/SysBar.vue'
import FixTabs from '/src/components/FixTabs.vue'
export default {
  name: 'App',

  components: {
    FixTabs,
   // SysBar,
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