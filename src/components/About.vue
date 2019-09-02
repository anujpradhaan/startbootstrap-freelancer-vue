<template>
  <section class="page-section" id="about">
    <div class="container">
      <div class="row">
        <div class="col-lg-12 text-center">
          <h2 class="section-heading text-uppercase">About</h2>
          <h3 class="section-subheading text-muted">Lorem ipsum dolor sit amet consectetur.</h3>
        </div>
      </div>
      <div class="row">
        <div class="col-lg-12">
          <ul class="timeline">
            <li v-for="(timeline,key) in timelines" :key=key :class="{'timeline-inverted': timeline.isInverted}">
              <div class="timeline-image">
                <img class="rounded-circle img-fluid" :src="require(`../assets/img/about/${timeline.img}`)" alt />
              </div>
              <div class="timeline-panel">
                <div class="timeline-heading">
                  <h4>{{timeline.heading}}</h4>
                  <h4 class="subheading">{{timeline.subHeading}}</h4>
                </div>
                <div class="timeline-body">
                  <p class="text-muted">
                      {{timeline.body}}
                </p>
                </div>
              </div>
            </li>
            <li class="timeline-inverted">
              <div class="timeline-image">
                <h4>
                  Be Part
                  <br />Of Our
                  <br />Story!
                </h4>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
    name:'About',
    data:() => ({
        timelines : [{
            img:'1.jpg',
            heading:'2009-2011',
            subHeading:'Our Humble Beginnings',
            body:'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sunt ut voluptatum eius sapiente, totam reiciendis temporibus qui quibusdam, recusandae sit vero unde, sed, incidunt et ea quo dolore laudantium consectetur!',
            isInverted:false
        },
        {
            img:'2.jpg',
            heading:'March 2011',
            subHeading:'An Agency is Born',
            body:'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sunt ut voluptatum eius sapiente, totam reiciendis temporibus qui quibusdam, recusandae sit vero unde, sed, incidunt et ea quo dolore laudantium consectetur!',
            isInverted:true
        },
        {
            img:'3.jpg',
            heading:'December 2012',
            subHeading:'Transition to Full Service',
            body:'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sunt ut voluptatum eius sapiente, totam reiciendis temporibus qui quibusdam, recusandae sit vero unde, sed, incidunt et ea quo dolore laudantium consectetur!',
            isInverted:false
        },
        {
            img:'4.jpg',
            heading:'July 2014',
            subHeading:'hase Two Expansion',
            body:'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sunt ut voluptatum eius sapiente, totam reiciendis temporibus qui quibusdam, recusandae sit vero unde, sed, incidunt et ea quo dolore laudantium consectetur!',
            isInverted:true
        }]
    })
}
</script>