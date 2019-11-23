<template>
  <div class="home">
    <div class="squere">
      <span id="roll1"></span>
      <span id="roll2"></span>
      <span id="roll3"></span>
      <div class="content">
        <h2>
          <span id="sp1">Ed</span>win S<span id="sp2">at</span>ya Yu<span
            id="sp3"
            >dis</span
          >tira
        </h2>
        <p>
          a little story about my background and some collections of my
          portfolio.
        </p>
        <a @click="goContent">
          <span></span>
          <span></span>
          <span></span>
          <span></span>
          Get Start
        </a>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "home",
  methods: {
    goContent() {
      this.$router.push("/content");
    }
  },
  mounted() {
    this.$nextTick(() => {
      //home
      $(".squere").hide();
      setTimeout(() => {
        $(".squere").fadeIn("very-slow");
      }, 1000);
      //end home
    });
  }
};
</script>
<style scoped>
@import url("https://fonts.googleapis.com/css?family=Roboto:500&display=swap");
.home {
  display: flex;
  justify-content: center;
  align-items: center;
  background: #000;
  box-sizing: border-box;
  min-height: 100vh;
}
.squere {
  position: relative;
  width: 400px;
  height: 400px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.squere #roll1 {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 2px solid white;
  border-radius: 38% 62% 63% 38% / 41% 44% 56% 59%;
  transition: 3s;
  animation: animate 4s linear infinite;
}
.squere:hover #roll1 {
  transition: 0.5s;
  border: none;
  background: rgba(111, 244, 0, 0.8);
}
.squere #roll2 {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 2px solid white;
  border-radius: 38% 62% 63% 38% / 41% 44% 56% 59%;
  transition: 2s;
  animation: animate 2s linear infinite;
}
.squere:hover #roll2 {
  transition: 1s;
  border: none;
  background: rgba(0, 233, 255, 0.8);
}
.squere #roll3 {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 2px solid white;
  border-radius: 38% 62% 63% 38% / 41% 44% 56% 59%;
  transition: 1s;
  animation: animate2 6s linear infinite;
}
.squere:hover #roll3 {
  transition: 1.5s;
  border: none;
  background: rgba(0, 0, 0, 0.8);
}
.squere:hover .content a {
  transform: translate(0, 0);
  opacity: 1;
}
@keyframes animate {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
@keyframes animate2 {
  0% {
    transform: rotate(360deg);
  }
  100% {
    transform: rotate(0deg);
  }
}
.content {
  position: relative;
  padding: 40px 60px;
  color: white;
  text-align: center;
  transition: 0.5s;
  z-index: 1000;
}
.content a {
  transform: translate(0, 30px);
  opacity: 0;
  margin-top: 20px;
  position: relative;
  display: inline-block;
  padding: 15px 30px;
  color: #2196f3;
  text-decoration: none;
  text-transform: uppercase;
  letter-spacing: 4px;
  font-size: 20px;
  overflow: hidden;
  transition: 0.2s;
}
.content a:hover {
  cursor: pointer;
  color: #255784;
  background: #2196f3;
  box-shadow: 0 0 10px #2196f3, 0 0 40px #2196f3, 0 0 #2196f3;
  transition-delay: 1s;
}
a span {
  position: absolute;
  display: block;
}
a span:nth-child(1) {
  top: 0;
  left: -100%;
  width: 100%;
  height: 2px;
  background: linear-gradient(90deg, transparent, #2196f3);
}
a:hover span:nth-child(1) {
  left: 100%;
  transition: 1s;
}
a span:nth-child(3) {
  bottom: 0;
  right: -100%;
  width: 100%;
  height: 2px;
  background: linear-gradient(270deg, transparent, #2196f3);
}
a:hover span:nth-child(3) {
  right: 100%;
  transition: 1s;
  transition-delay: 0.5s;
}
a span:nth-child(2) {
  top: -100%;
  right: 0;
  width: 2px;
  height: 100%;
  background: linear-gradient(180deg, transparent, #2196f3);
}
a:hover span:nth-child(2) {
  top: 100%;
  transition: 1s;
  transition-delay: 0.25s;
}
a span:nth-child(4) {
  bottom: -100%;
  left: 0;
  width: 2px;
  height: 100%;
  background: linear-gradient(360deg, transparent, #2196f3);
}
a:hover span:nth-child(4) {
  bottom: 100%;
  transition: 1s;
  transition-delay: 0.75s;
}
#sp1 {
  color: rgba(111, 244, 0, 0.8);
}
#sp2 {
  color: rgba(0, 233, 255, 0.8);
}
#sp3 {
  color: rgba(100, 100, 100, 0.8);
}
</style>
