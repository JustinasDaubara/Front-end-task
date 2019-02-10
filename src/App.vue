<template>
  <div id="app">
    <div class="container" style="width: 100%; padding-right: 15px; padding-left: 15px; margin-right: auto; margin-left: auto;">
    <div class="front-page" style="display: flex; justify-content: space-between; align-items: center;">
  <div class="front-page__left" style="text-align: left; color: white; font-weight: bold; font-size: 30px; width: 50%;">
    <p>New Year Offer</p>
    <p><span style="color:red">82% OFF</span> Web Hosting</p>
    <div class="row">
      <i class="fas fa-caret-right" style="color:red"></i>
      <Countdown style="font-size: 10px" date="June 07, 2019"/>
      <i class="fas fa-caret-left" style="color:red"></i>
      </div>
    <button type="button" class="btn btn-danger" style="font-size: 18px; padding: 5px 25px; align: center">GET STARTED NOW</button>
  </div>


  <div class="component-price" >
    <div class="component-price__save" style="display: flex; align-items: center; justify-content: center; flex-direction: column;">
      <div class="component-price-save__rect" style="text-transform: uppercase;
    font-size: 20px;
    padding: 10px 30px;
    color: #fff;
    background: #ff7678;">Save 82%</div>
      <div class="component-price-save__arrow" style="background: #ff7678;
    -webkit-transform: rotate(45deg);
    transform: rotate(45deg);
    width: 20px;
    height: 20px;
    margin-top: -10px;"></div>
    </div>
    <div class="price-block" style="font-size: 110px; color: white">
      <div class="price-block-wrapper" style="display: flex; justify-content: center;">
    <div class="price-block__cur" style="font-size: 1em;
    font-weight: 700;
    margin-top: .2em">$</div>
    <div class="price-block__big" style="font-size: 3em;
    font-weight: 700;
    line-height: .8em;">1</div> 
    <div class="price-block__right" style="display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: flex-start;">
      <div class="price-block-right__cents" style="font-size: .8em; font-weight: 700;">45</div>
      <div class="price-block-right__unit" style="display: flex">
        <div class="price-block-right-unit__term" style="font-size: .5em;
    display: flex;
    align-items: flex-end;
    margin: .3em">/mo</div>
      </div>
    </div>
    
    
  </div>
  </div>
</div>


  </div>
  </div>
  <ul style="position: relative; top: 130px; color: #fff; font-size: 12px; font-weight: 400; display: flex;
      justify-content: space-between; list-style-type: none;">
        <li>
            <i class="fas fa-check" style="color:green"></i>&nbsp;Guaranteed
                99,9% Uptime
        </li>
        <li>
            <i class="fas fa-check" style="color:green"></i>&nbsp;Superior Speed Performance
        </li>
        <li>
            <i class="fas fa-check" style="color:green"></i>&nbsp;24/7 Support Chat
        </li>
        <li>
            <i class="fas fa-check" style="color:green"></i>&nbsp;30-Day-Money-Back Guarantee
        </li>
      </ul>
</div>

</template>

<script>
import Countdown from './components/Countdown.vue';

export default {
  name: 'app',
  components: {
    Countdown
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
