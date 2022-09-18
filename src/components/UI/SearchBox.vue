<template>
  <div class="card">
    <h5 class="card-header">Search City</h5>
    <div class="card-body">
      <input />
      <button href="#" class="btn btn-primary">Search</button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    searchCity() {
      var APIKey = "205e65f3bbbf65a0b6de249409614a50";
    //   let city = "Lakeville";
      var queryURL = `https://api.openweathermap.org/data/2.5/weather?lat=44.34&lon=10.99&appid=${APIKey}`;

      fetch(
        queryURL
      ).then((response) => {
          if (response.ok) {
            return response.json();
          }
        })
        .then((data) => {
            console.log("data", data);
        //   const results = [];
        //   for (const id in data) {
        //     results.push({ id: id, password: data[id].password });
        //   }
        //   this.results = results;
        })
        .catch((error) => {
          console.log('ERROR:', error);
        });
    }

  },
  mounted() {
    this.searchCity();
  },
};
</script>
