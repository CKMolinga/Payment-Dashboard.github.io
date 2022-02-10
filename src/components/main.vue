/* eslint-disable prettier/prettier */
/* eslint-disable no-undef */
/* eslint-disable no-undef */
/* eslint-disable prettier/prettier */
/* eslint-disable prettier/prettier */
<template>
  <div id="main" @toggle-data="dataListener">
    <div class="menu drop-menu" v-if="toggleMenu">
      <h3 class="pt-2">Home</h3>
      <h3 id="dashboard" class="text-white">Dashboard</h3>
      <h3>Profile</h3>
      <h3>Settings</h3>
      <h3>Logout</h3>
    </div>
    <div class="flex main-header">
      <h2 class="text-2xl">Dashboard</h2>
      <select name="filter" id="">
        <option value="1" selected>Today</option>
        <option value="2">Last 3 days</option>
        <option value="3">Last 7 days</option>
        <option value="4">Last 28 days</option>
      </select>
    </div>

    <div class="transactions-container cards-container mt-4 pb-5 mb-10">
      <div class="transaction-headings flex py-4 px-3">
        <h3 class="text-1xl text-black">Diamond Card</h3>
        <h3 class="text-1xl">Platinum Card</h3>
        <h3 class="text-1xl">Gold Card</h3>
      </div>
      <div class="cards">
        <div class="premium-card">
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
        <div class="cards-headings flex py-4 px-3">
          <h3 class="text-1xl text-black p-2">
            <span class="text-blue-300">1852 </span>Transactions
          </h3>
          <h3 class="text-1xl p-2">
            <span class="text-green-500">$77500 </span>Received
          </h3>
          <h3 class="text-1xl p-2">
            <span class="text-red-300">$57300 </span>Withdrawn
          </h3>
        </div>
      </div>
    </div>

    <div class="flex transactions">
      <h3 class="text-1xl">Transactions</h3>
    </div>
    <div class="transactions-container mt-4">
      <!-- Sandbox passing transactions data from an array of objects  -->

      <div
        class="flex py-2 px-3"
        v-for="(transaction, index) in transactions"
        :key="index"
      >
        <h3 class="text-1xl">{{ transaction.name }}</h3>
        <h3 class="text-1xl">{{ transaction.date }}</h3>
        <h3 class="text-1xl">{{ transaction.amount }}</h3>
        <h3 class="text-1xl text-green-500">{{ transaction.status }}</h3>
      </div>

      <!-- Sandbox end  -->

      <!-- <div class="transaction-headings flex py-4 px-3">
        <h3 class="text-1xl">Transactions</h3>
        <h3 class="text-1xl">Date</h3>
        <h3 class="text-1xl">Amount</h3>
        <h3 class="text-1xl">Status</h3>
      </div>
      <div class="flex py-2 px-3">
        <h3 class="text-1xl">New Order</h3>
        <h3 class="text-1xl">02-10-2021</h3>
        <h3 class="text-1xl">$1200</h3>
        <h3 class="text-1xl text-green-500">Completed</h3>
      </div>
      <div class="flex py-2 px-3">
        <h3 class="text-1xl">Withdraw</h3>
        <h3 class="text-1xl">02-10-2021</h3>
        <h3 class="text-1xl">$1800</h3>
        <h3 class="text-1xl text-blue-300">In Progress</h3>
      </div>
      <div class="flex py-2 px-3">
        <h3 class="text-1xl">Divi pro</h3>
        <h3 class="text-1xl">29-09-2021</h3>
        <h3 class="text-1xl">$399</h3>
        <h3 class="text-1xl text-red-300">Declined</h3>
      </div>
      <div class="flex py-2 px-3">
        <h3 class="text-1xl">New Order</h3>
        <h3 class="text-1xl">25-09-2021</h3>
        <h3 class="text-1xl">$4000</h3>
        <h3 class="text-1xl text-green-500">Completed</h3>
      </div>
      <div class="flex py-2 px-3">
        <h3 class="text-1xl">New Order</h3>
        <h3 class="text-1xl">25-09-2021</h3>
        <h3 class="text-1xl">$2000</h3>
        <h3 class="text-1xl text-green-500">Completed</h3>
      </div> -->
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      toggleMenu: true,

      // userStatus: [0,1,1,0,1,1,0],
      // transactions: [
      //   {users: [Jude, Prince, Henry],
      //     amount: [2000,8000,50000],
      //   },
      //   {users: [Kerry, Loise, Julius],
      //     amount: [1000,-8000,-6000],
      //   },
      //   {users: [Ben, Tracy, William],
      //     amount: [3000,7000,4000],
      //   },
      //   {users: [Jude, Prince, Henry],
      //     amount: [2000,8000,50000],
      //   },
      // ],
      transactions: [
        {
          name: "New Order",
          date: "02-10-2021",
          amount: "$1200",
          status: "Completed",
        },
        {
          name: "Withdraw",
          date: "02-10-2021",
          amount: "$1800",
          status: "In Progress",
        },
        {
          name: "Divi pro",
          date: "29-09-2021",
          amount: "$399",
          status: "Declined",
        },
        {
          name: "New Order",
          date: "25-09-2021",
          amount: "$4000",
          status: "Completed",
        },
        {
          name: "New Order",
          date: "25-09-2021",
          amount: "$2000",
          status: "Completed",
        },
      ],
    };
  },
  methods: {
dataListener(data) {
  console.log(data);
  this.toggleMenu = !this.toggleMenu;
}
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Ubuntu:wght@300;400;500;700&display=swap");

#main {
  margin: 25px 25px;
  max-width: 86vw;
  height: 100vh;
}

.menu {
  background: #0c1f2b;
  color: rgba(255, 255, 255, 0.733);
  display: block;
  margin-top: 25px;
  padding: 15px 10px;
  display: block;
}

h3 {
  // padding: 25px 0;
  margin: 0 0 25px 0;
  cursor: pointer;
}
h3:hover {
  color: #fff;
}

.flex {
  display: flex;
  justify-content: space-between;
}
.main-header {
  padding: 25px 0;
  padding-top: 45px;
}
.transactions-container {
  height: auto;
  width: 100%;
  border: 1px solid #f1efef;
  border-radius: 6px;
}
.transaction-headings {
  color: rgba(128, 128, 128, 0.479);
}
.cards-container {
  background: #f7f7f7;
}
.cards {
  display: flex;
}
div.premium-card {
  background: #0c1f2b;
  color: #fff;
  margin: 0 15px;
  width: 0%;
  height: 120px;
  border-radius: 15px;
  visibility: hidden;
}
.circle {
  width: 150px;
  height: 150px;
  border-radius: 50%;
}
.gold-circle {
  margin-left: -10px;
}

@media (min-width: 768px) {
  .menu {
    background: #0c1f2b;
    color: rgba(255, 255, 255, 0.733);
    text-align: center;
    display: none;
  }
}

@media (min-width: 992px) {
  #main {
    margin: 0 25px;
    width: 50vw;
    height: 100vh;
  }
  .main-header {
    padding: 25px 0;
  }
  div.premium-card {
    background: #0c1f2b;
    color: #fff;
    margin: 0 15px;
    width: 40%;
    height: 120px;
    border-radius: 15px;
    visibility: visible;
  }
  .white-circle {
    margin-left: 5px;
  }
}
</style>
