<template>
<div id="misc">
  <section id="links">
    <ul>
      <li><nuxt-link to="asteroids">ASTEROIDS, METEORS & COMETS</nuxt-link></li>
      <li><nuxt-link to="blackholes">BLACK HOLES</nuxt-link></li>
      <li><nuxt-link to="galaxies">GALAXIES</nuxt-link></li>
      <li><nuxt-link to="gravity">GRAVITY</nuxt-link></li>
      <li><nuxt-link to="nebulas">NEBULA</nuxt-link></li>
      <li><nuxt-link to="solarflares">SOLAR FLARES & RADIATION</nuxt-link></li>
    </ul>
  </section>
  <div class="content">
    <section id="lead">
        <h5 id="intro">Here we look at other miscellaneous topics that have not been discussed in detail so far, like asteroids, black holes, comets, gravity, nebula, solar flares and solar radiation.<br>
        <span class="highlight_text">Click on a link to continue..</span>
        </h5>
    </section>
    <section id="info">
      <nuxt-child to="asteroids"/>
    </section>
  </div>
</div>
</template>

<style scoped>
/* DEFAULT MOBILE VIEW */
#misc {
  display: flex;
  color: #c0c0c0;
  flex-flow: column;
  height:100%;
}

#links {
  display: flex;
  flex-wrap: wrap;
  width: 100%;
}

#links ul {
  padding: 0;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}

#links ul li {
  display: flex;
  flex-wrap: wrap;
  margin:auto;
  margin-bottom:25px;
  padding: 8px;
  font-size: 1rem;
  align-items: center;
  justify-content: center;
}

#lead {
  padding: 5px;
  font-size: 1rem;
  text-align: center;
}

span {
  display: none;
}

/* MEDIUM UP VIEW */
@media screen and (min-width: 991px) {
  #misc {
    display: grid;
    grid-template-columns: 300px auto;
    grid-template-rows: auto;
    padding: 0 30px;
    margin-right: 20px;
  }

  #links {
    grid-column: 1 / 2;
    grid-row: 1 / -1;
    padding-left: 30px;
    justify-items: start;
    align-items: start;
    position: fixed;

  }

  #lead {
    margin-bottom: 15px;
  }

  #links ul {
    margin-top: 0;
    flex-flow: column;
    align-items: center;
    justify-content: flex-start;
  }

  #links ul li {
    list-style: none;
    margin:0;
    padding: 10px;
    font-size: 1rem;
  }

  #intro {
    text-align: center;
  }

  .content {
    grid-column: 2 / 3;
    grid-row: 1 / -1;
    padding: 0 50px;
  }

  #lead {
    margin-bottom: 30px;
  }
}
</style>

