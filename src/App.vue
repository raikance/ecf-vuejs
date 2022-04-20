<template>
<div id="app">
<!-- composant non dépendant de la nav -->
  <MagicNav />

<!-- contenu principal qui va changé en fct de la nav -->
  <!-- <router-view /> -->

<!-- composant non dépendant de la nav -->
  <MagicFooter />

</div>
</template>

<script>
import MagicNav    from '@/components/MagicNav'
import MagicFooter from '@/components/MagicFooter'

export default {
  name: 'App',
  props: {  },
  components:{
    MagicNav,
    MagicFooter
  }
}
</script>

