<template>
  <div v-on:click="testConsole()" class="aa" v-bind:style="{backgroundColor:randomColor()}">
  {{msg}}
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data() {
    return {
      color: "blue"
    };
  },
  methods: {
    randomColor() {
      return (this.color =
        "#" + ((Math.random() * 0xffffff) << 0).toString(16));
    },

    testConsole(){
      return console.log(this.msg)
    }

  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.aa {
  width: 100px;
  height: 100px;
  margin: 10px 1px 10px 1px;
  display:flex;
  justify-content: center;
  align-items:center;

}
.aa:hover{
  border: 1px solid black;
}
</style>
