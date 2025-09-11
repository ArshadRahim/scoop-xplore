<template>
  <div>
    <div class="topbar">Just Launched: Combi Deals - Now Available!</div>

    <header class="header">
      <div class="container header-inner">
        <div class="brand">
          <div class="logo-circle">
          <img class="logo-img" src="/public/images/IMG_0254.WEBP" alt="ScootXplore Logo" />
          </div>
          
        </div>
        <nav class="nav">
          <a href="#">Combi deals</a>
          <a href="#">Activities</a>
          <a href="#">Bike tours</a>
          <a href="#">Support</a>
          <button class="btn" style="background:var(--accent); color:#0b3948;">EN</button>
        </nav>
      </div>
    </header>

    <section class="hero">
      <div class="overlay container">
        <h1>FIND A BIKE RENTAL LOCATION</h1>
        <p style="margin-top:8px;font-weight:600;color:rgba(255,255,255,0.9)">Bike rentals starting at only €28,50*</p>

        <div class="searchbar" style="margin-top:20px;">
          <select aria-label="Country">
            <option>All Countries</option>
            <option>Spain</option>
            <option>Netherlands</option>
          </select>
          <input placeholder="Search city, location..." />
          <button class="btn" style="background:var(--accent);">Search</button>
        </div>
      </div>
    </section>

    <main class="container">
      <section class="section">
        <h2>EXPLORE <span style="color:var(--teal)">EUROPE</span></h2>
        <p style="color:var(--muted)">These popular countries have a lot to offer</p>

        <div class="cards" style="margin-top:18px;">
          <div class="card">
            <img src="/images/IMG_0097.png" alt="Spain">
            <div class="card-body">
              <div class="card-title">SPAIN <span style="float:right; font-weight:600">🇪🇸</span></div>
              <div class="card-sub">Barcelona, Malaga</div>
            </div>
          </div>

          <div class="card">
            <img src="/images/IMG_0224.jpeg" alt="Netherlands">
            <div class="card-body">
              <div class="card-title">NETHERLANDS <span style="float:right; font-weight:600">🇳🇱</span></div>
              <div class="card-sub">Amsterdam & more</div>
            </div>
          </div>
        </div>
      </section>

      <section class="section">
        <h2>TRENDING RENTALS AND ACTIVITIES</h2>
        <p style="color:var(--muted)">People with similar searches booked these options.</p>

        <div class="trending" style="margin-top:18px;">
          <div class="small-card">
            <img src="/images/IMG_0254.webp" style="height:160px;width:100%;object-fit:cover" />
            <div style="padding:12px">
              <div style="font-weight:800">ScootXplore | MALAGA</div>
              <div style="color:var(--muted);font-size:13px;margin-top:8px">The sunniest city in Spain</div>
              <div style="margin-top:12px"><button class="btn" style="background:var(--accent)">BOOK BIKES</button></div>
            </div>
          </div>

          <div class="small-card">
            <img src="/images/IMG_0224.jpeg" style="height:160px;width:100%;object-fit:cover" />
            <div style="padding:12px">
              <div style="font-weight:800">ScootXplore | BARCELONA</div>
              <div style="color:var(--muted);font-size:13px;margin-top:8px">Between the beach and Gaudi</div>
              <div style="margin-top:12px"><button class="btn" style="background:var(--accent)">BOOK BIKES</button></div>
            </div>
          </div>

          <div class="small-card">
            <img src="/images/IMG_0097.png" style="height:160px;width:100%;object-fit:cover" />
            <div style="padding:12px">
              <div style="font-weight:800">THE SOCIAL HUB BARCELONA</div>
              <div style="color:var(--muted);font-size:13px;margin-top:8px">Welcome to the creative district</div>
              <div style="margin-top:12px"><button class="btn" style="background:var(--accent)">BOOK BIKES</button></div>
            </div>
          </div>

        </div>
      </section>

      <section class="section">
        <div style="display:flex;justify-content:space-between;align-items:center;gap:18px;flex-wrap:wrap">
          <div style="flex:1;min-width:260px">
            <h2>EXPERIENCE THE CITY <span style="color:var(--teal)">CAREFREE</span></h2>
            <p style="color:var(--muted)">Cycle on an award winning bike in your favorite Spanish city.</p>
            <p style="margin-top:12px">Our fleet offers lightweight stability and long range with electric options available. Replace this text with your real marketing copy.</p>
            <div style="margin-top:18px"><button class="btn" style="background:var(--teal);color:#fff;padding:12px 18px;border-radius:12px">FIND YOUR RENTAL LOCATION HERE</button></div>
          </div>

          <div style="width:300px">
            <img src="/images/IMG_0097.png" style="width:100%; border-radius:16px; box-shadow:var(--card-shadow)" />
          </div>
        </div>

        <div class="steps" style="margin-top:30px">
          <div class="step">
            <div style="font-size:26px;font-weight:800;color:var(--accent)">1</div>
            <h3>FIND, BOOK & PAY</h3>
            <p style="color:var(--muted)">Using the booking system above you can quickly and easily reserve your bike.</p>
          </div>

          <div class="step">
            <div style="font-size:26px;font-weight:800;color:var(--accent)">2</div>
            <h3>PICK-UP & ENJOY</h3>
            <p style="color:var(--muted)">Report to your rental point with your reservation number.</p>
          </div>

          <div class="step">
            <div style="font-size:26px;font-weight:800;color:var(--accent)">3</div>
            <h3>RETURN FOR THE NEXT RIDE</h3>
            <p style="color:var(--muted)">Return the bike to the rental point on time.</p>
          </div>
        </div>
      </section>

      <section class="section faq">
        <h2>FAQ</h2>
        <div v-for="(q,i) in faqs" :key="i">
          <div class="q" @click="toggle(i)">
            <div>{{ q.q }}</div>
            <div style="font-weight:700">{{ active===i ? '-' : '+' }}</div>
          </div>
          <div v-if="active===i" class="a">
            {{ q.a }}
          </div>
        </div>
      </section>
    </main>

    <footer class="footer">
      <div class="container">
        <div style="display:flex;justify-content:space-between;gap:18px;flex-wrap:wrap">
          <div style="max-width:600px">
            <div style="font-weight:800;font-size:20px">ScootXplore</div>
            <div class="small" style="margin-top:6px">Smooth and easy riding with enhanced stability. Replace with your footer text.</div>
          </div>
          <div style="min-width:220px">
            <div style="font-weight:700">CONTACT</div>
            <div class="small" style="margin-top:6px">info@example.com</div>
          </div>
        </div>

        <div style="margin-top:18px;color:rgba(255,255,255,0.7);font-size:13px">© 2025 Scoot Xplore Rentals. All rights reserved.</div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  data(){
    return {
      faqs:[
        { q:'WHAT IS ScootXplore?', a:'ScootXplore is a bike rental platform. Replace this with real answer.' },
        { q:'CAN I JOIN A GUIDED BIKE TOUR?', a:'Yes — you can join guided tours... replace with real details.' },
        { q:'HOW LONG CAN I RENT A BIKE FOR?', a:'From 1 hour to several days, depending on the location.' },
        { q:'WHAT SAFETY FEATURES ARE INCLUDED?', a:'Helmet, lock and safety briefing included in most rentals.' }
      ],
      active:null
    }
  },
  methods:{
    toggle(i){
      this.active = this.active === i ? null : i
    }
  }
}
</script>

<style scoped>
/* Scoped fine-tuning for App view (keeps global CSS lean) */
.hero {
  /* provide a soft teal gradient overlay to look like the screenshot */
  background: linear-gradient(0deg, rgba(11,57,72,0.18), rgba(11,57,72,0.18)), url('/images/hero-placeholder.jpg') center/cover no-repeat;
}
</style>
