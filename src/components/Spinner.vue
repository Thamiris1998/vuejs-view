<template>
    <div id="loader" class="overlay">
        <div v-show="loading" class="loading" id="g-spinner" style="zoom: 0.5;">
            <div class="circle c1"></div>
            <div class="circle c2"></div>
            <div class="circle c3"></div>
            <div class="circle c4"></div>
        </div>
    </div>
</template>

<style scoped>
#g-spinner{position:relative;margin:0 auto;height:200px;width:200px;border-radius:50%;opacity:0;-ms-filter:"progid:DXImageTransform.Microsoft.Alpha(Opacity=0)"}#g-spinner.loading{opacity:1;-ms-filter:"progid:DXImageTransform.Microsoft.Alpha(Opacity=100)";-webkit-transition:1s ease-in-out all;transition:1s ease-in-out all;-webkit-animation:rotate 2s cubic-bezier(.465,.183,.153,.946) infinite;animation:rotate 2s cubic-bezier(.465,.183,.153,.946) infinite}#g-spinner>.circle{position:absolute;height:40px;width:40px;border-radius:50%}#g-spinner.loading>.circle.c1{left:80px;top:5px;background:#4384f8;-webkit-animation:c1Center 4s cubic-bezier(.645,.045,.355,1) infinite;animation:c1Center 4s cubic-bezier(.645,.045,.355,1) infinite}#g-spinner.loading>.circle.c2{left:5px;top:80px;background:#34a855;-webkit-animation:c2Center 4s cubic-bezier(.645,.045,.355,1) infinite;animation:c2Center 4s cubic-bezier(.645,.045,.355,1) infinite}#g-spinner.loading>.circle.c3{left:80px;bottom:5px;background:#fbbd06;-webkit-animation:c3Center 4s cubic-bezier(.645,.045,.355,1) infinite;animation:c3Center 4s cubic-bezier(.645,.045,.355,1) infinite}#g-spinner.loading>.circle.c4{right:5px;top:80px;background:#ea4436;-webkit-animation:c4Center 4s cubic-bezier(.645,.045,.355,1) infinite;animation:c4Center 4s cubic-bezier(.645,.045,.355,1) infinite}@-webkit-keyframes rotate{from{-webkit-transform:rotate(0deg);transform:rotate(0deg)}to{-webkit-transform:rotate(360deg);transform:rotate(360deg)}}@keyframes rotate{from{-webkit-transform:rotate(0deg);transform:rotate(0deg)}to{-webkit-transform:rotate(360deg);transform:rotate(360deg)}}@-webkit-keyframes c1Center{0%{top:5px;background:#4384f8}24%{background:#4384f8}24%{background:#4384f8}25%{background:#fbbd06;top:80px}50%{background:#fbbd06;top:5px}55%{background:#fbbd06;top:5px}74%{background:#fbbd06}75%{background:#4384f8;top:80px}100%{background:#4384f8;top:5px}}@keyframes c1Center{0%{top:5px;background:#4384f8}24%{background:#4384f8}24%{background:#4384f8}25%{background:#fbbd06;top:80px}50%{background:#fbbd06;top:5px}55%{background:#fbbd06;top:5px}74%{background:#fbbd06}75%{background:#4384f8;top:80px}100%{background:#4384f8;top:5px}}@-webkit-keyframes c2Center{0%{background:#34a855;left:5px}24%{background:#34a855}25%{background:#ea4436;left:80px}50%{background:#ea4436;left:5px}55%{background:#ea4436;left:5px}74%{background:#ea4436}75%{background:#34a855;left:80px}100%{background:#34a855;left:5px}}@keyframes c2Center{0%{background:#34a855;left:5px}24%{background:#34a855}25%{background:#ea4436;left:80px}50%{background:#ea4436;left:5px}55%{background:#ea4436;left:5px}74%{background:#ea4436}75%{background:#34a855;left:80px}100%{background:#34a855;left:5px}}@-webkit-keyframes c3Center{0%{background:#fbbd06;bottom:5px}24%{background:#fbbd06}25%{background:#4384f8;bottom:80px}50%{background:#4384f8;bottom:5px}55%{background:#4384f8;bottom:5px}74%{background:#4384f8}75%{background:#fbbd06;bottom:80px}100%{background:#fbbd06;bottom:5px}}@keyframes c3Center{0%{background:#fbbd06;bottom:5px}24%{background:#fbbd06}25%{background:#4384f8;bottom:80px}50%{background:#4384f8;bottom:5px}55%{background:#4384f8;bottom:5px}74%{background:#4384f8}75%{background:#fbbd06;bottom:80px}100%{background:#fbbd06;bottom:5px}}@-webkit-keyframes c4Center{0%{background:#ea4436;right:5px}24%{background:#ea4436}25%{background:#34a855;right:80px}50%{background:#34a855;right:5px}55%{background:#34a855;right:5px}74%{background:#34a855}75%{background:#ea4436;right:80px}100%{background:#ea4436;right:5px}}@keyframes c4Center{0%{background:#ea4436;right:5px}24%{background:#ea4436}25%{background:#34a855;right:80px}50%{background:#34a855;right:5px}55%{background:#34a855;right:5px}74%{background:#34a855}75%{background:#ea4436;right:80px}100%{background:#ea4436;right:5px}}/* Absolute Center Spinner */.overlay{position:fixed;z-index:9999;height: 2em;width: 2em;overflow: show;margin: auto;top: 0;left: 0;bottom: 0;right: 0;}
</style>

<script>
export default {
  name: 'loading-spinner',
  props: {
    loading: Boolean,
  },
};
</script>
