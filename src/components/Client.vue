<template>
  <!-- Un élément de liste, un client -->
  <q-item clickable v-ripple>
    <!-- Photo du client -->
    <q-item-section avatar>
      <q-avatar>
        <img src="https://randomuser.me/api/portraits/thumb/women/9.jpg">
      </q-avatar>
    </q-item-section>

    <!-- Nom, prénom et email du client -->
    <q-item-section>
      <q-item-label lines="1">
        Marchand Pauline
      </q-item-label>
      <q-item-label caption lines="2">
        pauline.marchand@divcom.ch
      </q-item-label>
    </q-item-section>

    <!-- Icône email -->
    <q-item-section side>
      <q-icon name="email" color="primary"/>
    </q-item-section>
  </q-item>
</template>

<script>
export default {
  name: 'CompClient'
}
</script>
