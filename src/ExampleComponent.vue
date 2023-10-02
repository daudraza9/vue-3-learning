<template>
  <div>
    <h2>{{ 3+3+4 }}</h2>
    <h2>{{ 10+15+4 }}</h2>
  </div>
</template>

<script>
export default {
  name: "ExampleComponent",
  data() {
    return {
      // names: ["Bruce", "Clark","Diannand","Barry"],
    };
  },
  // methods: { 
  //   shuffle(){
  //     console.log(this.names);
  //   }
  // },
};
</script>

<style>
#ExampleComponent {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.underline {
  text-decoration: underline;
}
.promoted {
  font-style: italic;
}
.new {
  color: green;
}
.sold-out {
  color: red;
}
</style>
