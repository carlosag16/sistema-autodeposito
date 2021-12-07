<template >
  <section class="section corfundo is-large ">
    <div class="columns is-mobile  ">
      <h1 class="subtitle textoCentralizado">
        Deposite seu trabalho acadêmico para que seja<p style="margin-left: 40px"> publicado através do autodepósito.</p>
      </h1>
    </div>
    <div class="card-image has-text-centered">
      <figure class="image is-128x128 is-inline-block">
        <img src="..\assets\logoSmFundo.png">
      </figure>
    </div>
  </section>
</template>

<script>
import Card from '~/components/Card'

export default {
  name: 'HomePage',

  components: {
    Card
  }
}
</script>

<style  scoped>
    .textoCentralizado{
    margin-left: auto;
    margin-right: auto;
  }
  .corfundo{
    height: 100%;
    width: 100%;
    background-image: url('../assets/fundoCadastro.jpeg');
  }

</style>