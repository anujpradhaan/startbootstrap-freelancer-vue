<template>
    <section class="py-5">
      <div class="container">
        <div class="row">
          <div class="col-md-3 col-sm-6" v-for="(client,key) in clients" :key="key">
            <a href="#">
              <img class="img-fluid d-block mx-auto" :src="require(`../assets/img/logos/${client.logo}`)" alt />
            </a>
          </div>
        </div>
      </div>
    </section>
</template>

<script>
    export default {
        name:'Clients',
        data:() => ({
            clients : [{
                logo:'envato.jpg' 
            },
            {
                logo:'designmodo.jpg'
            },
            {
                logo:'themeforest.jpg'
            },
            {
                logo:'creative-market.jpg'    
            }]
        })            
    }
</script>