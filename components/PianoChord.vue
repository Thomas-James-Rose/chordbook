<template>
  <div>
    <ul class="keys">
      <div>
        <li class="white c" :class="highlightKey('c')"></li>
        <li class="black cs" :class="highlightKey('cs')"></li>
        <li class="white d" :class="highlightKey('d')"></li>
        <li class="black ds" :class="highlightKey('ds')"></li>
        <li class="white e" :class="highlightKey('e')"></li>
        <li class="white f" :class="highlightKey('f')"></li>
        <li class="black fs" :class="highlightKey('fs')"></li>
        <li class="white g" :class="highlightKey('g')"></li>
        <li class="black gs" :class="highlightKey('gs')"></li>
        <li class="white a" :class="highlightKey('a')"></li>
        <li class="black as" :class="highlightKey('as')"></li>
        <li class="white b" :class="highlightKey('b')"></li>
      </div>
      <div>
        <li class="white c" :class="highlightKey('c2')"></li>
        <li class="black cs" :class="highlightKey('cs2')"></li>
        <li class="white d" :class="highlightKey('d2')"></li>
        <li class="black ds" :class="highlightKey('ds2')"></li>
        <li class="white e" :class="highlightKey('e2')"></li>
        <li class="white f" :class="highlightKey('f2')"></li>
        <li class="black fs" :class="highlightKey('fs2')"></li>
        <li class="white g" :class="highlightKey('g2')"></li>
        <li class="black gs" :class="highlightKey('gs2')"></li>
        <li class="white a" :class="highlightKey('a2')"></li>
        <li class="black as" :class="highlightKey('as2')"></li>
        <li class="white b" :class="highlightKey('b2')"></li>
      </div>
    </ul>
  </div>
</template>

<style>
.chord-name {
  text-align: center;
}

.keys {
  height: 18.875em;
  width: 62em;
  margin: 3em auto;
  padding: 3em 0 0 3em !important;
  position: relative;
  border: 1px solid #160801;
  border-radius: 1em;
  background: grey;
}

.keys li {
  margin: 0;
  padding: 0;
  list-style: none;
  position: relative;
  float: left;
}

.keys .white {
  height: 16em;
  width: 4em;
  z-index: 1;
  border-left: 1px solid #bbb;
  border-bottom: 1px solid #bbb;
  border-radius: 0 0 5px 5px;
  box-shadow: -1px 0 0 rgba(255, 255, 255, 0.8) inset, 0 0 5px #ccc inset,
    0 0 3px rgba(0, 0, 0, 0.2);
  background: linear-gradient(to bottom, #eee 0%, #fff 100%);
}

.keys .black {
  height: 8em;
  width: 2em;
  margin: 0 0 0 -1em;
  z-index: 2;
  border: 1px solid #000;
  border-radius: 0 0 3px 3px;
  box-shadow: -1px -1px 2px rgba(255, 255, 255, 0.2) inset,
    0 -5px 2px 3px rgba(0, 0, 0, 0.6) inset, 0 2px 4px rgba(0, 0, 0, 0.5);
  background: linear-gradient(45deg, #222 0%, #555 100%);
}

.keys .a,
.keys .g,
.keys .d,
.keys .b,
.keys .e {
  margin: 0 0 0 -1em;
}

.keys .highlight {
  background: #3c9add !important;
}
</style>

<script>
export default {
  name: 'PianoChord',
  props: {
    notes: {
      type: Array,
      required: true,
    },
  },
  methods: {
    highlightKey(key) {
      return this.notes.includes(key) ? 'highlight' : ''
    },
  },
}
</script>
