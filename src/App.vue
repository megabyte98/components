<template>
<v-app>
  <v-container class="fluid"> 
    <v-row>
      <v-spacer></v-spacer>
    <v-btn  class="mx-12"  @click="addRow">ADD LEG</v-btn>
    </v-row>
    <v-card 
    class="overflow-y-auto ma-9 pa-11"
       style="height:500px; max-width:auto">
    <v-container class="overflow-y-auto ma-9" v-scroll:#scroll-target="onScroll"
        align="center"
        justify="center"
        style="height: 400px"
         v-for="(value,index) in rows" :key="index">
      <v-row>
      <v-col cols="2">
      <v-text-field v-model="value.name"/>
      </v-col>
      <v-col cols="2">
      <v-btn><v-icon color="red">mdi-delete</v-icon></v-btn>
      </v-col>
      <v-col cols="7" align="end">
      <p pa-5>x profit</p>
      </v-col>
      <v-col cols="1"></v-col>
      </v-row>
      <ledger-table  v-scroll:#scroll-target="onScroll"
        align="center"
        justify="center"
        style="height: 400px" :id="index"></ledger-table>
    </v-container>
    </v-card> 
    <v-row>
      <v-col cols="3"></v-col>
      <v-col cols="3"><h3>PROFIT = </h3></v-col>
      <v-col cols="3"></v-col>
      <v-col cols="3"><v-btn rounded outlined class="yellow"><v-icon>mdi-check</v-icon>DONE</v-btn></v-col>
    
    </v-row>
  </v-container>
  </v-app>
</template>
 
<script>

import ledgerTable from "./app2.vue";
export default {
  components: { ledgerTable },
  data: () => ({
    rows: []
  }),

 
  methods: {
   
    addRow() {
      this.rows.push({
        name: ""
      });
     
    }
 
  }
  ,
 
};
</script>



  