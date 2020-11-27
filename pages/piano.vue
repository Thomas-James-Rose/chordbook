<template>
  <div>
    <select id="piano-chord-selector" v-model="selectedChord" name="chord">
      <option v-for="chord in chords" :key="chord.name">
        {{ chord.name }}
      </option>
    </select>
    <piano-chord
      :chord-name="getChordDataByName(chords, selectedChord).name"
      :notes="getChordDataByName(chords, selectedChord).notes"
    />
  </div>
</template>

<style>
#piano-chord-selector {
  background: #fff;
  padding: 0.2em;
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
        { name: 'None', notes: [] },
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
      return chords.find((chord) => chord.name === name)
    },
  },
}
</script>
