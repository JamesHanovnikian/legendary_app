<template>
  <div class="home">
    <div class="container">
    <main class="signup-grid">
      <div class="header">
        <h1> Sign Up</h1>
      </div>
      <div class="registration-form">
        <div class="card">
          <div class="card-body">
            <form>
             <div class="form-group input-group-sm">
                <label for="exampleInputEmail1">Username</label>
                <input type="text" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Username">
              </div>
              <div class="form-group input-group-sm ">
                <label for="exampleInputEmail1">Email address</label>
                <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Enter email">
                <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
              </div>
              <div class="form-group input-group-sm ">
                <label class="justify-content-start" for="exampleInputPassword1">Password</label>
                <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
              </div>
              <div class="row">
                <div class="col-6">
                  <div class="form-group input-group-sm ">
                    <label for="exampleInputPassword1">First Name</label>
                    <input type="text" class="form-control" id="exampleInputPassword1" placeholder="First Name">
                  </div>
                </div>
                <div class="col-6">
                  <div class="form-group input-group-sm ">
                    <label for="exampleInputPassword1"> Last Name</label>
                    <input type="text" class="form-control" id="exampleInputPassword1" placeholder="Last Name">
                  </div>
                </div>
              </div>
              <div class="row">
                <div class="col-6 ">
                  <div class="form-group input-group-sm ">
                    <label for="exampleInputPassword1"> Address </label>
                    <input type="text" class="form-control" id="exampleInputPassword1" placeholder="Address">
                  </div>
                </div>
                <div class="col-3">
                  <div class="form-group input-group-sm ">
                    <label for="exampleInputPassword1"> State </label>
                    <input type="text" class="form-control" id="exampleInputPassword1" placeholder="Last Name">
                  </div>
                </div>
                <div class="col-3">
                  <div class="form-group input-group-sm ">
                    <label class="control-label"> Country </label>
                    <input type="dropdown" class="form-control" id="exampleInputPassword1" placeholder="">
                  </div>
                </div>
              </div>
              <div class="form-check">
                <input type="checkbox" class="form-check-input" id="exampleCheck1">
                <label class="form-check-label" for="exampleCheck1">Check me out </label>
              </div>
              <button type="submit" class="btn btn-primary">Submit</button>
              <br> <br> 
              <button class= "btn btn-primary"> Close </button>
            </form>
          </div>
        </div>
      </div>
      <div class="subscription-options">
        <div v-for="product in products">
          <div class="product-box">
            <h3 class="title"> {{ product.name }}</h3>
            <hr>
             <i class="fas fa-baseball-ball fa-2x "></i>
            <p> <span class="price"> $ {{ product.price }}</span> /month </p>
            <p> {{ product.description }} </p>
            <button class="btn btn-primary"> Select </button>
          </div>
        </div>
      </div>



<!-- <div class="card">
            <div class="card-body">
              <div class="text-center">
                <h5 class="card-title">  {{ product["name"] }} </h5>
                <p> <i class="fas fa-baseball-ball fa-2x"></i>  </p>
                <div v-show="product.price != 0">
                  <span class="price">
                  ${{ product["price"] }} 
                </span> /month
                </div>
                <p class="card-text">  {{ product["description"] }} </p>
              </div>
              <br>
              <div class="card-body text-center">
                <button v-on:click="showSignup()" class="btn btn-primary" style="border-radius:30px"> Select </button>
            </div>
            </div>
          </div> -->

    </main>
    </div>
    
          
          
          
          
          
          
          
          
          


      
           


    
      
    
    
  </div>
</template>

<style>
.signup-grid {
  display: grid;
  gap: 1.5rem;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: 100px;
  height: 100vh;
}

.header {
  grid-column-start: 1;
  grid-column-end: 4;
  grid-row-start: 1;
  grid-row-end: 1;
}

.registration-form {
  grid-column-start: 1;
  grid-column-end: 3;
  grid-row-start: 2;
  grid-row-end: 4;
}

.registration-form .card {
  border: 1.5px solid rgb(146, 146, 146, 0.8);
}

.registration-form .form-control {
  border-radius: 8px;
  font-size: 10px;
}

.registration-form label {
  font-size: 12px;
}

.subscription-options {
  grid-column-start: 3;
  grid-column-end: 5;
  grid-row-start: 1;
  color: #fff;
}

.subscription-options .title {
  text-transform: uppercase;
}

.subscription-options .product-box {
  border-radius: 3rem;
  border: 1.5px solid rgb(146, 146, 146, 0.8);
  width: 65%;
  padding: 4.5px;
  margin: 15px;
  background-color: #fff;
  color: #333;
}

.subscription-options label {
  font-size: 8px;
}

form {
  padding: 10px;
  width: 75%;
}

form .form-group input {
  border-radius: 3rem;
}
body {
  background-color: rgb(54, 54, 54);
}

h1 {
  color: #fff;
  font-weight: 600;
}

h3 {
  font-size: 18px;
}

.card-title {
  font-size: 1.2rem;
}
.price {
  font-size: 1.25rem;
}

.subscription-options .card {
  font-size: 11px;
}

* {
  font-family: "Nunito";
}

.btn {
  width: 30%;
  border-radius: 3rem;
}

.card {
  border-radius: 2.5rem;
  border: none;
}

.card-text {
}

.subscription-options .product-box:hover {
  transform: scale(1.02, 1.02);
  box-shadow: 0 1rem 3rem rgba(0, 0, 0, 0.75) !important;
  will-change: transform;
  backface-visibility: hidden;
  background-color: rgba(226, 221, 221, 0.8);
}

.card:hover::after {
  opacity: 1;
}

.card:hover .btn-primary {
  color: #007bff;
  background: #fff;
}
</style>

<script>
export default {
  data: function () {
    return {
      message: "Create an Account",
      products: [
        {
          name: "Trial",
          description: "Seven day trial period",
          price: "0",
          bulletOne: "Try out the service",
          bulletTwo: "Join the legendary community",
          bulletThree: "",
          subscriptionLength: "seven days",
        },
        {
          name: "Month",
          description: "Monthly subscription",
          price: 5,
          bulletOne: "Cancel at anytime",
          bulletTwo: "Join the legendary community",
          bulletThree: "",
          subscriptionLength: "month",
        },
        {
          name: "Year",
          description: "Subscribe for a year",
          price: 40,
          bulletOne: "Best value",
          bulletTwo: "Join the legendary community",
          bulletThree: "",
          subscriptionLength: "yearly",
        },
      ],
    };
  },
  created: function () {},
  methods: {
    showSignup: function () {
      console.log("hello");
      document.querySelector("#signup-details").showModal();
    },
  },
};
</script>
