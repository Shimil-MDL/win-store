<template>
  <div class="appStoreMain">
    <div class="preview" :class="previewBackground">
      <div class="previewContainer">
        <div
          @click="previewBackground = 'greenGradient'"
          class="previewItems greenGradient"
        ></div>
        <div
          @click="previewBackground = 'seeOffGradient'"
          class="previewItems seeOffGradient"
        ></div>
        <div
          @click="previewBackground = 'clearSkyGradient'"
          class="previewItems clearSkyGradient"
        ></div>
        <div
          @click="previewBackground = 'suzyGradient'"
          class="previewItems suzyGradient"
        ></div>
        <div
          @click="previewBackground = 'purpleGradient'"
          class="previewItems purpleGradient"
        ></div>
        <div
          @click="previewBackground = 'sweetMorningGradient'"
          class="previewItems sweetMorningGradient"
        ></div>
      </div>
    </div>
    <TrendingApps />
  </div>
</template>

<script>
import TrendingApps from "./AppStoreMain/TrendingApps.vue";
export default {
  name: "AppStoreMain",
  components: {
    TrendingApps,
  },
  data() {
    return {
      previewBackground: "greenGradient",
    };
  },
};
</script>

<style scoped>
.appStoreMain {
  position: absolute;
  top: 9%;
  left: 6.8%;
  width: 93%;
  height: 90%;

  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: space-around;
}

.appStoreMain .preview {
  height: 63%;
  width: 98%;
  border-radius: 5px;

  display: flex;
  align-items: flex-end;
  justify-content: center;
}

.appStoreMain .previewContainer {
  width: 100%;
  height: 40%;

  display: flex;
  align-items: center;
  justify-content: space-evenly;
}
.appStoreMain .preview .previewItems {
  /* background: rgba(20, 20, 20, 0.623); */
  height: 85%;
  width: 16%;
  border-radius: 5px;
  transition: 0.5s;

  /* box-sizing: border-box; */
}

.greenGradient {
  --gradientBg: linear-gradient(45deg, hsl(175, 30%, 33%), hsl(143, 59%, 43%));
  background-image: linear-gradient(
    45deg,
    hsl(175, 30%, 33%),
    hsl(143, 59%, 43%)
  );
}
.seeOffGradient {
  --gradientBg: linear-gradient(45deg, #df4b1f, #df60a8);
  background-image: linear-gradient(45deg, #df4b1f, #df60a8);
}
.clearSkyGradient {
  --gradientBg: linear-gradient(45deg, #00d2aa, #3a7bd5);
  background-image: linear-gradient(45deg, #00d2aa, #3a7bd5);
}
.suzyGradient {
  --gradientBg: linear-gradient(45deg, #d0a423, #d65100);
  background-image: linear-gradient(45deg, #d0a423, #d65100);
}
.purpleGradient {
  --gradientBg: linear-gradient(45deg, #a044ff, #6a3093);
  background-image: linear-gradient(45deg, #a044ff, #6a3093);
}
.sweetMorningGradient {
  --gradientBg: linear-gradient(45deg, #d5af19, #de2711);
  background-image: linear-gradient(45deg, #d5af19, #de2711);
}

.appStoreMain .preview .previewItems:hover {
  transform: scale(1.02);
  opacity: 0.6;
}
</style>
