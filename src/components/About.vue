<template>
  <div id="about">
    <section class="hero has-bg-img is-medium">
    <div class="overlay hero-body">
        <div class="container">
            <div class="columns is-mobile">
            <div class="column is-three-fifths is-offset-one-fifth">
            <nav class="level">

            <div class="level-item">
                <div>
                <h1 class="w300 is-size-3">
                    about me
                </h1>
                <p class="pt-50"> Birthyear ： 2004</p>
                <p class="lo">     Name : toi kawashima</p>
                <p class="li"> Living ： kanagawa</p>
                <p class="lp"> Likes ： manga, soccer</p>

                </div>
            </div>
            </nav> 
            </div>
            </div>
        </div>
    </div>
    </section>  
    
  </div>
</template>

<script>

export default {
  data() {
    return {
      
    }
  }
}
</script>

<style scoped>
@media screen and (max-width: 768px) {
  .column.is-three-fifths.is-offset-one-fifth {
    width: 100%;
    margin-left: 0;
  }
}
.padding-lr {
    padding: 10px 30px 10px 30px;
    background: #f3f3f300;
}

.has-bg-img {
    background: url("../assets/raphael-biscaldi-7RQf2X6aXXI-unsplash.jpg")center center;
    background-size:cover;
    width:110%;                              
    height:740px;  
}

.overlay {
    background-color: rgba(0, 0, 0, 0);
}


.level-item{
  font-family: "Hiragino Mincho ProN W6";
  padding-top: 20%;
  color: rgba(0, 0, 0, 0.715);
  font-size: 130%;
  padding-right: 150px;
}

.underline {
  display: inline;
  position: relative;
  overflow: hidden;
}
.underline:after {
  content: "";
  position: absolute;
  z-index: -1;
  right: 0;
  left: 150px;
  width: 0;
  bottom: -5px;
  height: 7px;
  transition-property: width;
  transition-duration: 0.3s;
  transition-timing-function: ease-out;
}
.underline:hover:after,
.underline:focus:after,
.underline:active:after {
  left: 0px;
  right: auto;
  width: 100%;
}
</style>