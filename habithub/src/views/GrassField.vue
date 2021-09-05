<template>
  <div>
    <!-- v-for, v-if로 여러개 element 만들기 -->
    <!-- <a v-for="index in 10" :key="index"> {{ index }} </a> -->
    <div id="grassfield">
      <svg xmlns="http://www.w3.org/2000/svg">
        <g transform="translate(10, 20)" ref="field"></g>
      </svg>
    </div>

    <div id="tooltip" class="hidden">
      <p>tooltip test</p>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    // console.log('hello')
    let el = this.$refs.field
    this.generateGrassField(el)
  },
  methods: {
    drawContour(e) {
      console.log(e)
      e.srcElement.style.stroke = 'blue'
    },
    generateGrassField(el) {
      console.log(el)
      var NS = "http://www.w3.org/2000/svg"
      for (var i = 0; i < 52; i++) {
        var g = document.createElementNS(NS, "g");
        g.setAttribute("translate", i*14);
        for (var j = 0; j < 7; j++) {
          var rect = document.createElementNS(NS, "rect");
          rect.setAttribute("width", 10)
          rect.setAttribute("height", 10)
          rect.setAttribute("x", 13 * i)
          rect.setAttribute("y", 13 * j)
          rect.setAttribute("rx", 2)
          rect.setAttribute("ry", 2)
          rect.setAttribute("fill", "#ebedf0")
          rect.setAttribute("stroke", "#1b1f230f")
          rect.setAttribute("transition", "all 5s linear")
          rect.addEventListener("mouseover", this.makeRectDark)
          rect.addEventListener("mouseout", this.makeRectBright)
          g.appendChild(rect)
        }
        el.appendChild(g)
      }
    },
    makeRectDark(e) {
      this.changeStyle(e.srcElement, 'black');
    },
    makeRectBright(e) {
      this.changeStyle(e.srcElement, '#ebedf0')
    },
    changeStyle(el, color) {
      el.style.fill = color
    }
  }
}
</script>

<style scoped>
svg {
  width: 722px;
  height: 112px;
}
rect {
  transition: all 0.3s linear;
}
rect:hover, rect:focus {
  fill: black;
}
.hidden {
  visibility: hidden;
}
</style>