<template>
  <div>
    <v-app>
      <section class="pb-10">
        <v-app-bar class="bg-grey">
          <v-app-bar-title class="bg-black text-h5"
            >Fake Store! Name Fake Things A1 Quality Branded
            !...$</v-app-bar-title
          >
          <div>
            <v-btn> Home </v-btn>
          </div>
          <div>
            <v-btn> About </v-btn>
          </div>
        </v-app-bar>
      </section>
      <section class="py-10 bg-grey-lighten-2">
        <v-row>
          <v-col cols="5 ">
            <v-img
              class="rounded-xl"
              src="https://images-prod.dazeddigital.com/3000/azure/dazed-prod/1230/3/1233236.JPG"
            >
            </v-img>
          </v-col>
          <v-col cols="7">
            <h1>
              Welcome to my Fake Store. Thanks for shopping by Fake Store!
            </h1>
            <P
              >fakeStoreApi is a free online REST API that you can use whenever
              you need Pseudo-real data for your e-commerce or shopping website
              without running any server-side code.Fake Store API. Tu API para
              tu prototipo de e-commerce o sitio web de compras. Ver
              Documentación .. Fake Ecommerce APIs mock server is free and easy
              ... This includes products, shopping carts, and user
              information.Fake Store isn't a store that exists in production, it
              is used to tests your apps quickly inside the editor.
              <h2>How to Use it..#</h2>
              fakeStoreApi can be used with any type of shopping project that
              needs products, carts, and users in JSON format. you can use
              examples below to check how fakeStoreApi works and feel free to
              enjoy it in your awesome projects!
              <h3>Uses of Fake Store are given Below %</h3>
              Fake Store API can be used with any type of project that needs
              products, users, categories, authentication, and users in JSON
              format. You can use this API for prototyping e-commerce and
              learning about how to connect to an API with the best practices.
            </P>
            <hr>
            <hr>
          </v-col>
        </v-row>
      </section>

      <section class="bg-grey-lighten-1 py-10  ">
        <v-select
  label="Select"
  :items="catagory.map((c) => c.title)"
  variant="solo-inverted"
 </v-select>
        <div>
         <v-row>
          <v-col cols="3" v-for=" product in products" :key="product">
              <v-card hover >
              <v-card-title>Buy Now & Get More Discount.</v-card-title>
                <v-img class="rounded-lg border-shadow"  width="350px" height="250px" :src="product.image" :lazy-src="product.image">
                  
                </v-img>
                <v-card-title> {{ product.title }} </v-card-title>
              </v-card>
            </v-col>
          
         </v-row>
        </div>
      </section>
    </v-app>
  </div>
</template>

<script setup>
const { data: products } = useFetch("https://fakestoreapi.com/products")
const {data:catagory} =useFetch("https://fakestoreapi.com/products")
</script>

<style lang="scss" scoped></style>
