<template>
  <section class="mt-12 md:mt-32 services">
    <h1 class="capitalize text-3xl md:text-4xl font-bold leading-none">
      Habilidades e Experiência
    </h1>
    <p class="capitalize mt-2 text-lg">O que eu faço</p>
    <CustomBorder />
    <div
      class="grid grid-cols-1 lg:grid-cols-2 mt-10 rounded-lg bg-kjColorLight dark:bg-kjColorBlack border-2 border-kjColorLight"
    >
      <div class="p-5 md:mx-8 services__data">
        <h2 class="text-lg font-black uppercase mb-3 data-2">
          Suporte Técnico e Infraestrutura
        </h2>
        <p class="mb-5 data-2">
          Experiência em manutenção de computadores, notebooks e periféricos,
          infraestrutura de redes, suporte ao usuário, administração de
          ambientes corporativos com Active Directory, Office 365 e Windows
          Azure.
        </p>

        <h2 class="text-lg font-black uppercase mb-3 data-1">
          Administração de Sistemas
        </h2>
        <p class="mb-5 data-1">
          Gerenciamento e administração de usuários e políticas no Active
          Directory, configuração e suporte a VPN, administração de PABX
          Virtual, gestão e suporte ao Office 365, manutenção de bancos de
          dados Microsoft SQL Server e monitoramento de ativos com Zabbix.
        </p>

        <h2 class="text-lg font-black uppercase mb-3 data-3">
          Desenvolvimento de Software
        </h2>
        <p class="data-3">
          Estudo e desenvolvimento em lógica de programação, Programação
          Orientada a Objetos (POO), Java, Python, HTML/CSS/JavaScript,
          SpringBoot, com foco em boas práticas de desenvolvimento e
          resolução de problemas.
        </p>

        <div class="mt-8 see-project-btn">
          <Button displayTitle="MEU PORTFÓLIO" linkTo="/portfolio" />
        </div>
      </div>
      <div class="hidden lg:block illustration">
        <img
          class="illustration__img illustration__img--1"
          src="../../assets/images/Illustrations/illustration-01.png"
          alt="illustration 1"
        />
        <img
          class="illustration__img illustration__img--2"
          src="../../assets/images/Illustrations/illustration-02.png"
          alt="illustration 2"
        />
        <img
          class="illustration__img illustration__img--3"
          src="../../assets/images/Illustrations/illustration-03.png"
          alt="illustration 3"
        />
        <img
          class="illustration__img illustration__img--4"
          src="../../assets/images/Illustrations/illustration-04.png"
          alt="illustration 4"
        />
        <img
          class="illustration__img illustration__img--5"
          src="../../assets/images/Illustrations/illustration-05.png"
          alt="illustration 5"
        />
        <img
          class="illustration__img illustration__img--6"
          src="../../assets/images/Illustrations/illustration-06.png"
          alt="illustration 6"
        />
        <img
          class="illustration__img illustration__img--7"
          src="../../assets/images/Illustrations/illustration-07.png"
          alt="illustration 7"
        />
      </div>
    </div>
  </section>
</template>

<script>
import { gsap, Back, Elastic, Expo } from 'gsap';

export default {
  name: 'Services',
  data() {
    return {
      services: [
        {
          title: 'Desenvolvimento Web',
          des: 'Crio websites e aplicações web.'
        },
        {
          title: 'Suporte Técnico',
          des: 'Suporte e manutenção de infraestrutura de TI.'
        },
        {
          title: 'Administração de Sistemas',
          des: 'Gerenciamento de Active Directory, Office 365 e redes.'
        }
      ]
    };
  },
  mounted() {
    this.animateServices();
  },
  methods: {
    animateServices() {
      const { services } = this.$refs;
      let tl = new TimelineMax({ onUpdate: updatePercentage });

      tl.from('.illustration__img--1', 0.5, { scale: 0.5 }, 0)
        .from('.illustration__img--2', 0.5, { opacity: 0, y: -50 }, 0.2)
        .from('.illustration__img--3', 0.5, { opacity: 0, y: -50 }, 0.5)
        .from('.data-1', 1, { opacity: 0, stagger: 1 }, 0.7)
        .from('.illustration__img--5', 0.5, { opacity: 0, x: 100 }, 1.4)
        .from('.illustration__img--6', 0.5, { opacity: 0, x: -100 }, 1.7)
        .from('.data-2', 1, { opacity: 0, stagger: 1 }, 1.9)
        .from('.illustration__img--4', 0.5, { opacity: 0, x: -100 }, 2.6)
        .from('.illustration__img--7', 0.5, { opacity: 0, x: 100 }, 2.9)
        .from('.data-3', 1, { opacity: 0, stagger: 1 }, 3.1)
        .to('.see-project-btn', 1, { opacity: 1 }, 3.5);

      const scene = this.$scrollmagic
        .scene({
          triggerElement: '.services',
          triggerHook: 0,
          duration: '300%'
        })
        .setPin('.services')
        .setTween(tl);

      this.$scrollmagic.addScene(scene);

      function updatePercentage() {
        tl.progress();
      }
    }
  }
};
</script>

<style lang="scss" scoped>
.illustration {
  position: relative;
  height: 30rem;

  &__img {
    position: absolute;
    bottom: 0;
    width: 80%;

    &--1 {
      left: 0;
      z-index: 2;
    }

    &--2 {
      top: 25%;
      z-index: 1;
    }

    &--3 {
      top: -2%;
    }

    &--4 {
      top: -20%;
      left: -20%;
    }

    &--5 {
      top: -20%;
      right: -5%;
    }

    &--7 {
      top: -2%;
      right: -2%;
    }

    &--6 {
      top: 0;
      left: -22%;
    }
  }
}

.services {
  &__data {
    text-align: center;
  }
}

.see-project-btn {
  opacity: 0;
}
</style>
