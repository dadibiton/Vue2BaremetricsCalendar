<template>
  <div id="app">
    <h1 class="heading">
      Vue Baremetrics Calendar
    </h1>
    <div class="calendars">
      <h3 class="heading">
        Date Range
      </h3>
      <Calendar
        @rangeEdit="processOutput"
        type="double"
        elementName="otherRangePicker"
      />
      <br />
      <br />
      <h3 class="heading">
        Vue Baremetrics Calendar
      </h3>
      <Calendar
        @dateEdit="processOutput"
        type="single"
        elementName="primaryRangePicker"
      />
    </div>
  </div>
</template>
<script>
import Calendar from "./components/Calendar";
export default {
  components: {
    Calendar
  },
  methods: {
    processOutput(output) {
      console.log(output);
    }
  }
};
</script>
<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  text-align: center;
}
.calendars {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
