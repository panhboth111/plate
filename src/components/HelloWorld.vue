<template>
  <v-container>
    <v-card class="pa-3">
      <v-row>
        <v-col
          sm="12"
          cols="12"
          md="8"
          class="display-1 font-weight-light text-capitalize grey--text text-darken-2"
        >Known license plates</v-col>

        <v-col sm="12" cols="12" md="4">
          <v-text-field
            v-model="search"
            append-icon="mdi-magnify"
            label="Search"
            outlined
            dense
            color="amber"
          ></v-text-field>
        </v-col>
      </v-row>
      <v-data-table :search="search" :headers="headers" :items="known_plates" multi-sort></v-data-table>
    </v-card>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",
  data: () => ({
    search: "",
    known_plates: [
      {
        fullname: "Neak Panhboth",
        phone: "085248484",
        email: "neakpanhboth18@kit.edu.kh",
        role: "Student",
        vehicle_type: "Moto",
        gender: "Male",
        age: "99",
        plate_number: "2Z-8934",
        organization_name: "Phnom Penh",
        id: "0001"
      },
      {
        fullname: "John Cena",
        phone: "098777666",
        email: "johncena@yahoo.com",
        role: "Staff",
        vehicle_type: "Bike",
        gender: "Male",
        age: "12",
        plate_number: "2Z-8991",
        organization_name: "Svay rieng",
        id: "0002"
      },
      {
        fullname: "Cristiano Ronaldo",
        phone: "097666542",
        email: "ronaldo@gmail.com",
        role: "Lecturer",
        vehicle_type: "Car",
        gender: "Male",
        age: "96",
        plate_number: "2Z-0734",
        organization_name: "Prey Veng",
        id: "0003"
      }
    ],
    headers: [
      {
        text: "License plate",
        align: "start",
        sortable: false,
        value: "plate"
      },
      { text: "Role", value: "role" },
      { text: "Phone", value: "phone" },
      { text: "Gender", value: "gender" },
      { text: "Vehicle", value: "vehicle_type" },
      { text: "Plate number", value: "plate_number", align: " d-none" },
      { text: "Organization", value: "organization_name", align: " d-none" }
    ]
  })
};
</script>
