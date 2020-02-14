<template>
  <div>
    <div v-if="showGrid===0" class="category-grid">
      <div
        v-for="(food, idx) in foodlist1"
        :key="`${food}-${idx}`"
        class="center-box"
      >
        <button @click="changeview(idx)">
          <img class="category-image" :src="category1Img[idx]" />
        </button>
      </div>
      <div class="center-box">Location</div>
      <div
        v-for="(food, idx) in foodlist2"
        :key="`${food}-${idx}`"
        class="center-box"
      >
        <button @click="changeview(idx)">
          <img class="category-image" :src="category2Img[idx]" />
        </button>
      </div>
    </div>

    <div v-else>
      
    </div>
  </div>
</template>

<script>
import "@/assets/style/css/gridStyle.css";
export default {
  name: "MobileFoodCategory",
  data() {
    return {
      foodlist1: [0, 1, 2, 3],
      foodlist2: [0, 1, 2, 3],
      category1Img: [
        "https://i.imgur.com/XIZOsMo.png",
        "https://i.imgur.com/iBTK8eT.png",
        "https://i.imgur.com/w1JOWBH.png",
        "https://i.imgur.com/gmDYKFw.png"
      ],
      category2Img: [
        "https://i.imgur.com/ZBrgtCR.png",
        "https://i.imgur.com/AVUnO3w.png",
        "https://i.imgur.com/IF2chC8.png",
        "https://i.imgur.com/6V4QzGn.png"
      ],
      showGrid:0,
    };
  },
  methods: {
    changeview(idx) {
      console.log("hello");
      console.log(idx);
      // this.$store.state.viewcategory = this.key;
      // this.showGrid = 1
      
    },
  }
};
</script>

<style></style>
