<template>
  <div class="item">
    <div class="card">
      <div class="card-header">
        <span>Fardamentos da Força Aérea Brasileira</span>
        <img
          src="https://api.fabhabbo.com/public/images/icons/uniform.png"
          alt="Icone do uniforme"
          width="40"
          height="52"
          lazy="loading"
        />
      </div>
      <div class="card-body">
        <div class="row">
          <div
            class="col-md-6 farda"
            v-for="(farda, index) in fardamentos.slice(0, 5)"
            :key="index"
          >
            <span>{{ farda.nome }}</span>
            <img
              :src="farda.image"
              alt="Imagem do fardamento"
              width="185"
              height="168"
              lazy="loading"
            />
          </div>
          <div
            class="col-md-6 farda"
            v-for="(farda, index) in fardamentos.slice(5, 10)"
            :key="index"
          >
            <span>{{ farda.nome }}</span>
            <img
              :src="farda.image"
              alt="Imagem do fardamento"
              width="185"
              height="168"
              lazy="loading"
            />
          </div>
        </div>
      </div>
      <div
        style="
          background-color: var(--bg-color-blue-Ofcourse);
          padding: 10px 0;
          margin-bottom: 1rem;
        "
      >
        <span style="text-align: center; display: block">Luto</span>
      </div>
      <div class="card-body">
        <div class="row">
          <div
            class="col-md-6 farda"
            v-for="(farda, index) in fardamentosLuto"
            :key="index"
          >
            <span>{{ farda.nome }}</span>
            <img
              :src="farda.image"
              alt="Imagem do fardamento"
              width="185"
              height="168"
              lazy="loading"
            />
          </div>
        </div>
      </div>
      <div
        style="
          background-color: var(--bg-color-blue-Ofcourse);
          padding: 10px 0;
          margin-bottom: 1rem;
        "
      >
        <span style="text-align: center; display: block">Ministros</span>
      </div>
      <div class="card-body">
        <div class="row">
          <div
            class="col-md-6 farda"
            v-for="(farda, index) in fardamentosMinistros"
            :key="index"
          >
            <span>{{ farda.nome }}</span>
            <img
              :src="farda.image"
              alt="Imagem do fardamento"
              width="185"
              height="168"
              lazy="loading"
            />
          </div>
        </div>
      </div>
      <div
        style="
          background-color: var(--bg-color-blue-Ofcourse);
          padding: 10px 0;
          margin-bottom: 1rem;
        "
      >
        <span style="text-align: center; display: block">Patrocinadores</span>
      </div>
      <div class="card-body">
        <div class="row">
          <div
            class="col-md-6 farda"
            v-for="(farda, index) in fardamentosPatrocinadores"
            :key="index"
          >
            <span>{{ farda.nome }}</span>
            <img
              :src="farda.image"
              alt="Imagem do fardamento"
              width="185"
              height="168"
              lazy="loading"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Fardamentos",
  data() {
    return {
      fardamentos: [
        {
          nome: "Recruta",
          image: "https://api.fabhabbo.com/public/images/uniforms/recruta.png",
        },
        {
          nome: "Soldado a SubOficial",
          image: "https://api.fabhabbo.com/public/images/uniforms/praca.png",
        },
        {
          nome: "EEAR Aluno",
          image: "https://api.fabhabbo.com/public/images/uniforms/eear.png",
        },
        {
          nome: "EPCAR Aluno",
          image: "https://api.fabhabbo.com/public/images/uniforms/epcar.png",
        },
        {
          nome: "AFA Cadete",
          image: "https://api.fabhabbo.com/public/images/uniforms/afa.png",
        },
        {
          nome: "Aspirante-a-Oficial",
          image: "https://api.fabhabbo.com/public/images/uniforms/aspirante.png",
        },
        {
          nome: "Oficial",
          image: "https://api.fabhabbo.com/public/images/uniforms/oficial.png",
        },
        {
          nome: "Alto Comando",
          image: "https://api.fabhabbo.com/public/images/uniforms/alto_comando.png",
        },
        {
          nome: "Aposentados",
          image: "https://api.fabhabbo.com/public/images/uniforms/oficial.png",
        },
        {
          nome: "Ex-Comandantes",
          image: "https://api.fabhabbo.com/public/images/uniforms/ministros.png",
        },
      ],
      fardamentosLuto: [
        {
          nome: "Luto Praça",
          image: "https://api.fabhabbo.com/public/images/uniforms/luto_praca.png",
        },
        {
          nome: "Luto Oficial",
          image: "https://api.fabhabbo.com/public/images/uniforms/luto_oficial.png",
        },
      ],
      fardamentosMinistros: [
        {
          nome: "Normal",
          image: "https://api.fabhabbo.com/public/images/uniforms/ministros.png",
        },
        {
          nome: "Opcional",
          image: "https://api.fabhabbo.com/public/images/uniforms/ministrosOptional.png",
        },
      ],
      fardamentosPatrocinadores: [
        {
          nome: "Praças",
          image: "https://api.fabhabbo.com/public/images/uniforms/patrocinadores.png",
        },
        {
          nome: "Opcional",
          image:
            "https://api.fabhabbo.com/public/images/uniforms/patrocinadoresOptional.png",
        },
      ],
    };
  },
};
</script>
<style scoped>
.item .farda {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.item .farda span {
  background-color: var(--bg-color-blue-Ofcourse);
  text-align: center;
  border-radius: 5px;
  width: 170px;
  margin-bottom: 10px;
  font-size: 11pt;
}
</style>
