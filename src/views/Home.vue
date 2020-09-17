<template>
  <div class="home">
    <h1>Welcome to Technology Trouble Shooter</h1>
    <img alt="Vue logo" src="../assets/img/techlogo.png" />
    <TroubleShooter />
  </div>
</template>

<script>
// @ is an alias to /src
import TroubleShooter from "@/components/TroubleShooter.vue";

export default {
  name: "Home",
  components: {
    TroubleShooter
  }
};
</script>
