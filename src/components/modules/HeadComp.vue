<template>
  <div class="headComp">
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  name: 'headComp',
  computed: mapGetters({
    'title': 'getTitle'
  })
}
</script>
