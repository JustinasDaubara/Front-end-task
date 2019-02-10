<template lang="pug">
  .countdown-to
    .container
      .row
        .col-sm
          p.digit {{ days | two_digits }}
          p.text(v-t="'Days'") Days
        .col-sm
          p.digit {{ hours | two_digits }}
          p.text(v-t="'Hours'") Hours
        .col-sm
          p.digit {{ minutes | two_digits }}
          p.text(v-t="'Minutes'") Minutes
        .col-sm
          p.digit {{ seconds | two_digits }}
          p.text(v-t="'Seconds'") Seconds
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
@Component({
  filters: {
    two_digits(value: number) {
      if (value.toString().length <= 1) {
        return "0" + value.toString();
      }
      return value.toString();
  }
}
})
export default class Countdown extends Vue {
  @Prop() private date!: string;
  now: number = Math.trunc(new Date().getTime() / 1000);
  created() {
    const self = this;
    window.setInterval(() => {
      self.now = Math.trunc(new Date().getTime() / 1000);
    }, 1000);
  }
  get parsedDate() {
    return Math.trunc(Date.parse(this.date) / 1000);
  }
  get days() {
    return Math.trunc((this.parsedDate - this.now) / 60 / 60 / 24);
  }
  get hours() {
    return Math.trunc((this.parsedDate - this.now) / 60 / 60) % 24;
  }
  get minutes() {
    return Math.trunc((this.parsedDate - this.now) / 60) % 60;
  }
  get seconds() {
    return Math.trunc(this.parsedDate - this.now) % 60;
  }
}
</script>

<style >
.text {
  color:white;
  font-size: 10px;
  margin-bottom: 10px;
  text-align: center;
}
.digit {
  color: white;
  font-size: 28px;
  font-weight: 100;
  text-align: center;
}
</style>