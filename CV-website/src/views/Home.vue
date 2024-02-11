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
          <p style="color: rgb(59,132,154,255);"><b> 23 yeares
              <span style="color: rgb(96,97,99,255)">/</span> Lovran
              <span style="color: rgb(96,97,99,255);">/</span> bacc.ing.comp</b></p>
          <p>Bachelor's degree in computer science from September 15, 2023.</p>
          <p>looking for a job that offers new knowledge and experience.</p>
          <p>Motivated to work, responsible and ready to learn.</p>



        </div>
      </div>
    </div>

    <hr>
    <div ref="myProjects">
      <h1 calss="reveal">My projects</h1>
      <div class="firstProjectContainer reveal">


        <a href="https://web-app-frontend.onrender.com/#/">
          <div id="image-container">
            <img id="image" class="project1" src="../assets/img/project_1.png">
          </div>

        </a>

        <p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit nam ipsam commodi culpa tempore dolores cupiditate beatae repellendus animi, quidem accusamus perferendis tempora voluptatibus minus modi ipsum dolor dolorem officiis!
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ea totam voluptates magni tenetur! Quis similique tempore architecto rem molestiae doloremque nam nesciunt, sed, reiciendis blanditiis, omnis impedit? Atque, similique officia?
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta, reiciendis odio odit ipsam repellendus et quaerat, nemo suscipit delectus, fugiat quasi nostrum nam harum. Commodi, eveniet! Omnis facere expedita voluptates?
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa fugiat quo illo est, deserunt voluptates eius reiciendis facilis alias debitis accusamus? Tempora, corporis saepe! Eos reprehenderit voluptas illum officiis exercitationem?
        </p>

      </div>
    </div>

    <hr ref="publications">
    <div ref=" reveal">
      <h1>Publications</h1>
      <h2 class="reveal">Elliptic Curve Cryptography in View of Quantum Computing</h2>
      <h3 class="reveal">Loris Solo, Neven Grbac, 2023, Elliptic Curve Cryptography in View of Quantum Computing, Zbornik
        studentskih
        radova, vol 2, page 313</h3>
      <div class="firstProjectContainer reveal">
        <a href="https://www.unipu.hr/zbornik-studentskih-radova/izdanja">
          <div id="image-container">
            <img id="image" class="project1" src='../assets/img/Publication.png'>
          </div>
        </a>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit dolore rem facilis. Reprehenderit facilis dignissimos alias corrupti neque iste repudiandae vitae. Vitae officia aperiam recusandae velit ad maiores nam blanditiis?
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis et aut id ad! Harum nostrum, corporis maiores eius laudantium inventore non dignissimos rem doloremque, cupiditate voluptatem velit blanditiis tempore doloribus?
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste alias laboriosam dicta eum voluptates similique fugiat suscipit, commodi nemo officiis? Repellendus quasi asperiores commodi cupiditate temporibus ullam vel nam repudiandae!
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente ratione reiciendis doloribus, labore explicabo dolor molestiae autem exercitationem amet tempore sit voluptatum neque, cupiditate placeat ipsam in officiis vero veritatis.
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores, tempore! Modi quos officiis incidunt non maxime sapiente eum temporibus veniam labore, perspiciatis deserunt quasi minima amet iure, repellat doloribus possimus.
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo est ut, culpa enim hic repudiandae maiores aliquid asperiores, vitae eveniet soluta dolores voluptas rem dolor earum illum consequatur fugit ducimus!
          
        </p>
      </div>
    </div>
    <hr ref="certificate">
    <div class="reveal">
      <h1>Certificate</h1>

      <img id="image" class="certificate " src='../assets/img/certificate.png'>
    </div>





  </div>
</template>
  
<style>
@import '../assets/Style.css';
</style>