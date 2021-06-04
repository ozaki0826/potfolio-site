<template>
  <div class="about">
    <h1>ozaki's Portfolio</h1>

    <section v-for="entry in entries">
      <h2 :onClick="() => linkEntry(entry.id)">{{entry.title}}</h2>
      <figure>
        <img 
          :src="entry.image.url"
          :width="entry.image.width"
          :height="entry.image.height"
          alt=""
        />
      </figure>
      <div v-html="entry.body" />
    </section>
    
  </div>
</template>

<script>
import { onMounted, computed } from 'vue'
import { useStore } from 'vuex'
import { useRouter } from 'vue-router'
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  setup() {
    const router = useRouter()
    const store = useStore();
    const getEntries = () => store.dispatch('getEntries')

    onMounted(() => {
      getEntries()
    })

    const linkEntry = (id) => {
      router.push(`/entry/${id}`)
    }

    return {
      getEntries,
      getEntry: (id) => store.dispatch('getEntry', id),
      entries: computed(() => store.state.entries),
      linkEntry
    }
  }
}
</script>