<template>
  <div class="card" style="width: 18rem">
    <!-- <div v-b-hover="handleHover"> -->
      <!-- <img
        v-if="isHovered"
        :src="require(`@/assets/images/bacteria/${memberData.id}.png`)"
        class="card-img-top"
        :alt="memberData.name"
      />

      <img
        v-else
        :src="require(`@/assets/images/profile/${memberData.id}.png`)"
        class="card-img-top"
        :alt="memberData.name"
      /> -->
      <img
        :src="require(`@/assets/images/profile/${memberData.id}.png`)"
        class="card-img-top"
        :alt="memberData.name"
      />
    <!-- </div> -->

    <div class="rectangle">
      <div class="lula-stokes">{{ memberData.name }}</div>
      <div class="cmo">{{ memberData.career }}</div>
    </div>
    <div class="mask"></div>
  </div>
</template>

<script>
export default {
  props: { memberData: {} },
  data() {
    return {
      isHovered: false,
    }
  },
  methods: {
    handleHover(hovered) {
      this.isHovered = hovered
    },
  },
  computed: {
    getImgUrl() {
      var images = require.context('../assets/images/profile', false, /\.png$/)
      return images('./' + 'jose' + '.png')
    },
  },
}
</script>

<style scoped>
.mask {
  height: 8px;
  /* width: 349px; */
  border-radius: 0 0 2px 2px;
  background-color: #69c183;
  box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.1);
}
.cmo {
  height: 24px;
  /* width: 277px; */
  color: #5c5c5c;
  font-family: Graphik;
  font-size: 12px;
  letter-spacing: 0;
  line-height: 24px;
}
.lula-stokes {
  height: 15px;
  /* width: 277px; */
  color: #27262d;
  font-family: Graphik;
  font-size: 14px;
  font-weight: 600;
  letter-spacing: -0.3px;
  line-height: 15px;
}
.rectangle {
  /* height: 83px; */
  /* width: 349px; */
  border-radius: 0 0 2px 2px;
  background-color: #ffffff;
  /* box-shadow: 0 0 20px 0 rgba(45,41,38,0.24); */
}
</style>