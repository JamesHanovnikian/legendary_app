<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <div v-for="product in products">
      {{ product["name"] }}
    </div>
    
    
    </div>

  </div>
</template>

<style></style>

<script>
export default {
  data: function () {
    return {
      message: "Sign Up",
      products: [
        {
          name: "trial",
          description: "seven days",
          price: 0,
          subscriptionLength: "seven days",
        },
        {
          name: "month",
          description: "subscription month by month",
          price: 5,
          subscriptionLength: "month",
        },
        {
          name: "year",
          description: "subscription by year",
          price: 40,
          subscriptionLength: "yearly",
        },
      ],
    };
  },
  created: function () {},
  methods: {},
};
</script>
