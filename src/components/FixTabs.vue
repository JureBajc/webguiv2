<template>

    <div class="l-flex flex-row justify-end">
        <v-tabs
        v-model="tab"
        bg-color="surface-variant"
        fixed-tabs=""
        align-with-title=""
    >
        <v-tab text="Device0" value="opt1"></v-tab>
        <v-tab text="Test2" value="opt2"></v-tab>
    </v-tabs>

        <v-tabs-window v-model="tab">
            <v-tabs-window-item value="opt1">
                <v-card flat>
                    <v-card-text>
                        <div class="bg-surface-variant rounded-pill" style="height: 64px; width: 164px;"></div>
                    </v-card-text>
                </v-card>
            </v-tabs-window-item>


            <v-tabs-window-item value="opt2">
                <v-card flat>
                    <v-card-text>
                        <p>Toerija2</p>
                    </v-card-text>
                </v-card>
            </v-tabs-window-item>

        </v-tabs-window>
    </div>
</template>

<script>
  export default {
    data: () => ({
      tab: 'option-1',
    }),
  }
</script>