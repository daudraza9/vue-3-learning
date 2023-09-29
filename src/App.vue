<template>
  <div>
    <div>{{ greet }} {{ name }}</div>
    <div v-html="channel"></div>
    <div v-html="hack"></div>
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
    <h2
      v-bind:style="{
        color: highlightColor,
        fontSize: headerSize + 'px',
        padding: '30px'
      }"
    >
      Inline style
    </h2>
    <h2 v-bind:style="headerStyleObject">Stye</h2>
    <div v-bind:style="[baseStyleObject,successStyleObject]">success</div>
    <div v-bind:style="[baseStyleObject,dangerStyleObject]">danger</div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      greet: "Hello",
      name: "Daud Raza",
      channel: "<b>Conovo technologies</b>",
      hack: `<a href="#" onclick="alert('You have been hacked!')">Win a prize</a>`,
      headingId: "heading",
      isDisabled: false,
      status: "success",
      isPromoted: true,
      isSoldOut: true,
      highlightColor: "orange",
      headerSize: 50,
      headerStyleObject: {
        color: 'red',
        fontSize: '30px',
        padding:'20px',
      },
      baseStyleObject: {
        fontSize: '50px',
        padding:'20px',
      },
      successStyleObject: {
        color: 'green',
        backgroundColor : 'lightgreen',
        border: '1px solid green',
        padding: '20px',
      },
      dangerStyleObject: {
        color: 'darkred',
        backgroundColor : 'red',
        border: '1px solid green',
      }
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
