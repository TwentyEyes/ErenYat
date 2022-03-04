<template>
  <div>
    <Nav />
    <PageHeader title="Hizmetlerimiz" />
    <Footer />
  </div>
</template>
<script>
  import Nav from "@/components/Nav";
  import PageHeader from "@/components/PageHeader";
  import Footer from "@/components/Footer";
  export default {
    components: {Footer, PageHeader, Nav},
    head(){
      return {
        title: "Eren Yatçılık | Boğaz Turu | Yemekli Turlar | Evlenme Teklifi | Yüzme Turlari"
      }
    }
  }
</script>
