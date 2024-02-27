<script>
import navBar from '../components/navBar.vue'
export default {
  components: {
    navBar
  },
  methods: {
    scrollToRef(refName) {
      this.$nextTick(() => {
        const el = this.$refs[refName];
        if (el) {
          el.scrollIntoView({ behavior: 'smooth' });
        } else {
          console.error('Element not found:', refName);
        }
      });
    },
    reveal() {
      var reveals = document.querySelectorAll('.reveal');
      for (var i = 0; i < reveals.length; i++) {
        var windowheight = window.innerHeight;
        var revealtop = reveals[i].getBoundingClientRect().top;
        var revealpoint = 150;
        if (revealtop < windowheight - revealpoint) {
          reveals[i].classList.add('active');
        } else {
          reveals[i].classList.remove('active');
        }
      }
    }
  },
  mounted() {

    window.addEventListener('scroll', this.reveal);
  },
  beforeDestroy() {

    window.removeEventListener('scroll', this.reveal);
  }
}







</script>


<template>
  <navBar @scroll-to-ref="scrollToRef"></navBar>
  <div class="container">





    <div ref="aboutMe">

      <div class="conteiner1">
        <img id="slikap" class="profilePicture" src='../assets/img/placeHolder.jpg'>
        <div class="profileText">
          <h1> Loris Solo</h1>
          <p style="color: rgb(59,132,154,255);"><b> 23 years
              <span style="color: rgb(96,97,99,255)">/</span> Lovran
              <span style="color: rgb(96,97,99,255);">/</span> bacc.ing.comp</b></p>
          <p>Bachelor's degree in Computer Science earned in September 2023.</p>
          <p>Currently seeking opportunities to expand my knowledge and gain valuable experience in the field.</p>
          <p>Motivated, responsible, and eager to embark on new learning journeys.</p>
          <a href="https://github.com/LorisSolo" style="padding-left: 50px;">https://github.com/LorisSolo</a>



        </div>
      </div>
    </div>

    <hr>

    <div ref="myProjects">

      <!--  
<div class="sectionContainer reveal">


        <a href="https://web-app-frontend.onrender.com/#/">
          <div id="image-container">
            <img id="image" class="project1" src="../assets/img/project_1.png" style="margin-bottom: 50px;">
          </div>
        </a>


        <p>My first project involved developing a dynamic web application facilitating users to upload and share their
          recipes seamlessly.
          The platform enabled users to explore a diverse array of recipes contributed by others, while also providing
          functionality to select ingredients and discover compatible dishes.
          Click on the image for further details.</p>




      </div>

  -->


      <h1 calss="reveal">My projects</h1>
<div class="project-conteiner">
  <div class="card reveal">
        <a href="https://web-app-frontend.onrender.com/#/">
          <img class="slika" id="image" src="../assets/img/project_1.png" alt="">
        </a>

        <h2>Food1e</h2>
        <p>My first project involved developing a dynamic web application facilitating users to upload and share their
          recipes seamlessly. The platform enabled users to explore a diverse array of recipes contributed by others,
          while also providing functionality to select ingredients and discover compatible dishes. Click on the image for
          further details.</p>

          <a href="https://github.com/LorisSolo/dwa-backend"><img class ="technology-icons" src="../assets/img/Node.js_logo.svg" alt=""></a>
          <a href ="https://github.com/LorisSolo/web-app.frontend"><img class ="technology-icons" src="../assets/img/Vue.js_Logo.svg" alt=""></a>

      </div>




      <div class="card reveal">
        <img class="slika" id="image" src="../assets/img/comingSoon.jpg" alt="">
        <h2>Coming soon</h2>
        <p>More projects coming soon</p>

      </div>

</div>
   




    </div>




    <hr ref="publications">
    <div ref=" reveal">
      <h1>Publications</h1>
      <h2 class="reveal">Elliptic Curve Cryptography in View of Quantum Computing</h2>
      <h3 class="reveal">Loris Solo, Neven Grbac, 2023, Elliptic Curve Cryptography in View of Quantum Computing, Zbornik
        studentskih
        radova, vol 2, page 313</h3>
      <div class="sectionContainer reveal">
        <a href="https://www.unipu.hr/zbornik-studentskih-radova/izdanja">
          <div id="image2-container">
            <img id="image2" class="project1" src='../assets/img/Publication.png'>
          </div>
        </a>
        <p>
          Summary: Elliptic curve cryptography is one of the most used methods today
          cryptography, which enables the security of most communications in the modern world
          information and communication technologies. It is based on complexity, for today
          classical computers, discrete logarithm problems in carefully selected groups
          elliptic curves. However, the accelerated development of quantum computers, which is expected in
          for years to come, calls into question the security of existing cryptography methods,
          given that it is already known how problems like discrete logarithm on quantum
          can be solved with computers in polynomial time. The aim of this paper is to explain how
          elliptic curve cryptography works today, see its shortcomings in the world
          of quantum computing and describe the methods by which these shortcomings can be eliminated.
          Key words: cryptography, elliptic curves, discrete logarithm problem,
          quantum computing, post-quantum cryptography
        </p>

      </div>
    </div>
    <hr ref="certificate">
    <h1>Certificate</h1>
    <div class="certificate reveal" style="display: flex;">
      <div class="image2-container">


        <img id="image2" class="certificate " src='../assets/img/certificate.png'>

      </div>
      <p>Certificate of Completion: 16-Hour Course on Programming in Python (D460)
        Enhanced proficiency in Python programming through comprehensive 16-hour course curriculum covering fundamental
        concepts and practical applications.
        Gained valuable insights and skills crucial for developing robust software solutions.</p>




    </div>
    <footer>
      <p>Work in progress!</p>

    </footer>



  </div>
</template>
  
<style>@import '../assets/Style.css';</style>