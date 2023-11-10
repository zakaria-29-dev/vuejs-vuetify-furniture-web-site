<template>
 <v-app>
  <NavBar />
  <v-main>
    <v-container>
      <v-card class="mar-top" flat>
        <v-tabs v-model="tab" color="deep-purple-accent-4" align-tabs="center">
        <v-tab :value="1">Newest</v-tab>
        <v-tab :value="2">Highest Rated</v-tab>
        <v-tab :value="3">Low Price to Hight</v-tab>
        <v-tab :value="4">Low Price to Low</v-tab>
        <v-tab :value="5">Delivery and Returns Products</v-tab>
        </v-tabs>
        <v-window v-model="tab">
        <v-window-item v-for="n in 5" :key="n" :value="n">
        <v-container fluid>
          <v-row>
            <v-col cols="12" sm="9">
              <Product />
            </v-col>
            <v-col cols="12" sm="3">
              <v-toolbar color="transparent">Categories
                <v-spacer></v-spacer>
                <v-btn icon="mdi-chevron-down"></v-btn>
              </v-toolbar>
              <v-row>
                <v-col cols="12" sm="6" md="6">
                        <v-checkbox
                          v-model="ex4"
                          label="Sofas"
                          color="info"
                          value="success"
                          hide-details
                        ></v-checkbox>
                        <v-checkbox
                          v-model="ex4"
                          label="Bethrooms"
                          color="info"
                          value="info"
                          hide-details
                        ></v-checkbox>
                        <v-checkbox
                          v-model="ex4"
                          label="Beds"
                          color="info"
                          value="red"
                          hide-details
                        ></v-checkbox>
                      </v-col>
                      <v-col cols="12" sm="6" md="6">
                        <v-checkbox
                          v-model="ex5"
                          label="Sofas"
                          color="info"
                          value="success"
                          hide-details
                        ></v-checkbox>
                        <v-checkbox
                          v-model="ex5"
                          label="Bethrooms"
                          color="info"
                          value="info"
                          hide-details
                        ></v-checkbox>
                        <v-checkbox
                          v-model="ex5"
                          label="Beds"
                          color="info"
                          value="red"
                          hide-details
                        ></v-checkbox>
                      </v-col>
              </v-row>
              <v-toolbar color="transparent">Colors<v-space></v-space>
              <v-btn icon="mdi-chevron-down"></v-btn>
              </v-toolbar>
              <v-avatar color="grey" class="ml-1"></v-avatar>
                    <v-avatar color="#DBEBCE" class="ml-1"></v-avatar>
                    <v-avatar color="#EBDFD1" class="ml-1"></v-avatar>
                    <v-avatar color="#E6C5B8" class="ml-1"></v-avatar>
                    <v-avatar color="#D5CAB4" class="ml-1"></v-avatar>
                    <v-avatar color="#E6C5B8" class="ml-1"></v-avatar><br />
                    <v-avatar color="#E0E1E0" class="ml-1 mt-3"></v-avatar>
                    <v-avatar color="#E2BAB6" class="ml-1 mt-3"></v-avatar>
                    <v-avatar color="#CCD0E0" class="ml-1 mt-3"></v-avatar>
                    <v-avatar color="#8B9DC2" class="ml-1 mt-3"></v-avatar>
                    <v-avatar color="#959DB6" class="ml-1 mt-3"></v-avatar>
                    <v-avatar color="#CFE7EB" class="ml-1 mt-3"></v-avatar>
                    <v-toolbar color="transparent">Materials <v-spacer></v-spacer>
                    <v-btn icon="mdi-chevron-down"></v-btn>
                    </v-toolbar>
                    <v-row>
                      <v-col cols="12" sm="6" md="6">
                        <v-checkbox
                          v-model="ex4"
                          label="Wood"
                          color="success"
                          value="success"
                          hide-details
                        ></v-checkbox>
                        <v-checkbox
                          v-model="ex4"
                          label="Metal"
                          color="success"
                          value="info"
                          hide-details
                        ></v-checkbox>
                        <v-checkbox
                          v-model="ex4"
                          label="Leathers"
                          color="success"
                          value="red"
                          hide-details
                        ></v-checkbox>
                      </v-col>
                      <v-col cols="12" sm="6" md="6">
                        <v-checkbox
                          v-model="ex5"
                          label="Fabrics"
                          color="success"
                          value="success"
                          hide-details
                        ></v-checkbox>
                        <v-checkbox
                          v-model="ex5"
                          label="Bethrooms"
                          color="success"
                          value="info"
                          hide-details
                        ></v-checkbox>
                        <v-checkbox
                          v-model="ex5"
                          label="Beds"
                          color="success"
                          value="red"
                          hide-details
                        ></v-checkbox>
                      </v-col>
                    </v-row>
                    <v-toolbar color="transparent">Store Ratings<v-spacer></v-spacer>
                    <v-btn icon="mdi-chevron-down"></v-btn>
                    </v-toolbar>
                    <v-rating v-model="r1" color="yellow-darken-3"></v-rating>
                    <v-rating v-model="r2" color="yellow-darken-3"></v-rating>
                    <v-rating v-model="r3" color="yellow-darken-3"></v-rating>
                    <v-toolbar color="transparent">Price<v-spacer></v-spacer>
                      <v-btn icon="mdi-chevron-down"></v-btn>
                    </v-toolbar>
                    <v-slider v-model="slider2" thumb-label="always" color="pink"></v-slider>
            </v-col>
          </v-row>
        </v-container>
        </v-window-item>
        </v-window>
      </v-card>
    </v-container>
  </v-main>
  <Footer />
 </v-app>
</template>

<script setup>
import NavBar from "@/components/NavBar.vue";
import Product from "@/components/Product.vue";
import Footer from "@/components/Footer.vue";
</script>
<script>
export default {
  data: () => ({
    tab: null,
    r1: 4,
    r2: 3,
    r3: 2,
    slider2: 50,

    ex4: [
      "red",
      "indigo",
      "orange",
      "primary",
      "secondary",
      "success",
      "info",
      "warning",
      "error",
      "red darken-3",
      "indigo darken-3",
      "orange darken-3",
    ],
    ex5: [
      "red",
      "indigo",
      "orange",
      "primary",
      "secondary",
      "success",
      "info",
      "warning",
      "error",
      "red darken-3",
      "indigo darken-3",
      "orange darken-3",
    ],
  }),
};
</script>
<style scoped>
.mar-top {
  margin-top: 250px;
}
</style>

