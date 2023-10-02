<template>
  <div>
    <!-- <div>{{ greet }} {{ name }}</div>
    <div v-html="channel"></div>
    <div v-html="hack"></div> -->
    <!-- <h2 v-bind:id="headingId">Heading</h2>
    <button v-bind:disabled="isDisabled">Bind</button>
    <h2 class="underline">Underlined Text</h2> -->
    <!-- <h2 v-bind:class="status">Status</h2>
    <h2 v-bind:class="isPromoted && 'promoted'">Promoted movie</h2>
    <h2 v-bind:class="isSoldOut ? 'sold-out' :'new'">SoldOut ? movie</h2>
    <h2 v-bind:class="['new','promoted']">Newly promoted movie</h2>
    <h2 v-bind:class="[isPromoted && 'promoted',isSoldOut ? 'sold-out' :'new']">Array conditional movie</h2> -->
    <!-- <h2 v-bind:class="{
      promoted: isPromoted,
      new:!isSoldOut,
      'sold-out':isSoldOut,
    }">Object conditional movie</h2> -->
    <!-- <h2
      :style="{
        color: highlightColor,
        fontSize: headerSize + 'px',
        padding: '30px',
      }"
    >
      Inline style
    </h2>
    <h2 :style="headerStyleObject">Style</h2>
    <div :style="[baseStyleObject, successStyleObject]">success</div>
    <div :style="[baseStyleObject, dangerStyleObject]">danger</div> -->
    <!-- <h2 v-if="num === 0"> The number is zero</h2>
    <h2 v-else-if="num < 0">The number is negative</h2>
    <h2 v-else-if="num > 0">The number is positive</h2>
    <h2 v-else>not a numher</h2>
    <template v-if="display">
      <h2>Daud</h2>
      <h2>Conovo technologies</h2>
      <h2>vue</h2>
    </template>
    <h2 v-show="showElement">Using v-show</h2>
    <h2 v-if="showElement">Using v-show</h2> -->
    <h2 v-for="(name, index) in names" :key="index">{{ index }} {{ name }}</h2>
    <h3 v-for="name in fullNames" :key="name.first">
      {{ name.first }} {{ name.last }}
    </h3>
    <div v-for="actor in actors" :key="actor.name">
      <h2>{{ actor.name }}</h2>
      <h3 v-for="movie in actor.movies" :key="movie">
      {{ movie }}</h3>
      <h2 v-for="(value,key,index) in myInfo" :key="value">{{ index }} {{ key }} {{ value }}</h2>
      <template v-for="name in names" :key="name">
        <h2>{{ name }}</h2>
        <hr>
      </template>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      names: ["daud", "david", "reza"],
      fullNames: [
        { first: "raza", last: "fukj" },
        { first: "david", last: "reza" },
        { first: "hey", last: "sameer" },
      ],
      actors: [
        {
          name: "Cristian Bale",
          movies: ["Batman", "The prestige"],
        },
        {
          name: "Di Caprio",
          movies: ["titanic", "inception"],
        },
      ],
      myInfo: {
        name: 'Daud',
        channel : 'CodeEvolutoin',
        course : 'Vue 3',
      }
      // num: 3,
      // display: true,
      // showElement:true,
      // greet: "Hello",
      // name: "Daud Raza",
      // channel: "<b>Conovo technologies</b>",
      // hack: `<a href="#" onclick="alert('You have been hacked!')">Win a prize</a>`,
      // headingId: "heading",
      // isDisabled: false,
      // status: "success",
      // isPromoted: true,
      // isSoldOut: true,
      // highlightColor: "orange",
      // headerSize: 50,
      // headerStyleObject: {
      //   color: "red",
      //   fontSize: "30px",
      //   padding: "20px",
      // },
      // baseStyleObject: {
      //   fontSize: "50px",
      //   padding: "20px",
      // },
      // successStyleObject: {
      //   color: "green",
      //   backgroundColor: "lightgreen",
      //   border: "1px solid green",
      //   padding: "20px",
      // },
      // dangerStyleObject: {
      //   color: "darkred",
      //   backgroundColor: "red",
      //   border: "1px solid green",
      // },
    };
  },
};
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
