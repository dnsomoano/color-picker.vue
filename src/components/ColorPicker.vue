<template>
  <section>
    <section class="*" :style="changingBox">
      <section class="main-content">
        <section class="box">
        </section>
        <fieldset>
          <!-- Hue -->
          <header class="field-name">Hue: </header>
          <input class="field-slider" type="range" min="0" max="360" v-on:input="addHue">
          <!-- Saturation -->
          <header class="field-name">Saturation: </header>
          <input class="field-slider" type="range" min="0" max="100" v-on:input="addSaturation">
          <!-- Lightness -->
          <header class="field-name">Lightness: </header>
          <input class="field-slider" type="range" min="0" max="100" v-on:input="addLightness">
        </fieldset>
      </section>
      <section class="hsl-display">
        hsl({{this.hue}}, {{this.saturation}}%, {{this.lightness}}%)
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
      lightness: 100
    };
  },
  methods: {
    addHue(event) {
      this.hue = event.target.value;
    },
    addSaturation(event) {
      this.saturation = event.target.value;
    },
    addLightness(event) {
      this.lightness = event.target.value;
    }
  },
  computed: {
    changingBox: function() {
      return {
        "background-color":
          "hsl(" +
          this.hue +
          ", " +
          this.saturation +
          "%, " +
          this.lightness +
          "%)"
      };
    },
    changingText: function() {
      return {
        color:
          "hsl(" +
          this.hue +
          ", " +
          this.saturation +
          "%, " +
          this.lightness +
          "%)"
      };
    }
  }
};
</script>

<style scoped>
.main-content {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
  padding: 1em;
}

.box {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: white;
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
  color: white;
}
</style>
