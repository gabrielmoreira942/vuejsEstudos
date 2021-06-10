<template>
  <div id="app">
    OLÁ KKKKKK
    <div class="container grid-xs py-2">
      OLÁ KKKKKK
      <img
        class="img-responsive img-totoro"
        src="@/assets/totoro.jpg"
        alt="Filtro com totoro"
      />
      <form @submit.prevent="recebePesquisa(pesquisa)">
        <div class="input-group">
          <input
            type="text"
            v-model="pesquisa.teste"
            class="form-input"
            placeholder="Spirited Away..."
          />
          <button class="btn btn-primary input-group-btn">
            Pesquisar filme
          </button>
        </div>
        {{ pesquisas }}
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
  return { 
    pesquisas: [], 
    pesquisa: {checked: false} 
    
    };
  },
  methods: {
    recebePesquisa(pesquisa) {
      pesquisa.id = Date.now()
      this.pesquisas.push(pesquisa)
    },
  },
};
</script>

<style scoped>
.img-totoro {
  max-width: 200px;
  margin: 0 auto;
}
</style>
