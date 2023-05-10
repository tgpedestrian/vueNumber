<script >
import ContainerVue from "./components/veiw/ContainerVue.vue";
import ContainerGuessVue from "./components/veiw/GuessNumberVue.vue";
import ContainerGuessSuccessVue from "./components/veiw/GuessNumberSuccessVue.vue";
export default{
  components:{
    ContainerVue,
    ContainerGuessVue,
    ContainerGuessSuccessVue,
  } 
}

</script>

<template>
  <div class="containerBody">
    <!-- <ContainerVue /> -->
    <ContainerGuessVue />
    <!-- <ContainerGuessSuccessVue /> -->

  </div>

</template>

<style lang="scss" scoped>

.containerBody{
  background-color: #E1B3AB;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}


</style>
