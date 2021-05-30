<template>
  <div class="container text-center" style="text-align: center">
    <h1>Home</h1>

    <div class="container text-center" style="text-align: center">
      <router-link :to="{ name: 'profile' }"> Profile </router-link> <br />
      <br />
      <button @click="goProfile()">
        <router-link :to="{ name: 'profile' }"
          ><img
            src="https://uploads.codesandbox.io/uploads/user/fe1e58e1-57c0-439b-90dd-8c1fd94f19b1/w6c--report_icon.png"
            width="150"
            height="150"
        /></router-link></button
      ><br />
      <br />
    </div>

    <div>
      <router-link :to="{ name: 'contact' }"> Contact </router-link> <br />
      <br />
      <button @click="goContact()">
        <router-link :to="{ name: 'home' }"
          ><img
            src="https://uploads.codesandbox.io/uploads/user/fe1e58e1-57c0-439b-90dd-8c1fd94f19b1/ltDj-Contact-icon.png"
            width="150"
            height="150"
        /></router-link></button
      ><br />
      <br />
    </div>
  </div>
</template>


<script>
export default {
  methods: {
    goContact() {
      this.$router.push("/contact");
    },
    goProfile() {
      this.$router.push("/profile");
    },
  },
};
</script>

<style scoped>
h1 {
  font-size: 2em;
  text-align: center;
  font-family: "Courier New", Courier, monospace;
}
p {
  text-align: center;
  font-family: "Courier New", Courier, monospace;
}
</style>