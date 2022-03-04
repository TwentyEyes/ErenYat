<template>
  <div>
    <Nav />
    <PageHeader title="Blog Details" />
    <Footer />
  </div>
</template>
<script>
  import Nav from "@/components/Nav";
  import PageHeader from "@/components/PageHeader";
  import Footer from "@/components/Footer";
  import CallToAction from "@/components/CallToAction";
  export default {
    name: 'Detail',
    components: {CallToAction, Footer, PageHeader, Nav},
    head(){
      return {
        title: "Apiton | Blog Details"
      }
    }
  }
</script>
