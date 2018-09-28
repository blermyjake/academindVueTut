<template>
    <div>
    <h1>Users Page</h1>
    <p>Team ID is {{ $route.params.teamId }}</p>
    <button @click="goHome">Go Home</button>
    </div>
</template>

<script>
export default {
  // lifecycle hook
  watch: {
    $route(to, from) {
      //   alert(to.params.teamId);
    }
  },
  created() {
    // alert(this.$route.params.teamId);
  },
  methods: {
    goHome() {
      // this adds a push to home on the button above
      this.$router.push("/");
    }
  }
};
</script>
