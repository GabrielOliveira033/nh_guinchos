<template>
  <q-page class="">
    <div class="row" style="padding:10px">
      <div class="col-12 row justify-around">
        <q-img
        src="~assets/black_logo.png"
        class="q-mt-auto"
        style="height: 90px; width: 470px; max-width: 300px"
        />
        <div class="col-xs-12 col-sm-12 col-md-4 gt-sm flex flex-center">
          <q-btn
          color="red"
          unelevated
          rounded
          icon-right="phone"
          label="(51) 99718-8828"
          href="tel:+55 51 99718-8828"

          />
        </div>
        <q-list class="row gt-sm flex flex-center">
          <q-item clickable v-ripple>
            <a href="#home"><q-item-section class="q-pa-sm">INICIO</q-item-section></a>
          </q-item>
          <q-item clickable v-ripple>
            <a href="#services"><q-item-section class="q-pa-sm">SERVIÇOS</q-item-section></a>
          </q-item>
          <q-item clickable v-ripple>
            <a href="#contacts"><q-item-section class="q-pa-sm">CONTATOS</q-item-section></a>
          </q-item>
        </q-list>
      </div>
    </div>
    <q-separator size="3px" color="red"/>
    <div id="home">
      <q-carousel
        animated
        v-model="carrouselTop"
        infinite
        :autoplay="autoplay"
      >
        <q-carousel-slide :name="1" img-src="~assets/freeway.gif">
          <div class="absolute-center text-weight-bolder text-h4 text-center text-white bg-red window-width">
            Guincho 24 horas
          </div>
        </q-carousel-slide>
        <q-carousel-slide :name="2" img-src="~assets/atendimento.jpeg">
          <div class="absolute-center text-weight-bolder text-h4 text-center text-white bg-red window-width">
            Atendimento em Campo Bom, Novo Hamburgo e Região - RS
          </div>
        </q-carousel-slide>
        <q-carousel-slide :name="3" img-src="~assets/call.png">
          <div class="absolute-center text-weight-bolder text-h4 text-center text-white bg-red window-width">
            Ligue agora! Temos os melhores preços
          </div>
        </q-carousel-slide>
      </q-carousel>
    </div>
    <div class="q-pa-md row" id="services">
      <div class="col-12 text-h4 text-center">
        Serviços
        <q-separator size="2px" color="red"/>
      </div>

      <div class="column col-xs-12 col-sm-6 col-md-3 flex flex-center q-pa-md">
        <q-icon name="mdi-tow-truck" size="4rem" color="red"/>
        <h5 class="text-center">Reboque</h5>
      </div>
      <div class="column col-xs-12 col-sm-6 col-md-3 flex flex-center q-pa-md">
        <q-icon name="mdi-medical-bag" size="4rem" color="red"/>
        <h5 class="text-center">Socorro</h5>
      </div>
      <div class="column col-xs-12 col-sm-6 col-md-3 flex flex-center q-pa-md">
        <q-icon name="mdi-truck" size="4rem" color="red"/>
        <h5 class="text-center">Frete</h5>
      </div>
      <div class="column col-xs-12 col-sm-6 col-md-3 flex flex-center q-pa-md">
        <q-icon name="mdi-hours-24" size="4rem" color="red"/>
        <h5 class="text-center">Guincho 24 Horas</h5>
      </div>
    </div>
    <div class="q-pa-md">
      <div class="col-12">
        <q-separator size="2px" color="red"/>
        <h4 class="text-center">
          Galeria
        </h4>
      </div>

      <q-carousel
        swipeable
        animated
        v-model="slide"
        infinite
        :autoplay="autoplay"
        height="400px"
        class="gt-sm"
      >
        <q-carousel-slide :name="1" class="column no-wrap gt-sm">
          <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
            <q-img class="rounded-borders col-6 full-height" src="~assets/guinch01.png"/>
            <q-img class="rounded-borders col-6 full-height" src="~assets/guinch02.jpeg"/>
          </div>
        </q-carousel-slide>
        <q-carousel-slide :name="2" class="column no-wrap gt-sm">
          <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
            <q-img class="rounded-borders col-6 full-height" src="~assets/guinch02.jpeg" />
            <q-img class="rounded-borders col-6 full-height" src="~assets/guinch03.jpeg" />
          </div>
        </q-carousel-slide>
        <q-carousel-slide :name="3" class="column no-wrap gt-sm">
          <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
            <q-img class="rounded-borders col-6 full-height" src="~assets/guinch03.jpeg" />
            <q-img class="rounded-borders col-6 full-height" src="~assets/guinch01.png" />
          </div>
        </q-carousel-slide>
      </q-carousel>

      <q-carousel
        swipeable
        animated
        v-model="slide"
        infinite
        :autoplay="autoplay"
        height="400px"
        class="lt-sm"
      >
        <q-carousel-slide :name="1" img-src="~assets/guinch01.png" />
        <q-carousel-slide :name="2" img-src="~assets/guinch02.jpeg" />
        <q-carousel-slide :name="3" img-src="~assets/guinch03.jpeg" />
      </q-carousel>
    </div>

    <div class="row flex items-start" id="contacts">
      <div class="col-xs-12 col-sm-12 col-md-12 flex flex-center">
        <div class="row">
          <div class="col-12">
            <h4 class="text-center">Contatos</h4>
          </div>
          <div class="row col-xs-12 col-sm-12 col-md-12 justify-around">
            <div class="row q-pa-xs text-center">
              <q-icon name="phone" class="row q-mr-xs" style="font-size:20px;"/>
              <p>(51) 99718-8828</p>
            </div>
            <div class="row q-pa-xs text-center">
              <q-icon name="mail" class="row q-mr-xs" style="font-size:20px;"/>
              <p>nh_guinchos@gmail.com</p>
            </div>
          </div>

          <div class="col-12 flex flex-center">
              <a href="https://wa.me/5551997188828" target="_blank" rel="noopener noreferrer" class="q-pa-xs col-1">
                <img
                src="~assets/whatsapp.png"
                style="height: 5%; max-width: 25px"
                />
              </a>
              <a href="https://instagram.com/nh_guinchos?igshid=YmMyMTA2M2Y=" target="_blank" rel="noopener noreferrer" class="q-pa-xs">
                <img
                src="~assets/instagram.png"
                style="height: 5%; max-width: 25px"
              />
              </a>
              <a href="https://www.facebook.com/bynho.guinchos" target="_blank" rel="noopener noreferrer" class="q-pa-xs">
                <img
                src="~assets/facebook.png"
                style="height: 5%; max-width: 25px"
                />
              </a>
          </div>
         <!-- Criar Back para enviar e-mail
          <EmailDialog/>
        -->
        </div>
      </div>
    </div>
    <q-footer
      class="lt-sm"
    >
      <div class="row">
          <q-btn
            class="col-6"
            icon="mdi-whatsapp"
            text-color="white"
            stack
            unelevated
            target="_blank"
            rel="noopener noreferrer"
            href="https://wa.me/5551997188828"
            label="WhatsApp"
            style=" background-color: #25d366"
          />
          <q-btn
            class="col-6"
            color="light blue"
            label="Ligue Agora!"
            href="tel:+55 51 99718-8828"
            icon="mdi-phone"
            stack
            unelevated
          />
      </div>
    </q-footer>
      <!--
        <div class="absolute-top-right text-right q-pa-xs">
          <a href="https://wa.me/5551997188828" target="_blank" rel="noopener noreferrer" class="q-pa-xs col-1">
            <img
            src="~assets/whatsapp.png"
            style="height: 5%; max-width: 25px"
            />
          </a>
          <a href="https://instagram.com/nh_guinchos?igshid=YmMyMTA2M2Y=" target="_blank" rel="noopener noreferrer" class="q-pa-xs">
            <img
            src="~assets/instagram.png"
            style="height: 5%; max-width: 25px"
            />
          </a>
          <a href="https://www.facebook.com/bynho.guinchos" target="_blank" rel="noopener noreferrer" class="q-pa-xs">
            <img
            src="~assets/facebook.png"
            style="height: 5%; max-width: 25px"
            />
          </a>
        </div>
       -->
    <div class="gt-sm q-mt-lg q-pa-xs">
      © 2022 Todos os direitos reservados
    </div>
  </q-page>
</template>

<script>
import { defineComponent, ref } from 'vue'

// import EmailDialog from './component/emailDialog.vue'

export default defineComponent({
  name: 'IndexPage',
  setup () {
    return {
      emailDialog: ref(false),
      carrouselTop: ref(1),
      slide: ref(1),
      phone: ref(null),
      autoplay: ref(true)
    }
  },
  components: {
    // EmailDialog
  }
})
</script>

<style scoped>
a {
  text-decoration: none;
  color: black;
  text-align: center;

}
</style>
