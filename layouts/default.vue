<template>
  <div>
    <b-navbar centered class="centralizarrr margem " >
        <!-- <template #brand>
        </template> -->
        <template #start >
            <b-navbar-item href="#">
                Home
            </b-navbar-item>
            <hr >
            <b-navbar-item href="#" class="linhaVertical">
                Blog
            </b-navbar-item>
            <b-navbar-item href="#" class="linhaVertical ">
                Suporte
            </b-navbar-item>
            <b-navbar-item href="#" class="linhaVertical">
                Contatos
            </b-navbar-item>
            <!-- <b-navbar-dropdown label="Info">
                <b-navbar-item href="#">
                    Suporte
                </b-navbar-item>
                <b-navbar-item href="#">
                    Contatos
                </b-navbar-item>
            </b-navbar-dropdown> -->
        </template>

        <template #end>
            <b-navbar-item tag="div" >
                <div class="buttons">
                    <a class="button botaoLogin">
                        <strong>Login</strong>
                    </a>
                    
                </div>
            </b-navbar-item>
        </template>
    </b-navbar>

    <section class="main-content columns" >
      <aside class="column is-2 section" style="display: none">
        <p class="menu-label is-hidden-touch">
          General
        </p>
        <ul class="menu-list">
          <li
            v-for="(item, key) of items"
            :key="key"
          >
            <NuxtLink
              :to="item.to"
              exact-active-class="is-active"
            >
              <b-icon :icon="item.icon" /> {{ item.title }}
            </NuxtLink>
          </li>
        </ul>
      </aside>

      <div class="container column is-10">
        <Nuxt />
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' }
        },
        {
          title: 'Inspire',
          icon: 'lightbulb',
          to: { name: 'inspire' }
        }
      ]
    }
  }
}
</script>

<style scoped>
  .centralizarrr{
    padding: 0% 8% 0% 12% ;
  }
  .linhaVertical{
    border-left: 2px solid #000 ;
    margin-top: 20px;
    margin-bottom: 7px;
    height: 5px;
  }
  .botaoLogin{
    background-color: #90EE90;
    color: #ffff
    ;
  }
  
  
</style>