<template>
  <div>
    <div class="page-container">
      <h1>Title</h1>
      <h3>Subtitle</h3>
      <div class="form-container">
        <div class="flex-row">
          <div class="col-9 form-content">
            <div class="flex-row">
              <div class="col-8">
                <div class="div-box">
                  <p>Div box</p>
                </div>Based on
                <span id="income-value">____</span> income in, after
                <span id="years-value">__</span> years:
              </div>
              <div class="col-4">
                <div class="form-group">
                  <form>
                    <label for="contribution-range-input">401(k) contribution
                      <br>x/month
                    </label>
                    <input type="number" v-bind:value="rangeSliderValue">
                    <input
                      type="range"
                      min="1"
                      max="100"
                      value="1"
                      class="range-slider"
                      name="contribution-range-input"
                      id="contribution-range-input"
                      v-model="rangeSliderValue"
                    >
                    
                    <label for="hsa-input">HSA (coming soon)</label>
                    <input type="text" v-model="hsa" id="hsa-input" name="hsa-input">

                    <div class="select-box-contanier">
                      <div>
                        <label for="tax-year-select">Tax year</label>
                        <select type="select" id="tax-year-select" name="tax-year-select"></select>
                      </div>

                      <div id="state-select-holder">
                        <label for="state-select">State</label>
                        <select type="select" id="state-select" name="state-select"></select>
                      </div>
                    </div>

                    <label for="employer-match-input">Employer match</label>
                    <input type="number" id="employer-match-input" name="employer-match-input">
                    
                    <label for="limit-input">Limit on mathcnig contributions</label>
                    <input type="number" id="limit-input" name="limit-input">
                    
                    <label for="portfolio-distribution">Portfolio Distribution</label>
                    <input type="text" class="portfolio-distribution" name="portfolio-distribution">
                    <input type="text" class="limit-input" name="portfolio-distribution">
                    <input type="text" class="limit-input" name="portfolio-distribution">
                    <input type="text" class="limit-input" name="portfolio-distribution">
                  </form>
                </div>
              </div>
            </div>
          </div>
          <div class="col-3 adv-content">
            <h2>adv</h2>
          </div>
        </div>
      </div>
    </div>
    <footer>
      <h4>Footer</h4>
    </footer>
  </div>
</template>

<script>
export default {
  name: "AppForm",
  data() {
    return {
      rangeSliderValue: "",
      hsa: ""
    };
  },
  computed: {
    rangeSliderValue2: function() {
      console.log(this.rangeSliderValue);
    }
  },
  props: {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  margin-left: 150px;
}
h3 {
  margin: 40px 0 0;
}
.page-container {
  max-width: 1200px;
  margin: 0 auto;
  display: block;
}
.flex-row {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: space-between;
}

.col-9 {
  flex: 0 0 80.666667%;
  max-width: 80.666667%;
}
.col-8 {
  flex: 0 0 68.666667%;
  max-width: 68.666667%;
}
.col-4 {
  flex: 0 0 30.333333%;
  max-width: 30.333333%;
  padding-left: 3px;
}
.col-3 {
  flex: 0 0 17.333333%;
  max-width: 17.333333%;
  padding-left: 3px;
}

.form-content,
.adv-content {
  border: solid rgba(0, 0, 0, 0.2);
}

.div-box {
  min-height: 400px;
  border: solid rgba(0, 0, 0, 0.2);
}

.form-group {
  display: flex;
  flex-direction: column;
}
.form-group label {
  display: block;
}

label {
  margin-top: 10px;
}

label[for="contribution-range-input"] {
  margin-top: 15px;
}

input {
  height: 20px;
  width: 200px;
  margin-top: 10px;
}

#contribution-range-input {
  -webkit-appearance: none;
  height: 5px;
  background: #d3d3d3;
  outline: none;
  opacity: 0.7;
  -webkit-transition: 0.2s;
  transition: opacity 0.2s;
}

#contribution-range-input:hover {
  opacity: 1;
}

#contribution-range-input::-webkit-slider-thumb {
  -webkit-appearance: none;
  appearance: none;
  width: 13px;
  height: 13px;
  border-radius: 50%;
  background: darkblue;
  cursor: pointer;
}

#contribution-range-input::-moz-range-thumb {
  width: 25px;
  height: 25px;
  border-radius: 50%;
  background: #4caf50;
  cursor: pointer;
}

.select-box-contanier {
  display: flex;
  flex-direction: row;
}

select {
  margin-top: 10px;
}

#tax-year-select {
  width: 100px;
}

#state-select-holder {
  margin-left: 52px;
}
#state-select {
  width: 50px;
}
</style>
