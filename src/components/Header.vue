<template>
  <nav class="navbar navbar-default">
    <div class="container-fluid">
    <!-- Brand and toggle get grouped for better mobile display -->
        <div class="navbar-header">
            <router-link to='/' class="navbar-brand">Chill Trading</a></router-link>
        </div>

    <!-- Collect the nav links, forms, and other content for toggling -->
          <div class="collapse navbar-collapse">
              <ul class="nav navbar-nav">

                  <router-link to="/portfolio" activeClass="active" tag="li"><a>PORTFOLIO</a></router-link>

                  <router-link to="/stocks" activeClass="active" tag="li"><a>STOCKS</a></router-link>
              </ul>
              <strong class="navbar-text navbar-right">Funds: {{ funds }}</strong>

              <ul class="nav navbar-nav navbar-right">
                  <li><a href="#">End Day</a></li>
                  <li class="dropdown">
                      <a 
                            class="nav-link dropdown-toggle" 
                            href="#" 
                            id="navbarDropdown" 
                            role="button" data-toggle="dropdown" 
                            aria-haspopup="true" 
                            aria-expanded="false">
                        Save & Load
                      </a>
                      <div class="dropdown-menu">
                        <li><a href="#">Save</a></li>
                        <li><a href="#">Load</a></li>
                      </div>
                  </li>
              </ul>
        </div><!-- /.navbar-collapse -->
  </div><!-- /.container-fluid -->
</nav>
</template>

<script>
  export default {
    computed: {
      funds() {
        return this.$store.getters.funds
      }
    }
  }
</script>
