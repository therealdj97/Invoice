<template id="page">
  <div class="">
    <!-- flex flex-col mx-10 space-y-10 -->
    <!-- <tutorial/> -->
    <Header />
    <sec1 />
    <Details />
    <footer />
    <button type="button" class="btn btn-outline-success btn-lg hover:bg-transparent" @click="print">Print</button>
  </div>
</template>

<script>
import sec1Vue from "../components/sec1.vue"
import Header from "../components/header.vue"
import Details from "../components/Details.vue"
import Tutorial from '../components/Tutorial.vue'
export default {
  components: { sec1Vue, Header, Details, Tutorial },
  name: 'IndexPage',
  data() {

  },
  methods: {
    print() {
      window.print();
    //  this.$VueHtmlToPaper('printMe');
      console.log("printed")
    }
  }
}
</script>
<style>
</style>
