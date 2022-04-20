<template>

  <body class="no-sidebar is-preload">
  <div id="page-wrapper">

    <!-- Header Wrapper -->
    <div id="header-wrapper">
      <div class="container">

        <!-- Header -->
        <header id="header">
          <div class="inner">

            <!-- Logo -->
            <h1><router-link :to="{ name: 'home' }" id="logo">Magic</router-link></h1>

            <!-- Nav -->
            <nav id="nav">
              <ul>
                <li ><router-link :to="{ name: 'home' }">Home</router-link></li>
                <li class="current_page_item"><router-link :to="{ name: 'collection' }">Ma Collection</router-link></li>
              </ul>
            </nav>

          </div>
        </header>

      </div>
    </div>

    <!-- Main Wrapper -->
    <div id="main-wrapper">
      <div class="wrapper style2">
        <div class="inner">
          <div class="container">
            <div id="content">

              <!-- Content -->

              <article>
                <header class="major">
                  <h2>Ma Collection</h2>
                </header>
                <div class='card-list'>
                  <div class='card-title'><b>#1</b> Card Title</div>
                  <div class='card-action'><a href='#'>👀</a></div>
                </div>
                <div class='card-list'>
                  <div class='card-title'><b>#2</b> Card Title</div>
                  <div class='card-action'><a href='#'>👀</a></div>
                </div>

              </article>

            </div>
          </div>
        </div>
      </div>

    </div>

    <!-- Footer Wrapper -->
    <div id="footer-wrapper">
      <footer id="footer" class="container">
        <div class="col-12">
          <div id="copyright">
            <ul class="menu">
              <li>&copy; Untitled. All rights reserved</li><li>Design: <a href="http://html5up.net">HTML5 UP</a></li>
            </ul>
          </div>
        </div>
    </div>
    </footer>
  </div>

  </div>


  </body>
</template>


<script>

  import axios from 'axios'
  const allCards = "https://api.magicthegathering.io/v1/cards"

  export default {
    name: 'MagicCollection',
    data:()=>({
    cards: []
    }),
    async created(){
    const cards = await axios.get(allCards)
    this.cards  = cards.data
    }
  }
</script>
