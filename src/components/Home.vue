<template>
  <div class="container">
    <div class="title">
      <h1>Pomodoro 🍅</h1>
    </div>
    <div class="timer">
      <svg
        width="163"
        height="165"
        viewBox="-8 -8 184 188"
        fill="none"
        id="first-segment"
      >
        <path
          stroke="#E9D2B1"
          stroke-width="15"
          stroke-linecap="round"
          d="M165.16,163.38A172,172,0,0,0,0,0"
        />
        <path
          id="top-right"
          stroke="#F85959"
          stroke-width="15"
          stroke-linecap="round"
          d="M165.16,163.38A172,172,0,0,0,0,0"
        />
      </svg>
      <svg
        width="163"
        height="165"
        viewBox="-8 -8 184 188"
        fill="none"
        id="second-segment"
      >
        <path
          stroke="#E9D2B1"
          stroke-width="15"
          stroke-linecap="round"
          d="M0,163.34A172,172,0,0,0,164.44,0"
        />
        <path
          id="bottom-right"
          stroke="#F85959"
          stroke-width="15"
          stroke-linecap="round"
          d="M0,163.34A172,172,0,0,0,164.44,0"
        />
      </svg>
      <svg
        width="163"
        height="165"
        viewBox="-8 -8 184 188"
        fill="none"
        id="third-segment"
      >
        <path
          stroke="#E9D2B1"
          stroke-width="15"
          stroke-linecap="round"
          d="M0,0A172,172,0,0,0,165.16,162.61"
        />
        <path
          id="bottom-left"
          stroke="#F85959"
          stroke-width="15"
          stroke-linecap="round"
          d="M0,0A172,172,0,0,0,165.16,162.61"
        />
      </svg>
      <svg
        width="163"
        height="165"
        viewBox="-8 -8 184 188"
        fill="none"
        id="fourth-segment"
      >
        <path
          stroke="#E9D2B1"
          stroke-width="15"
          stroke-linecap="round"
          d="M160.17,0A172,172,0,0,0,0,161.51"
        />
        <path
          id="top-left"
          stroke="#F85959"
          stroke-width="15"
          stroke-linecap="round"
          d="M160.17,0A172,172,0,0,0,0,161.51"
        />
      </svg>
      <h2>{{pomodoroDuration}}</h2>
    </div>
    <button>Start</button>
  </div>
</template>

<script>
import ProgressBar from 'progressbar.js';

export default {
  name: "HomeVue",
  data:()=>{
    const  pomodoroDuration= 25;
        return {
           
            currentTimeInSeconds:pomodoroDuration *60
        }
  },
  mounted:function(){
    const topRight=new ProgressBar.Path('#top-right',{
        easing:'linear',
        duration: 1 *60 *1000,

    });
    topRight.set(1);
    topRight.animate(0);
  },

  computed:{
    timeDisplay(){
        const minutes=parseInt(this.currentTimeInSeconds/60);


    }
  }
};
</script>

<style>
.container {
  height: 100vh;
  display: flex;
  align-items: center;
  flex-direction: column;
}

.title {
  margin-top: 50px;
}

h1 {
  font-size: 64px;
  color: #c44747;
  margin-right: 10px;
}

.timer {
  position: relative;
  margin-top: 100px;
  width: 330px;
  height: 330px;
}

#first-segment{
    position: absolute;
    top: 0;
    right: 0;
}
#second-segment{
    position: absolute;
    bottom: 0;
    right: 0;
}

#third-segment{
    position: absolute;
    bottom: 0;
    left: 0;
}


#fourth-segment{
    position: absolute;
    top: 0;
    left: 0;
}

h2{
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%,-50%);
    font-size: 64px;
    color:#f85959;
}


button {
  margin-top: 50px;
  width: 200px;
  height: 60px;
  background: #f85959;
  border-radius: 20px;
  border: none;
  cursor: pointer;
  font-size: 36px;
  line-height: 45px;
  text-align: center;
  color: #fff8ec;
}

button:focus {
  outline: none;
}

</style>
