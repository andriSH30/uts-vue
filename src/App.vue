<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->

    <nav class="navbar navbar-expand-lg navbar-light">
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item active">
            <a class="nav-link nav-kanan" href="#">Home <span class="sr-only">(current)</span></a>
          </li>
          <li class="nav-item active">
            <a class="nav-link nav-kanan" href="#">Shop</a>
          </li>
          <li class="nav-item active">
            <a class="nav-link nav-kanan" href="#">Features</a>
          </li>
          <li class="nav-item active">
            <a class="nav-link nav-kanan" href="#">Pages</a>
          </li>
          <li class="nav-item active">
            <a class="nav-link nav-kanan" href="#">Blog</a>
          </li>
        </ul>
        <ul class="navbar-nav ml-auto mr-auto">
          <li class="nav-item active">
              <a href="" class="nav-link brand">Sober</a>
          </li>
        </ul>
        <ul class="navbar-nav ml-auto">
            <li class="nav-item active">
                <a class="nav-link icon" href="#"><b-icon icon="search"></b-icon></a>
            </li>
            <li class="nav-item active">
                <a class="nav-link icon" href="#"><b-icon icon="person"></b-icon></a>
            </li>
            <li class="nav-item active">
                <a class="nav-link icon" href="#"><b-icon icon="bucket"></b-icon></a>
            </li>
        </ul>
      </div>
    </nav>

  <div class="jumbotron jumbotron-fluid">
      <div class="wrapper-satu">
        <h1>New Arrivals</h1>
        <br>
        <br>
        <a href="">Woman Collection</a>
        <a href="">Man Collection</a>
      </div>
  </div>

  <div class="wrapper-dua">
    <div class="header">
      <b-tabs content-class="mt-3" class="tab-link" justified>
        <b-tab title="Best Seller" active>
          <div class="isi">
            <div v-for="(bestSeller) in bestSellers" :key="bestSeller.no" class="card" style="width: 18rem;">
              <img src="./assets/gambar1.jpg" class="card-img-top" alt="">
              <div class="card-body">
                <h5 class="card-title">{{ bestSeller.nama }}</h5>
                <p class="card-text">{{ bestSeller.harga}} / Pcs</p>
                <p class="card-text">Ready {{ bestSeller.stok}} Pcs</p>
                <a href="#" class="btn btn-primary">Detail</a>
              </div>
            </div>
          </div>

          <b-button variant="dark">Load More</b-button>
        </b-tab>

        <b-tab title="New Products" class="tab-link">
            <div class="isi">
              <div v-for="(newProduct) in newProducts" :key="newProduct.no" class="card" style="width: 18rem;">
                <img src="./assets/gambar1.jpg" class="card-img-top" alt="">
                <div class="card-body">
                  <h5 class="card-title">{{newProduct.nama}}</h5>
                  <p class="card-text">{{newProduct.harga}} / Pcs</p>
                  <p class="card-text">Ready {{newProduct.stok}} Pcs</p>
                  <a href="#" class="btn btn-primary">Detail</a>
                </div>
              </div>
            </div>
            <b-button variant="dark">Load More</b-button>
        </b-tab>
      </b-tabs>
    </div>
    <br>
    <hr>
  </div>


  <div class="wrapper-tiga">
    <div class="header">
      <h3>Newsletter</h3>
    </div>
    <div class="sub-header">
      <p>Get timely updates from your favorite products</p>
    </div>
    <div class="input">
      <b-form-input v-model="text" class="email" placeholder="Enter your email address"></b-form-input>
      <a type="button" href="" class="subscribe">Subscribe</a>
    </div>
  </div>
  <hr>

  <div class="footer">
    <nav class="navbar navbar-expand-lg navbar-light">
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link footer-link" href="#">@2016 Saber</a>
          </li>
          <li class="nav-item">
            <a class="nav-link footer-link" href="#">Blog</a>
          </li>
          <li class="nav-item">
            <a class="nav-link footer-link" href="#">FAQs</a>
          </li>
          <li class="nav-item">
            <a class="nav-link footer-link" href="#">Contact us</a>
          </li>
        </ul>

        <ul class="navbar-nav ml-auto">
          <li class="nav-item"><a href=""><i class="fab fa-twitter"></i></a></li>
          <li class="nav-item"><a href=""><i class="fab fa-facebook-f"></i></a></li>
          <li class="nav-item"><a href=""><i class="fab fa-instagram"></i></a></li>
          <li class="nav-item"><a href=""><i class="fab fa-pinterest"></i></a></li>
          <li class="nav-item"><a href=""><i class="fab fa-google-plus-g"></i></a></li>
        </ul>
      </div>
    </nav>
  </div>

  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    
  },
  data(){
    return{
      bestSellers: [
        {
          no: '1',
          nama: 'Best Seller 1',
          harga: 'Rp 98.000',
          stok: '120'
        },
        {
          no: '2',
          nama: 'Best Seller 2',
          harga: 'Rp 220.000',
          stok: '50'
        },
        {
          no: '3',
          nama: 'Best Seller 3',
          harga: 'Rp 53.500',
          stok: '276'
        },
        {
          no: '4',
          nama: 'Best Seller 4',
          harga: 'Rp 470.000',
          stok: '59'
        },
        {
          no: '5',
          nama: 'Best Seller 5',
          harga: 'Rp 120.000',
          stok: '88'
        },
        {
          no: '6',
          nama: 'Best Seller 6',
          harga: 'Rp 268.000',
          stok: '310'
        },
        {
          no: '7',
          nama: 'Best Seller 7',
          harga: 'Rp 350.000',
          stok: '100'
        },
        {
          no: '8',
          nama: 'Best Seller 8',
          harga: 'Rp 415.000',
          stok: '30'
        },
        {
          no: '9',
          nama: 'Best Seller 9',
          harga: 'Rp 220.000',
          stok: '210'
        },
        {
          no: '10',
          nama: 'Best Seller 10',
          harga: 'Rp 70.000',
          stok: '120'
        },
        {
          no: '11',
          nama: 'Best Seller 11',
          harga: 'Rp 78.000',
          stok: '31'
        },
        {
          no: '12',
          nama: 'Best Seller 12',
          harga: 'Rp 58.000',
          stok: '47'
        },
      ],
      newProducts: [
        {
          no: '1',
          nama: 'New Product 1',
          harga: 'Rp 98.000',
          stok: '120'
        },
        {
          no: '2',
          nama: 'New Product 2',
          harga: 'Rp 220.000',
          stok: '50'
        },
        {
          no: '3',
          nama: 'New Product 3',
          harga: 'Rp 53.500',
          stok: '276'
        },
        {
          no: '4',
          nama: 'New Product 4',
          harga: 'Rp 470.000',
          stok: '59'
        },
        {
          no: '5',
          nama: 'New Product 5',
          harga: 'Rp 120.000',
          stok: '88'
        },
        {
          no: '6',
          nama: 'New Product 6',
          harga: 'Rp 268.000',
          stok: '310'
        },
        {
          no: '7',
          nama: 'New Product 7',
          harga: 'Rp 350.000',
          stok: '100'
        },
        {
          no: '8',
          nama: 'New Product 8',
          harga: 'Rp 415.000',
          stok: '30'
        },
        {
          no: '9',
          nama: 'New Product 9',
          harga: 'Rp 220.000',
          stok: '210'
        },
        {
          no: '10',
          nama: 'New Product 10',
          harga: 'Rp 70.000',
          stok: '120'
        }
      ]
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
  color: black;
  font-variant: small-caps;
  box-sizing: border-box;
}

  .jumbotron{
        background-image: url(./assets/gambar1.jpg);
        background-size: cover;
        height: 573px;
    
        
    }

.jumbotron .wrapper-satu{
  margin-top: 250px;
  
}

.jumbotron .wrapper-satu h1{
  letter-spacing: 20px;
}

.jumbotron .wrapper-satu a{
  letter-spacing: 3px;
  color: black;
  font-weight: 600;
  margin: 20px;
}

.jumbotron .wrapper-satu a:hover{
  text-decoration: none;
  border-bottom: 2px solid black;
}s

.wrapper-dua .header .tab-link{
  text-decoration: none;
  color: black !important;
}

.wrapper-dua .header .isi{
  width: 100%;
  margin: 10px auto;
  padding: 10px;
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
}

.wrapper-dua .header .isi .card{
  width: 45% !important;
  margin: 5px;
}

.wrapper-dua .header .isi .card .card-body p{
  color: black;
  font-size: 15px;
}

.wrapper-tiga{
  width: 100%;
  height: 200px;
  padding-left: 10px;
  padding-right: 10px;
  font-variant: normal;
}

.wrapper-tiga .header{
  padding: 20px;
  letter-spacing: 1px !important;
}

.wrapper-tiga .sub-header{
  margin-top: -10px;
  letter-spacing: 0.1;
  color: dimgray;
  word-spacing: 2px;
}

.wrapper-tiga .input{
  padding-left: 10px;
  padding-right: 10px;
  padding-top: 30px;
  display: flex;
}

.wrapper-tiga .input .email{
  width: 75%;
  margin: 15px;
  border-top-color: white !important;
  border-left-color: white !important;
  border-right-color: white !important;
}

.wrapper-tiga .input .subscribe{
  width: 15%;
  margin: 15px;
  color: black;
  font-weight: 700;
  border-bottom: 1px solid lightgray;
  border-top-color: white !important;
  border-left-color: white !important;
  border-right-color: white !important;
}

.wrapper-tiga .input .subscribe:hover{
  text-decoration: none;
}

.footer{
  font-size: 13px;
  margin-top: -20px;
}

.footer ul li .footer-link{
  margin-right: 20px;
}

.footer ul li .footer-link:hover{
  color: black;
}

.footer ul li .fab{
  margin-left: 30px;
  color: dimgray;
}

.footer ul li .fab:hover{
  color: black;
}

/* TAMPILAN RESPONSIVE */
@media(min-width: 600px){

.jumbotron{
        background-image: url(./assets/gambar1.jpg);
        background-size: cover;
        height: 673px;
        margin-top: -75px;
        display: flex;
        justify-content: center;
    }

.navbar{
  padding-left: 20px;
  padding-right: 30px;
  font-family: 'Patua One', cursive;
  color: black;
  position: sticky;
}

.navbar ul li .nav-kanan{
  margin-left: 20px;
}

.navbar ul li .nav-kanan:hover{
  border-bottom: 2px solid black;
  margin-bottom: -3px;
}

.navbar ul li .icon{
  margin-left: 1px;
  margin-right: 1px;
}

.navbar ul li .icon:hover{
  border-bottom: 2px solid black;
  margin-bottom: -3px;
}

.navbar ul li .brand{
  letter-spacing: 5px;
  font-size: 20px;
  font-family: 'Orbitron', sans-serif;
  font-weight: 1000;
}

.wrapper-dua .header .isi{
  width: 100%;
  margin: 5px auto;
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
  padding: 10px;
}

.wrapper-dua .header .isi .card{
  width: 18% !important;
  margin: 10px;
}

.wrapper-tiga{
  width: 100%;
  height: 400px;
  padding-left: 200px;
  padding-right: 200px;
  font-variant: normal;
}

.wrapper-tiga .header{
  padding: 50px;
  letter-spacing: 1px !important;
}

.wrapper-tiga .sub-header{
  margin-top: -30px;
  letter-spacing: 0.1;
  color: dimgray;
  word-spacing: 2px;
}

.wrapper-tiga .input{
  padding-left: 100px;
  padding-right: 100px;
  padding-top: 50px;
  display: flex;
}

.wrapper-tiga .input .email{
  width: 75%;
  margin: 15px;
  border-top-color: white !important;
  border-left-color: white !important;
  border-right-color: white !important;
}

.wrapper-tiga .input .subscribe{
  width: 15%;
  margin: 15px;
  color: black;
  font-weight: 700;
  border-bottom: 1px solid lightgray;
  border-top-color: white !important;
  border-left-color: white !important;
  border-right-color: white !important;
}

.wrapper-tiga .input .subscribe:hover{
  text-decoration: none;
}

}

</style>
