<template>
      <div ref="myListRef" class="row justify-right q-gutter-sm">

        <q-page class="column items-right justify-center">
            <q-card class="create-account-card">
            <div>

                <q-card-section class="row justify-center">
                    <div class="text-h6">Correo de contacto</div>
                </q-card-section>
                <q-card-section>
                    <div class="text-subtitle1">
                        ¡Envianos un correo de información acerca de tu consulta!
                    </div>
                </q-card-section>


                <q-separator inset />

                <q-card-section class="column q-gutter-md">

                    <q-select
                        label="Motivo"
                        transition-show="jump-up"
                        transition-hide="jump-up"
                        filled
                        v-model="select"
                        :options="options"
                    />

                    <q-input filled v-model="fullName" label="Nombre Completo *"></q-input>

                    <q-input filled v-model="enterprise" label="Empresa *"></q-input>

                    <q-input filled v-model="email" type="email" suffix="@gmail.com"></q-input>


                    <h7 style="margin-top: 40px;">Envianos tu Solicitud:</h7>
                    <q-editor v-model="message"/>

                </q-card-section>

                <q-card-actions align="right">
                    <q-btn flat>Cancelar</q-btn>
                    <q-btn color="primary" type="submit">Enviar</q-btn>
                </q-card-actions>
            </div>
            </q-card>
        </q-page>

      </div>
  </template>

<script setup>
import { ref } from 'vue'

const fullName = ref('')
const message = ref('')
const enterprise = ref('')
const select = ref('')
const options = ref([
        'Solicitud de cotización', 'Otras consultas',
      ])
</script>
