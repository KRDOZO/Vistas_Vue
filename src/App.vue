<template>
  <head>
    <title>Clinica TuEsperanza</title>
  </head>
  <body>
    <header>
      <h1>Bienvenido a la Clinica Tu Esperanza</h1>
    </header>
    <nav>
      <a v-on:click="loadLogIn">Ingresar</a>
      <a href="signUp" v-on:click="loadSignUp" id="singUp">Registrarse</a>
      <a href="services">Servicios</a>
      <a href="contact">Contacto</a>
      <a href="us">Nosotros</a>
    </nav>
    <div class="main-component"></div>
    <div class="banner"></div>
    <div class="news-container">
      <section class="news">
        <h2>Nuestra historia</h2>
        <p>La Clinica Tu Esperanza nace en un momento en que los servicios medicos de Colombia colapsaron, causando una necesidad de un portal capaz de soportar la cantidad de usuarios.</p>
      </section>

      <section class="news">
        <h2>Premio a la Clinica más Sofisticada del Mundo</h2>
        <article>
          <p>En el año 2021 la Clinica Tu Esperanza se hace acreedora del premio a la Clinica más sofisticada del mundo entregado por la OMS.</p>
        </article>
      </section>

      <section class="news">
        <h2>¿Buscas trabajo?</h2>
        <article>
          <p>Envianos tu hoja de vida al correo: cliniesperanza@gmail.com</p>
        </article>
      </section>

      <section class="news">
        <h2>Hábitos de Vida Saludables</h2>
        <article>
          <p>Conoce los hábitos saludables que deben adquirir para cuidar de tu salud y la de tu familia.</p>
        </article>
      </section>

      <section class="news">
        <h2>¿La pandemía esta llegando a su fin?</h2>
        <article>
          <p>Lee el artículo completo de nuestro doctor Paticas donde aborda el tema del COVID-19 y su repercusión a corto y largo plazo.</p>
        </article>
      </section>

      <section class="news">
        <h2>Reconocimientos</h2>
        <article>
          <p> Medicos de la Clinica TuEsperanza participan en una misión de rescate </p>
        </article>
      </section>
    </div>
    <footer>
      <section class="foot">
        <a href="#">Contactar desarrolladores</a>
        <a href="#">Ubicación</a>
        <a href="#">Soporte</a>
      </section>
    </footer>
  </body>
</template>

<script>
export default {
  methods: {
    loadLogIn: function () {
      this.$router.push({ name: "logIn" });
    },
    loadSignUp: function () {
      this.$router.push({ name: "signUp" });
    },
  },
};
</script>


<style>
body {
  margin: 0;
  padding: 0;
  background-color: whitesmoke;
}

header {
  color: whitesmoke;
  text-align: center;
  font-size: 20px;
  border: 0.5px solid #78c6a3;
  background: linear-gradient(#78c6a3, #14746f);
}

header h1 {
  text-shadow: 2px 2px 2px #073b4c;
}

nav {
  width: 20%;
  float: left;
}

nav a {
  background: linear-gradient(#78c6a3, #14746f);
  border-radius: 10px 0px 10px 0px;
  color: whitesmoke;
  margin: 10px;
  padding: 10px;
  display: block;
  text-align: center;
  letter-spacing: 5px;
  font-size: 20px;
  text-decoration: none;
}

nav a:hover {
  box-shadow: 0px 3px 0px 0px rgb(129, 117, 117);
}

.banner {
  background-color: rgba(245, 245, 245, 0.4);
  float: right;
  border-radius: 20px 0px 20px 0px;
  width: 75%;
  height: 220px;
  border: 1px solid #78c6a3;
  box-shadow: 1px 0 4px rgb(0, 0, 0, 0.2);
  margin-bottom: 15px;
  margin-top: 10px;
  margin-right: 10px;
  padding: 15px;
  cursor: pointer;
  animation: banner 6s infinite;
  animation-direction: alternate;
  background-size: 100% 100%;
}

@keyframes banner {
  0%,
  30% {
    background-image: url(./bannerImages/ClinicaTuEsperanza.png);
    opacity: 1;
  }

  30%,
  34% {
    opacity: 0.1;
  }

  35%,
  65% {
    background-image: url(./bannerImages/Publicidad.png);
    opacity: 1;
  }

  66%,
  69% {
    opacity: 0.1;
  }

  70%,
  100% {
    background-image: url(./bannerImages/Recomendaciones.png);
  }
}

.news-container {
  width: 100%;
  background-color: transparent;
  z-index: -1;
}

.news {
  float: left;
  background: linear-gradient(white, whitesmoke);
  border-radius: 20px 0px 20px 0px;
  width: 45%;
  height: 100px;
  border: 1px solid #78c6a3;
  box-shadow: 1px 0 4px rgb(0, 0, 0, 0.2);
  margin-bottom: 15px;
  margin-top: 10px;
  margin-right: 10px;
  margin-left: 20px;
  padding: 15px;
  cursor: pointer;
}

section h2 {
  margin-top: 2px;
  color: black;
  text-shadow: 2px 2px 2px #e5e5e5;
  font-style: italic;
}

aside {
  float: right;
  width: 30%;
  padding: 10px;
  margin: -30px;
  font-style: italic;
  color: black;
  box-shadow: inset 5px 0 5px -5px #0d0d0e;
}

footer {
  clear: both;
  background: linear-gradient(#78c6a3, #14746f);
  height: 50px;
  padding: 1px;
  text-align: center;
  border: 0.4px solid rgba(7, 59, 76, 0.2);
}

.foot {
  float: left;
  width: 100%;
  margin: 15px;
}

.foot a {
  margin: 10px;
  padding: 10px;
  color: whitesmoke;
  text-decoration: none;
  text-decoration: none;
}

.foot a:hover {
  text-decoration: overline;
}
</style>
