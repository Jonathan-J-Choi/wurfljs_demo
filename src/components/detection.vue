<template>
  <div class="detection">
    <div class="wurfljs" id="js-detection">
      <h2>
        WURFL is the industry's most advanced device detection solution. Using
        WURFL.JS version:
      </h2>
      <p>
        <span id="version"></span>
      </p>
      <p>With the WURFL device data snapshot XML dated:</p>
      <p>
        <span id="date"></span>
      </p>
      <p>We have inspected your device's User-Agent:</p>
      <p>
        <span id="ua"></span>
      </p>
      <p>Which is identified as:</p>
      <p>
        <span id="complete_name"></span>
      </p>
    </div>
    <div class="capabilities">
      <h2>WURFL Device Capabilities</h2>
      <div class="info">
        <ul class="capability_name">
          <li>Complete Device Name:</li>
          <li>Form Factor:</li>
          <li>Device OS:</li>
          <li>Advertised Browser:</li>
          <li>Max Image Height:</li>
          <li>Max Image Width:</li>
          <li>Release MSRP:</li>
          <li>Release Date:</li>
          <li>WebP Support:</li>
        </ul>
        <ul class="capability_result">
          <li><span id="complete_name"></span></li>
          <li><span id="form_factor"></span></li>
          <li><span id="device_os"></span></li>
          <li><span id="adv_browser"></span></li>
          <li><span id="max_image_height"></span></li>
          <li><span id="max_image_width"></span></li>
          <li><span id="release_msrp"></span></li>
          <li><span id="release_date"></span></li>
          <li><span id="webp"></span></li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "detection",
  mounted() {
    // window.addEventListener('load', () => {
    //   // let cn = document.getElementById("complete_name");
    //     // let ff = document.getElementById("form_factor");
    //     // let im = document.getElementById("is_mobile");
    //     // cn.innerHTML = WURFL.complete_device_name;
    //     // ff.innerHTML = WURFL.form_factor;
    //     // im.innerHTML = WURFL.is_mobile;
    //     console.log(WURFL.is_mobile)
    // })
    document.onreadystatechange = () => {
      if (document.readyState == "complete") {
        /*global WURFL*/
        /*eslint no-undef: "error"*/
        console.log(WURFL);
        let cn = document.getElementById("complete_name");
        let ff = document.getElementById("form_factor");
        let im = document.getElementById("is_mobile");
        cn.innerHTML = WURFL.complete_device_name;
        ff.innerHTML = WURFL.form_factor;
        im.innerHTML = WURFL.is_mobile;
      }
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
a {
  color: #42b983;
}
.info {
  display: grid;
  grid-template-areas: "left right";
}
.capability_name {
  grid-area: left;
}
.capability_result {
  grid-area: right;
}
</style>
