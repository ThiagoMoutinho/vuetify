<template>
  <v-app>
    <v-navigation-drawer v-model="isDrawerOpen">
      <v-list>
        <v-list-item prepend-icon="mdi-home">Home</v-list-item>
        <v-list-group value="Clientes">
          <template #activator="{ props }">
            <v-list-item
              v-bind="props"
              prepend-icon="mdi-account-circle"
              title="Clientes"
            ></v-list-item>
        </template>
        <v-list-item prepend-icon="mdi-currency-usd">Faturamento</v-list-item>
        <v-list-item prepend-icon="mdi-chart-line">Relatorio</v-list-item>
        </v-list-group>
      </v-list>

    </v-navigation-drawer>
    <v-app-bar flat class="border-b">
      <v-app-bar-nav-icon @click="isDrawerOpen = !isDrawerOpen"></v-app-bar-nav-icon>
      <v-app-bar-title>Meu app</v-app-bar-title>

      <template #append>
        <v-bt icon class="mr-2">
          <v-badge dot color="info">
            <v-icon icon="mdi-bell-outline"></v-icon>
          </v-badge>
        </v-bt>
        <v-avatar>
          <v-img 
            cover
            src="https://gratisography.com/wp-content/uploads/2019/01/gratisography-nerdtastic-free-stock-photo.jpg"
          >
        </v-img>
       </v-avatar>
      </template>
    </v-app-bar>

    <v-main>
      <v-container>
        <h1>Dashboard</h1>

        <v-row>
          <v-col cols="12" sm="6" md="4" lg="3">
            <v-card flat class="border">
              <v-img
                class="align-end text-white"
                src="https://images.pexels.com/photos/1058314/pexels-photo-1058314.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1260&amp;h=750&amp;dpr=1" srcset="https://images.pexels.com/photos/1058314/pexels-photo-1058314.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1260&amp;h=750&amp;dpr=1 1x, https://images.pexels.com/photos/1058314/pexels-photo-1058314.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1260&amp;h=750&amp;dpr=2 2x" alt="grátis Pessoas Perto Da Fonte Foto profissional"
              >
                <v-card-title>
                  Top pontos turísticos de curitiba
                </v-card-title>

              </v-img>
              <v-card-subtitle class="pt-3">
                Curitiba
              </v-card-subtitle>

              <v-card-text>
                <div>Parque tanguá</div>
                <div>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Itaque quia dicta et
                </div>
              </v-card-text>
              <v-card-actions>
                <V-btn color="primary" variant="outlined">VER MAIS</V-btn>
                <V-btn color="success" variant="tonal">COMPAR</V-btn>
              </v-card-actions>
            </v-card>
          </v-col>
          <v-col cols="12" sm="6" md="4" lg="3">
            <v-card flat class="border">
              <v-img
                class="align-end text-white"
                src="https://images.pexels.com/photos/1058314/pexels-photo-1058314.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1260&amp;h=750&amp;dpr=1" srcset="https://images.pexels.com/photos/1058314/pexels-photo-1058314.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1260&amp;h=750&amp;dpr=1 1x, https://images.pexels.com/photos/1058314/pexels-photo-1058314.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1260&amp;h=750&amp;dpr=2 2x" alt="grátis Pessoas Perto Da Fonte Foto profissional"
              >
                <v-card-title>
                  Top pontos turísticos de curitiba
                </v-card-title>

              </v-img>
              <v-card-subtitle class="pt-3">
                Curitiba
              </v-card-subtitle>

              <v-card-text>
                <div>Parque tanguá</div>
                <div>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Itaque quia dicta et
                </div>
              </v-card-text>
              <v-card-actions>
                <V-btn color="primary" variant="outlined">VER MAIS</V-btn>
                <V-btn color="success" variant="tonal">COMPAR</V-btn>
              </v-card-actions>
            </v-card>
          </v-col>
          <v-col cols="12" sm="6" md="4" lg="3">
            <v-card flat class="border">
              <v-img
                class="align-end text-white"
                src="https://images.pexels.com/photos/1058314/pexels-photo-1058314.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1260&amp;h=750&amp;dpr=1" srcset="https://images.pexels.com/photos/1058314/pexels-photo-1058314.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1260&amp;h=750&amp;dpr=1 1x, https://images.pexels.com/photos/1058314/pexels-photo-1058314.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1260&amp;h=750&amp;dpr=2 2x" alt="grátis Pessoas Perto Da Fonte Foto profissional"
              >
                <v-card-title>
                  Top pontos turísticos de curitiba
                </v-card-title>

              </v-img>
              <v-card-subtitle class="pt-3">
                Curitiba
              </v-card-subtitle>

              <v-card-text>
                <div>Parque tanguá</div>
                <div>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Itaque quia dicta et
                </div>
              </v-card-text>
              <v-card-actions>
                <V-btn color="primary" variant="outlined">VER MAIS</V-btn>
                <V-btn color="success" variant="tonal">COMPAR</V-btn>
              </v-card-actions>
            </v-card>
          </v-col>
          <v-col cols="12" sm="6" md="4" lg="3">
            <v-card flat class="border">
              <v-img
                class="align-end text-white"
                src="https://images.pexels.com/photos/1058314/pexels-photo-1058314.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1260&amp;h=750&amp;dpr=1" srcset="https://images.pexels.com/photos/1058314/pexels-photo-1058314.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1260&amp;h=750&amp;dpr=1 1x, https://images.pexels.com/photos/1058314/pexels-photo-1058314.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1260&amp;h=750&amp;dpr=2 2x" alt="grátis Pessoas Perto Da Fonte Foto profissional"
              >
                <v-card-title>
                  Top pontos turísticos de curitiba
                </v-card-title>

              </v-img>
              <v-card-subtitle class="pt-3">
                Curitiba
              </v-card-subtitle>

              <v-card-text>
                <div>Parque tanguá</div>
                <div>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Itaque quia dicta et
                </div>
              </v-card-text>
              <v-card-actions>
                <V-btn color="primary" variant="outlined">VER MAIS</V-btn>
                <V-btn color="success" variant="tonal">COMPAR</V-btn>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script setup>
import {ref} from 'vue';

const isDrawerOpen = ref(false);

</script>
