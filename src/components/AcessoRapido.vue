<template>
  <aside class="acesso_rapido">
    <div class="card">
      <div class="card-header">
        <span style="font-size: 13pt">Acesso Rápido</span>
      </div>
      <ul>
        <li v-for="(item, index) in acessosRapidos" :key="index">
          <router-link :to="item.link" v-if="item.link !== '#'">
            <img
              :src="item.image"
              :alt="item.alt"
              :width="item.width"
              :height="item.height"
              lazy="loading"
            />
            <span>{{ item.text }}</span>
          </router-link>
          <a :href="item.link" v-else>
            <img
              :src="item.image"
              :alt="item.alt"
              :width="item.width"
              :height="item.height"
              lazy="loading"
            />
            <span>{{ item.text }}</span>
          </a>
        </li>
      </ul>
    </div>
  </aside>
</template>

<script>
export default {
  name: "AcessoRapido",
  data() {
    return {
      acessosRapidos: [
        {
          link: "/instituicao/fardamentos",
          image: "https://api.fabhabbo.com/public/images/icons/uniform.png",
          text: "Fardamentos",
          alt: "Ícone que representa - Fardamentos",
        },
        {
          link: "/apostilas/peles-e-cabelos",
          image: "https://api.fabhabbo.com/public/images/icons/peles.png",
          text: "Peles e cabelos",
          alt: "Ícone que representa - Peles e cabelos",
        },
        {
          link: "#",
          image:
            "https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjv8bd1tiv_f6KCyEtq5QEB4GWM1rsPIjlY9RboA-miz22V4uM5WUM6J9QDO7sq2-0z_qZ2FH3Gqbq1bJDKV8yp8zTthPMRW1pR3fY2OkpfnrT_IYYiSyid77fxlvi2agiPhkIXmhqLGJXB/s1600/FR09A.gif",
          text: "Hierarquia Militar",
          alt: "Ícone que representa - Hierarquia Militar",
        },
        {
          link: "#",
          image:
            "https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiQrhMlmV231lS074OnvP4LiAgJgzbbO4GfGnmXmTBP9T8Z_3vF66WFeGIsgaiodg1FtNww326LaKNtGBp3icih82IHt5rjiw8PqKwmAKtPta9YyvLH6GEn9tntQNHD_dcrqlO0SJh5y7I/s1600/ARM28.gif",
          text: "Academias",
          alt: "Ícone que representa - Academias",
        },
      ],
    };
  },
};
</script>
