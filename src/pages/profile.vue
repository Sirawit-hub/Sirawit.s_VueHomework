<template>
  <div class="container text-center" style="text-align: center">
    <h1>Profile</h1>
    <img
      src="https://uploads.codesandbox.io/uploads/user/fe1e58e1-57c0-439b-90dd-8c1fd94f19b1/dRtL-Profile_image.jpg"
      width="500"
    />
    <p>Name : {{ name }}</p>
    <p>Nickname : {{ nickname }}</p>
    <p>Age : {{ age }} years</p>
    <p>Weight : {{ weight }} kg. height : {{ height }} cm</p>
    <p>Hobby : {{ hobby }}</p>
    <p>
      Skills : {{ skill }}<br />
      {{ skill2 }}
    </p>
  </div>

  <p style="text-align: center">
    <button @click="goHome()">
      <router-link :to="{ name: 'home' }"
        ><img
          src="https://uploads.codesandbox.io/uploads/user/fe1e58e1-57c0-439b-90dd-8c1fd94f19b1/Lea7-home-icon.png"
          width="40"
          height="40"
      /></router-link>
    </button>

    <button @click="goContact()">
      <router-link :to="{ name: 'contact' }"
        ><img
          src="https://uploads.codesandbox.io/uploads/user/fe1e58e1-57c0-439b-90dd-8c1fd94f19b1/ltDj-Contact-icon.png"
          width="40"
          height="40"
      /></router-link>
    </button>
  </p>

  <div class="container text-center" style="text-align: center">
    <router-link :to="{ name: 'home' }"> Home </router-link> <br />
    <br />
    <router-link :to="{ name: 'contact' }"> Contact </router-link>
  </div>
</template>

<script>
export default {
  data: () => ({
    name: "Sirawit Srisuchat",
    nickname: "kla",
    age: "21",
    weight: "65",
    height: "173",
    hobby: "read a book",
    skill:
      "C# (visual studio 2017) , JAVA (eclipse) , SQL (Oracle SQL Developer) , HTML / CSS / bootstrap / PHP for web",
    skill2:
      "R for statistics , Basic network design cisco router / cisco switch / VMware, Power bi",
  }),
  methods: {
    goContact() {
      this.$router.push("/contact");
    },
    goHome() {
      this.$router.push("/");
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