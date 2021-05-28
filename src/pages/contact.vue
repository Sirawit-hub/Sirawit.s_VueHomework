<template>
  <div class="container text-center" style="text-align: center">
    <h1>Contact</h1>
    <p>Phone : {{ phone }}</p>
    <p>E-mail : {{ email }}</p>
    <p>
      Address : {{ address }} <br />
      {{ address2 }}
    </p>

    <p style="text-align: center">
      <button @click="goHome()">
        <router-link :to="{ name: 'home' }"
          ><img src="@/assets/home-icon.png" width="40" height="40"
        /></router-link>
      </button>

      <button @click="goProfile()">
        <router-link :to="{ name: 'contact' }"
          ><img src="@/assets/report_icon.png" width="40" height="40"
        /></router-link>
      </button>
    </p>

    <div>
      <router-link :to="{ name: 'home' }"> Home </router-link> <br />
      <br />
      <router-link :to="{ name: 'profile' }"> Profile </router-link>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    email: "sr.sirawit_st@tni.ac.th",
    phone: "094-782-3888",
    address: "88/449 Atoll maldives palms, Bang Kaeo Subdistrict",
    address2: ",Bang Phli District, Samut Prakan 10540 ",
  }),
  methods: {
    goHome() {
      this.$router.push("/");
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
  font-size: 20px;
  --margin-left: 550px;
  font-family: "Courier New", Courier, monospace;
}
</style>