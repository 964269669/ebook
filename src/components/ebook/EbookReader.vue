<template>
  <div class="ebook-reader">
    <div class="div">你好</div>
  </div>
</template>

<script>
export default {
  name: 'EbookReader',
  components: {},
  data() {
    return {

    }
  },
  created() {
  },
  mounted() {
    // const baseUrl = 'http://192.168.43.99:9001/epub/'
    // // 2017_Book_InterdisciplinaryPerspectivesO
    // const fileName = this.$route.params.fileName.split('|').join('/')
    // console.log(`${baseUrl}${fileName}`)
  },
  methods: {
  }
}
</script>

<style lang="scss" scoped>
  @import '~@/assets/styles/global';

.div{
  font-size: px2rem(30);
}
</style>
