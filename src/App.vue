<template>
<v-app>
 <!-- <div class="container d-flex ma-auto">
  <v-card raised outlined:loading="loading" class="mx-auto my-12" width="450"> 
     <v-system-bar  class="pa-6 yellow black--text">
      <v-card-text class="pa-2 text-center"><h1>Carrier Company</h1></v-card-text>
      <v-icon color="black" medium>mdi-pencil</v-icon>
      <v-icon color="black" medium>mdi-delete</v-icon>
    </v-system-bar>
    <v-divider></v-divider>
      <v-row>
        <v-card-text class="text-center"><h2>LOGO</h2></v-card-text>
        <v-card-text class="text-center pa-0" ><p class="pa-0 ma-0">expires in <span class="red--text">{{item.expiryDate}}</span></p></v-card-text>
      </v-row>
    <v-divider></v-divider>
   <v-card-text class="pa-0">
      <v-row align="center">
        <v-col  cols="6 pa-1">
          <p class=" text-center ma-0">Liner name</p>
        </v-col>
        <v-col cols="6 pa-1">
          <p class=" text-center ma-0">{{item.liner}}</p>
        </v-col>
      </v-row>
    </v-card-text>
    <v-card-text class="pa-0">
      <v-row align="center">
        <v-col  cols="6 pa-1">
          <p class=" text-center ma-0">Port of Loading</p>
          <p class="text-center ma-0">{{item.originPort}}</p>
        </v-col>
        <v-col cols="6 pa-1">
          <p class=" text-center ma-0">Port of Discharge</p>
          <p class="text-center ma-0">{{destinationPort}}</p>
        </v-col>
      </v-row>
    </v-card-text>
   <v-card-text class="pa-0">
      <v-row align="center">
        <v-col  cols="6 pa-1">
          <p class=" text-center ma-0">Rates By</p>
        </v-col>
        <v-col cols="6">
          <p class=" text-center ma-0">{{item.ratesBy}}</p>
        </v-col>
      </v-row>
    </v-card-text>
     <v-card-text class="pa-0">
      <v-row align="center">
        <v-col  cols="6 pa-1">
          <p class=" text-center ma-0">Service Type</p>
        </v-col>
        <v-col cols="6 pa-1">
          <p class=" text-center ma-0">{{item.serviceType}}</p>
        </v-col>
      </v-row>
    </v-card-text>
    <v-divider></v-divider>
    <v-card-actions>
       <v-card-text class="pa-3">
      <v-row align="center">
        <v-col  cols="6 pa-1" class="green yellow--text" >
          <p class="text-center ma-0"><strong>Profit</strong></p>
          <p class="text-center ma-0">{{item.totalProfit}}</p> 
        </v-col>
        <v-col cols="6 pa-1" class="red yellow--text">
          <p class="text-center ma-0 "><strong>FREIGHT COST</strong></p>
         <p class="text-center ma-0">x$</p> 
        </v-col>
      </v-row>
    </v-card-text>
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
          <p class=" text-center ma-0">Sailing Date</p>
        </v-col>
        <v-col cols="6 pa-1">
          <p class=" text-center ma-0">{{item.sailingDate}}</p>
        </v-col>
      </v-row>
    </v-card-text>
     <v-card-text class="pa-0">
      <v-row align="center">
        <v-col  cols="6 pa-1" >
          <p class=" text-center ma-0">detention free</p>
          <p class="text-center ma-0">{{item.detentionFree}}</p>
        </v-col>
        <v-col cols="6 pa-1">
          <p class="text-center ma-0">Vessel Name</p>
          <p class="text-center ma-0">x,y,z</p>
        </v-col>
      </v-row>
    </v-card-text>
   
  <v-card-text class="pa-0">
      <v-row align="center">
        <v-col  cols="6 pa-1">
          <p class=" text-center ma-0">Demurrage</p>
        </v-col>
        <v-col cols="6 pa-1">
          <p class=" text-center ma-0">{{item.demurrage}}</p>
        </v-col>
      </v-row>
    </v-card-text>
     <v-card-text class="pa-0">
    <v-row align="center">
       <v-col  cols="6 pa-1">
         <v-card-actions>
          <h2 class="pa-4"><v-btn class="red--text yellow">VIEW BREAKDOWN</v-btn></h2>
         </v-card-actions>
        </v-col>
        <v-col cols="6 pa-1">
          <v-card-actions class="d-flex justify-center">
             <h2><v-btn class="red--text yellow">SCHEDULE</v-btn></h2>
            </v-card-actions>
        </v-col>
      </v-row>
    </v-card-text> 
       
      </div>
    </v-expand-transition>
    <v-divider></v-divider>
      <div>
        <v-card-actions>
         <v-btn block tile dark class="blue yellow--text">
        ADD TO QUOTE
        </v-btn>
        </v-card-actions>
      </div>
    </v-card>
  </div> -->
 


  <!-- strip type kuch -->

<v-card  class="ma-auto" max-width="auto" raised >
    <v-container>
      <v-row>
      <v-col>
         <v-list-item single-line>
      <v-list-item-content>
        <v-list-item-title><v-btn inactive class="green" raised>Rates Available</v-btn></v-list-item-title>
      </v-list-item-content>
         </v-list-item>
      <v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>Created By</v-list-item-title>
        <v-list-item-subtitle>N/A</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
      </v-col>
      <v-col>
         <v-list-item single-line>
      <v-list-item-content>
        <v-list-item-title><h3>Enquiry ID</h3></v-list-item-title>
      </v-list-item-content>
         </v-list-item>
         <v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>Sales Co-ordinator</v-list-item-title>
        <v-list-item-subtitle>N/A</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
      </v-col>
      <v-col>
         <v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>Quotation No</v-list-item-title>
        <v-list-item-subtitle>N/A</v-list-item-subtitle>
      </v-list-item-content>
         </v-list-item>
          <v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>Customer Company</v-list-item-title>
        <v-list-item-subtitle>N/A</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
      </v-col>
      <v-col>
           <v-list-item single-line>
      <v-list-item-content>
        <v-list-item-title></v-list-item-title>
      </v-list-item-content>
         </v-list-item>
            <v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>Created On</v-list-item-title>
        <v-list-item-subtitle>DD/MM/YYYY</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
      </v-col>
      <v-col>
        <v-row>
           <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Port Of Origin</v-list-item-title>
        <v-list-item-subtitle>xyz</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
       <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Port Of Destination</v-list-item-title>
        <v-list-item-subtitle>abc</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
          </v-row>
      </v-col>
      <v-col>
        <v-row>
           <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Mode</v-list-item-title>
        <v-list-item-subtitle>Sea-FCL</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
       <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Load</v-list-item-title>
        <v-list-item-subtitle>xyz</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
        </v-row>
      </v-col>
      </v-row>
    </v-container>
  </v-card>

<!-- add rate card -->
<div class="text-center">
    <v-btn
      color="blue"
      dark
      @click="sheet = !sheet"
    >
      ADD NEW RATE
    </v-btn>
    <v-bottom-sheet v-model="sheet">
      <v-sheet class="text-center" >
        <v-container class="fluid">
        <div class=" d-flex ma-auto">
  <v-card raised outlined:loading="loading" class="mx-auto my-12" width="600" > 
        <v-card-title class="blue pa-2">Add New Rate</v-card-title>
       <v-divider ></v-divider>
       <v-card-text class="pa-0">
      <v-row align="center">
       <v-col  cols="4 pa-2">
        <v-card-actions>
          <v-select
          :items="items"
          label="Liner Name"
          class="px-1"
        ></v-select>
        </v-card-actions>
       
        </v-col>
        <v-col cols="4 pa-2">
       <v-card-actions>
         <v-text-field class="pr-5" label="Rates By" ></v-text-field>
         
        </v-card-actions>
        </v-col>
        <v-col cols="4 pa-1">
           <v-card-actions>
          <v-select
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
       <v-col  cols="4 px-6">
          <v-text-field label="Port Of Loading"></v-text-field> 
        </v-col>
        <v-col cols="4 px-6" align-center>
         <v-text-field label="Port Of Discharge"></v-text-field> 
        </v-col>
         <v-col cols="4 pa-1">
           <v-card-actions>
          <v-select
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
         <v-col cols="4 pa-1">
           <v-card-actions>
          <v-select
          :items="items"
          label="Expiry Date"
          class="px-1"
        ></v-select>
        </v-card-actions>
        </v-col>
         <v-col  cols="4 px-6">
          <v-text-field label="Detention Free"></v-text-field> 
        </v-col>
        <v-col cols="4 px-6" align-center>
         <v-text-field label="Demurrage"></v-text-field> 
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
          <p class=" text-center ma-0 ">CUSTOM RATES</p>
        </v-col>
        <v-col cols="6 pa-1">
          <v-card-actions class="d-flex justify-center">
            <v-btn raised class="fluid"  color="lime accent-2">Add Custom Rates</v-btn>
            </v-card-actions>
        </v-col>
      </v-row>
    </v-card-text> 

     <v-card-text class="pa-0">
      <v-row align="center">
       <v-col  cols="6 pa-1">
          <p class=" text-center ma-0 ">SCHEDULE</p>
        </v-col>
        <v-col cols="6 pa-1">
          <v-card-actions class="d-flex justify-center">
            <v-btn raised class="fluid"  color="lime accent-2">Schedule</v-btn>
            </v-card-actions>
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
        </v-container>
        <v-btn
          class="mt-6"
          text
          color="red"
          @click="sheet = !sheet"
        >close</v-btn>
      </v-sheet>
    </v-bottom-sheet>
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


<!-- dialog box -->

 <v-card raised outlined:loading="loading" width="1000" id="scroll-target"
      style="max-height: 400px"
      class="overflow-y-auto mx-auto my-12" > 
        
     <v-container v-scroll:#scroll-target="onScroll"
        align="center"
        justify="center"
        style="height: 500px">
      

    <v-card-text class="pa-0">
      <v-row align="center">
       <v-col  cols="4 px-6">
         <v-select
          :items="items"
          label="Start Date"
          class="px-1"
        ></v-select>
        </v-col>
        <v-col cols="4 px-6" align-center>
           <v-select
          :items="items"
          label="Expiry Date"
          class="px-1"
        ></v-select>
        </v-col>
         <v-col cols="4 pa-1">
           <v-card-actions>
          <v-select
          :items="items"
          label="Incoterms"
          class="px-1"
        ></v-select>
        </v-card-actions>
        </v-col>
      </v-row>
    </v-card-text>
    <v-card-text class="pa-0">
      <v-row align="center">
       <v-col  cols="6 pa-6 pb-0">
         <p style="font-size:1rem">Terms And Conditions</p>
        </v-col>
        <v-col cols="6 pa-2 pb-0" align-center>
          <v-row>
           <v-checkbox
      v-model="checkbox"
      :label="`Use Standard terms and conditions`"
    ></v-checkbox>
          </v-row>
        </v-col>
      </v-row>
    </v-card-text>
    <v-card-text class="py-0">
    <v-row class="pa-0">
    <v-col cols="12 py-0">
        <v-textarea
          filled
          name="input-7-4"
          value="Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum. "
         class="my-0"></v-textarea>
      </v-col>
    </v-row>
    </v-card-text>
  <v-card-text class="pa-0">
      <v-row align="center">
       <v-col  cols="4 px-6">
        <v-checkbox
      v-model="checkbox"
      :label="`Send Email Notification`"
    ></v-checkbox>
        </v-col>
        <v-col cols="4 px-6" align-center>
          <v-checkbox
      v-model="checkbox"
      :label="`Generate PDF`"
    ></v-checkbox>
        </v-col>
         <v-col cols="4 pa-1">
           <v-card-actions>
           <v-checkbox
      v-model="checkbox"
      :label="`Print Schedule`"
    ></v-checkbox>
        </v-card-actions>
        </v-col>
      </v-row>
    </v-card-text>
    <v-card-text class="pa-0">
      <v-row align="center">
       <v-col  cols="4 px-6">
        <v-switch v-model="mandatory" class="mx-2" label="Customs"></v-switch>
        </v-col>
        <v-col cols="4 px-6" align-center>
         <v-switch v-model="mandatory" class="mx-2" label="Perishable"></v-switch>
        </v-col>
         <v-col cols="4 pa-1">
           <v-card-actions>
           <v-switch v-model="mandatory" class="mx-2" label="Hazardous"></v-switch>
        </v-card-actions>
        </v-col>
      </v-row>
    </v-card-text>

     <v-row class="d-flex justify-end pa-6">
        <v-card-actions>
          <v-btn color="yellow" @click="reserve">
         NEXT
        </v-btn>
         <v-btn color="green" @click="reserve">
         DONE
        </v-btn>
        </v-card-actions>
        </v-row>
   
     </v-container>
  </v-card>


<!-- 2 part -->

  <v-card raised outlined:loading="loading" width="1000" id="scroll-target"
      style="max-height: 400px"
      class="overflow-y-auto mx-auto my-12" > 
        
     <v-container v-scroll:#scroll-target="onScroll"
        align="center"
        justify="center"
        style="height: 500px">
      

    <v-card-text class="pa-0">
      <v-row align="center">
       <v-col  cols="4 px-6">
         <v-text-field label="Customer Email"></v-text-field> 
        </v-col>
        <v-col cols="8">
        <v-row>
        <v-col cols="4 px-6" align-center>
           <v-text-field label="First Name"></v-text-field> 
        </v-col>
         <v-col cols="4 pa-1">
           <v-card-actions>
          <v-text-field label="Last Name"></v-text-field> 
        </v-card-actions>
        </v-col>
        </v-row></v-col>
      </v-row>
    </v-card-text>
  
      <v-card-text class="pa-0">
      <v-row align="center">
       <v-col  cols="4 pa-2">
        <v-card-actions>
          <v-select
          :items="items"
          label="Country"
          class="px-1"
        ></v-select>
        </v-card-actions>
       
        </v-col>
        <v-col cols="4 pa-2">
       <v-card-actions>
         <v-text-field label="Company"></v-text-field> 
        </v-card-actions>
        </v-col>
         <v-col cols="4 pa-2">
       <v-card-actions>
         <v-text-field label="CC Emails"></v-text-field> 
        </v-card-actions>
        </v-col>
      </v-row>
    </v-card-text><br>

        <v-card-text class="pa-0">
          <h3 class="text--disabled">Customer Address</h3>
      <v-row align="center">
       <v-col  cols="6 pa-2">
        <v-card-actions>
         <v-text-field label="Street Address"></v-text-field>
        </v-card-actions>
        <v-card-actions>
         <v-text-field label="City"></v-text-field>
        </v-card-actions>
          <v-card-actions>
         <v-text-field label="Postal/ZIP Code"></v-text-field>
        </v-card-actions>
        </v-col>
         <v-col  cols="6 pa-2">
        <v-card-actions>
         <v-text-field label="Address line 2"></v-text-field>
        </v-card-actions>
        <v-card-actions>
         <v-text-field label="State/Province/Region"></v-text-field>
        </v-card-actions> <v-card-actions>
          <v-select
          :items="items"
          label="Country"
          class="px-1"
        ></v-select>
        </v-card-actions>

        </v-col>
      </v-row>
    </v-card-text>

     <v-row class="d-flex justify-end pa-6">
        <v-card-actions>
          <v-btn color="yellow" @click="reserve">
         Genreate Quotation
        </v-btn>
         <v-btn color="green" @click="reserve">
         <v-icon>mdi-eye</v-icon>Preview Quote
        </v-btn>
        </v-card-actions>
        </v-row>
   
     </v-container>
  </v-card>


<!-- quotation review -->


  <!-- <v-card class="mx-auto" raised width="1250">
  <v-card-title><h2>QUOTATION REVIEW</h2></v-card-title>
  <v-card-text>
    <v-row>
      <v-col cols="4"><v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>Start Date</v-list-item-title>
        <v-list-item-subtitle>{{item.startDate}}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"><v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>Expiry Date</v-list-item-title>
        <v-list-item-subtitle>{{item.expiryDate}}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"><v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>Incoterms</v-list-item-title>
        <v-list-item-subtitle>{{item.incoTerms}}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
    </v-row>
    <v-row>
      <v-col cols="4"><v-list-item single-line>
      <v-list-item-content>
        <v-list-item-title> <v-checkbox v-model="disabled" readonly class="mx-2" :value="customs" label="Customs"></v-checkbox></v-list-item-title>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"><v-list-item single-line>
      <v-list-item-content>
        <v-list-item-title> <v-checkbox v-model="disabled" readonly class="mx-2" :value="perishable" label="Perishable"></v-checkbox></v-list-item-title>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"><v-list-item single-line>
      <v-list-item-content>
        <v-list-item-title> <v-checkbox v-model="disabled" readonly class="mx-2" :value="hazardous" label="Hazardous"></v-checkbox></v-list-item-title>
      </v-list-item-content>
    </v-list-item></v-col>
    </v-row>
    <v-row>
      <v-col cols="3"><v-list-item single-line>
      <v-list-item-content>
        <v-list-item-title> <v-checkbox v-model="disabled" readonly class="mx-2" :value="sendEmail" label="Send Email"></v-checkbox></v-list-item-title>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="3"><v-list-item single-line>
      <v-list-item-content>
        <v-list-item-title> <v-checkbox v-model="disabled" readonly class="mx-2" :value="generatePDF" label="Generate PDF"></v-checkbox></v-list-item-title>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="3"><v-list-item single-line>
      <v-list-item-content>
        <v-list-item-title> <v-checkbox v-model="disabled" readonly class="mx-2" :value="printSchedule" label="Print Schedule"></v-checkbox></v-list-item-title>
      </v-list-item-content>
    </v-list-item></v-col>
    <v-col cols="3"><v-list-item single-line>
      <v-list-item-content>
        <v-list-item-title> <v-checkbox v-model="disabled" readonly class="mx-2" :value="termsAndCondition" label="Terms & Conditions"></v-checkbox></v-list-item-title>
      </v-list-item-content>
    </v-list-item></v-col>
    </v-row>
    <v-divider></v-divider>
  </v-card-text>
  <v-card-text>
    <h2>Customer Details</h2>
    <v-row>
      <v-col cols="4"><v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>Customer Email</v-list-item-title>
        <v-list-item-subtitle>{{item.customerEmail}}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"><v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>First Name</v-list-item-title>
        <v-list-item-subtitle>{{item.firstName}}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"><v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>Last Name</v-list-item-title>
        <v-list-item-subtitle>{{item.lastName}}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
    </v-row>
     <v-row>
      <v-col cols="4"><v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>Country</v-list-item-title>
        <v-list-item-subtitle>{{item.country}}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"><v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>Company Name</v-list-item-title>
        <v-list-item-subtitle>{{item.company}}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"><v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>CC Emails</v-list-item-title>
        <v-list-item-subtitle>{{item.ccEmails}}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
    </v-row>
  </v-card-text>
  <v-card-text>
    <h3 class="text--disabled"><span>Customer Address</span></h3>
    <v-row>
      <v-col cols="6"><v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>Street Address</v-list-item-title>
        <v-list-item-subtitle>{{item.streetAddress}}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="6"><v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>City</v-list-item-title>
        <v-list-item-subtitle>{{item.city}}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
    </v-row>
    <v-row>
      <v-col cols="6"><v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>State</v-list-item-title>
        <v-list-item-subtitle>{{item.state}}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="6"><v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>Zip Code</v-list-item-title>
        <v-list-item-subtitle>{{item.zipCode}}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
    </v-row>
  </v-card-text>
  <v-divider></v-divider>
  <v-card-text>
    <h2>Cargo Details</h2>
    <v-row>
     <v-col cols="6"><v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>Load Details</v-list-item-title>
        <v-list-item-subtitle>{{item.loadDetails}}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
     <v-col cols="6">  <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Port Of Origin</v-list-item-title>
        <v-list-item-subtitle>{{item.origin}}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
       <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Port Of Destination</v-list-item-title>
        <v-list-item-subtitle>{{item.destination}}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
    </v-row>
  </v-card-text>
  <v-divider></v-divider>
  <v-card-text>
    <h2>Rate Cards</h2>
    <v-row>
     
    </v-row>
  </v-card-text>
  </v-card> -->


<v-card class="mx-auto my-12" raised max-width="auto">
  <v-card-text class="text-center pa-5"><h1>FCL</h1></v-card-text>
  <v-divider></v-divider>
  <v-card-text>
    <h3>ENQUIRY ID : </h3>
    <v-row>
      <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Origin</v-list-item-title>
        <v-list-item-subtitle>Delhi</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Destination</v-list-item-title>
        <v-list-item-subtitle>Bengaluru</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>No Of Containers</v-list-item-title>
        <v-list-item-subtitle>x</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
    </v-row>
    <v-row>
         <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Cargo Ready Date</v-list-item-title>
        <v-list-item-subtitle>DD/MM/YYYY</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Created At</v-list-item-title>
        <v-list-item-subtitle>DD/MM/YYYY</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Updated At</v-list-item-title>
        <v-list-item-subtitle>DD/MM/YYYY</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
    </v-row>
  </v-card-text>
  <v-divider></v-divider>
  <v-card-text>
    <h3>LOAD DETAILS</h3>
    <v-row>
          <v-col cols="3"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>20GP</v-list-item-title>
        <v-list-item-subtitle></v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="3"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>40GP</v-list-item-title>
        <v-list-item-subtitle></v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="3"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>20TC</v-list-item-title>
        <v-list-item-subtitle></v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
     <v-col cols="3"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>40TC</v-list-item-title>
        <v-list-item-subtitle></v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
    </v-row>
    <v-row>
           <v-col cols="3"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>20RE</v-list-item-title>
        <v-list-item-subtitle></v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="3"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>40RE</v-list-item-title>
        <v-list-item-subtitle></v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="3"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>20HC</v-list-item-title>
        <v-list-item-subtitle></v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
     <v-col cols="3"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>40HC</v-list-item-title>
        <v-list-item-subtitle></v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
    </v-row>
  </v-card-text>
  <v-divider></v-divider>
  <v-card-actions>
    <v-btn block class="yellow">DONE</v-btn>
  </v-card-actions>

</v-card>


<v-card class="mx-auto my-12" raised max-width="auto">
  <v-card-text class="text-center pa-5"><h1>LCL</h1></v-card-text>
  <v-divider></v-divider>
  <v-card-text>
    <h3>ENQUIRY ID : </h3>
    <v-row>
      <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Origin</v-list-item-title>
        <v-list-item-subtitle>Delhi</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Destination</v-list-item-title>
        <v-list-item-subtitle>Bengaluru</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>No Of Packages</v-list-item-title>
        <v-list-item-subtitle>x</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
    </v-row>
    <v-row>
         <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Cargo Ready Date</v-list-item-title>
        <v-list-item-subtitle>DD/MM/YYYY</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Created At</v-list-item-title>
        <v-list-item-subtitle>DD/MM/YYYY</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Updated At</v-list-item-title>
        <v-list-item-subtitle>DD/MM/YYYY</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
    </v-row>
  </v-card-text>
  <v-divider></v-divider>
  <v-card-text>
    <h3>LOAD DETAILS</h3>
    <v-row>
          <v-col cols="6"> <v-list-item three-line>
       <v-list-item-content>
        <v-list-item-title><h4>Weight</h4></v-list-item-title>
        <v-list-item-title>Value :</v-list-item-title>
        <v-list-item-title>Unit :</v-list-item-title>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="6"> <v-list-item three-line>
       <v-list-item-content>
        <v-list-item-title><h4>Volume</h4></v-list-item-title>
       <v-list-item-title>Value :</v-list-item-title>
       <v-list-item-title>Unit :</v-list-item-title>
      </v-list-item-content>
    </v-list-item></v-col>
    </v-row>
  </v-card-text>
  <v-divider></v-divider>
  <v-card-actions>
    <v-btn block class="yellow">DONE</v-btn>
  </v-card-actions>

</v-card>

<v-card class="mx-auto my-12" raised max-width="auto">
  <v-card-text class="text-center pa-5"><h1>AIR</h1></v-card-text>
  <v-divider></v-divider>
  <v-card-text>
    <h3>ENQUIRY ID : </h3>
    <v-row>
      <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Origin</v-list-item-title>
        <v-list-item-subtitle>Delhi</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Destination</v-list-item-title>
        <v-list-item-subtitle>Bengaluru</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Goods Type</v-list-item-title>
        <v-list-item-subtitle>adsa</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
    </v-row>
    <v-row>
         <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Shipment Date</v-list-item-title>
        <v-list-item-subtitle>DD/MM/YYYY</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Created At</v-list-item-title>
        <v-list-item-subtitle>DD/MM/YYYY</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title>Updated At</v-list-item-title>
        <v-list-item-subtitle>DD/MM/YYYY</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item></v-col>
    </v-row>
  </v-card-text>
  <v-divider></v-divider>
  <v-card-text>
    <h3>CARGO DETAILS</h3>
    <v-row>
          <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title><h4>Weight</h4></v-list-item-title>
        <v-list-item-title>Value :</v-list-item-title> 
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title><h4>Quantity</h4></v-list-item-title>
       <v-list-item-title>Value :</v-list-item-title>
      </v-list-item-content>
    </v-list-item></v-col>
     <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title><h4>Weight Type</h4></v-list-item-title>
       <v-list-item-title>Value :</v-list-item-title>
      </v-list-item-content>
    </v-list-item></v-col>
    </v-row>
       <v-row>
          <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title><h4>Length</h4></v-list-item-title>
        <v-list-item-title>Value :</v-list-item-title> 
      </v-list-item-content>
    </v-list-item></v-col>
      <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title><h4>Breadth</h4></v-list-item-title>
       <v-list-item-title>Value :</v-list-item-title>
      </v-list-item-content>
    </v-list-item></v-col>
     <v-col cols="4"> <v-list-item two-line>
       <v-list-item-content>
        <v-list-item-title><h4>Height</h4></v-list-item-title>
       <v-list-item-title>Value :</v-list-item-title>
      </v-list-item-content>
    </v-list-item></v-col>
    </v-row>
    <v-row>
      <v-col cols="4"><v-checkbox v-model="disabled" readonly class="mx-2"  label="Turnable"></v-checkbox></v-col>
      <v-col cols="4"><v-checkbox v-model="disabled" readonly class="mx-2"  label="Stackable"></v-checkbox></v-col>
      <v-col cols="4"><v-checkbox v-model="disabled" readonly class="mx-2"  label="Screened"></v-checkbox></v-col>
    </v-row>
  </v-card-text>
  <v-divider></v-divider>
  <v-card-actions>
    <v-btn block class="yellow">DONE</v-btn>
  </v-card-actions>

</v-card>

  </v-app>
</template>




<script>
  export default {
    data: () => ({
      loading: false,
      selection: 1,
      show: false,
      sheet:false
    }),
    

    methods: {
      reserve () {
        this.loading = true

        setTimeout(() => (this.loading = false), 2000)
      },
    },
  }
</script>




  