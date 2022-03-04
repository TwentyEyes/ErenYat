<template>
  <header class="site-header header-one">
    <nav :class="`navbar navbar-expand-lg navbar-light header-navigation stricky ${sticky ? 'stricked-menu stricky-fixed' : ''}`">
      <div class="topNavHeaderContent mobile">
        <ul>
          <li><a href="https://www.google.com/maps/dir//eren+yatcilik/data=!4m6!4m5!1m1!4e2!1m2!1m1!1s0x14cac90c29942c69:0xde90b3fc6a2e3e69?sa=X&ved=2ahUKEwj60MDZoaf2AhWVP-wKHSa_DmgQ9Rd6BAgREAU" target="_blank"><i class="fa fa-map-pin"></i>Bebek / İstanbul</a></li>
          <li><a href="mailto:erenyatcilik@gmail.com"><i class="fa fa-paper-plane"></i>erenyatcilik@gmail.com</a></li>
          <li><a href="tel:+905327078095"><i class="fa fa-phone"></i>0532 707 80 95</a></li>
          <li class="wha"><a href="https://api.whatsapp.com/send?phone=905327078095&amp;text=Merhabalar..%20Yat%20Kiralama%20ile%20ilgili%20bilgi%20almak%20istiyorum" target="_blank"><i class="fa fa-whatsapp"> </i></a></li>
          <li class="inst"><a href="https://www.instagram.com/erenyacht/" target="_blank"><i class="fa fa-instagram"></i></a></li>
        </ul>
      </div>
      <div class="container clearfix">
        <!-- Brand and toggle get grouped for better mobile display -->
        <div class="logo-box clearfix">
          <a class="navbar-brand" href="/">
            <img src="/images/logo.png" class="main-logo" width="60%" alt="Awesome Image" />
          </a>
          <button class="menu-toggler" data-target=".main-navigation">
            <span @click="mobileToggle = !mobileToggle" class="fa fa-bars"></span>
          </button>
        </div><!-- /.logo-box -->
        <!-- Collect the nav links, forms, and other content for toggling -->
        <div :class="`main-navigation ${mobileToggle ? 'showen' : ''}`" :style="`display: ${mobileToggle ? 'block' : 'none'}`">
          <ul class=" navigation-box one-page-scroll-menu ">
            <li class="current scrollToLink">
              <a href="/">Ana Sayfa</a>
            </li>
            <li class="scrollToLink">
              <a href="/hakkimizda">Hakkımızda</a>
            </li>
            <li class="scrollToLink">
              <a href="#blog">Hizmetlerimiz & Yatlarımız</a>
              <ul class="sub-menu" style="display: block">
                <li><nuxt-link to="/blog">Yatlarımız</nuxt-link></li>
                <li><nuxt-link to="/blog/detail">Hizmetlerimiz</nuxt-link>
                  <ul class="sub-menu" style="display: block">
                    <li><nuxt-link to="/blog">Yatlarımız</nuxt-link></li>
                    <li><nuxt-link to="/blog/detail">Hizmetlerimiz</nuxt-link>
                      
                    </li>
                  </ul><!-- /.sub-menu -->
                </li>
              </ul><!-- /.sub-menu -->
            </li>
            <li class="scrollToLink">
              <a href="#contact">İletişim</a>
            </li>
          </ul>
        </div>
      </div>
      <!-- /.container -->
    </nav>


  </header>
</template>

<script>
  export default {
    name: "Nav",
    data(){
      return {
        sticky: false,
        mobileToggle: false
      }
    },
    mounted() {
      window.addEventListener('scroll', this.handleScroll);
    },
    methods: {

      handleScroll() {
        if (window.scrollY > 70) {
          this.sticky = true
        } else if (window.scrollY < 70) {
          this.sticky = false
        }
      },
    }
  }
</script>

<style scoped>
.navbar-brand img{
 
    background:#fff;
    border-radius: 50px;
    padding:10px;
  
}
.topNavHeaderContent {
  background:#fff;
  width:100%;
  height: 40px;
}
.stricked-menu.stricky-fixed .topNavHeaderContent ul {
  box-shadow: 2px 2px 9px 2px transparent;
}
.topNavHeaderContent ul {
  margin:0px;
  list-style-type: none;
  padding:0px;
  display:inline-flex;
  justify-content: center;
  align-content: center;
  width:100%;
  height: 40px;
  transition-duration:0.3s;
}
.topNavHeaderContent ul li{
  text-align: center;
  display:flex;
  justify-content: center;
  align-content: center;
  align-items: center;
}
.topNavHeaderContent ul li a{
  padding:0px 25px;
  color:#9053dd;
  text-align: center;
  font-size:15px;
  height: 25px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.topNavHeaderContent ul li a i{
  margin-right: 10px;
  color:#f7c324;
  font-size:25px;
}
.topNavHeaderContent ul li.wha a i {
  color:#44be53;
}
.topNavHeaderContent ul li.inst a i {
  color:#a461e5;
}

.navbar  {
  display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    width: 100%;
}
</style>
