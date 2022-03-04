<template>
  <section class="service-one" id="services">
    <div class="container">
      <div class="block-title text-center">
        <h2 class="block-title__title black-text-color">Neler mi var <br> Size Özel?</h2><!-- /.block-title__title -->
      </div><!-- /.block-title -->
      <div class="row">
        <div  v-for="item in dataItem" :key="item.id" :class="'col-lg-' + item.col">
          <div class="service-one__single">
            <span class="service-one__dot-1"></span>
            <span class="service-one__dot-2"></span>
            <span class="service-one__dot-3"></span>
            <div class="service-one__icon">
              <img :src="item.img" :alt="item.img">
            </div><!-- /.service-one__icon -->
            <h3 class="service-one__title" v-html="item.title"></h3><!-- /.service-one__title -->
            <p class="service-one__text" v-html="item.desc">There are many variations of <br> passages of lorem ipsum is <br> simply free text but majority <br> have suffered.</p><!-- /.service-one__text -->
            <a :href="item.link" class="service-one__btn">{{item.linkName}}</a>
          </div><!-- /.service-one__single -->
        </div><!-- /.col-lg-4 -->
      </div><!-- /.row -->
    </div><!-- /.container -->
  </section>
</template>

<script>
    export default {
        name: "Service",
        props: ['dataServis'],
        data () {
          return {
            dataItem: this.dataServis
          }
        }
    }
</script>

<style scoped>

</style>
