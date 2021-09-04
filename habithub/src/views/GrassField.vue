<template>
  <div>
    <!-- v-for, v-if로 여러개 element 만들기 -->
    <!-- <a v-for="index in 10" :key="index"> {{ index }} </a> -->
    <svg xmlns="http://www.w3.org/2000/svg">
      <g transform="translate(10, 20)" ref="field">
        <!-- <g v-for="i in 52" :key=i :config="{translate: (14 * i, 0)}">
          <rect v-for="j in 7" :key="j" :config="{width : 10, height: 10, x:13, y:13 * j, rx:2, ry:2}">
          </rect>
        </g> -->
        <!-- <g transform="translate(0, 0)">
            <rect width="10" height="10" x="14" y="65" class="cc ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-01" data-level="0" @click="drawContour"></rect>
            <rect width="10" height="10" x="14" y="78" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-02" data-level="0"></rect>
        </g>
        <g transform="translate(14, 0)">
            <rect width="10" height="10" x="13" y="0" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-03" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="13" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-04" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="26" class="ContributionCalendar-day" rx="2" ry="2" data-count="18" data-date="2021-01-05" data-level="4"></rect>
            <rect width="10" height="10" x="13" y="39" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-06" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="52" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-07" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="65" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-08" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="78" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-09" data-level="0"></rect>
        </g>
        <g transform="translate(28, 0)">
            <rect width="10" height="10" x="13" y="0" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-03" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="13" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-04" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="26" class="ContributionCalendar-day" rx="2" ry="2" data-count="18" data-date="2021-01-05" data-level="4"></rect>
            <rect width="10" height="10" x="13" y="39" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-06" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="52" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-07" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="65" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-08" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="78" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-09" data-level="0"></rect>
        </g>
        <g transform="translate(42, 0)">
            <rect width="10" height="10" x="13" y="0" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-03" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="13" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-04" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="26" class="ContributionCalendar-day" rx="2" ry="2" data-count="18" data-date="2021-01-05" data-level="4"></rect>
            <rect width="10" height="10" x="13" y="39" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-06" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="52" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-07" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="65" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-08" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="78" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-09" data-level="0"></rect>
        </g>
        <g transform="translate(56, 0)">
            <rect width="10" height="10" x="13" y="0" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-03" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="13" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-04" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="26" class="ContributionCalendar-day" rx="2" ry="2" data-count="18" data-date="2021-01-05" data-level="4"></rect>
            <rect width="10" height="10" x="13" y="39" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-06" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="52" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-07" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="65" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-08" data-level="0"></rect>
            <rect width="10" height="10" x="13" y="78" class="ContributionCalendar-day" rx="2" ry="2" data-count="0" data-date="2021-01-09" data-level="0"></rect>
        </g>
        <text x="14" y="-7" class="ContributionCalendar-label">Jan</text> -->
      </g>
    </svg>
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
          rect.setAttribute("fill", "#888888")
          g.appendChild(rect)
        }
        el.appendChild(g)
        // <g transform="translate(14, 0)">
        // Runs 5 times, with values of step 0 through 4.
        // console.log('Walking east one step');
      }
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
  fill: gray;
}
</style>