<template>
<v-container>
  <v-form ref="form" v-model="valid" lazy-validation >
    <v-select
      v-model="dataList.subject"
      :items="items1"
      :rules="[(v) => !!v || 'Item is required']"
      label="cs code"
      required
    ></v-select>

    <v-btn :disabled="!valid" color="purple lighten-3"  @click="save" width="80">
      Submit
    </v-btn>
    <br>
    <br>
    
  </v-form>


  <v-card max-width="800" class="mx-auto">
    <v-toolbar color="pink lighten-4" dark>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>TO DO</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-toolbar>
    <v-list>
      <v-list-item v-for="(item,index) in List" :key="index">
        <v-list-item-content>
          <v-list-item-title v-text="item.name"></v-list-item-title>
        </v-list-item-content>
        <v-btn @click="Del(index)" color="light-green accent-1">Delete</v-btn>
      </v-list-item>
    </v-list>
  </v-card>
</v-container>
</template>

<script>
export default {
  data: () => ({
    valid: true,
    dataList: {
      subject: "",
    },
    List: [
      {
        name: "cs code",
      },
    ],
    items1: ["cs code1", "cs code2", "cs code3", "cs code4"],
  }),
  methods: {
    save() {
      this.List.push({
        name: this.dataList.subject,
      });
    },
    Del(n){
        this.List.splice(n,1);
        }
  },
};
</script>

<style></style>
