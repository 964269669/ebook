<template>
  <div class="ebook-reader">
    <div id="read" @touchstart="touchStart">哈哈</div>
  </div>
</template>

<script>
import { mapGetters} from 'vuex'
import Epub from 'epubjs'
export default {
  name: 'EbookReader',
  components: {},
  data() {
    return {

    }
  },
  computed: {
    ...mapGetters(['fileName'])
  },
  created() {
  },
  mounted() {
    // const baseUrl = 'http://192.168.137.167:9001/epub/'
    // 2017_Book_InterdisciplinaryPerspectivesO
    // const fileName = this.$route.params.fileName.split('|').join('/')
    // this.$store.dispatch('setFileName', fileName).then(() => {
    //   // this.initEpub()
    // })
  },
  methods: {
    initEpub() {
      const baseUrl = 'http://192.168.137.167:9001/epub/' + this.fileName + '.epub'
      this.book = new Epub(baseUrl)
      this.rendition = this.book.renderTo('read', {
        width: innerWidth,
        height: innerHeight,
        method: 'default'
      })
      this.rendition.display()
      console.log(this.book) 
    },
    touchStart(e) {
      console.log(e)
    }
  }
}
</script>

<style lang="scss" scoped>
  @import '~@/assets/styles/global';

.div{
  font-size: px2rem(30);
}
</style>
