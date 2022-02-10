<template>
  <div id="profile">
    <div class="profile-img"></div>
    <p class="text-center">Welcome back,</p>
    <h3 class="username text-center">CK Molinga</h3>

    <div class="transactions-container mt-4">
      <div class="cashflow">
        <p class="text-gray-400">Income</p>
        <p class="text-black">$77500</p>
      </div>
    </div>
    <div class="transactions-container mt-4">
      <div class="cashflow">
        <p class="text-gray-400">Expenses</p>
        <p class="text-black">$57300</p>
      </div>
    </div>

    <div class="premium-card one">
      <p class="text-left px-4 pt-5 blurred">4358 7190 7782 9108</p>
      <p class="text-left px-4 pt-1 blurred">
        CK Molinga
        <span class="circle white-circle bg-transparent text-transparent ml-20"
          >uiii</span
        ><span class="circle gold-circle bg-transparent text-transparent"
          >ioo</span
        >
      </p>
    </div>
    <div
      class="
        premium-card
        two
        bg-gradient-to-br
        from-gray-500
        via-transparent
        to-gray-500
      "
    >
      <p class="text-left px-4 pt-5">4358 7190 7782 9108</p>
      <p class="text-left px-4 pt-1">
        CK Molinga
        <span class="circle white-circle bg-white text-transparent ml-20"
          >uiii</span
        ><span class="circle gold-circle bg-yellow-400 text-yellow-400"
          >ioo</span
        >
      </p>
    </div>
  </div>
</template>

<script></script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Ubuntu:wght@300;400;500;700&display=swap");
#profile {
  margin: 0 25px;
  width: 20vw;
  height: 100vh;
  display: none;
}
.profile-img {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  background: #f7f7f7;
  margin: 0 auto;
  margin-top: 100px;
}
.username {
  font-size: 24px;
  font-weight: bold;
}
.transactions-container {
  height: 60px;
  width: 100%;
  border: 1px solid #f1efef;
  border-radius: 6px;
}

.one {
  position: absolute;
  // right:0;
  // bottom:0;
  z-index: 2;
  transform: rotate(-25deg);
  background: #0c1f2b;
}

div.premium-card {
  color: #fff;
  margin: 0 25px;
  margin-top: 55px;
  height: 120px;
  border-radius: 15px;
}
.two {
  // background: transparent;
  position: absolute;
  // right:0;
  // bottom:0;
  z-index: 10;
}
.circle {
  width: 150px;
  height: 150px;
  border-radius: 50%;
}
.gold-circle {
  margin-left: -10px;
}
.blurred {
  filter: blur(3px);
}
.cashflow {
  display: flex;
  flex-direction: column;
}
.profile-img {
  background-image: url("../assets/user.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
@media (min-width: 992px) {
  #profile {
    margin: 0 25px;
    width: 20vw;
    height: 100vh;
    display: block;
  }
  .white-circle {
    margin-left: 5px;
  }
}
</style>
