<template>
    <div>
    <h1>Dogs for Adoption</h1>
    <b-table stripped hover :items="dogs">
      <template #cell(name)="data">
        <router-link :to="`/pet/dogs/${data.index}`">{{ data.value }}</router-link>
      </template>
    </b-table>
    </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  data () {
    return {}
  },
  computed: {
    ...mapState([
      'dogs'
    ])
  }
}
</script>
