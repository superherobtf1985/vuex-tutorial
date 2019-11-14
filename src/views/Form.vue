<template>
  <div class="form">
    <h1>Formページ</h1>
    <HeadComp/>
    <component :is="isComponent"></component>
    <button @click="buttonAction">{{ button }}</button>
  </div>
</template>

<script>
import HeadComp from '@/components/modules/HeadComp.vue'
import TextareaComp from '@/components/modules/TextareaComp.vue'
import StringComp from '@/components/modules/StringComp.vue'
import { mapActions, mapGetters } from 'vuex'

export default {
  name: 'form',
  methods: mapActions('Form', {
    'buttonAction': 'buttonAction'
  }),
  computed: mapGetters('Form', {
    'button': 'getButton',
    'isComponent': 'getComponent'
  }),
  components: {
    HeadComp,
    TextareaComp,
    StringComp,
  }
}
</script>
