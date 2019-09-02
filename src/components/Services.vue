<template>
  <section class="page-section" id="services">
    <div class="container">
      <div class="row">
        <div class="col-lg-12 text-center">
          <h2 class="section-heading text-uppercase">Services</h2>
          <h3 class="section-subheading text-muted">Lorem ipsum dolor sit amet consectetur.</h3>
        </div>
      </div>
      <div class="row text-center">
        <div class="col-md-4" v-for="service in services" :key=service.key>
          <span class="fa-stack fa-4x">
            <i class="fas fa-circle fa-stack-2x text-primary"></i>
            <i class="fas fa-stack-1x fa-inverse" :class="service.serviceType"></i>
          </span>
          <h4 class="service-heading">{{service.name}}</h4>
          <p class="text-muted">
              {{service.description}}
          </p>
        </div>
     </div>
    </div>
  </section>
</template>

<script>
export default {
    name : 'Services',
    data: () => ({
        services:[{
            name:'E-Commerce',
            description:'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Minima maxime quam architecto quo inventore harum ex magni, dicta impedit.',
            serviceType:'fa-shopping-cart'
        },{
            name:'Responsive Design',
            description:'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Minima maxime quam architecto quo inventore harum ex magni, dicta impedit.',
            serviceType:'fa-laptop'
        },{
            name:'Web Security',
            description:'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Minima maxime quam architecto quo inventore harum ex magni, dicta impedit.',
            serviceType:'fa-lock'
        }]
    })
}
</script>