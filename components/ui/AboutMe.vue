<template>
  <div class="md:w-3/4 px-2 py-4 mt-12 md:mt-32 m-auto">
    <div class="select-none mb-6 w-full">
      <div class="px-4 relative">
        <div
          class="bg-kjColorLight dark:bg-kjColorBlack rounded-lg shadow-2xl border-2 border-kjColorLight"
        >
          <div class="p-4 grid md:gap-5 grid-cols-1 md:grid-cols-2">
            <img
              class="w-128 rounded-lg"
              src="~/assets/images/profile.jpg"
            />
            <div class="pt-10">
              <div>
                <font-awesome-icon
                  :icon="['fas', 'envelope']"
                  class="text-lg inline-block"
                />
                <p class="inline-block ml-1">
                  <a href="mailto:pablogabriel1941@gmail.com" class="font-bold underline">pablogabriel1941@gmail.com</a>
                </p>
              </div>

              <div>
                <font-awesome-icon
                  :icon="['fas', 'phone']"
                  class="text-lg inline-block"
                />
                <p class="inline-block ml-1">
                  31 975127912
                </p>
              </div>

              <div class="mt-2">
                <font-awesome-icon
                  :icon="['fas', 'map-marker-alt']"
                  class="text-lg inline-block"
                />
                <p class="inline-block ml-1">
                  Belo Horizonte, MG
                </p>
              </div>

              <div class="mt-2">
                <font-awesome-icon
                  :icon="['fab', 'linkedin']"
                  class="text-lg inline-block"
                />
                <p class="inline-block ml-1">
                  <a href="https://linkedin.com/in/pgabrielsw" target="_blank" class="font-bold underline">linkedin.com/in/pgabrielsw</a>
                </p>
              </div>
            </div>
          </div>

          <div class="p-4">
            <div class="mt-10">
              <div class="text-lg mb-5">
                <span class="font-medium uppercase">Sobre Mim</span>
                <CustomBorder />
              </div>

              <p>
                Profissional de Tecnologia da Informação com experiência em
                suporte técnico, infraestrutura e administração de ambientes
                corporativos, atuando com Active Directory, Office 365,
                virtualização, redes, monitoramento e bancos de dados.
                Atualmente direcionando a carreira para desenvolvimento de
                software, com estudos em lógica de programação, Programação
                Orientada a Objetos (POO), bancos de dados e desenvolvimento
                de aplicações.
              </p>

              <p class="mt-2">
                Possuo perfil analítico, foco em resolução de problemas,
                aprendizado contínuo e facilidade para adaptação a novas
                tecnologias, buscando oportunidade para atuar nas áreas de
                desenvolvimento, suporte ou infraestrutura de TI.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      numOfYears: 5
    };
  },
  mounted() {
    this.numOfYears = new Date().getFullYear() - 2018;
  }
};
</script>
