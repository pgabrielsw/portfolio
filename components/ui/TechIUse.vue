<template>
  <div>
    <!-- LINGUAGENS DE PROGRAMAÇÃO -->
    <div
      class="mb-8 p-3 md:px-10 md:py-5 bg-kjColorLight dark:bg-kjColorBlack border-2 border-kjColorLight"
    >
      <h2 class="text-gray mb-10">
        <i>Linguagens de Programação</i>
      </h2>
      <div class="flex flex-wrap">
        <div
          v-for="lang in languages"
          :key="lang.name"
          class="w-16 inline-block mb-4 brand"
        >
          <span :title="lang.name">
            <a :href="lang.website" target="_blank">
              <img
                :src="lang.url"
                :alt="lang.name"
                class="h-12 inline brand__img"
              />
            </a>
          </span>
          <p class="text-xs mt-1 text-center">{{ lang.name }}</p>
        </div>
      </div>
    </div>

    <!-- FRAMEWORKS E BANCOS DE DADOS -->
    <div
      class="mb-8 p-3 md:px-10 md:py-5 bg-kjColorLight dark:bg-kjColorBlack border-2 border-kjColorLight"
    >
      <h2 class="text-gray mb-10">
        <i>Frameworks e Bancos de Dados</i>
      </h2>
      <div class="flex flex-wrap">
        <div
          v-for="tool in frameworks"
          :key="tool.name"
          class="w-16 inline-block mb-4 brand"
        >
          <span :title="tool.name">
            <a :href="tool.website" target="_blank">
              <img
                :src="tool.url"
                :alt="tool.name"
                class="h-12 inline brand__img"
              />
            </a>
          </span>
          <p class="text-xs mt-1 text-center">{{ tool.name }}</p>
        </div>
      </div>
    </div>

    <!-- SISTEMAS OPERACIONAIS -->
    <div
      class="mb-8 p-3 md:px-10 md:py-5 bg-kjColorLight dark:bg-kjColorBlack border-2 border-kjColorLight"
    >
      <h2 class="text-gray mb-10">
        <i>Sistemas Operacionais</i>
      </h2>
      <div class="flex flex-wrap">
        <div
          v-for="os in operatingSystems"
          :key="os.name"
          class="w-16 inline-block mb-4 brand"
        >
          <span :title="os.name">
            <a :href="os.website" target="_blank">
              <img
                :src="os.url"
                :alt="os.name"
                class="h-12 inline brand__img"
              />
            </a>
          </span>
          <p class="text-xs mt-1 text-center">{{ os.name }}</p>
        </div>
      </div>
    </div>

    <!-- INFRAESTRUTURA E DEVOPS -->
    <div
      class="mb-8 p-3 md:px-10 md:py-5 bg-kjColorLight dark:bg-kjColorBlack border-2 border-kjColorLight"
    >
      <h2 class="text-gray mb-10">
        <i>Infraestrutura e DevOps</i>
      </h2>
      <div class="flex flex-wrap">
        <div
          v-for="infra in infrastructure"
          :key="infra.name"
          class="w-16 inline-block mb-4 brand"
        >
          <span :title="infra.name">
            <a :href="infra.website" target="_blank">
              <img
                :src="infra.url"
                :alt="infra.name"
                class="h-12 inline brand__img"
              />
            </a>
          </span>
          <p class="text-xs mt-1 text-center">{{ infra.name }}</p>
        </div>
      </div>
    </div>

    <!-- GESTÃO E MONITORAMENTO -->
    <div
      class="mb-8 p-3 md:px-10 md:py-5 bg-kjColorLight dark:bg-kjColorBlack border-2 border-kjColorLight"
    >
      <h2 class="text-gray mb-10">
        <i>Gestão, Monitoramento e Segurança</i>
      </h2>
      <div class="flex flex-wrap">
        <div
          v-for="tool in management"
          :key="tool.name"
          class="w-16 inline-block mb-4 brand"
        >
          <span :title="tool.name">
            <a :href="tool.website" target="_blank">
              <img
                :src="tool.url"
                :alt="tool.name"
                class="h-12 inline brand__img"
              />
            </a>
          </span>
          <p class="text-xs mt-1 text-center">{{ tool.name }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import {
  html,
  css,
  javascript,
  java,
  python,
  springboot,
  vuejs,
  sqlserver,
  mysql,
  mongodb,
  git,
  github,
  docker,
  kubernetes,
  postman,
  linux,
  windows,
  macos,
  azure,
  vmware,
  activeDirectory,
  office365,
  zabbix,
  totvs,
  vpn,
  pabx,
  cftv
} from '~/docs/brands.js';

export default {
  name: 'TechIUse',
  data() {
    return {
      languages: [html, css, javascript, java, python],
      frameworks: [springboot, vuejs, sqlserver, mysql, mongodb],
      operatingSystems: [linux, windows, macos],
      infrastructure: [git, github, docker, kubernetes, azure, vmware, postman],
      management: [activeDirectory, office365, zabbix, totvs, vpn, pabx, cftv]
    };
  }
};
</script>

<style lang="scss" scoped>
.brand {
  text-align: center;

  &:not(:last-child) {
    margin-right: 25px;
  }

  &__img {
    filter: grayscale(100%);
    transition: all 0.2s;
    object-fit: contain;

    &:hover {
      transform: scale(1.3);
      filter: none;
    }
  }
}
</style>
