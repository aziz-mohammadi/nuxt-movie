<template>
  <div class="px-10 bg-gray-200">
    <TheHeader />
    <Movies />
    <TheFooter />
  </div>
</template>

<script>
import TheHeader from '../components/UI/TheHeader.vue'
import TheFooter from '../components/UI/TheFooter.vue'
export default {
  name: 'IndexPage',
  components: {
    TheHeader,
    TheFooter,
  }
}
</script>
