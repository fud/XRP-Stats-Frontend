<template>
  <div id="app">
    <main role="main">
      <div class="d-flex flex-column flex-md-row align-items-center p-3 px-md-4 mb-3 bg-white border-bottom box-shadow">
        <router-link tag="h5" class="my-0 mr-md-auto font-weight-normal logo" to="/">
          XRP Stats
        </router-link>
        <nav class="my-2 my-md-0 mr-md-3">
          <router-link to="/rich-index" class="p-2 routerlink btn" active-class="btn btn-outline-primary">Your Richlist Index</router-link>
        </nav>
        <nav class="my-2 my-md-0 mr-md-3">
          <router-link to="/rich-stats" class="p-2 routerlink btn" active-class="btn btn-outline-primary">Richlist stats</router-link>
        </nav>
        <nav class="my-2 my-md-0 mr-md-3">
          <router-link to="/escrow-stats" class="p-2 routerlink btn" active-class="btn btn-outline-primary">Escrow stats</router-link>
        </nav>
      </div>
      <div class="container">
        <router-view/>
      </div>
    </main>

    <footer class="footer">
      <div class="container text-center">
        <small>
          <span class="text-muted">By <a href="https://twitter.com/WietseWind" target="_blank">@WietseWind</a></span>
          &dash;
          <span class="text-muted">Check the XRPTipBot: <a href="https://xrptipbot.com" target="_blank">xrptipbot.com</a></span>
          &dash;
          Github:
          <span class="text-muted"><a href="https://github.com/WietseWind/XRP-Stats-Frontend" target="_blank">Frontend</a></span>
          &amp;
          <span class="text-muted"><a href="https://github.com/WietseWind/XRP-Ledger-to-MongoDB" target="_blank">Backend</a></span>
        </small>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style lang="scss">
html {
  font-size: 14px;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
html {
  position: relative;
  min-height: 100%;
}
body {
  margin-bottom: 60px; /* Margin bottom by footer height */
}
@media (min-width: 768px) {
  html {
    font-size: 16px;
  }
}

.container {
  max-width: 960px;
}

.pricing-header {
  max-width: 700px;
}

.card-deck .card {
  min-width: 220px;
}

.border-top { border-top: 1px solid #e5e5e5; }
.border-bottom { border-bottom: 1px solid #e5e5e5; }

.box-shadow { box-shadow: 0 .25rem .75rem rgba(0, 0, 0, .05); }

.routerlink {
  &:not(.btn) {
    color: #343a40!important;
  }
}

.footer {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 60px; /* Set the fixed height of the footer here */
  overflow: hidden;
  line-height: 60px; /* Vertically center the text there */
  background-color: #f5f5f5;
}

.logo {
  background-image: url('assets/logo.png');
  background-repeat: no-repeat;
  background-position: top left;
  background-size: contain;
  padding: 10px;
  padding-left: 55px;
  cursor: pointer;
  &:hover {
    text-decoration: underline;
  }
}
</style>
