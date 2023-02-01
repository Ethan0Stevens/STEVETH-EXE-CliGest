<template>
  <q-page padding>
    <h3>Liste des clients</h3>
    <q-list
      class="rounded-borders"
      bordered
      separator
    >
      <client/>
    </q-list>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'
import { mapGetters } from 'vuex'

export default defineComponent({
  name: 'PageClients',
  components: {
    client: require('../components/Client').default
  },
  computed: {
    // Mappage des getters ('nomNamespace', ['nomGetter'])
    ...mapGetters('clients', ['getClients'])
  }
})
</script>
