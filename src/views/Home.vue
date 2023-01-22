<template>
  <div>
	  <Header />
	<main>
        <section class="hero">
          <div class="hero-content">
          <h1>MarketMystery</h1>
            <p>
              Present MarkeyMystery, the ultimate stock market simulation bot for Discord. 
              Experience the thrill of buying and selling stocks without any risk. 
              Great for beginners and experts.
            </p>
          <a href="#" class="cta-btn">Try it out now!</a>
         </div>
       </section>
        <section class="features">
            <div class="feature">
                <i class="fas fa-chart-line"></i>
                <h2>Real-time Market Data</h2>
                <p>Get real-time market data and updates to make informed decisions.</p>
            </div>
            <div class="feature">
                <i class="fas fa-users"></i>
                <h2>Community Features</h2>
                <p>Join a community of traders and investors to share insights and strategies.</p>
            </div>
            <div class="feature">
                <i class="fas fa-cog"></i>
                <h2>Customizable Settings</h2>
                <p>Customize the bot's settings to fit your trading style and preferences.</p>
            </div>
        </section>
    </main>
    <footer>
		<p class="copyright">&copy; Market Mystery Bot 2023</p>
    </footer>
  </div>
</template>

<script>
import Header from "../components/Header.vue"

export default {
  mount() {
	  document.title = "MarketMystery"
  },
  components: {
    Header
  }
}
</script>