<template>
  <div>

    <div class="position-relative">
      <!-- shape Hero -->
      <section class="section-shaped my-0">
        <div class="shape shape-style-1 shape-default shape-skew">
          <span></span>
          <span></span>
        </div>
        <div class="container shape-container d-flex">

          <div class="col text-white">
            <h1 class="display-3 text-white">{{ $t('faq.title') }}</h1>

            <h3 class="text-white">{{ $t(`faq.goalQuestion`, {disease: 'Covid-19'}) }}</h3>
            <p>{{ $t(`faq.goalResponse`, {disease: 'Covid-19'}) }}</p>

            <h3 class="text-white">{{ $t(`faq.othersQuestion1`, {disease: 'Covid-19'}) }}</h3>
            <p>{{ $t(`faq.othersResponse1`, {disease: 'Covid-19'}) }}</p>

            <h3 class="text-white">{{ $t(`faq.othersQuestion2`, {disease: 'Covid-19'}) }}</h3>
            <p>{{ $t(`faq.othersResponse2`, {disease: 'Covid-19'}) }}</p>

            <h3 class="text-white">{{ $t(`faq.othersQuestion3`, {disease: 'Covid-19'}) }}</h3>
            <p>{{ $t(`faq.othersResponse3`, {disease: 'Covid-19'}) }}</p>

            <h3 class="text-white">{{ $t(`faq.othersQuestion4`, {disease: 'Covid-19'}) }}</h3>
            <p>{{ $t(`faq.othersResponse4`, {disease: 'Covid-19'}) }}</p>

            <h3 class="text-white">{{ $t(`faq.othersQuestion5`, {disease: 'Covid-19'}) }}</h3>
            <p>{{ $t(`faq.othersResponse5`, {disease: 'Covid-19'}) }}</p>

            <h3 class="text-white">{{ $t(`faq.othersQuestion6`, {disease: 'Covid-19'}) }}</h3>
            <p>{{ $t(`faq.othersResponse6`, {disease: 'Covid-19'}) }}</p>

            <h3 class="text-white">{{ $t(`faq.othersQuestion7`, {disease: 'Covid-19'}) }}</h3>
            <p>{{ $t(`faq.othersResponse7`, {disease: 'Covid-19'}) }}</p>

          </div>
        </div>
      </section>
    </div>

  </div>
</template>

<script>

  export default {
    name: "faq",
    components: {},
    data() {
      return {}
    },
  };

</script>

<style scoped>

</style>
