<template>
  <div class="entries">
    <section class="entry" v-for="entry in entries" :key="entry.id">
      <h2 class="entry-title"><router-link :to="`/entry/${entry.id}`">{{entry.title}}</router-link></h2>

      <router-link :to="`/entry/${entry.id}`">
        <figure class="entry-image">
          <img
            :src="entry.image.url"
            :width="entry.image.width" 
            :height="entry.image.height"
          />
        </figure>
      </router-link>
    </section>
  </div>
</template>

<script>
export default {
  props: {
    entries: Object,
  },
}
</script>

<style lang="scss" scoped>
.entries {
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  max-width: 896px;
}

.entry {
  margin: 0 12px 64px;
  width: calc(25% - 24px);
  &:hover a {
    opacity: 0.8;
  }
  & a {
    display: block;
  }

  @media screen and (max-width:600px) {
    width: calc(33% - 24px);
  }
  @media screen and (max-width:480px) {
    width: calc(50% - 24px);
  }
}

.entry-title {
  font-size: 16px;
  line-height: 1.6;
  font-weight: normal;
  & a {
    color: #333;
    text-decoration: none;
  }
}
.entry-image {
  & img {
    width: 100%;
    height: auto;
  }
}
</style>