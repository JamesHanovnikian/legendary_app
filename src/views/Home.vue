<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <div class="container">
      <div class="row"> 
          <div v-for="product in products" class="col-lg-4 col-md-12">
          <div class="card">
            <div class="card-body">
              <div class="text-center">
                <h5 class="card-title">  {{ product["name"] }} </h5>
                <div v-show="product.price != 0">
                  <span class="price">
                  ${{ product["price"] }} 
                </span> /month
                </div>
                
                <br><br> 
                <p class="card-text">  {{ product["description"] }} </p>
              </div>
              <br>
              <ul class="list-group list-group-flush">
                <li class="list-group-item">  {{ product["bulletOne"] }} </li>
                <li class="list-group-item">  {{ product["bulletTwo"] }}  </li>
                <li class="list-group-item">  {{ product["bulletThree"] }}  </li>
              </ul>
              <div class="card-body text-center">
                <button v-on:click="showSignup()" class="btn btn-primary btn-lg" style="border-radius:30px"> Sign Up</button>
            </div>
            </div>
          </div>
        </div>


        </div>

         <dialog id="signup-details">
           <form>
  <div class="form-group">
    <label for="exampleInputEmail1">Email address</label>
    <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Enter email">
    <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
  </div>
  <div class="form-group">
    <label for="exampleInputPassword1">Password</label>
    <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
  </div>
  <div class="form-check">
    <input type="checkbox" class="form-check-input" id="exampleCheck1">
    <label class="form-check-label" for="exampleCheck1">Check me out</label>
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
  <button> Close </button>
</form>
         
        </dialog>
      </div>
    
      
    
    </div>
  </div>
</template>

<style>
form {
  padding: 75px;
}
body {
  background-color: rgb(54, 54, 54);
}

h1 {
  padding: 25px;
  color: #fff;
  font-weight: 600;
}

dialog {
  border-radius: 3rem;
}

.card-title {
  font-size: 1.75rem;
}
.price {
  font-size: 2.5rem;
}

* {
  font-family: "Nunito";
}
.row {
  display: flex;
}

.flex-container {
  display: flex;
  flex-direction: column;
}

.btn {
  width: 100%;
}

.card {
  border-radius: 4rem;
  border: none;
  padding: 10px 50px;
}

.card-text {
  font-size: 1.2rem;
}

.card:hover {
  transform: scale(1.02, 1.02);
  box-shadow: 0 1rem 3rem rgba(0, 0, 0, 0.75) !important;
  will-change: transform;
  backface-visibility: hidden;
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
