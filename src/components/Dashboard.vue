<template>
  <div>
    
    <div class="row">
      <!-- menu -->
      <div class="col-lg-3">

        <div class="row p-3 mb-3">
          <img class="w-25" src="../assets/logo.png" alt="logo" >
          <h5 class="text">Komgrip Technology</h5>
          <hr width=80% size=3>
        </div>
        
        <div class="d-flex align-items-start">
          <div class="nav flex-column nav-pills me-3 w-100" id="v-pills-tab" role="tablist" aria-orientation="vertical">
            <button class="nav-link active p-3" id="menu" data-bs-toggle="pill" data-bs-target="#v-pills-dashboard" type="button" role="tab" aria-controls="v-pills-dashboard" aria-selected="true">Dashboard</button>
            <button class="nav-link p-3" id="menu" data-bs-toggle="pill" data-bs-target="#v-pills-menu_1" type="button" role="tab" aria-controls="v-pills-menu_1" aria-selected="false">menu 1</button>
            <button class="nav-link p-3" id="menu" data-bs-toggle="pill" data-bs-target="#v-pills-menu_2" type="button" role="tab" aria-controls="v-pills-menu_2" aria-selected="false" >menu 2</button>
            <button class="nav-link p-3" id="menu" data-bs-toggle="pill" data-bs-target="#v-pills-menu_3" type="button" role="tab" aria-controls="v-pills-menu_3" aria-selected="false">menu 3</button>
            <button class="nav-link p-3" id="menu" data-bs-toggle="pill" data-bs-target="#v-pills-menu_4" type="button" role="tab" aria-controls="v-pills-menu_4" aria-selected="false">menu 4</button>
          </div>
          <div class="tab-content" id="v-pills-tabContent">
            <div class="tab-pane fade show active" id="v-pills-dashboard" role="tabpanel" aria-labelledby="v-pills-dashboard-tab" tabindex="0">

            </div>
          </div>
        </div>

        <div class="sidenav-footer mx-3 col-2 ">
          <div class="card card-background shadow-none card-background-mask-secondary" id="sidenavCard">
            <!-- <div class="full-background" style="background-image: url('../assets/img/curved-images/white-curved.jpeg')"></div> -->
            <div class="card-body text-start p-3 w-100">
              <div class="icon icon-shape icon-sm bg-white shadow text-center mb-3 d-flex align-items-center justify-content-center border-radius-md">
                <i class="ni ni-diamond text-dark text-gradient text-lg top-0" aria-hidden="true" id="sidenavCardIcon"></i>
              </div>
              <div class="docs-info">
                <h6 class="text-white up mb-0">Need help?</h6>
                <p class="text-xs font-weight-bold">CoinCap API 2.0</p>
                <a class="btn btn-white btn-sm w-100 mb-0">Documentation</a>
              </div>
            </div>
          </div>
        </div>

      </div>

      <!-- body -->
      <div class="col-lg-9">

        <div class="row mb-5">
          <div class="col">
            <nav aria-label="breadcrumb">
              <ol class="breadcrumb bg-transparent mb-0 pb-0 pt-1 px-0 me-sm-6 me-5">
                <li class="breadcrumb-item text-sm"><a class="opacity-5 text-dark" href="javascript:;">Pages</a></li>
                <li class="breadcrumb-item text-sm text-dark active" aria-current="page">Dashboard</li>
              </ol>
              <h6 class="font-weight-bolder mt-2" style="text-align: left;"><b>Dashboard</b></h6>
            </nav>
          </div>
          <div class="col">
            <i class="fa fa-user" aria-hidden="true"></i><h6 style="text-align: right;">Jaroon Ritdechwong</h6>
          </div>
          
        </div>

        <div class="row">
          <div class="col p-2">
            <div class="card" style="width: 18rem;">
              <div class="card-body">
                <h5 class="card-title text-uppercase text-secondary text-xx font-weight-bolder opacity-7" id="name_1"></h5>
                <h6 class="card-subtitle mb-2 text-body-secondary" id="Usd_1"></h6>
                <p class="card-text" id="Per_1"></p>
              </div>
            </div>
          </div>
          <div class="col p-2">
            <div class="card" style="width: 18rem;">
              <div class="card-body">
                <h5 class="card-title text-secondary text-xx font-weight-bolder opacity-7" id="name_2"></h5>
                <h6 class="card-subtitle mb-2 text-body-secondary"  id="Usd_2"></h6>
                <p class="card-text" id="Per_2"></p>
              </div>
            </div>
          </div>
          <div class="col p-2">
            <div class="card" style="width: 18rem;">
              <div class="card-body">
                <h5 class="card-title text-secondary text-xx font-weight-bolder opacity-7" id="name_3"></h5>
                <h6 class="card-subtitle mb-2 text-body-secondary" id="Usd_3"></h6>
                <p class="card-text" id="Per_3"></p>
              </div>
            </div>
          </div>
          <div class="col p-2">
            <div class="card" style="width: 18rem;">
              <div class="card-body">
                <h5 class="card-title text-secondary text-xx font-weight-bolder opacity-7" id="name_4"></h5>
                <h6 class="card-subtitle mb-2 text-body-secondary" id="Usd_4"></h6>
                <p class="card-text" id="Per_4"></p>
              </div>
            </div>
          </div>
        </div>

        <div class="card-body px-0 pb-2 mt-3">
              <div class="table-responsive">
                <div class="row p-3">
                  <div class="col-lg-3 col-7">
                    <h5><b>Cryptocurrencies</b></h5>
                  </div>
                  <div class="col-lg-9 col-5 my-auto text-end">
                    <button class="btn btn-info m-3" @click="prevBtn()"> prev </button>
                    <button class="btn btn-info m-3" @click="nextBtn()"> next </button>
                  </div>
                </div>
                <table class="table align-items-center mb-0">
                  <thead>
                    <tr>
                      <th class="text-uppercase text-secondary text-xx font-weight-bolder opacity-7">NO</th>
                      <th class="text-uppercase text-secondary text-xx font-weight-bolder opacity-7">NAME</th>
                      <th class="text-center text-uppercase text-secondary text-xx font-weight-bolder opacity-7">SYMBOL</th>
                      <th class="text-center text-uppercase text-secondary text-xx font-weight-bolder opacity-7">SUPPLY / MAX SUPPLY</th>
                      <th class="text-center text-uppercase text-secondary text-xx font-weight-bolder opacity-7">USD</th>
                      <th class="text-center text-uppercase text-secondary text-xx font-weight-bolder opacity-7">24 HR</th>
                    </tr>
                  </thead>
                  <tbody >
                    <!-- <tr v-for="(item, index) in list" :key="item.name">
                        <td>{{ index + 1 }}.</td>
                        <td class="text ">{{ item.name }}</td>
                        <td>{{ item.symbol || 'NO LIMIT' }}</td>
                        <td>{{ item.supply || 'NO LIMIT' }}</td>
                        <td>{{ item.price}}</td>
                        <td>{{ item.change}}</td>
                    </tr> -->
                  </tbody>
                </table>
              </div>
            </div>

            
        <div class="row mt-5">Copyright @ 2024 Technologies Co., Ltd.</div>
        

      </div>
    </div>
     
  </div>
</template>


<script>
  import axios from 'axios';
  
  export default {
    name: 'HelloWorld',
    data() {
      return {
        list: {},
        ID: ["bitcoin","ethereum","solana","dogecoin"],
        currentPage: 1,
        itemsPerPage: 10,
        Total: [],
        row: ""
      }
    },
    mounted() {

      this.getID();

      this.fetchData();
      
    },
    methods: {
      async getID() {
        await axios.get(`https://komgrip.co.th/coincap/assets/bitcoin`).then(res => { this.send(res.data.data, 1); })
        await axios.get(`https://komgrip.co.th/coincap/assets/ethereum`).then(res => { this.send(res.data.data, 2); })
        await axios.get(`https://komgrip.co.th/coincap/assets/solana`).then(res => { this.send(res.data.data, 3); })
        await axios.get(`https://komgrip.co.th/coincap/assets/dogecoin`).then(res => { this.send(res.data.data, 4); })
      },
      send(data, index) {
        let Usd = parseFloat(data.priceUsd);
        let per = parseFloat(data.changePercent24Hr);
        
        let per_show = per < 0 ? "text-danger" : "text-success";

        document.querySelector(`#name_${index}`).innerHTML = data.name;
        document.querySelector(`#Usd_${index}`).innerHTML = `$${Usd.toFixed(2)}`;
        document.querySelector(`#Per_${index}`).innerHTML = `<span class="${isNaN(per) ? '' : per_show}">${per.toFixed(2)}%</span>`;
      },
      // ฟังกชันเรียกหลังโหลดหน้า
      async fetchData() {
        try {
          const response = await fetch("https://komgrip.co.th/coincap/assets")
          if (!response.ok) throw new Error("Failed to fetch data");

          this.Total = await response.json();
          
          this.page();

        } catch (error) {
          console.error("Error fetching data:", error);
          // document.querySelector("table tbody").innerHTML = `<tr><td colspan="6">Error loading data</td></tr>`;
        }
      },

    // ฟังก์ชันสำหรับดึงข้อมูลจาก API และเพิ่มลงในตาราง
    async page() {
      const tableBody = document.querySelector("table tbody");

      const start = (this.currentPage - 1) * this.itemsPerPage;
      const end = start + this.itemsPerPage;
      const pageData = this.Total.data.slice(start, end);
  
      tableBody.innerHTML = "";
  
      pageData.forEach((item, index) => {
        const row = document.createElement("tr");
        
        const price = parseFloat(item.priceUsd);
        const change = parseFloat(item.changePercent24Hr);
        const supply = parseFloat(item.supply);
        const maxSupply = parseFloat(item.maxSupply);

        const change_show = change < 0 ? "text-danger" : "text-success";

        row.innerHTML = `
          <td class="text-center opacity-7">${(index + 1) + start}.</td>
          <td class="opacity-7">${item.name}</td>
          <td class="text-center opacity-7">${item.symbol}</td>
          <td class="text-right opacity-7">${isNaN(supply) ? "NO LIMIT" : supply.toLocaleString()} / ${isNaN(maxSupply) ? "NO LIMIT" : maxSupply.toLocaleString()}</td>
          <td class="text-right opacity-7">$${price.toFixed(2)}</td>
          <td class="text-center text-danger opacity-7" v-if="change <= 0">
            <span class="${isNaN(change) ? '' : change_show}"> ${change.toFixed(2)}%</span>
          </td>
        `;
        tableBody.appendChild(row);
      });
    },

    // จัดการปุ่ม Previous
    prevBtn() {
      if (this.currentPage > 1) {
        this.currentPage--;
        console.log('-cur',this.currentPage)
        this.page();
      }
    },

    // จัดการปุ่ม Next
    nextBtn() {
      const totalPages = Math.ceil(this.Total.data.length / this.itemsPerPage);
      if (this.currentPage < totalPages) {
        this.currentPage++;
        this.page();
      }
    }

    }
  }
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#menu {
  color: grey;
  background-color: white;
  font-size: 18px;
  height: 60px;
}
#menu active {
  background-color: gray;
}
.card-body {
  padding: 10px;
  box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.1); /* เพิ่มเงาเล็กน้อย */
  border-top: 1px solid #ddd; /* เส้นขอบด้านบน */
  text-align: center;
  border-radius: 10px;
}
.sidenav-footer {
  position: fixed; /* ตำแหน่งคงที่ที่ด้านล่าง */
  box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.1); /* เพิ่มเงาเล็กน้อย */
  border-top: 1px solid #ddd; /* เส้นขอบด้านบน */
  text-align: center;
  border-radius: 10px;
}
</style>



