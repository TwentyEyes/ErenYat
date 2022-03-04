<template>
  <div>
    <Nav />
    <Banner />
    <Service :data-servis="serviseArray" />
    <Testimonial />
    <Brands />
    <FunFact />
    <Footer />
  </div>
</template>

<script>

  import Nav from "../components/Nav";
  import Banner from "../components/Banner";
  import Footer from "../components/Footer";
  import Service from "../components/Service";
  import CallToActionThree from "../components/CallToActionThree";
  import CallToActionTwo from "../components/CallToActionTwo";
  import Pricing from "../components/Pricing";
  import Testimonial from "../components/Testimonial";
  import Brands from "../components/Brands";
  import FunFact from "../components/FunFact";
  export default {
    head(){
      return {
        title: "Eren Yatçılık | Boğaz Turu | Yemekli Turlar | Evlenme Teklifi | Yüzme Turlari"
      }
    },
    name: 'IndexVue',
    components: {
      FunFact,
      Brands,
      Testimonial,
      Pricing,
      CallToActionTwo,
      CallToActionThree,
      Service,
      Footer,
      Banner,
      Nav
    },
    data() {
      return {
        serviseArray: [
          {
            col: '12',
            img: '/images/bogaz-turu.jpeg',
            title: 'Boğaz Turu',
            desc: 'Vip yatları ile Marmara denizinin incileri olan doğa harikası adalarımıza "Kınalıada (Proti: İlk), Burgaz (Antigoni), Heybeli (Halki: Bakır), Büyükada (Prinkipo: Prens)" seyahat edebilirsiniz.',
            link: 'test',
            linkName: 'Daha Fazla Bilği'
          },
          {
            col: '6',
            img: '/images/evlenme-teklifi.JPG',
            title: 'Evlenme Teklifi',
            desc: 'Evlilik Teklifi Paketleri, İstanbul Boğazı’na hayran olanlar için Boğazda yat turu şeklinde gerçekleşen vazgeçilmez sürpriz paketleridir. Köprüde lazerle evlilik teklifi organizasyonları , kimi zaman sürpriz evlilik teklifi ve kimi zaman da doğum günü organizasyonları için uzun süre cazibesini korumaya devam edecektir.',
            link: 'test',
            linkName: 'Daha Fazla Bilği'
          },
          {
            col: '6',
            img: '/images/dogum-gunu.JPG',
            title: 'Doğum Günü',
            desc: 'Eşinizin yada kız arkadaşınızın doğum günüde ona bir sürpriz hazırlamak ve bu önemli günü unutulmaz kılmak istiyorsunuz. Fakat nasıl bir organizasyon yapacağınıza karar veremiyorsunuz. Alışılmış basmakalıp bir etkinlik ile hem gönlünü almak hem de davetlilere gücünüzü göstermek istiyorsunuz. Ayrıca gelen konukların bu geceden olumlu düşünceler ile ayrılması en büyük isteğiniz. O halde bu doğum gününü yatta kutlamaya ne dersiniz?',
            link: 'test',
            linkName: 'Daha Fazla Bilği'
          },
          {
            col: '6',
            img: '/images/yuzme.jpg',
            title: 'Yüzme Turları',
            desc: 'Yüzme turu organizasyonları hakkında bilmek ve görmek isteyeceğiniz her şey bu sayfada mevcuttur. Yüzmek için nerelere gidildiği ve ne kadar ücret talep edildiği ile menü olarak nelerin sunulduğunu yazının devamında okuyacaksınız. Fiyatları öğrenmek için firmamızla iletişim kurmanız gerekmiyor çünkü şeffaf bir fiyat politikası izlediğimiz için saatlik ve günlük yat kiralama fiyatlarının yanı sıra menü ücretleri ve ekstra hizmetler için sizlerden talep ettiğimiz tüm fiyatları bu sayfada paylaştık. Firmamızla sadece rezervasyon aşamasında iletişim kurarak seçtiğiniz yatın istediğiniz tarihte müsait olup olmadığını yetkililere sorabilir ve müsaitlik varsa kendi adınıza yatı rezerve edebilirsiniz.',
            link: 'test',
            linkName: 'Daha Fazla Bilği'
          },
          {
            col: '6',
            img: '/images/yemek.jpg',
            title: 'Yemekli Turlar',
            desc: 'Yemekli yat turu İstanbul’da yapılabilecek en keyifli ve büyüleyici organizasyonların başında gelmekte. İstanbul’da yaşayan veya ziyaret eden herkesin mutlaka en az bir defa bu deneyimi yaşamasını öneriyoruz. İstanbul’un büyülü atmosferini boğazda yaşamak, yemeğinizi yerken tarihi yalıları ve sarayları izlemek gerçekten büyüleyici.',
            link: 'test',
            linkName: 'Daha Fazla Bilği'
          }
        ]
      }
    }
  }
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=League+Spartan:wght@100;200;300;400;500;600;700;800;900&family=Open+Sans:ital,wght@0,400;0,700;1,400&display=swap');

ul, li, a, h1, h2, h3, h4, h5, h6, div, p {
  display:block;
  font-family: 'League Spartan', sans-serif !important;
} 
</style>