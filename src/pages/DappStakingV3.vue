<template>
  <div v-if="isReady" class="wrapper--dapp-staking">
    <div class="container--dapp-staking">
      <router-view />
    </div>
  </div>
</template>

<script lang="ts">
import { usePageReady } from 'src/hooks';
import { defineComponent } from 'vue';
export default defineComponent({
  setup() {
    const { isReady } = usePageReady();
    return { isReady };
  },
});
</script>

<style lang="scss" scoped>
@import 'src/css/quasar.variables.scss';

.wrapper--dapp-staking {
  @media (min-width: $lg) {
    padding-left: 0px;
    padding-right: 0px;
  }
}
</style>
