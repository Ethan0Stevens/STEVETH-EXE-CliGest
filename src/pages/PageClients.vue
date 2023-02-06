<template>
  <q-page padding>
    <h3>Liste des clients</h3>
    <q-list
      class="rounded-borders"
      bordered
      separator
    >
      <client
        v-for="client in clients"
        :key="client.id.value"
        :client="client" />

    </q-list>
  </q-page>
</template>

<script>

import { mapActions, mapGetters } from 'vuex'

export default {
  name: 'PageClients',
  components: {
    client: require('components/Client.vue').default
  },
  computed: {
    // Mappage des getters du store
    ...mapGetters('clients', ['clients'])
  },
  methods: {
    // Mappage des actions du store
    ...mapActions('clients', ['getClientsApi'])
  },
  // A la creation de la page
  created () {
    // Essai de générer la liste de clients depuis l'api
    this.getClientsApi()
  }
}
</script>
