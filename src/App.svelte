<script lang="ts">
  import Button from './lib/Button.svelte';
  import Footer from './lib/Footer.svelte';
</script>



<main>
  <div class="Section-header">

    <h1 class="Header-main Effect-rainbow-text">ePortfolio</h1>
    <div class="Effect-rainbow-bg Bottom"></div>

  </div>
  

  <section class="Section-description">
    <p class="Text-italic">
      This is my E-Portfolio. It includes achievements, development, and accomplishments.
    </p>
  </section>


  <section>
    <h1 class="Effect-rainbow-text">Achievments</h1>
    <p>
      In Term 2, I was able to score a respectable 35 out of 40 in my science test - which just so happened to be the highest mark in the class :)
    </p>
    <p>
      In the topic of exam marks, I also achieved a 28.5 out of 30 in my ICT assessment in the second term.
    </p>
    <p>
      In the topic of academic achievements, I also achieved an <i>astonishing</i> 83 house points.
    </p>
  </section>


  <section>
    <h1 class="Effect-rainbow-text">Developments</h1>
    <p>
      I got a certificate for Digital Learning in term 2.
    </p>
  </section>


  <section>
    <h1 class="Effect-rainbow-text">Accomplishments</h1>
    <p>
      My only accomplishments so far are just making a few websites. That's it.
    </p>
    <p>
      Hey, Look at this cool button
    </p>
    <div class="Bottom"></div> <!-- A little space -->

    <Button buttonText = "Hello!" />
  </section>


  <section>
    <h1 class="Effect-rainbow-text">Conclusion</h1>
    <p>
      To conclude, This was my E - Portfolio. Thanks for reading!
    </p>
  </section>

  <Footer />

</main>





<style>
  .Header-main {
    font-size: 120px; font-weight: 1000;
    padding-top: 2px;
    margin: 0 0 20px 0;
  }

  .Section-header {
    background-color: #242424;
    position: sticky;
    top: 0;
    margin-bottom: 10%;
    z-index: 1;
  }

  section {
    font-size: 140%;
    margin-bottom: 400px;
  }

  .Section-description {
    margin-bottom: 30%;
  }

  .Text-italic {
    font-style: italic;
  }


  @media (prefers-color-scheme: light) {
    :root {
      color: #213547;
      background-color: #ffffff;
    }

    .Section-header {
      background-color: #ffffff;
    }
  }

  .Effect-rainbow-bg {
    animation: effect-rainbow-bg 10s linear infinite;

    width: 100%; height: 5px;

    background-image: linear-gradient(to right, rgb(255, 80, 80), rgb(243, 166, 24),
     rgb(255, 255, 93), rgb(106, 255, 106), rgb(93, 93, 255), rgb(179, 74, 255),
      violet, rgb(255, 80, 80));

    color: transparent;

    background-size: 200% 100%;

  }
</style>



