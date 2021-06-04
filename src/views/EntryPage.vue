<template>
  <article v-if="entry">
    <h1>{{entry.title}}</h1>

    <div class="body" v-html="entry.body">
    </div>
  </article>
</template>

<script>
import { onMounted, computed } from 'vue'
import { useStore } from 'vuex'
import { useRoute } from 'vue-router'

export default {
  components: {
    },
  setup() {
    const store = useStore()
    const route = useRoute()
    const getEntry = () => store.dispatch('getEntry', route.params.id)

    onMounted(() => {
      getEntry()
    })

    return {
      getEntry,
      entry: computed(() => store.state.entry),
    }
  }
}
</script>

<style>
.body {
  ::v-deep img {
    width: 100%;
    height: auto;
  }
}
</style>