<template>
  <q-btn
    label="Detalhes"
    color="secondary"
    class="full-width shadow-3"
    outline
    rounded
    @click="emailDialog = true"
  />

  <q-dialog v-model="emailDialog">
    <q-card>
    <div class="col-xs-12 col-sm-12 col-md-6 flex flex-center">
        <div class="column">
          <div class="col-12">
            <h4 class="text-center">Entre em contato</h4>
          </div>
          <q-form class="row q-pa-md q-col-gutter-xs">

            <q-input
            outlined
            v-model="name"
            label="Nome"
            type="text"
            class="col-xs-12 col-sm-12 col-md-9"
            lazy-rules
            :rules="[ val => val && val.length >= 2 || 'Informe um nome valido']"
            dense
            />

            <q-input
            outlined
            dense
            label="Telefone"
            class="col-xs-12 col-sm-12 col-md-3"
            color="secondary"
            mask="(##) #####-####"
            lazy-rules
            :rules="[ val => val && val.length === 15 || 'Informe um contato valido']"
            v-model="phone"
            />

            <q-input
            outlined
            v-model="email"
            label="E-mail"
            class="col-xs-12 col-sm-12 col-md-12"
            requerid
            lazy-rules
            :rules="[ val => val && val.length >= 3 || 'Informe um e-mail válido']"
            type="email"
            dense
            />
            <q-input
              v-model="text"
              label="Mensagem"
              class="col-xs-12 col-sm-12 col-md-12"
              outlined
              dense
              type="textarea"
            />
            <div class="col-12">
              <q-btn
              class="full-width"
              label="Enviar"
              type="submit"
              color="primary"/>
            </div>
          </q-form>
        </div>
      </div>
    </q-card>
  </q-dialog>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'emailDialog',

  setup () {
    return {
      emailDialog: ref(false),
      phone: ref(null)
    }
  }
}
</script>

<style>

</style>
