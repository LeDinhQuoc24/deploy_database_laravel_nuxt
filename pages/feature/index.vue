<template>
  <div>
    <div class="hello1"> Công ty Lampart 117-119 Lý Chính Thắng</div>
    <div class="hello2"> Công ty Lampart Lý Chính Thắng</div>
    <nuxt-child/>
  </div>
</template>

<script>

export default {
  name: "index.vue"
}
</script>


<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Dancing+Script&display=swap');
.hello1 {
  font-family: 'Dancing Script', cursive;
  font-size: 40px;
  margin-right: 5%;
}
.hello2 {
  font-family: 'dinh_quoc', cursive;
  font-size: 40px;
}

</style>
