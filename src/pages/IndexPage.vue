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

    <div class="bg-red text-center text-weight-bolder flex flex-center q-pa-xs" style="font-size: 4vw;">
      <div class="text-white">
        Não somos depósito do Detran e
      </div>
      <div class="text-white">
       não realizamos remoções para guarda municipal e brigada militar
      </div>
    </div>

    <div class="q-px-md q-pt-md row" id="services">
      <div class="col-12 text-h4 text-center">
        Serviços
        <q-separator size="2px" color="red" class="q-my-md"/>
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

    <div class="q-px-md">
      <div class="col-12 text-h4 text-center">

          Galeria
          <q-separator size="2px" color="red" class="q-my-md"/>

      </div>

      <q-carousel
        swipeable
        animated
        v-model="slide"
        infinite
        thumbnails
        :autoplay="autoplay"

      >
        <!--<q-carousel-slide v-for="slide in slides" :key="slide.id" :name="slide.id" :img-src="slide.url" class="column no-wrap"/>-->
        <q-carousel-slide :name="1" img-src="~assets/new_carrousel/guincho1.png"/>
        <q-carousel-slide :name="2" img-src="~assets/new_carrousel/guincho2.png"/>
        <q-carousel-slide :name="3" img-src="~assets/new_carrousel/guincho3.png"/>
        <q-carousel-slide :name="4" img-src="~assets/new_carrousel/guincho4.png"/>
        <q-carousel-slide :name="5" img-src="~assets/new_carrousel/guincho5.png"/>
        <q-carousel-slide :name="6" img-src="~assets/new_carrousel/guincho6.png"/>
        <q-carousel-slide :name="7" img-src="~assets/new_carrousel/guincho7.png"/>
        <q-carousel-slide :name="8" img-src="~assets/new_carrousel/guincho8.png"/>
        <q-carousel-slide :name="9" img-src="~assets/new_carrousel/guincho9.png"/>
        <q-carousel-slide :name="10" img-src="~assets/new_carrousel/guincho22.png"/>
        <q-carousel-slide :name="11" img-src="~assets/new_carrousel/guincho11.png"/>
        <q-carousel-slide :name="12" img-src="~assets/new_carrousel/guincho12.png"/>
        <q-carousel-slide :name="13" img-src="~assets/new_carrousel/guincho13.png"/>
        <q-carousel-slide :name="14" img-src="~assets/new_carrousel/guincho14.png"/>
        <q-carousel-slide :name="15" img-src="~assets/new_carrousel/guincho15.png"/>
        <q-carousel-slide :name="16" img-src="~assets/new_carrousel/guincho23.png"/>
        <q-carousel-slide :name="17" img-src="~assets/new_carrousel/guincho17.png"/>
        <q-carousel-slide :name="18" img-src="~assets/new_carrousel/guincho18.png"/>
        <q-carousel-slide :name="19" img-src="~assets/new_carrousel/guincho19.png"/>
        <q-carousel-slide :name="20" img-src="~assets/new_carrousel/guincho20.png"/>
      </q-carousel>
      <!--
      <q-carousel
        animated
        swipeable
        infinite
        v-model="slide"
        :autoplay="autoplay"
        max-height="720px"
        class="lt-sm"
      >
        <q-carousel-slide v-for="slide in slides" :key="slide.id" :name="slide.id" :img-src="slide.url" ></q-carousel-slide>
      </q-carousel>
    -->
    </div>

    <div class="row flex items-start" id="contacts">
      <div class="col-xs-12 col-sm-12 col-md-12 flex flex-center">
        <div class="row">
          <div class="col-12 text-h4 text-center q-my-md">
            Contatos
          </div>
          <div class="row col-xs-12 col-sm-12 col-md-12 justify-around">
            <div class="row q-pa-xs text-center">
              <q-icon name="phone" class="row q-mr-xs" style="font-size:20px;"/>
              <p>(51) 99718-8828</p>
            </div>
            <div class="row q-pa-xs text-center">
              <q-icon name="mail" class="row q-mr-xs" style="font-size:20px;"/>
              <p>guinchonh@gmail.com</p>
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
            class="col-6 whatsapp"
            icon="mdi-whatsapp"
            text-color="white"
            stack
            unelevated
            target="_blank"
            rel="noopener noreferrer"
            href="https://wa.me/5551997188828"
            label="WhatsApp"
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
    const slides = [
      { id: 1, url: 'src/assets/new_carrousel/guincho1.png' },
      { id: 2, url: 'src/assets/new_carrousel/guincho2.png' },
      { id: 3, url: 'src/assets/new_carrousel/guincho3.png' },
      { id: 4, url: 'src/assets/new_carrousel/guincho4.png' },
      { id: 5, url: 'src/assets/new_carrousel/guincho5.png' },
      { id: 6, url: 'src/assets/new_carrousel/guincho6.png' },
      { id: 7, url: 'src/assets/new_carrousel/guincho7.png' },
      { id: 8, url: 'src/assets/new_carrousel/guincho8.png' },
      { id: 9, url: 'src/assets/new_carrousel/guincho9.png' },
      { id: 10, url: 'src/assets/new_carrousel/guincho22.png' },
      { id: 11, url: 'src/assets/new_carrousel/guincho11.png' },
      { id: 12, url: 'src/assets/new_carrousel/guincho12.png' },
      { id: 13, url: 'src/assets/new_carrousel/guincho13.png' },
      { id: 14, url: 'src/assets/new_carrousel/guincho14.png' },
      { id: 15, url: 'src/assets/new_carrousel/guincho15.png' },
      { id: 16, url: 'src/assets/new_carrousel/guincho23.png' },
      { id: 17, url: 'src/assets/new_carrousel/guincho17.png' },
      { id: 18, url: 'src/assets/new_carrousel/guincho18.png' },
      { id: 19, url: 'src/assets/new_carrousel/guincho19.png' },
      { id: 20, url: 'src/assets/new_carrousel/guincho20.png' },
      { id: 21, url: 'src/assets/atendimento.jpeg' }
    ]

    return {
      emailDialog: ref(false),
      carrouselTop: ref(1),
      slide: ref(1),
      phone: ref(null),
      autoplay: ref(true),
      slides
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

.whatsapp {
  background-color: #25d366;
}
</style>
