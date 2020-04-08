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
    <v-card-actions>
      <v-spacer></v-spacer>
      <v-btn icon @click="show = !show">
        <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
      </v-btn>
    </v-card-actions>

    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>
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
       
      </div>
    </v-expand-transition>
 
     
 

   
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
  <v-card raised outlined:loading="loading" class="mx-auto my-12" width="450" > 
        <v-card-title class="blue pa-2">Add New Rate</v-card-title>
       <v-divider ></v-divider>
       <v-card-text class="pa-0">
      <v-row align="center">
       <v-col  cols="6 pa-2">
        <v-card-actions><v-select
          :items="items"
          label="Liner Name"
          class="px-1"
        ></v-select>
        </v-card-actions>
       
        </v-col>
        <v-col cols="6 pa-2">
       <v-card-actions><v-select
          :items="items"
          label="Sailing Date"
          class="px-1"
        ></v-select>
        </v-card-actions>
        </v-col>
      </v-row>
    </v-card-text>

    <v-card-text class="pa-0">
      <v-row align="center">
       <v-col  cols="6 px-6">
          <v-text-field label="Port Of Loading"></v-text-field> 
        </v-col>
        <v-col cols="6 px-6" align-center>
         <v-text-field label="Port Of Discharge"></v-text-field> 
        </v-col>
      </v-row>
    </v-card-text>

    <v-card-actions>
      <v-spacer></v-spacer>
      <v-btn icon @click="show = !show">
        <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
      </v-btn>
    </v-card-actions>

     <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>

     <v-card-text class="pa-0">
      <v-row align="center">
       <v-col  cols="6 px-5">
           <v-text-field label="Via Ports"></v-text-field> 
        </v-col>
        <v-col cols="6 pa-1">
         <v-card-actions><v-select
          :items="items"
          label="Expiry Date"
          class="px-1"
        ></v-select>
        </v-card-actions>
        </v-col>
      </v-row>
    </v-card-text>
  <v-card-text class="pa-0">
      <v-row align="center">
       <v-col  cols="6 px-5">
        <v-text-field label="Demurrage" ></v-text-field> 
        </v-col>
        <v-col cols="6 pa-1" align-center>
         <v-text-field class="pr-5" label="Rates By" ></v-text-field> 
        </v-col>
      </v-row>
    </v-card-text>


     <v-card-text class="pa-0">
      <v-row align="center">
       <v-col  cols="6 px-5">
         <v-text-field label="Detention Free"></v-text-field> 
        </v-col>
        <v-col cols="6 pa-1"> <v-card-actions><v-select
          :items="items"
          label="Service Type"
          class="px-1"
        ></v-select>
        </v-card-actions>
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
     </div>
    </v-expand-transition>
   

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

<!-- add rate card -->


<div class="container d-flex ma-auto">
  <v-card raised outlined:loading="loading" class="mx-auto my-12" width="450"> 
     <v-system-bar class=" white pa-5">
      <v-spacer><span class="blue pa-2">special Offer</span></v-spacer> 
      <v-icon>mdi-pencil</v-icon>      
       <v-icon>mdi-share-variant</v-icon>
       <v-icon>mdi-delete</v-icon>
    </v-system-bar>
    <v-divider></v-divider>
      <v-row>
        <v-card-text class="text-center"><h2>Carrier Company with LOGO </h2></v-card-text>
        <v-card-text class="text-center pa-0" ><p class="pa-0 ma-0">expires in <span class="red--text">x days</span></p></v-card-text>
      </v-row>
    <v-divider></v-divider>
     
     <v-card-text class="pa-0">
      <v-row align="center">
        <v-col  cols="6 pa-1">
          <p class="text-center ma-0">Service</p>
        </v-col>
        <v-col cols="6 pa-1">
          <p class=" text-center ma-0 font-weight-black">BTL Turclain Service</p>
        </v-col>
      </v-row>
    </v-card-text>
    
     <v-card-text class="pa-0">
      <v-row align="center">
        <v-col  cols="6 pa-1">
          <p class=" text-center ma-0">Via <span class="font-weight-black">xyz port</span></p>
        </v-col>
        <v-col cols="6 pa-1">
          <p class=" text-center ma-0">takes <span class="font-weight-black">x days</span></p>
        </v-col>
      </v-row>
    </v-card-text>
   
 <v-card-text class="pa-0">
      <v-row align="center">
        <v-col  cols="6 pa-1">
          <p class=" text-center ma-0">Next Sailing On</p>
        </v-col>
        <v-col cols="6 pa-1">
          <p class="font-weight-black text-center ma-0">DD/MM/YYYY</p>
        </v-col>
      </v-row>
    </v-card-text>
    <v-divider></v-divider>
   <v-row class="text-center">
    <v-card-text> <h1>$790</h1>
     <p>landing cost per container</p>
     <br>
     <h2><v-btn class="blue--text">VIEW BREAKDOWN</v-btn></h2>
    </v-card-text>
   </v-row>
   <v-divider></v-divider>
      <v-card-actions>
         <v-btn block tile color="green">
        ADD TO QUOTE
        </v-btn>
        
        </v-card-actions>
  </v-card>

</div>

  </v-app>
</template>




<script>
  export default {
    data: () => ({
      loading: false,
      selection: 1,
      show: false
    }),
    

    methods: {
      reserve () {
        this.loading = true

        setTimeout(() => (this.loading = false), 2000)
      },
    },
  }
</script>




  