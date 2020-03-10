<template>
  <div class="chrono-container">
    <div class="round">
      <p>{{ chronos.days }}</p>
    </div>
    <div class="round">
      <p>{{ chronos.hours }}</p>
    </div>
    <div class="round">
      <p>{{ chronos.minutes }}</p>
    </div>
    <div class="round">
      <p>{{ chronos.seconds }}</p>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      countDownDate: new Date("April 23, 2020 15:37:25").getTime(),
      now: 0,
      distance: null,
      chronos: {
        days: null,
        hours: null,
        minutes: null,
        seconds: null
      }
    };
  },
  created() {
    this.startInterval();
  },
  mounted() {},

  methods: {
    startInterval() {
      setInterval(() => {
        this.now = new Date().getTime();
        this.distance = this.countDownDate - this.now;
        var days = Math.floor(this.distance / (1000 * 60 * 60 * 24));
        var hours = Math.floor(
          (this.distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60)
        );
        var minutes = Math.floor(
          (this.distance % (1000 * 60 * 60)) / (1000 * 60)
        );
        var seconds = Math.floor((this.distance % (1000 * 60)) / 1000);
        this.chronos.days = days;
        this.chronos.hours = hours;
        this.chronos.minutes = minutes;
        this.chronos.seconds = seconds;
      }, 1000);
    }
  }
};
</script>
<style lang="less" scoped>
.chrono-container
{
  display: flex;
  width: 100%;
  text-align: center;
  vertical-align: middle;
}
.round {
  margin: 1rem;
  width: 6rem;
  height: 6rem;
  border: 4px dotted coral;
  border-radius: 100%;
  text-align: center;

  p {
    vertical-align: middle;
    padding-top: 22%;
    font-size: 2rem;
  }
}
i {
  background-color: red;
}
</style>
