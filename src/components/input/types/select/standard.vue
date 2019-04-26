<template>
  <div>
    <v-select
      :options="items"
      label="name"
      :placeholder="placeholder"
      v-model="item"/>
  </div>
</template>

<script>
  import select_methods from './methods'

  export default {
    name: "select_standard",
    props: {
      type: {
        type: String,
        required: true,
      },
      clist:{
        type: String,
        required: true,
        default: null
      },
      cvalue:{
        required: true
      },
      placeholder:{
        type: String,
        required: false
      },
      citems:{
        type: Array,
        required: false,
        default: null
      },
    },
    data () {
      return {
        items: [],
        item: null
      }
    },
    mixins:[select_methods]
  }
</script>
