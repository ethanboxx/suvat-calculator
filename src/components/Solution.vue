<template>
  <div id="solution">
    <template v-if="formular() !== null">
      <template v-if="letter === s">
        <Ssutat2
          v-if="formular() === 2"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Ssutat2>
        <Suvt
          v-else-if="formular() === 3"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Suvt>
        <Sv2u22as
          v-else-if="formular() === 4"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Sv2u22as>
        <Ssvtat2
          v-if="formular() === 5"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Ssvtat2>
      </template>
      <template v-if="letter === u">
        <Uvuat
          v-if="formular() === 1"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Uvuat>
        <Usutat2
          v-if="formular() === 2"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Usutat2>
        <Uuvt
          v-if="formular() === 3"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Uuvt>
        <Uv2u22as
          v-if="formular() === 4"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Uv2u22as>
      </template>
      <template v-if="letter === v">
        <Vvuat
          v-if="formular() === 1"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Vvuat>
        <Vuvt
          v-if="formular() === 3"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Vuvt>
        <Vuv2u22as
          v-if="formular() === 4"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Vuv2u22as>
        <Vsvtat2
          v-if="formular() === 5"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Vsvtat2>
      </template>
      <template v-if="letter === a">
        <Avuat
          v-if="formular() === 1"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Avuat>
        <Asutat2
          v-if="formular() === 2"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Asutat2>
        <Av2u22as
          v-if="formular() === 4"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Av2u22as>
        <Asvtat2
          v-if="formular() === 5"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Asvtat2>
      </template>
      <template v-if="letter === t">
        <Tvuat
          v-if="formular() === 1"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Tvuat>
        <Tsutat2
          v-if="formular() === 2"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Tsutat2>
        <Tuvt
          v-if="formular() === 3"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Tuvt>
        <Tsvtat2
          v-if="formular() === 5"
          :suvat="suvat"
          :letter="letter"
          :dp="dp"
        ></Tsvtat2>
      </template>
    </template>
  </div>
</template>

<script>
import Ssutat2 from "./solutions/s/Ssutat2.vue";
import Suvt from "./solutions/s/Suvt.vue";
import Sv2u22as from "./solutions/s/Sv2u22as.vue";
import Ssvtat2 from "./solutions/s/Ssvtat2.vue";
import Uvuat from "./solutions/u/Uvuat.vue";
import Usutat2 from "./solutions/u/Usutat2.vue";
import Uuvt from "./solutions/u/Uuvt.vue";
import Uv2u22as from "./solutions/u/Uv2u22as.vue";
import Vvuat from "./solutions/v/Vvuat.vue";
import Vuvt from "./solutions/v/Vuvt.vue";
import Vuv2u22as from "./solutions/v/Vuv2u22as.vue";
import Vsvtat2 from "./solutions/v/Vsvtat2.vue";
import Avuat from "./solutions/a/Avuat.vue";
import Asutat2 from "./solutions/a/Asutat2.vue";
import Av2u22as from "./solutions/a/Av2u22as.vue";
import Asvtat2 from "./solutions/a/Asvtat2.vue";
import Tvuat from "./solutions/t/Tvuat.vue";
import Tsutat2 from "./solutions/t/Tsutat2.vue";
import Tuvt from "./solutions/t/Tuvt.vue";
import Tsvtat2 from "./solutions/t/Tsvtat2.vue";
export default {
  name: "Solution",
  components: {
    Ssutat2,
    Suvt,
    Sv2u22as,
    Ssvtat2,
    Uvuat,
    Usutat2,
    Uuvt,
    Uv2u22as,
    Vvuat,
    Vuvt,
    Vuv2u22as,
    Vsvtat2,
    Avuat,
    Asutat2,
    Av2u22as,
    Asvtat2,
    Tvuat,
    Tsutat2,
    Tuvt,
    Tsvtat2,
  },
  props: ["suvat", "letter", "dp"],
  data: () => ({
    s: "s",
    u: "u",
    v: "v",
    a: "a",
    t: "t",
  }),
  methods: {
    formular() {
      switch (this.letter) {
        case "s":
          if (
            this.suvat.u !== null &&
            this.suvat.t !== null &&
            this.suvat.a !== null
          )
            return 2;
          if (
            this.suvat.u !== null &&
            this.suvat.v !== null &&
            this.suvat.t !== null
          )
            return 3;
          if (
            this.suvat.v !== null &&
            this.suvat.u !== null &&
            this.suvat.a !== null
          )
            return 4;
          if (
            this.suvat.v !== null &&
            this.suvat.t !== null &&
            this.suvat.a !== null
          )
            return 5;

          break;

        case "u":
          if (
            this.suvat.v !== null &&
            this.suvat.a !== null &&
            this.suvat.t !== null
          )
            return 1;
          if (
            this.suvat.s !== null &&
            this.suvat.t !== null &&
            this.suvat.a !== null
          )
            return 2;
          if (
            this.suvat.s !== null &&
            this.suvat.v !== null &&
            this.suvat.t !== null
          )
            return 3;
          if (
            this.suvat.v !== null &&
            this.suvat.a !== null &&
            this.suvat.s !== null
          )
            return 4;
          break;

        case "v":
          if (
            this.suvat.u !== null &&
            this.suvat.a !== null &&
            this.suvat.t !== null
          )
            return 1;
          if (
            this.suvat.s !== null &&
            this.suvat.u !== null &&
            this.suvat.t !== null
          )
            return 3;
          if (
            this.suvat.u !== null &&
            this.suvat.a !== null &&
            this.suvat.s !== null
          )
            return 4;
          if (
            this.suvat.s !== null &&
            this.suvat.t !== null &&
            this.suvat.a !== null
          )
            return 5;
          break;

        case "a":
          if (
            this.suvat.v !== null &&
            this.suvat.u !== null &&
            this.suvat.t !== null
          )
            return 1;
          if (
            this.suvat.s !== null &&
            this.suvat.u !== null &&
            this.suvat.t !== null
          )
            return 2;
          if (
            this.suvat.v !== null &&
            this.suvat.u !== null &&
            this.suvat.s !== null
          )
            return 4;
          if (
            this.suvat.s !== null &&
            this.suvat.v !== null &&
            this.suvat.t !== null
          )
            return 5;
          break;

        case "t":
          if (
            this.suvat.v !== null &&
            this.suvat.u !== null &&
            this.suvat.a !== null
          )
            return 1;
          if (
            this.suvat.s !== null &&
            this.suvat.u !== null &&
            this.suvat.a !== null
          )
            return 2;
          if (
            this.suvat.s !== null &&
            this.suvat.u !== null &&
            this.suvat.v !== null
          )
            return 3;
          if (
            this.suvat.s !== null &&
            this.suvat.v !== null &&
            this.suvat.a !== null
          )
            return 5;
          break;
      }
      return null;
    },
  },
};
</script>

<style lang="sass">


#solution
  overflow-x: auto
  width: auto
  > div
    display: inline-flex
    align-items: center
    justify-content: flex-start
    align-items: stretch
    flex-direction: row
    height: 100%
    min-width: 100%
    h1, h2, h3
      margin: 0
      white-space: nowrap
    h3
      math
        display: inline-block
        font-size: 1.4em

    > *
      min-width: 300px
      max-width: auto
      padding-left: 10px
      padding-right: 10px
      box-shadow: inset 0px 0px 5px 0px rgba(0,0,0,0.75)
      display: flex
      align-items: center
      justify-content: center

      math
        font-size: 3em
        white-space: nowrap
        padding: 10px
      @for $i from 1 through 20
        &:nth-child(#{$i})
            transition-delay: (($i - 1s) / 10) + .02
    > h2
      writing-mode: vertical-lr
      text-orientation: sideways
      transform: rotate(180deg)
      width: 100px
      min-width: unset
.fade-enter-active, .fade-leave-active
  transition: .5s
  transform: scale(1)
.fade-enter, .fade-leave-to
  opacity: 0
  transform: scale(0.8)
</style>
