<template>
<v-app>
 <div class="container ma-auto d-flex" > 
   <v-card raised outlined:loading="loading" class="mx-auto my-12" width="400"  >
      <v-row align="left">
        <v-col  cols="7">
         <v-card-title>Rate Card</v-card-title>
        </v-col>
        <v-col cols="5">
         <p class="text-center ma-0">Expiry Date</p>
         <p class="text-center ma-0">DD/MM/YYYY</p>
        </v-col>
      </v-row>
       <v-divider ></v-divider>
   <v-card-text class="pa-0">
      <v-row align="center">
        <v-col  cols="6 pa-1">
          <p class="text--disabled text-center ma-0">vessel name</p>
        </v-col>
        <v-col cols="6 pa-1">
          <p class="text--disabled text-center ma-0">XXXXX</p>
        </v-col>
      </v-row>
    </v-card-text>
    <v-card-text class="pa-0">
      <v-row align="center">
        <v-col  cols="6 pa-1">
          <p class="text--disabled text-center ma-0">Port of Loading</p>
          <p class="text-center ma-0">XXXXX</p>
        </v-col>
        <v-col cols="6 pa-1">
          <p class="text--disabled text-center ma-0">Port of Discharge</p>
          <p class="text-center ma-0">XXXXX</p>
        </v-col>
      </v-row>
    </v-card-text>
   <v-card-text class="pa-0">
      <v-row align="center">
        <v-col  cols="6 pa-1">
          <p class="text--disabled text-center ma-0">Rates By</p>
        </v-col>
        <v-col cols="6">
          <p class="text--disabled text-center ma-0">xyz</p>
        </v-col>
      </v-row>
    </v-card-text>
     <v-card-text class="pa-0">
      <v-row align="center">
        <v-col  cols="6 pa-1">
          <p class="text--disabled text-center ma-0">Service Type</p>
        </v-col>
        <v-col cols="6 pa-1">
          <p class="text--disabled text-center ma-0">a,b,c</p>
        </v-col>
      </v-row>
    </v-card-text>
 
     <v-card-text class="pa-0">
      <v-row align="center">
        <v-col  cols="6 pa-1">
          <p class="text--disabled text-center ma-0">Via ports</p>
        </v-col>
        <v-col cols="6 pa-1">
          <p class="text--disabled text-center ma-0">x ports</p>
        </v-col>
      </v-row>
    </v-card-text>
 
 <v-card-text class="pa-0">
      <v-row align="center">
        <v-col  cols="6 pa-1">
          <p class="text--disabled text-center ma-0">Sailing Date</p>
        </v-col>
        <v-col cols="6 pa-1">
          <p class="text--disabled text-center ma-0">DD/MM/YYYY</p>
        </v-col>
      </v-row>
    </v-card-text>
  
    <v-card-text class="pa-0">
      <v-row align="center">
        <v-col  cols="6 pa-1">
          <p class="text--disabled text-center ma-0">Transit time</p>
        </v-col>
        <v-col cols="6 pa-1">
          <p class="text--disabled text-center ma-0">x days</p>
        </v-col>
      </v-row>
    </v-card-text>
    
    
    
    <v-card-text class="pa-0">
      <v-row align="center">
        <v-col  cols="6 pa-1" >
          <p class="text--disabled text-center ma-0">detention free</p>
          <p class="text-center ma-0">in days</p>
        </v-col>
        <v-col cols="6 pa-1">
          <p class="text-center ma-0"><strong>FREIGHT COST</strong></p>
        </v-col>
      </v-row>
    </v-card-text>
   
  <v-card-text class="pa-0">
      <v-row align="center">
        <v-col  cols="6 pa-1">
          <p class="text--disabled text-center ma-0">Demurrage</p>
          <p class="text-center ma-0">in days</p>
        </v-col>
        <v-col cols="6 pa-1">
          <p class="text--disabled text-center ma-0">X USD</p>
        </v-col>
      </v-row>
    </v-card-text>
 

   
      <div>
        <v-row class="d-flex justify-center">
        <v-card-actions>
         <v-btn color="lime accent-2" @click="reserve">
        ADD TO QUOTE
        </v-btn>
        </v-card-actions>
        </v-row>
      </div>
    </v-card>
  </div>

<!-- add rate card -->


<div class="container d-flex ma-auto">
  <v-card raised outlined:loading="loading" class="mx-auto my-12" width="450"> 
        <v-card-title class="blue pa-2">Add New Rate</v-card-title>
       <v-divider ></v-divider>
       <v-card-text class="pa-0">
      <v-row align="center">
       <v-col  cols="6 pa-1">
          <p class=" text-center ma-0 ">Liner Name</p>
        </v-col>
        <v-col cols="6 pa-1"> <v-expansion-panel >
      <v-expansion-panel-header>Select Liner Name</v-expansion-panel-header>
      <v-expansion-panel-content>
        ........
      </v-expansion-panel-content>
    </v-expansion-panel>
        </v-col>
      </v-row>
    </v-card-text>

     <v-card-text class="pa-0">
      <v-row align="center">
       <v-col  cols="6 pa-1">
          <p class=" text-center ma-0 ">Expiry Date</p>
        </v-col>
        <v-col cols="6 pa-1">
          <v-expansion-panel >
      <v-expansion-panel-header>Select Expiry Date</v-expansion-panel-header>
      <v-expansion-panel-content>
        ........
      </v-expansion-panel-content>
    </v-expansion-panel>
        </v-col>
      </v-row>
    </v-card-text>
  <v-card-text class="pa-0">
      <v-row align="center">
       <v-col  cols="6 pa-1">
          <p class=" text-center ma-0 ">Rates By</p>
        </v-col>
        <v-col cols="6 pa-1" align-center>
         <v-text-field class="pr-5" ></v-text-field> 
        </v-col>
      </v-row>
    </v-card-text>


     <v-card-text class="pa-0">
      <v-row align="center">
       <v-col  cols="6 pa-1">
          <p class=" text-center ma-0 ">Service Type</p>
        </v-col>
        <v-col cols="6 pa-1"> <v-expansion-panel >
      <v-expansion-panel-header>Select Service Type</v-expansion-panel-header>
      <v-expansion-panel-content>
        ........
      </v-expansion-panel-content>
    </v-expansion-panel>
        </v-col>
      </v-row>
    </v-card-text>
    
        <v-card-text class="pa-0">
      <v-row align="center">
       <v-col  cols="6 pa-1">
          <p class=" text-center ma-0 ">CUSTOM RATES</p>
        </v-col>
        <v-col cols="6 pa-1">
          <v-card-actions class="d-flex justify-center"><v-btn raised class="fluid"  color="lime accent-2">Add Custom Rates</v-btn></v-card-actions>
        </v-col>
      </v-row>
    </v-card-text> 

     <v-card-text class="pa-0">
      <v-row align="center">
       <v-col  cols="6 pa-1">
          <p class=" text-center ma-0 ">SCHEDULE</p>
        </v-col>
        <v-col cols="6 pa-1">
          <v-card-actions class="d-flex justify-center"><v-btn raised class="fluid"  color="lime accent-2">Schedule</v-btn></v-card-actions>
        </v-col>
      </v-row>
    </v-card-text> 
     <v-divider></v-divider> 

     <v-row class="d-flex justify-center">
      <v-card-actions>
         <v-btn color="lime accent-2" @click="reserve">
        VIEW DETAILS
        </v-btn>
         <v-btn color="green" @click="reserve">
        DONE
        </v-btn>
        </v-card-actions>
        </v-row>
  </v-card>

</div>

  </v-app>
</template>




<script>
  export default {
    data: () => ({
      loading: false,
      selection: 1,
    }),

    methods: {
      reserve () {
        this.loading = true

        setTimeout(() => (this.loading = false), 2000)
      },
    },
  }
</script>




  