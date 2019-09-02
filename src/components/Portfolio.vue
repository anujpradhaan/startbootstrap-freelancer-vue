<template>
  <div>
    <section class="bg-light page-section" id="portfolio">
      <div class="container">
        <div class="row">
          <div class="col-lg-12 text-center">
            <h2 class="section-heading text-uppercase">Portfolio</h2>
            <h3 class="section-subheading text-muted">Lorem ipsum dolor sit amet consectetur.</h3>
          </div>
        </div>
        <div class="row">
          <div class="col-md-4 col-sm-6 portfolio-item" v-for="portfolio in portfolios" v-bind:key="portfolio.key">
            <a class="portfolio-link" data-toggle="modal" href="#portfolioModal1">
              <div class="portfolio-hover">
                <div class="portfolio-hover-content">
                  <i class="fas fa-plus fa-3x"></i>
                </div>
              </div>
              <img class="img-fluid" :src="require(`../assets/img/portfolio/${portfolio.img}`)" alt />
            </a>
            <div class="portfolio-caption">
              <h4>{{portfolio.title}}</h4>
              <p class="text-muted">{{portfolio.caption}}</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
    export default {
        name:'Portfolio',
        data: () => ({
            portfolios : [{
              img:'01-thumbnail.jpg',  
              title:'Threads',
              caption:'Illustration'
            },{
              img:'02-thumbnail.jpg',  
              title:'Explore',
              caption:'Graphic Design'
            },{
              img:'03-thumbnail.jpg',  
              title:'Finish',
              caption:'Identity'
            },{
              img:'04-thumbnail.jpg',  
              title:'Lines',
              caption:'Branding'
            },{
              img:'05-thumbnail.jpg',  
              title:'Southwest',
              caption:'Website Design'
            },{
              img:'06-thumbnail.jpg',  
              title:'Window',
              caption:'Photography'
            }]
        })
    };
</script>