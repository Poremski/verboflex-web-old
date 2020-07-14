<template>
  <div>
    <div class="links top-right">
      <ul>
        <LocaleDropdown />
      </ul>
    </div>

    <div class="text-center">
      <div class="title mb-4">
        {{ $t(title) }}
      </div>

      <div class="links">
        <span>{{ $t('online_soon') }}</span>
      </div>
    </div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
import LocaleDropdown from '../components/LocaleDropdown'

export default {
  layout: 'Landing',

  components: {
    LocaleDropdown
  },

  metaInfo () {
    return { title: this.$t('home') }
  },

  data: () => ({
    title: window.config.appName
  }),
}
</script>

<style scoped>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.top-right {
  position: absolute;
  right: 10px;
  top: 18px;
}

.title {
  font-size: 85px;
}
</style>
