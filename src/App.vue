<template>
  <div>
    <!--  Config NAVBAR  -->
    <b-navbar class="py-3 box-shadow" fixed="top" toggleable="md" type="light" variant="light">
    <!--  Marca NAVBAR  -->
      <b-navbar-brand href="#">
        <img src="./img/caravan.svg" alt="Caravan">
      </b-navbar-brand>
    <!--   MENU HAmburguer   -->
      <b-navbar-toggle target="nav-collapse"/>
    <!--  Config MENU Hamburguer    -->
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item-dropdown text="Locais" right>
            <b-dropdown-item href="#">California</b-dropdown-item>
            <b-dropdown-item href="#">Paris</b-dropdown-item>
            <b-dropdown-item href="#">Dublin</b-dropdown-item>
          </b-nav-item-dropdown>
          <b-nav-item href="#">Planos</b-nav-item>
          <b-nav-item href="#">Contato</b-nav-item>
          <b-nav-item href="#">Login</b-nav-item>
          <b-button class="ml-md-2" variant="outline-primary" href="#">Inscreva-se</b-button>
        </b-navbar-nav>

      </b-collapse>
    </b-navbar>
    <section>
      <b-container fluid class="config-after-top">
        <div class="row bg-dark text-white">
          <div class="col-lg-7 p-0">
            <b-carousel
                    id="carousel-1"
                    v-model="slide"
                    :interval="4000"
                    controls
                    indicators
                    background="#ababab"
                    img-width="1024"
                    img-height="480"
                    style="text-shadow: 1px 1px 2px #333;"
                    @sliding-start="onSlideStart"
                    @sliding-end="onSlideEnd"
            >
              <!-- Text slides with image -->
              <b-carousel-slide
                      img-src="./img/california.jpg"
              >
                <div class="carousel-caption">
                  <h3 class="display-4">California</h3>
                </div>
              </b-carousel-slide>

              <!-- Slides with custom text -->
              <b-carousel-slide
                      img-src="./img/paris.jpg"
              >
                <div class="carousel-caption">
                  <h3 class="display-4">Paris</h3>
                </div>
              </b-carousel-slide>
              <b-carousel-slide
                      img-src="./img/dublin.jpg"
              >
                <div class="carousel-caption">
                  <h3 class="display-4">Dublin</h3>
                </div>
              </b-carousel-slide>
            </b-carousel>
          </div>

          <div class="col-lg-5 p-4">
            <h1 class="display-4">
              Realiza a viagem do seu sonho
            </h1>
            <p class="lead">
              O melhor local para viajar é com a Caravan,
              mais de 5.000 excursões concluídas.
            </p>
            <div class="input-group input-group-lg">
              <input type="text" class="form-control" placeholder="E-mail" aria-label="E-mail" aria-describedby="button-addon2">
              <div class="input-group-append">
                <button class="btn btn-primary" type="button" id="button-addon2">inscreva-se</button>
              </div>
            </div>
          </div>
        </div>
      </b-container>
    </section>
    <section class="py-5 bg-light text-center">
      <div class="container">
        <div class="my-5">
          <span class="h6 d-block"> TUDO DE MELHOR PRA VOCÊ </span>
          <h2 class="display-4 text-primary"> Aproveite as Vantagens </h2>
        </div>
      </div>
      <div class="row">
        <!--
          justify-content-center - Justifica o item no centro
          display-flex - 100px no display flex, alinha ao centro.
        -->
        <div class="col-xl-4 col-md-6">
          <div class="icone d-flex justify-content-center">
            <img src="./img/icones/passaporte.svg" alt="Passaporte">
          </div>
          <h3>Documentos</h3>
          <p>O Lorem Ipsum é um texto modelo da indústria tipográfica e de impressão. O Lorem Ipsum tem vindo a ser o texto padrão usado por estas indústrias desde o ano de 1500.</p>
        </div>
        <div class="col-xl-4 col-md-6">
          <div class="icone d-flex justify-content-center">
            <img src="./img/icones/passagens.svg" alt="Passaporte">
          </div>
          <h3>Passagens</h3>
          <p>O Lorem Ipsum é um texto modelo da indústria tipográfica e de impressão. O Lorem Ipsum tem vindo a ser o texto padrão usado por estas indústrias desde o ano de 1500.</p>
        </div>
        <div class="col-xl-4 col-md-6">
          <div class="icone d-flex justify-content-center">
            <img src="./img/icones/translado.svg" alt="Passaporte">
          </div>
          <h3>Translado</h3>
          <p>O Lorem Ipsum é um texto modelo da indústria tipográfica e de impressão. O Lorem Ipsum tem vindo a ser o texto padrão usado por estas indústrias desde o ano de 1500.</p>
        </div>
        <div class="col-xl-4 col-md-6">
          <div class="icone d-flex justify-content-center">
            <img src="./img/icones/praias.svg" alt="Praias">
          </div>
          <h3>Praias</h3>
          <p>O Lorem Ipsum é um texto modelo da indústria tipográfica e de impressão. O Lorem Ipsum tem vindo a ser o texto padrão usado por estas indústrias desde o ano de 1500.</p>
        </div>
        <div class="col-xl-4 col-md-6">
          <div class="icone d-flex justify-content-center">
            <img src="./img/icones/bagagens.svg" alt="Bagagens">
          </div>
          <h3>Bagagens</h3>
          <p>O Lorem Ipsum é um texto modelo da indústria tipográfica e de impressão. O Lorem Ipsum tem vindo a ser o texto padrão usado por estas indústrias desde o ano de 1500.</p>
        </div>
        <div class="col-xl-4 col-md-6">
          <div class="icone d-flex justify-content-center">
            <img src="./img/icones/turismo.svg" alt="Turismo">
          </div>
          <h3>Turismo</h3>
          <p>O Lorem Ipsum é um texto modelo da indústria tipográfica e de impressão. O Lorem Ipsum tem vindo a ser o texto padrão usado por estas indústrias desde o ano de 1500.</p>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
export default {
  data: () => ({
    slide: 0,
    sliding: null
  }),
  methods: {
    onSlideStart() {
      this.sliding = true
    },
    onSlideEnd() {
      this.sliding = false
    }
  }
}
</script>
<style scoped>
.box-shadow {
  box-shadow: 0 2px 4px 0 rgba(0, 0, 0, .05),
              0 2px 4px 0 rgba(0, 0, 0, .05);
}
.config-after-top {
  padding-top: 75px;
}
.icone {
  height: 100px;
}
</style>