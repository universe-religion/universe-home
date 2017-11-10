<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <hr id="hr-line">
    <div>
      <p>Und als ich so lange, so lange gesäumt,</p>
      <p>In fremden Landen geschwärmt und geträumt;</p>
      <p>Da ward meiner Liebsten zu lang die Zeit,</p>
      <p>Und sie nähete sich ein Hochzeitskleid,</p>
      <p>Und hat mit zärtlichen Armen umschlungen,</p>
      <p>Als Bräutgam, den dümmsten der dummen Jungen.</p>
      <p></p>
      <p>Mein Liebchen ist so schön und mild,</p>
      <p>Noch schwebt mir vor ihr süßes Bild;</p>
      <p>Die Veilchenaugen, die Rosenwänglein,</p>
      <p>Die glühen und blühen, jahraus, jahrein.</p>
      <p>Daß ich von solchem Lieb konnt weichen,</p>
      <p>War der dümmste von meinen dummen Streichen.</p>    
    </div>
    <canvas class="canvas-bg" id="star"></canvas>
  </div>
</template>

<script>
const star = require('../assets/script/star')

export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Universe Sect'
    }
  },
  beforeRouteEnter (to, from, next) {
    next(() => {
      star('#star')
      window.addEventListener('resize', function(e) {
        console.log(e)
      })
    })
  },
  beforeDestroy: function () {
    console.log
    // window.removeEventListener('resize', this.handleResize)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #4277b9;
}

#hr-line {
  height: 1px;
  width: 40vw;
  margin: auto;
  border: none;
  background-color: #fff;
}

.canvas-bg {
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
}
</style>
