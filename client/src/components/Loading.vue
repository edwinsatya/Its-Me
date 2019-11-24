<template>
  <div class="loading">
    <div id="loader-container">
      <div class="loader-div">
        <div class="loader-div">
          <div class="loader-div">
            <div class="loader-div">
              <div class="loader-div"></div>
            </div>
          </div>
        </div>
      </div>
      <h1 style="color:white;">
        Loading
        <span>.</span>
        <span>.</span>
        <span>.</span>
        <span>.</span>
        <span>.</span>
      </h1>
    </div>
  </div>
</template>

<script>
export default {
  name: "loading",
  created() {
    setTimeout(() => {
      this.$router.push("/content");
    }, 5000);
  },
  mounted() {
    this.$nextTick(() => {
      $("h1 span").each(function(index) {
        setTimeout(() => {
          $("h1 span")
            .eq(index)
            .addClass("display");
        }, 1000 * (index + 1));
      });
    });
  }
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css?family=Roboto:500&display=swap");
.loading {
  font-family: "Roboto", sans-serif;
  margin: 0;
  padding: 0;
  background: black;
  width: 100%;
  height: 100vh;
  font-size: 10px;
  letter-spacing: 2px;
  text-align: center;
}
#loader-container {
  width: 175px;
  height: 175px;
  position: relative;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.loader-div {
  width: calc(100% - 16px);
  height: calc(100% - 16px);
  border: 8px solid #162534;
  border-top: 8px solid #09f;
  border-radius: 50%;
  animation: rotate 5s linear infinite;
  margin-bottom: 10px;
}
span {
  opacity: 0;
}
.display {
  opacity: 1;
}
@keyframes rotate {
  100% {
    transform: rotate(360deg);
  }
}

/*dekstop vers*/
@media (min-width: 720px) {
  .loading {
    font-size: 14px;
    letter-spacing: 2px;
  }
}
</style>