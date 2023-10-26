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
        <v-menu>
          <template #activator="{ props }">
            <v-avatar v-bind="props">
              <v-img 
                cover
                src="https://gratisography.com/wp-content/uploads/2019/01/gratisography-nerdtastic-free-stock-photo.jpg"
              >
            </v-img>
           </v-avatar>
          </template>

         <v-card min-width="200px">
          <v-list :lines="false" density="compact" nav>
            <v-list-item prepend-icon="mdi-account-outline">
              <v-list-item-title>Meu perfil</v-list-item-title>
            </v-list-item>
            <v-list-item prepend-icon="mdi-heart-outline">
              <v-list-item-title>Favoritos</v-list-item-title>
            </v-list-item>
          </v-list>
         </v-card>
        </v-menu>
      </template>
    </v-app-bar>

    <v-main>
      <v-container>
        <h1 class="mb-5">Dashboard</h1>

        <v-card flat class="border mb-4">
          <div class="d-flex justify-space-between">
            <v-card-title>Últimos usuários</v-card-title>
            <v-card-title>
              <v-btn @click="isDialog = true" variant="tonal" size="small">Adicionar usuário</v-btn>
              <v-dialog
                v-model="isDialog" 
                width="600px"
              >
                <v-card>
                  <v-card-title>Adicionar Usuário</v-card-title>
                  <v-card-text>
                    <v-row>
                      <v-col>
                        <v-text-field label="Nome" variant="outlined"></v-text-field>
                      </v-col>
                      <v-col>
                        <v-text-field label="E-mail" variant="outlined" :rules="emailRules"></v-text-field>
                      </v-col>
                    </v-row>

                    <v-select 
                      label="Cargo" 
                      variant="outlined"
                      :items="['Admin', 'Gerente', 'Convidado']"
                    >
                    </v-select>
                  </v-card-text>

                  <v-card-actions> <v-spacer></v-spacer>
                    <v-btn variant="text" @click="isDialog = !isDialog">Cancelar</v-btn>
                    <v-btn variant="tonal" color="success">Salvar</v-btn>
                  </v-card-actions>
                </v-card>
              </v-dialog>
            </v-card-title>
          </div>
          <v-table>
            <thead>
              <tr>
                <th>Nome</th>
                <th>Email</th>
                <th>Cargo</th>
                <th>Ações</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>Fulano</td>
                <td>fulano@gmail.com</td>
                <td>Admin</td>
                <td>
                  <v-btn variant="tonal" color="primary" >Editar</v-btn>
                </td>
              </tr>
              <tr>
                <td>teste 2</td>
                <td>teste@gmail.com</td>
                <td>Admin2</td>
                <td>
                  <v-btn variant="tonal" color="primary" >Editar</v-btn>
                </td>
              </tr>
            </tbody>
          </v-table>
        </v-card>

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
const isDialog = ref(false);

const emailRules = [
  value => {
    if(value) {
      return true;
    }

    return 'O email é obrigatório';
  },
  value => {
    if(value.includes('@')) {
      return true;
    }

    return 'Email inválido'
  }
]

</script>
