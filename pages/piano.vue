<template>
  <div>
    <piano-chord
      v-for="chord in chords"
      :key="chord.name"
      :chord-name="chord.name"
      :notes="chord.notes"
    />
  </div>
</template>

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
    }
  },
}
</script>
