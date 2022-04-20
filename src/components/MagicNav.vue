<template>
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
</template>

<script>
export default {
  name: 'MagicNav'
}
</script>