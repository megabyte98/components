<template>
  <v-container >
    <v-simple-table dense>
      <template v-slot:default>
        <thead>
          <tr>
            <th class="text-left">Charges</th>
            <th class="text-left">Basis</th>
            <th class="text-left">equipment type</th>
            <th class="text-left">qty/slab</th>
            <th>
              <v-row justify="center">BUY RATES</v-row>
              <v-row>
                <v-col justify="center" col="6">unit price</v-col>
                <v-col justify="center" col="6">amount</v-col>
              </v-row>
            </th>
            <th>
              <v-row justify="center">Sell RATES</v-row>
              <v-row>
                <v-col justify="center" col="6">unit price</v-col>
                <v-col justify="center" col="6">amount</v-col>
              </v-row>
            </th>
            <th>Delete Icon</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(value, index) in rows" :key="index">
            <td>
              <v-text-field v-model="value.charges"  @change="updateData"></v-text-field>
            </td>
            <td>
              <v-select v-model="value.basis" :items="['per equipment', 'per B/L']"  @change="updateData"></v-select>
            </td>
            <td>
              <v-select
                v-model="value.equipmentType"
                :items="[
                  '20GP',
                  '40GP',
                  '20TC',
                  '40TC',
                  '20RE',
                  '40RE',
                  '20HC',
                  '40HC'
                ]"
                @change="updateData"
              ></v-select>
            </td>
            <td>
              <v-text-field v-model="value.qty" type="number" @change="updateData"></v-text-field>
            </td>
            <td>
              <v-row>
                <v-col col="6">
                  <v-text-field v-model="value.buyRates" type="number" @change="updateData"></v-text-field>
                </v-col>
                <v-col col="6" class="justify-content-center d-flex align-item-center">
                  <p class="ma-auto">{{ value.qty * value.buyRates }}</p>
                </v-col>
              </v-row>
            </td>
            <td>
              <v-row>
                <v-col col="6">
                  <v-text-field v-model="value.sellRates" type="number" @change="updateData"></v-text-field>
                </v-col>
                <v-col col="6" class="justify-content-center d-flex align-item-center">
                  <p class="ma-auto" justify="center">{{ value.qty * value.sellRates }}</p>
                </v-col>
              </v-row>
            </td>
            <td>
              <v-btn @click="deleteRow(index)"><v-icon color="red">mdi-delete</v-icon></v-btn>
            </td>
          </tr>
        </tbody>
      </template>
    </v-simple-table>
    <v-btn class="ma-5 pink" fab @click="addRow">
      <v-icon>mdi-plus</v-icon>
    </v-btn>
  </v-container>
</template>
 
<script>

export default {
  props: ["id"],
  data: () => ({
    rows: []
  }),
  methods: {
    
    addRow() {
      this.rows.push({
        charges: "",
        basis: "per equipment",
        equipmentType: "20GP",
        qty: 0,
        buyRates: 0,
        sellRates: 0
      });
 
    },
    deleteRow(index) {
      this.rows.splice(index, 1);

     
      
    },
    updateData(){
      var a={data:this.rows,profit:this.profit},b=this.id
     console.log(a,b)
   
    
    }
  },
  computed: {
    profit() {
      return this.rows.reduce(function(a, b) {
       
        return +a + +b.qty * (-+b.buyRates + +b.sellRates);
      }, 0);
 
     
    }
  }
};
</script>