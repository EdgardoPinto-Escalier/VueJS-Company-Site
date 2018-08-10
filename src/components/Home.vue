<template>
  <div class="home">
    <section class="hero is-light">
      <div class="hero-body">
        <div class="container">
          <h1 class="title home">{{ heading }}</h1>
          <div class="is-two-thirds column is-paddingless">
              <h2 class="subtitle is-4">{{ subheading }}</h2>
          </div>
          <a class="button is-large isprimary" id="btnHero">LEARN MORE</a>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="container">
        <div class="columns padd is-desktop">
          <div class="column is-1 has-text-centered">
            <i class="fas fa-cog is-primary"></i>
          </div>
          <div class="column is-one-third-desktop">
            <p class="title"><strong>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut pretium pharetra dolor. Praesent sed sollicitudin.</strong></p>
          </div>
          <div class="column">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras nibh metus, lacinia quis fringilla at, maximus vel metus. Mauris ullamcorper elit ullamcorper, cursus leo gravida.</p>
          </div>
        </div>
      

      <div class="columns padd">
        <div class="columm">
          <div class="card">
            <div class="card-content">
              <p class="title">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum hendrerit bibendum nulla et imperdiet. Maecenas ullamcorper.</p>
              <p class="subtitle">-The Company Team</p>
            </div>
          </div>  
        </div> 

        <div class="columm">
          <div class="card">
            <div class="card-content">
              <p class="title">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum hendrerit bibendum nulla et imperdiet. Maecenas ullamcorper.</p>
              <p class="subtitle">-The Company Team</p>
            </div>
          </div>  
        </div>

        <div class="columm">
          <div class="card">
            <div class="card-content">
              <p class="title">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum hendrerit bibendum nulla et imperdiet. Maecenas ullamcorper.</p>
              <p class="subtitle">-The Company Team</p>
            </div>
          </div>  
        </div> 

      </div>
    </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      heading: 'Welcome to our company site',
      subheading: 'Non reprehenderit pariatur culpa reprehenderit consequat cillum occaecat voluptate ex. Eu ipsum voluptate sint fugiat voluptate. In occaecat laborum ullamco.'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
@import '../mq'

.title.home
  +mobile
    font-weight: bold
  +tablet
    font-size: 2.5rem
  +desktop
    font-size: 4rem
    margin-top: 3rem

h2  
  margin: 1.5rem 0 2rem 0 !important

.fa-cog
  font-size: 4rem

#btnHero
  +desktop
    margin-bottom: 4rem

.padd
  +tablet
    padding: 3em 0 5rem

section
  +desktop
    margin-bottom: 3rem

.card
  margin-left: 25px   
  margin-right: 25px 

.card-content p.subtitle
  +desktop
    margin-top: 10px

</style>
