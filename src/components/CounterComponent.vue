<template>
    <div class="container">
  <div class="row max-height align-items-center">
   <div class="col-10 mx-auto col-md-6 text-center main-container p-5">
    <h1 class="text-uppercase text-white" >counter</h1>
    <h1 id="counter" :style="{ color: getColor}">{{counter}} </h1>
    <div class="btn-container d-flex justify-content-around flex-wrap">
     <button @click="updateCounter(-1)" class="btn counterBtn prevBtn text-uppercase m-2">lower count</button>
     <button @click="updateCounter(+1)" class="btn counterBtn nextBtn text-uppercase m-2">add count</button>
    </div>
   </div>
  </div>
 </div>
</template> 

<script>
export default {
    data() {
        return {
            counter: 0
        }
    },

    methods : {
        updateCounter(num) {
            this.counter += num
        },
    },

    computed: {
       getColor() {
      let finalColor = "grey";
      if (this.counter > 0) {
        finalColor = "green";
      } else if (this.counter < 0) {
        finalColor = "red";
      }

      return finalColor;
    },
    }
}
</script>

<style scoped>

#counter {
  color: var(--mainGreen);
  font-size: 10rem;
  color: var(--mainWhite);
}
.prevBtn,
.nextBtn {
  box-shadow: 0 0.2rem 0.5rem rgba(0, 0, 0, 0.9);
  background: var(--mainBlue);
  color: var(--mainWhite);
}
.prevBtn:hover {
  background: var(--lightBlue);
}
.nextBtn:hover {
  background: var(--lightBlue);
}

#counter.positive {
  color : green
}

#counter.negative {
  color: red
}


</style>