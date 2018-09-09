<template>
  <section>
    <section class="body">
      <section class="main-content">
        <section class="box">
        </section>
        <fieldset>
          <!-- Hue -->
          <header class="field-name">Hue: </header>
          <input class="field-slider" type="range" min="0" max="360">
          <!-- Saturation -->
          <header class="field-name">Saturation: </header>
          <input class="field-slider" type="range" min="0" max="100">
          <!-- Lightness -->
          <header class="field-name">Lightness: </header>
          <input class="field-slider" type="range" min="0" max="100">
        </fieldset>
      </section>
      <section class="hsl-display">
        hsl(0degrees, 0%, 0%)
      </section>
    </section>
  </section>
</template>

<script>
export default {
  name: "ColorPicker",
  data: function() {
    return {
      hue: 1,
      saturation: 50,
      lightness: 50
    };
  },
  methods: {
    addHue() {
      this.hue++;
    },
    addSaturation() {
      this.saturation++;
    },
    addLightness() {
      this.lightness++;
    }
  }
};
</script>

<style scoped>
.main-content {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
  padding: 1em;
}

.box {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: black;
  border-radius: 1em;
  color: whitesmoke;
  height: 10em;
  width: 10em;
}

fieldset {
  display: flex;
  flex-direction: column;
  background-color: gray;
  color: white;
  padding: 0.8em;
}

.field-name {
  margin-top: 0.2em;
  text-align: left;
}

.field-slider {
  background-color: black;
  color: black;
}

.hsl-display {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
