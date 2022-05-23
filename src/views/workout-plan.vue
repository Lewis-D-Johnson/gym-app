<template>
    <v-card>
    <v-tabs
      v-model="tab"
      background-color="primary"
      dark
    >
      <v-tab
        v-for="item in items"
        :key="item.tab"
      >
        {{ item.tab }}
      </v-tab>
    </v-tabs>

    <v-tabs-items v-model="tab">
      <v-tab-item
        v-for="item in items"
        :key="item.tab"
      >
        <v-card flat>
          <v-card-text>{{ item.content }}</v-card-text>
          <v-list
            two-line
            flat
            >
            <v-list-item-group
                v-model="settings"
                multiple
              >
                <v-list-item>
                <template v-slot:default="{ active, }">
                    <v-list-item-action>
                    <v-checkbox
                        :input-value="active"
                        color="primary"
                    ></v-checkbox>
                    </v-list-item-action>

                    <v-list-item-content>
                    <v-list-item-title>Bench Press</v-list-item-title>
                    <v-list-item-subtitle>1-2 warm up sets (light weight), 3x working sets 8-12 reps</v-list-item-subtitle>
                    <v-col
                        cols="12"
                        sm="6"
                        md="4"
                    >
                    <v-text-field
                        label="WEIGHT"
                        placeholder="12.5kg"
                        filled
                        rounded
                        dense
                    ></v-text-field>
                    </v-col>
                    </v-list-item-content>
                </template>
                </v-list-item>
            </v-list-item-group>
          </v-list>
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </v-card>
</template>
<script>
  export default {
    data () {
      return {
        tab: null,
        items: [
          { tab: 'One', content: 'Tab 1 Content' },
          { tab: 'Two', content: 'Tab 2 Content' },
          { tab: 'Three', content: 'Tab 3 Content' },
          { tab: 'Four', content: 'Tab 4 Content' },
          { tab: 'Five', content: 'Tab 5 Content' },
          { tab: 'Six', content: 'Tab 6 Content' },
          { tab: 'Seven', content: 'Tab 7 Content' },
          { tab: 'Eight', content: 'Tab 8 Content' },
          { tab: 'Nine', content: 'Tab 9 Content' },
          { tab: 'Ten', content: 'Tab 10 Content' },
        ],
      }
    },
  }
</script>