<template>
  <nav class="navbar navbar-expand-lg navbar-bytebank">
    <a class="navbar-brand" href="#">ByteBank</a>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarSupportedContent"
      aria-controls="navbarSupportedContent"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <NavBarLogada v-if="usuarioEstaLogado"/>
      <NavBarDeslogada v-else/>
    </div>
  </nav>
</template>

<script>
import { mapGetters } from 'vuex'
import NavBarLogada from './NavBarLogada.vue'
import NavBarDeslogada from './NavBarDeslogada.vue'

export default {
  computed: {
    ...mapGetters(['usuarioEstaLogado'])
  },
  components: {
    NavBarLogada,
    NavBarDeslogada,
  }
};
</script>
