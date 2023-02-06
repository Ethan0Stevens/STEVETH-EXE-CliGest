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
    ...mapGetters('clients', ['clients'])
  },
  methods: {
    ...mapActions('clients', ['getClientsApi'])
  },
  beforeMount () {
    this.getClientsApi()
  }
}
</script>
