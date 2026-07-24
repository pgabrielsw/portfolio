<template>
  <section class="mt-12 md:mt-32 services">
    <h1 class="capitalize text-3xl md:text-4xl font-bold leading-none">
      Experiência e Formação
    </h1>
    <p class="capitalize mt-2 text-lg">minha trajetória profissional</p>
    <CustomBorder />

    <div>
      <div class="mt-8">
        <PortfolioWebApps />
      </div>

      <div
        class="max-w-xl shadow-2xl h-40 py-5 md:py-0 px-5 md:px-10 mt-10 md:flex justify-between items-center"
      >
        <p class="text-lg font-bold mb-3 md:mb-0">
          Conheça minhas habilidades 👉
        </p>
        <Button displayTitle="SKILLS" linkTo="/resume" />
      </div>
    </div>
  </section>
</template>
