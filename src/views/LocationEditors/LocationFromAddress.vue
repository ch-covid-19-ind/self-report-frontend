<template>
  <div>Location from address (TBD)</div>
</template>

<script>

  export default {
    name: "location-from-address",
    components: {},
    props: {
      location: null,
      valid: Boolean,
    },
    methods: {
      locationChanged(value) {
        //this.$emit('update:valid', ...);
        //this.$emit('update:location', value);
      }
    },
  }
</script>

<style>

</style>
