<template>
  <div>
    <h1 class="mt-6 text-2xl font-bold capitalize">Experiência Profissional / Formação</h1>
    <CustomBorder />

    <div class="mt-8">
      <PortfolioWebApps />
    </div>

    <h1 class="mt-6 text-2xl font-bold capitalize">Aplicações</h1>
    <CustomBorder />

    <div class="mt-8">
      <PortfolioNativeApps />
    </div>

    <p class="mt-6 text-sm text-kjColorGray dark:text-kjColorLight italic">
      Prometo que daqui a pouco você ainda vai ver meus projetos aqui mesmo nessa aba ^^
    </p>

    <div
      class="max-w-xl shadow-2xl h-40 py-5 md:py-0 px-5 md:px-10 mt-10 md:flex justify-between items-center"
    >
      <p class="text-lg font-bold mb-3 md:mb-0">
        Conheça minhas habilidades 👉
      </p>
      <Button displayTitle="SKILLS" linkTo="/resume" />
    </div>
  </div>
</template>
