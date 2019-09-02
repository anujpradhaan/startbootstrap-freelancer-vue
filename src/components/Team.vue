<template>
    <section class="bg-light page-section" id="team">
      <div class="container">
        <div class="row">
          <div class="col-lg-12 text-center">
            <h2 class="section-heading text-uppercase">Our Amazing Team</h2>
            <h3 class="section-subheading text-muted">Lorem ipsum dolor sit amet consectetur.</h3>
          </div>
        </div>
        <div class="row">
          <div class="col-sm-4" v-for="teamMember in team" :key="teamMember.key" >
            <div class="team-member">
              <img class="mx-auto rounded-circle" :src="require(`../assets/img/team/${teamMember.img}`)" alt />
              <h4>{{teamMember.name}}</h4>
              <p class="text-muted">{{teamMember.designation}}</p>
              <ul class="list-inline social-buttons">
                <li class="list-inline-item">
                  <a href="#">
                    <i class="fab fa-twitter"></i>
                  </a>
                </li>
                <li class="list-inline-item">
                  <a href="#">
                    <i class="fab fa-facebook-f"></i>
                  </a>
                </li>
                <li class="list-inline-item">
                  <a href="#">
                    <i class="fab fa-linkedin-in"></i>
                  </a>
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col-lg-8 mx-auto text-center">
            <p
              class="large text-muted"
            >Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aut eaque, laboriosam veritatis, quos non quis ad perspiciatis, totam corporis ea, alias ut unde.</p>
          </div>
        </div>
      </div>
    </section>
</template>

<script>
export default {
    name:'Team',
    data: () => ({
        team : [{
            img:'1.jpg',
            name:'Kay Garland',
            designation:'Lead Designer'
        },{
            img:'2.jpg',
            name:'Larry Parker',
            designation:'Lead Marketer'
        },{
            img:'3.jpg',
            name:'Diana Pertersen',
            designation:'Lead Developer'
          }]
    })
}
</script>