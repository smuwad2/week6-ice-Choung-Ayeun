<script>
export default { 
  data() {
    return {
      id: "demo1",
      blueBox: true,   // div starts blue
      blueBtn: true,   // button starts primary
    }
  },
  methods: { 
    toggleColor() {
      // toggle both box color and button variant
      this.blueBox = !this.blueBox;
      this.blueBtn = !this.blueBtn;
    }
  }
}
</script>

<template>
  <div id="part1">
    <div 
      :id="id"
      class="m-2"
      :class="{ blueBox: blueBox, redBox: !blueBox }"
    >
      div ID : {{ id }}
    </div>

    <button
      type="button"
      :class="['btn', blueBtn ? 'btn-primary' : 'btn-danger']"
      @click="toggleColor"
    >
      Change Color
    </button>
  </div>
</template>

<style scoped>
.redBox { background-color: red; }
.blueBox { background-color: blue; }
#demo1 { color: white; }
</style>