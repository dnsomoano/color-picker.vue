<template>
  <section>
    This is a componentaaaaaa
  </section>
</template>

<script>
export default {
  name: "ColorPicker",
  data: function() {
    return {
      hue: 0,
      saturation: 50,
      lightness: 50
    }
  },
  methods: {
    addHue () {
      this.hue++;
    }
  }
};
</script>

<style>
</style>
