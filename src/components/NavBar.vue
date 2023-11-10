<template>
<div class="image shape" style="background: url('1.jpg'); background-size: contain; position: absolute;height: 300px;width:100%">
<v-app-bar color="transparent" class="text-white">
  <template v-slot:prepend
>
<v-app-bar-nav-icon></v-app-bar-nav-icon>
</template>
<v-app-bar-title>Constructor</v-app-bar-title>
<v-btn append-icon="mdi mdi-chevron-down">Goods</v-btn>
<v-btn append-icon="mdi mdi-chevron-down">Rooms</v-btn>
<v-btn append-icon="mdi mdi-chevron-down">Inspiration</v-btn>
<v-btn append-icon="mdi mdi-chevron-down">News items</v-btn>
<v-text-field density="compact" label="Search products" prepend-inner-icon="mdi-magnify" single-line hide-details flat></v-text-field>
<v-spacer></v-spacer>
<v-btn prepend-icon="mdi mdi-account">Account</v-btn>
<v-btn prepend-icon="mdi mdi-cart">Bag</v-btn>

</v-app-bar>
<v-row>
  <v-col cols="12" sm="4" class="d-flex justify-center align-center">
    <v-btn prepend-icon="mdi mdi-basket" append-icon="mdi mdi-chevron-down" color="transparent text-white" class="top">
      Living Room
    </v-btn>
  </v-col>
  <v-col cols="12" sm="4" class="d-flex justify-center align-center">
    <h1 class="top text-white"><strong>Furniture</strong> & Furnishings</h1>
  </v-col>
  <v-col cols="12" sm="4" class="d-flex justify-center align-center">
    <v-btn prepend-icon="mdi mdi-email" color="transparent text-white" class="top">
      Subscribe
    </v-btn>
  </v-col>
  <v-col cols="12" sm="12" class="d-flex justify-center align-center">
    <v-btn rounded="xl" class="tope">Shop Now</v-btn>
  </v-col>
</v-row>
</div>
</template>

<script>
export default {

}
</script>

<style>
.shape {
  border-radius: 0 0 30% 30%;
}
.top {
  margin-top: 120px;
}
.tope {
  margin-top: 90px;
}
</style>
