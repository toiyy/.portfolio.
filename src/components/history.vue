<template>
  <div id="history">
    <section class="section">
    <div class="has-text-centered">
    <span class="underline heading is-size-2 w300">History</span>
    </div>
    <div>
    <div class="timeline">
        <div v-for="(value) in history" :key="value" class="timeline__group">
            <span class="timeline__year">{{ value.year }}</span>
            <div v-for="(value) in value.events" :key="value" class="timeline__box">
                
                <div class="timeline__post">
                <div class="timeline__content">
                    <div class="columns">
                    <div class="column is-two-thirds">
                        <span class="subtitle">{{ value.name }}  {{ value.award }}</span>
                        <p class="has-text-grey">{{ value.desc }}</p>
                    </div>
                    
                    </div>
                </div>
                </div>
            </div>
        </div>
    </div>
    </div>
  </section>
  </div>
</template>

<script>
import history_data from '../data/history.json';
export default {
  data() {
    return {
      history:history_data
    }
  }
}
</script>


<style scoped>

.timeline{
  --uiTimelineMainColor: var(--timelineMainColor, rgb(194, 23, 23));
  --uiTimelineSecondaryColor: var(--timelineSecondaryColor, #fff);
  position: relative;
  width: 80%;
  margin: auto;
  padding-top: 1rem;
  padding-bottom: 1rem;
}

.timeline:before{
  content: "";
  width: 3px;
  height: 100%;
  background-color: #989999  ; /*var(--uiTimelineMainColor);*/
  position: absolute;
  top: 0;
}

.timeline__group{
  position: relative;
}

.timeline__group:not(:first-of-type){
  margin-top: 2rem;
}

.timeline__year{
  padding: .5rem 1.5rem;
  color: var(--uiTimelineSecondaryColor);
  background-color: #1ED7EF;
  position: absolute;
  left: -11px;
  top: 0;
}

.timeline__box{
  position: relative;
}

.timeline__box:not(:last-of-type){
  margin-bottom: 10px;
}

.timeline__box:before{
  content: "";
  width: 100%;
  height: 1px;
  background-color: #989999; /*var(--uiTimelineMainColor);*/
  position: absolute;
  left: 0;
  z-index: -1;
}

.timeline__date{
  min-width: 70px;
  position: absolute;
  left: -2px;
  box-sizing: border-box;
  padding: .8rem 0.5rem;
  text-align: center;
  background-color: #626567;/*var(--uiTimelineMainColor);*/
  color: var(--uiTimelineSecondaryColor);
}

.timeline__month{
  display: block;
  font-size: 1em;
  text-transform: uppercase;
  text-align: center;
}

.timeline__post{
  padding: 0.5rem 1rem;
  border-radius: 2px;
  border-left: 3px solid #989999;
  box-shadow: 0 1px 5px 0 rgba(0, 0, 0, .12), 0 2px 5px 0 rgba(0, 0, 0, .05);
  background-color: var(--uiTimelineSecondaryColor);
}

.timeline__post:hover {
  transition: 0.7s ease;
  box-shadow: 0 5px 10px 0 rgba(0,0,0,0.2);
}

@media screen and (min-width: 641px){

  .timeline:before{
    left: 30px;
  }

  .timeline__group{
    padding-top: 40px;
  }

  .timeline__box{
    padding-left: 100px;
  }

  .timeline__box:before{
    top: 50%;
    transform: translateY(-50%);  
  }  

  .timeline__date{
    top: 50%;
    width: 70px;
    margin-top: -25px;
  }
}

@media screen and (max-width: 640px){

  .timeline {
    width: 100%;
  }

  .timeline:before{
    left: 0px;
  }

  .timeline__group{
    padding-top: 50px;
  }

  .timeline__box{
    padding-left: 20px;
    padding-top: 70px;
  }

  .timeline__box:before{
    top: 150px;
  }    

  .timeline__year{
      left: 0px;
  }

  .timeline__date{
    top: 0;
    left: 0;
  }
}

</style>
