<template>
  <div class="chord-page-wrapper">
    <div class="select-wrapper">
      <v-select
        v-model="selectedChord"
        :items="chords"
        item-text="name"
        item-value="name"
        label="Select Chord..."
      ></v-select>
    </div>
    <piano-chord :notes="getChordDataByName(chords, selectedChord).notes" />
  </div>
</template>

<style>
.chord-page-wrapper {
  display: flex;
  flex-direction: column;
}

.select-wrapper {
  text-align: center;
}

#piano-chord-selector {
  background: #fff;
  padding: 0.2em;
  width: 3em;
  appearance: initial;
}
</style>

<script>
import PianoChord from '~/components/PianoChord.vue'

export default {
  components: {
    PianoChord,
  },
  data() {
    return {
      chords: [
        // TODO: Finish populating this
        { name: 'A', notes: ['a', 'cs2', 'e2'] },
        // { name: 'Am', notes: [] },
        { name: 'Bb', notes: ['as', 'd2', 'f2'] },
        // { name: 'Bbm', notes: [] },
        // { name: 'B', notes: [] },
        // { name: 'Bm', notes: [] },
        { name: 'C', notes: ['c', 'e', 'g'] },
        // { name: 'Cm', notes: [] },
        { name: 'D', notes: ['d', 'fs', 'a'] },
        // { name: 'Dm', notes: [] },
        { name: 'E', notes: ['e', 'gs', 'b'] },
        // { name: 'Em', notes: [] },
        { name: 'F', notes: ['f', 'a', 'c2'] },
        // { name: 'Fm', notes: [] },
        // { name: 'F#', notes: [] },
        // { name: 'F#m', notes: [] },
        { name: 'G', notes: ['g', 'b', 'd2'] },
        // { name: 'Gm', notes: [] },
      ],
      selectedChord: 'None',
    }
  },
  methods: {
    getChordDataByName(chords, name) {
      return chords.find((chord) => chord.name === name) || { notes: [] }
    },
  },
}
</script>
