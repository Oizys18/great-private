<template>
  <div class="tab-review-card">
        <div class="review-card-name">
          <h4>
            {{this.reviewItem.store}}
          </h4>
        </div>

        <div class="review-card-contents">
          <p>{{this.reviewItem.contents}}</p>
        </div>

        <div class="review-card-rating">
          <StarRating :rating="reviewItem.rating" /> 
        </div>

    </div>
</template>
 
<script>
import StarRating from '@/components/common/StarRating.vue'
export default {
  name: "TabCard",
  props:["reviewItem"],
  components:{
    StarRating,
  },
};
</script>



<style>
 
</style>