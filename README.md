[index (2).html](https://github.com/user-attachments/files/27493662/index.2.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LUMÉ — Clean Beauty & Wellness</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,500;0,700;1,400;1,500&family=Jost:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{margin:0;padding:0;box-sizing:border-box}
:root{
  --black:#0F0F0D;
  --cream:#FAF7F2;
  --warm:#F3EDE3;
  --blush:#F2D4C8;
  --rose:#C8836A;
  --rose-dark:#A3614A;
  --sage:#8FAF8A;
  --sage-dark:#5A7A56;
  --gold:#C9A96E;
  --mid:#6E6E6A;
  --light:#B0ABA4;
  --border:#E6DFD5;
  --dp:'Playfair Display',serif;
  --body:'Jost',sans-serif;
}
html{scroll-behavior:smooth}
body{font-family:var(--body);background:var(--cream);color:var(--black);overflow-x:hidden}

.topbar{background:var(--black);color:#fff;text-align:center;padding:11px 20px;font-size:12px;letter-spacing:.08em;text-transform:uppercase}
.topbar span{color:var(--gold)}

nav{background:var(--cream);border-bottom:1px solid var(--border);padding:0 5%;height:76px;display:flex;align-items:center;justify-content:space-between;position:sticky;top:0;z-index:200}
.nav-logo{font-family:var(--dp);font-size:26px;font-weight:700;letter-spacing:.12em;text-transform:uppercase;color:var(--black);text-decoration:none}
.nav-logo sup{font-size:10px;color:var(--rose);vertical-align:super}
.nav-links{display:flex;gap:34px;list-style:none}
.nav-links a{text-decoration:none;color:var(--mid);font-size:13px;font-weight:500;letter-spacing:.06em;text-transform:uppercase;transition:color .2s}
.nav-links a:hover{color:var(--black)}
.nav-right{display:flex;align-items:center;gap:18px}
.nav-icon{background:none;border:none;cursor:pointer;color:var(--mid);font-size:19px;transition:color .2s}
.nav-icon:hover{color:var(--black)}
.btn-bag{background:var(--black);color:#fff;border:none;padding:11px 26px;font-family:var(--body);font-size:12px;font-weight:600;letter-spacing:.08em;text-transform:uppercase;cursor:pointer;transition:background .2s;border-radius:2px}
.btn-bag:hover{background:var(--rose-dark)}

/* HERO */
.hero{display:grid;grid-template-columns:1fr 1fr;min-height:92vh}
.hero-left{position:relative;overflow:hidden}
.hero-left img{width:100%;height:100%;object-fit:cover;object-position:center top;display:block;transition:transform 8s ease}
.hero-left:hover img{transform:scale(1.04)}
.hero-overlay{position:absolute;inset:0;background:linear-gradient(to top,rgba(15,15,13,.6) 0%,rgba(15,15,13,.1) 60%,transparent 100%)}
.hero-text{position:absolute;bottom:48px;left:44px;right:44px;color:#fff}
.hero-tag{display:inline-block;border:1px solid rgba(255,255,255,.45);color:#fff;font-size:11px;letter-spacing:.12em;text-transform:uppercase;padding:5px 14px;border-radius:100px;margin-bottom:18px}
.hero-text h1{font-family:var(--dp);font-size:clamp(38px,4.5vw,64px);font-weight:400;line-height:1.12;margin-bottom:16px}
.hero-text h1 em{font-style:italic;color:var(--blush)}
.hero-text p{font-size:15px;color:rgba(255,255,255,.8);line-height:1.65;max-width:380px;margin-bottom:28px;font-weight:300}
.hero-btns{display:flex;gap:12px;flex-wrap:wrap}
.btn-w{background:#fff;color:var(--black);border:none;padding:14px 32px;font-family:var(--body);font-size:12px;font-weight:600;letter-spacing:.06em;text-transform:uppercase;cursor:pointer;border-radius:2px;transition:background .2s;text-decoration:none;display:inline-block}
.btn-w:hover{background:var(--cream)}
.btn-ow{background:transparent;color:#fff;border:1px solid rgba(255,255,255,.55);padding:14px 32px;font-family:var(--body);font-size:12px;font-weight:500;letter-spacing:.06em;text-transform:uppercase;cursor:pointer;border-radius:2px;transition:all .2s;text-decoration:none;display:inline-block}
.btn-ow:hover{border-color:#fff;background:rgba(255,255,255,.1)}

.hero-right{background:var(--warm);display:flex;flex-direction:column}
.hero-right-img{flex:1;overflow:hidden;position:relative}
.hero-right-img img{width:100%;height:100%;object-fit:cover;display:block;transition:transform 6s ease}
.hero-right-img:hover img{transform:scale(1.04)}
.hero-card{margin:20px;background:rgba(250,247,242,.96);backdrop-filter:blur(12px);border-radius:16px;padding:20px 22px;display:flex;align-items:center;gap:14px;border:1px solid var(--border)}
.hero-card-img{width:58px;height:58px;border-radius:10px;overflow:hidden;flex-shrink:0}
.hero-card-img img{width:100%;height:100%;object-fit:cover}
.hero-card-label{font-size:11px;letter-spacing:.08em;text-transform:uppercase;color:var(--rose);font-weight:600;margin-bottom:3px}
.hero-card-name{font-family:var(--dp);font-size:17px;font-weight:500;color:var(--black);margin-bottom:2px}
.hero-card-price{font-size:13px;color:var(--mid)}
.hero-card-add{margin-left:auto;background:var(--black);color:#fff;border:none;width:38px;height:38px;border-radius:50%;font-size:20px;cursor:pointer;flex-shrink:0;transition:background .2s,transform .15s}
.hero-card-add:hover{background:var(--rose);transform:scale(1.1)}

/* TICKER */
.ticker{background:var(--rose);overflow:hidden;padding:13px 0}
.ticker-track{display:flex;animation:ticker 24s linear infinite;width:max-content}
.ticker-item{color:#fff;font-size:12px;letter-spacing:.1em;text-transform:uppercase;white-space:nowrap;padding:0 36px;display:flex;align-items:center;gap:14px}
.ticker-item::after{content:'✦';opacity:.55;font-size:10px}
@keyframes ticker{from{transform:translateX(0)}to{transform:translateX(-50%)}}

/* SECTION HEADER */
.sh{text-align:center;margin-bottom:56px}
.sh-tag{display:inline-block;font-size:11px;letter-spacing:.14em;text-transform:uppercase;color:var(--rose);font-weight:600;margin-bottom:14px}
.sh-title{font-family:var(--dp);font-size:clamp(30px,4vw,52px);font-weight:400;color:var(--black);line-height:1.2}
.sh-title em{font-style:italic;color:var(--sage-dark)}
.sh-sub{font-size:15px;color:var(--mid);margin-top:12px;font-weight:300;line-height:1.7}

/* PRODUCTS */
.products{padding:100px 5%;background:var(--cream)}
.filter-row{display:flex;gap:8px;justify-content:center;flex-wrap:wrap;margin-bottom:52px}
.filter-btn{padding:9px 24px;border:1px solid var(--border);background:transparent;font-family:var(--body);font-size:12px;font-weight:500;letter-spacing:.06em;text-transform:uppercase;color:var(--mid);cursor:pointer;border-radius:100px;transition:all .2s}
.filter-btn.active,.filter-btn:hover{background:var(--black);color:#fff;border-color:var(--black)}
.pgrid{display:grid;grid-template-columns:repeat(4,1fr);gap:20px;max-width:1400px;margin:0 auto}
.pcard{background:#fff;border-radius:16px;overflow:hidden;border:1px solid var(--border);transition:transform .35s,box-shadow .35s;cursor:pointer}
.pcard:hover{transform:translateY(-8px);box-shadow:0 28px 60px rgba(0,0,0,.1)}
.pcard-img{height:260px;position:relative;overflow:hidden}
.pcard-img img{width:100%;height:100%;object-fit:cover;transition:transform .5s}
.pcard:hover .pcard-img img{transform:scale(1.08)}
.badge{position:absolute;top:14px;left:14px;padding:5px 12px;border-radius:100px;font-size:11px;font-weight:600;letter-spacing:.04em;text-transform:uppercase}
.b-best{background:var(--black);color:#fff}
.b-new{background:var(--sage);color:#fff}
.b-hot{background:var(--gold);color:#fff}
.b-sale{background:var(--rose);color:#fff}
.wish{position:absolute;top:14px;right:14px;width:34px;height:34px;background:#fff;border:none;border-radius:50%;cursor:pointer;font-size:16px;display:flex;align-items:center;justify-content:center;transition:transform .2s;box-shadow:0 2px 12px rgba(0,0,0,.1)}
.wish:hover{transform:scale(1.15)}
.pcard-body{padding:18px 20px 22px}
.pcard-cat{font-size:11px;letter-spacing:.08em;text-transform:uppercase;color:var(--light);margin-bottom:5px}
.pcard-name{font-family:var(--dp);font-size:18px;font-weight:500;color:var(--black);margin-bottom:5px;line-height:1.3}
.pcard-desc{font-size:13px;color:var(--mid);margin-bottom:10px;font-weight:300}
.pcard-stars{color:var(--rose);font-size:13px;margin-bottom:14px}
.pcard-stars span{color:var(--light);margin-left:4px;font-size:12px}
.pcard-foot{display:flex;align-items:center;justify-content:space-between}
.pcard-price{font-size:20px;font-weight:600;color:var(--black)}
.pcard-price s{font-size:13px;color:var(--light);font-weight:400;margin-left:5px}
.atb{background:var(--black);color:#fff;border:none;padding:10px 18px;font-family:var(--body);font-size:12px;font-weight:600;letter-spacing:.05em;text-transform:uppercase;cursor:pointer;border-radius:100px;transition:background .2s}
.atb:hover{background:var(--rose)}

/* LIFESTYLE SPLIT */
.lifestyle{display:grid;grid-template-columns:1fr 1fr;min-height:600px}
.ls-img{position:relative;overflow:hidden}
.ls-img img{width:100%;height:100%;object-fit:cover;display:block;transition:transform 6s ease}
.ls-img:hover img{transform:scale(1.04)}
.ls-content{background:var(--black);padding:80px 70px;display:flex;flex-direction:column;justify-content:center}
.ls-tag{font-size:11px;letter-spacing:.14em;text-transform:uppercase;color:var(--gold);font-weight:600;margin-bottom:20px}
.ls-title{font-family:var(--dp);font-size:clamp(32px,3.5vw,50px);font-weight:400;color:#fff;line-height:1.2;margin-bottom:20px}
.ls-title em{font-style:italic;color:var(--blush)}
.ls-body{font-size:15px;color:#999;line-height:1.8;font-weight:300;margin-bottom:36px}
.btn-gold{background:var(--gold);color:var(--black);border:none;padding:14px 32px;font-family:var(--body);font-size:12px;font-weight:700;letter-spacing:.1em;text-transform:uppercase;cursor:pointer;border-radius:2px;transition:background .2s;text-decoration:none;display:inline-block}
.btn-gold:hover{background:#d4b47a}
.ls-stats{display:flex;gap:40px;margin-top:48px;padding-top:40px;border-top:1px solid rgba(255,255,255,.08)}
.ls-num{font-family:var(--dp);font-size:34px;color:#fff}
.ls-lbl{font-size:12px;color:#555;letter-spacing:.06em;text-transform:uppercase;margin-top:2px}

/* BENTO */
.bento{padding:100px 5%;background:var(--warm)}
.bento-grid{display:grid;grid-template-columns:1fr 1fr 1fr;grid-template-rows:300px 300px;gap:16px;max-width:1300px;margin:0 auto}
.bc{border-radius:20px;overflow:hidden;position:relative;cursor:pointer}
.bc.tall{grid-row:span 2}
.bc.wide{grid-column:span 2}
.bc img{width:100%;height:100%;object-fit:cover;display:block;transition:transform .5s}
.bc:hover img{transform:scale(1.06)}
.bc-ov{position:absolute;inset:0;background:linear-gradient(to top,rgba(15,15,13,.75) 0%,transparent 55%)}
.bc-txt{position:absolute;bottom:24px;left:24px;right:24px;color:#fff}
.bc-txt h3{font-family:var(--dp);font-size:22px;font-weight:400;margin-bottom:4px}
.bc-txt p{font-size:13px;color:rgba(255,255,255,.7);font-weight:300}

/* REVIEWS */
.reviews{padding:100px 5%;background:var(--cream)}
.rev-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:24px;max-width:1200px;margin:0 auto}
.rcard{background:#fff;border-radius:20px;padding:36px;border:1px solid var(--border);transition:transform .3s}
.rcard:hover{transform:translateY(-5px)}
.rcard-top{display:flex;align-items:center;gap:14px;margin-bottom:18px}
.rav{width:52px;height:52px;border-radius:50%;overflow:hidden;flex-shrink:0;border:2px solid var(--border)}
.rav img{width:100%;height:100%;object-fit:cover}
.rname{font-size:15px;font-weight:600;color:var(--black)}
.rrole{font-size:12px;color:var(--light);margin-top:2px}
.rverified{font-size:11px;color:var(--sage-dark);font-weight:500;margin-top:3px}
.rstars{color:var(--rose);font-size:14px;margin-bottom:14px;letter-spacing:2px}
.rquote{font-family:var(--dp);font-size:17px;font-style:italic;color:var(--black);line-height:1.65}
.rprod{display:flex;align-items:center;gap:10px;margin-top:20px;padding-top:16px;border-top:1px solid var(--border)}
.rpimg{width:36px;height:36px;border-radius:8px;overflow:hidden;flex-shrink:0}
.rpimg img{width:100%;height:100%;object-fit:cover}
.rpname{font-size:12px;color:var(--mid)}

/* GALLERY */
.gallery{display:grid;grid-template-columns:repeat(5,1fr)}
.gi{position:relative;overflow:hidden;aspect-ratio:1;cursor:pointer}
.gi img{width:100%;height:100%;object-fit:cover;display:block;transition:transform .5s}
.gi:hover img{transform:scale(1.08)}
.gi-ov{position:absolute;inset:0;background:rgba(15,15,13,0);transition:background .3s;display:flex;align-items:center;justify-content:center}
.gi:hover .gi-ov{background:rgba(15,15,13,.38)}
.gi-tag{color:#fff;font-size:13px;opacity:0;transition:opacity .3s;font-weight:500;letter-spacing:.04em}
.gi:hover .gi-tag{opacity:1}

/* NEWSLETTER */
.nl{position:relative;overflow:hidden;min-height:520px;display:flex;align-items:center}
.nl-bg{position:absolute;inset:0}
.nl-bg img{width:100%;height:100%;object-fit:cover;object-position:center 30%}
.nl-ov{position:absolute;inset:0;background:rgba(15,15,13,.72)}
.nl-content{position:relative;z-index:2;max-width:600px;margin:0 auto;text-align:center;padding:80px 40px}
.nl-tag{display:inline-block;border:1px solid rgba(255,255,255,.3);color:rgba(255,255,255,.8);font-size:11px;letter-spacing:.12em;text-transform:uppercase;padding:5px 16px;border-radius:100px;margin-bottom:22px}
.nl-title{font-family:var(--dp);font-size:clamp(32px,4vw,52px);font-weight:400;color:#fff;line-height:1.2;margin-bottom:14px}
.nl-title em{font-style:italic;color:var(--blush)}
.nl-sub{font-size:15px;color:rgba(255,255,255,.7);font-weight:300;line-height:1.7;margin-bottom:34px}
.nl-form{display:flex;gap:0;max-width:460px;margin:0 auto;border-radius:100px;overflow:hidden;border:1px solid rgba(255,255,255,.2)}
.nl-input{flex:1;padding:15px 24px;background:rgba(255,255,255,.1);border:none;color:#fff;font-family:var(--body);font-size:14px;outline:none}
.nl-input::placeholder{color:rgba(255,255,255,.45)}
.nl-btn{background:var(--rose);color:#fff;border:none;padding:15px 28px;font-family:var(--body);font-size:12px;font-weight:600;letter-spacing:.08em;text-transform:uppercase;cursor:pointer;transition:background .2s;white-space:nowrap}
.nl-btn:hover{background:var(--rose-dark)}
.nl-perks{display:flex;gap:20px;justify-content:center;margin-top:22px;flex-wrap:wrap}
.nl-perk{font-size:12px;color:rgba(255,255,255,.55);display:flex;align-items:center;gap:6px}
.nl-perk::before{content:'✓';color:var(--sage)}

/* FOOTER */
footer{background:var(--black);color:#fff;padding:80px 5% 36px}
.ft{display:grid;grid-template-columns:2.2fr 1fr 1fr 1fr;gap:60px;margin-bottom:60px;padding-bottom:60px;border-bottom:1px solid rgba(255,255,255,.07)}
.flogo{font-family:var(--dp);font-size:26px;font-weight:700;letter-spacing:.12em;text-transform:uppercase;margin-bottom:16px}
.flogo span{color:var(--rose)}
.fdesc{font-size:14px;color:#666;line-height:1.8;font-weight:300;max-width:280px;margin-bottom:24px}
.fsoc{display:flex;gap:10px}
.fsoc a{width:38px;height:38px;border:1px solid rgba(255,255,255,.12);border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:13px;color:#666;cursor:pointer;transition:border-color .2s,color .2s;text-decoration:none;font-family:var(--body)}
.fsoc a:hover{border-color:var(--rose);color:var(--rose)}
.fcol h4{font-size:11px;font-weight:600;letter-spacing:.12em;text-transform:uppercase;color:#fff;margin-bottom:22px}
.fcol ul{list-style:none}
.fcol li{font-size:14px;color:#666;margin-bottom:12px;cursor:pointer;transition:color .2s;font-weight:300}
.fcol li:hover{color:var(--rose)}
.fb{display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:16px}
.fcopy{font-size:13px;color:#444}
.fpay{display:flex;gap:8px}
.fp{background:rgba(255,255,255,.06);border:1px solid rgba(255,255,255,.08);border-radius:6px;padding:5px 10px;font-size:11px;color:#555;font-weight:500}

/* ANIMATE */
.ani{opacity:0;transform:translateY(30px);transition:opacity .7s ease,transform .7s ease}
.ani.vis{opacity:1;transform:translateY(0)}

/* RESPONSIVE */
@media(max-width:1100px){
  .pgrid{grid-template-columns:repeat(2,1fr)}
  .ft{grid-template-columns:1fr 1fr;gap:40px}
}
@media(max-width:800px){
  .hero{grid-template-columns:1fr;min-height:auto}
  .hero-left{min-height:72vh}
  .lifestyle{grid-template-columns:1fr}
  .ls-img{min-height:380px}
  .ls-content{padding:60px 30px}
  .gallery{grid-template-columns:repeat(3,1fr)}
  .nav-links{display:none}
  nav{padding:0 20px}
  .bento-grid{grid-template-columns:1fr 1fr;grid-template-rows:auto}
  .bc.tall{grid-row:span 1}
  .bc.wide{grid-column:span 2}
  .rev-grid{grid-template-columns:1fr}
}
@media(max-width:560px){
  .pgrid{grid-template-columns:1fr}
  .gallery{grid-template-columns:repeat(2,1fr)}
  .ft{grid-template-columns:1fr}
  .ls-stats{gap:20px}
  .bento-grid{grid-template-columns:1fr}
  .bc.wide{grid-column:span 1}
}
</style>
</head>
<body>

<div class="topbar">Free shipping on orders over $65 &nbsp;·&nbsp; Use code <span>GLOW20</span> for 20% off your first order</div>

<nav>
  <a href="#" class="nav-logo">Lumé<sup>®</sup></a>
  <ul class="nav-links">
    <li><a href="#">Shop</a></li>
    <li><a href="#">Skincare</a></li>
    <li><a href="#">Wellness</a></li>
    <li><a href="#">Bundles</a></li>
    <li><a href="#">Journal</a></li>
  </ul>
  <div class="nav-right">
    <button class="nav-icon">🔍</button>
    <button class="nav-icon">♡</button>
    <button class="btn-bag">Bag (0)</button>
  </div>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-left">
    <img src="https://images.unsplash.com/photo-1487412947147-5cebf100ffc2?w=900&auto=format&fit=crop&q=85" alt="Woman wellness">
    <div class="hero-overlay"></div>
    <div class="hero-text">
      <div class="hero-tag">New Collection — 2026</div>
      <h1>Your skin deserves<br><em>pure luxury</em></h1>
      <p>Science-meets-nature skincare crafted for the modern woman. Clean, effective, beautifully simple.</p>
      <div class="hero-btns">
        <a href="#products" class="btn-w">Shop Now</a>
        <a href="#" class="btn-ow">Explore Collection</a>
      </div>
    </div>
  </div>
  <div class="hero-right">
    <div class="hero-right-img">
      <img src="https://images.unsplash.com/photo-1570172619644-dfd03ed5d881?w=700&auto=format&fit=crop&q=85" alt="Skincare flatlay">
    </div>
    <div class="hero-card">
      <div class="hero-card-img">
        <img src="https://images.unsplash.com/photo-1598440947619-2c35fc9aa908?w=200&auto=format&fit=crop" alt="Serum">
      </div>
      <div>
        <div class="hero-card-label">Best Seller</div>
        <div class="hero-card-name">Glow Serum</div>
        <div class="hero-card-price">$68.00 — 4.9 ★ (2.4k)</div>
      </div>
      <button class="hero-card-add">+</button>
    </div>
  </div>
</section>

<!-- TICKER -->
<div class="ticker">
  <div class="ticker-track">
    <div class="ticker-item">Clean Beauty</div>
    <div class="ticker-item">Cruelty Free</div>
    <div class="ticker-item">Dermatologist Approved</div>
    <div class="ticker-item">Free Shipping $65+</div>
    <div class="ticker-item">100% Natural Actives</div>
    <div class="ticker-item">Vegan Certified</div>
    <div class="ticker-item">30-Day Glow Guarantee</div>
    <div class="ticker-item">Sustainable Packaging</div>
    <div class="ticker-item">Clean Beauty</div>
    <div class="ticker-item">Cruelty Free</div>
    <div class="ticker-item">Dermatologist Approved</div>
    <div class="ticker-item">Free Shipping $65+</div>
    <div class="ticker-item">100% Natural Actives</div>
    <div class="ticker-item">Vegan Certified</div>
    <div class="ticker-item">30-Day Glow Guarantee</div>
    <div class="ticker-item">Sustainable Packaging</div>
  </div>
</div>

<!-- PRODUCTS -->
<section class="products ani" id="products">
  <div class="sh">
    <div class="sh-tag">Our Collection</div>
    <h2 class="sh-title">Products your skin will<br><em>love forever</em></h2>
    <p class="sh-sub">Expertly formulated with the finest natural ingredients</p>
  </div>
  <div class="filter-row">
    <button class="filter-btn active">All</button>
    <button class="filter-btn">Serums</button>
    <button class="filter-btn">Moisturisers</button>
    <button class="filter-btn">Eye Care</button>
    <button class="filter-btn">Bundles</button>
  </div>
  <div class="pgrid">
    <div class="pcard ani">
      <div class="pcard-img">
        <img src="https://images.unsplash.com/photo-1556228578-8c89e6adf883?w=500&auto=format&fit=crop&q=80" alt="Vitamin C Serum">
        <span class="badge b-best">Best Seller</span>
        <button class="wish">♡</button>
      </div>
      <div class="pcard-body">
        <div class="pcard-cat">Serums</div>
        <div class="pcard-name">Vitamin C Glow Serum</div>
        <div class="pcard-desc">Brightening + anti-aging formula</div>
        <div class="pcard-stars">★★★★★ <span>(2.4k reviews)</span></div>
        <div class="pcard-foot">
          <div class="pcard-price">$68.00</div>
          <button class="atb">Add to Bag</button>
        </div>
      </div>
    </div>
    <div class="pcard ani">
      <div class="pcard-img">
        <img src="https://images.unsplash.com/photo-1617897903246-719242758050?w=500&auto=format&fit=crop&q=80" alt="Cloud Cream">
        <span class="badge b-new">New</span>
        <button class="wish">♡</button>
      </div>
      <div class="pcard-body">
        <div class="pcard-cat">Moisturisers</div>
        <div class="pcard-name">Cloud Cream Moisturiser</div>
        <div class="pcard-desc">24hr deep hydration</div>
        <div class="pcard-stars">★★★★★ <span>(1.8k reviews)</span></div>
        <div class="pcard-foot">
          <div class="pcard-price">$54.00</div>
          <button class="atb">Add to Bag</button>
        </div>
      </div>
    </div>
    <div class="pcard ani">
      <div class="pcard-img">
        <img src="https://images.unsplash.com/photo-1608248543803-ba4f8c70ae0b?w=500&auto=format&fit=crop&q=80" alt="Eye Cream">
        <span class="badge b-hot">Trending</span>
        <button class="wish">♡</button>
      </div>
      <div class="pcard-body">
        <div class="pcard-cat">Eye Care</div>
        <div class="pcard-name">Retinol Eye Revival</div>
        <div class="pcard-desc">Dark circles + fine lines</div>
        <div class="pcard-stars">★★★★★ <span>(987 reviews)</span></div>
        <div class="pcard-foot">
          <div class="pcard-price">$48.00</div>
          <button class="atb">Add to Bag</button>
        </div>
      </div>
    </div>
    <div class="pcard ani">
      <div class="pcard-img">
        <img src="https://images.unsplash.com/photo-1612817288484-6f916006741a?w=500&auto=format&fit=crop&q=80" alt="Glow Kit">
        <span class="badge b-sale">Save 30%</span>
        <button class="wish">♡</button>
      </div>
      <div class="pcard-body">
        <div class="pcard-cat">Bundles</div>
        <div class="pcard-name">The Glow Starter Kit</div>
        <div class="pcard-desc">Serum + Cream + Eye Care</div>
        <div class="pcard-stars">★★★★★ <span>(3.1k reviews)</span></div>
        <div class="pcard-foot">
          <div class="pcard-price">$124.00 <s>$178</s></div>
          <button class="atb">Add to Bag</button>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- LIFESTYLE SPLIT -->
<section class="lifestyle ani">
  <div class="ls-img">
    <img src="https://images.unsplash.com/photo-1522337360788-8b13dee7a37e?w=800&auto=format&fit=crop&q=85" alt="Woman beauty routine">
  </div>
  <div class="ls-content">
    <div class="ls-tag">Our Philosophy</div>
    <h2 class="ls-title">Beauty rooted<br>in <em>nature's wisdom</em></h2>
    <p class="ls-body">We believe your skin deserves only the purest ingredients — no harmful fillers, no synthetic shortcuts. Every drop is crafted with purpose, backed by science, and inspired by the natural world.</p>
    <a href="#" class="btn-gold">Discover Our Story</a>
    <div class="ls-stats">
      <div><div class="ls-num">82k+</div><div class="ls-lbl">Customers</div></div>
      <div><div class="ls-num">4.9★</div><div class="ls-lbl">Avg Rating</div></div>
      <div><div class="ls-num">100%</div><div class="ls-lbl">Natural</div></div>
    </div>
  </div>
</section>

<!-- BENTO GRID -->
<section class="bento ani">
  <div class="sh">
    <div class="sh-tag">Key Ingredients</div>
    <h2 class="sh-title">Nature's finest,<br><em>in every bottle</em></h2>
  </div>
  <div class="bento-grid">
    <div class="bc tall">
      <img src="https://images.unsplash.com/photo-1540420773420-3366772f4999?w=600&auto=format&fit=crop&q=80" alt="Natural ingredients">
      <div class="bc-ov"></div>
      <div class="bc-txt"><h3>Hyaluronic Acid</h3><p>Deep hydration from nature</p></div>
    </div>
    <div class="bc">
      <img src="https://images.unsplash.com/photo-1518895949257-7621c3c786d7?w=500&auto=format&fit=crop&q=80" alt="Rosehip">
      <div class="bc-ov"></div>
      <div class="bc-txt"><h3>Rose Hip Oil</h3><p>Nourish & renew skin cells</p></div>
    </div>
    <div class="bc">
      <img src="https://images.unsplash.com/photo-1556228453-efd6c1ff04f6?w=500&auto=format&fit=crop&q=80" alt="Vitamin C">
      <div class="bc-ov"></div>
      <div class="bc-txt"><h3>Vitamin C Complex</h3><p>Brighten & protect daily</p></div>
    </div>
    <div class="bc wide">
      <img src="https://images.unsplash.com/photo-1542601906990-b4d3fb778b09?w=900&auto=format&fit=crop&q=80" alt="Green botanicals">
      <div class="bc-ov"></div>
      <div class="bc-txt"><h3>Green Botanicals</h3><p>Sustainably sourced — ethically made for a better planet</p></div>
    </div>
  </div>
</section>

<!-- REVIEWS -->
<section class="reviews ani">
  <div class="sh">
    <div class="sh-tag">Real Results</div>
    <h2 class="sh-title">Women who found<br><em>their glow</em></h2>
  </div>
  <div class="rev-grid">
    <div class="rcard ani">
      <div class="rcard-top">
        <div class="rav"><img src="https://images.unsplash.com/photo-1531746020798-e6953c6e8e04?w=100&auto=format&fit=crop" alt="Sarah"></div>
        <div>
          <div class="rname">Sarah Mitchell</div>
          <div class="rrole">Yoga Instructor, New York</div>
          <div class="rverified">✓ Verified Purchase</div>
        </div>
      </div>
      <div class="rstars">★★★★★</div>
      <div class="rquote">"I've tried every luxury skincare brand out there. Nothing has transformed my skin like Lumé. My friends keep asking what I'm doing differently!"</div>
      <div class="rprod">
        <div class="rpimg"><img src="https://images.unsplash.com/photo-1556228578-8c89e6adf883?w=80&auto=format&fit=crop" alt="Serum"></div>
        <div class="rpname">Vitamin C Glow Serum</div>
      </div>
    </div>
    <div class="rcard ani">
      <div class="rcard-top">
        <div class="rav"><img src="https://images.unsplash.com/photo-1494790108755-2616b612b5ab?w=100&auto=format&fit=crop" alt="Priya"></div>
        <div>
          <div class="rname">Priya Nair</div>
          <div class="rrole">Nutritionist, London</div>
          <div class="rverified">✓ Verified Purchase</div>
        </div>
      </div>
      <div class="rstars">★★★★★</div>
      <div class="rquote">"The Cloud Cream is unlike anything I've used before. My skin literally drinks it up. It's the first moisturiser that doesn't leave me oily by noon."</div>
      <div class="rprod">
        <div class="rpimg"><img src="https://images.unsplash.com/photo-1617897903246-719242758050?w=80&auto=format&fit=crop" alt="Cream"></div>
        <div class="rpname">Cloud Cream Moisturiser</div>
      </div>
    </div>
    <div class="rcard ani">
      <div class="rcard-top">
        <div class="rav"><img src="https://images.unsplash.com/photo-1517841905240-472988babdf9?w=100&auto=format&fit=crop" alt="Amara"></div>
        <div>
          <div class="rname">Amara Osei</div>
          <div class="rrole">Model, Paris</div>
          <div class="rverified">✓ Verified Purchase</div>
        </div>
      </div>
      <div class="rstars">★★★★★</div>
      <div class="rquote">"As someone in front of cameras daily, my skin has to be flawless. The Glow Starter Kit gave me the most luminous, even skin tone I've ever had."</div>
      <div class="rprod">
        <div class="rpimg"><img src="https://images.unsplash.com/photo-1612817288484-6f916006741a?w=80&auto=format&fit=crop" alt="Kit"></div>
        <div class="rpname">The Glow Starter Kit</div>
      </div>
    </div>
  </div>
</section>

<!-- GALLERY STRIP -->
<div class="gallery">
  <div class="gi"><img src="https://images.unsplash.com/photo-1545205597-3d9d02c29597?w=400&auto=format&fit=crop&q=80" alt="Lifestyle"><div class="gi-ov"><div class="gi-tag">#LuméGlow</div></div></div>
  <div class="gi"><img src="https://images.unsplash.com/photo-1571781926291-c477ebfd024b?w=400&auto=format&fit=crop&q=80" alt="Lifestyle"><div class="gi-ov"><div class="gi-tag">#LuméGlow</div></div></div>
  <div class="gi"><img src="https://images.unsplash.com/photo-1512290923902-8a9f81dc236c?w=400&auto=format&fit=crop&q=80" alt="Lifestyle"><div class="gi-ov"><div class="gi-tag">#LuméGlow</div></div></div>
  <div class="gi"><img src="https://images.unsplash.com/photo-1596178065887-1198b6148b2b?w=400&auto=format&fit=crop&q=80" alt="Lifestyle"><div class="gi-ov"><div class="gi-tag">#LuméGlow</div></div></div>
  <div class="gi"><img src="https://images.unsplash.com/photo-1526045612212-70caf35c14df?w=400&auto=format&fit=crop&q=80" alt="Lifestyle"><div class="gi-ov"><div class="gi-tag">#LuméGlow</div></div></div>
</div>

<!-- NEWSLETTER -->
<section class="nl">
  <div class="nl-bg"><img src="https://images.unsplash.com/photo-1556909172-54557c7e4fb7?w=1400&auto=format&fit=crop&q=80" alt="Background"></div>
  <div class="nl-ov"></div>
  <div class="nl-content">
    <div class="nl-tag">Join the Lumé Community</div>
    <h2 class="nl-title">Glow from the<br><em>inside out</em></h2>
    <p class="nl-sub">Join 82,000+ women who get exclusive skincare tips, first access to new launches, and members-only offers.</p>
    <div class="nl-form">
      <input class="nl-input" type="email" placeholder="Your email address">
      <button class="nl-btn">Subscribe</button>
    </div>
    <div class="nl-perks">
      <div class="nl-perk">20% off your first order</div>
      <div class="nl-perk">Early access to launches</div>
      <div class="nl-perk">Expert glow tips weekly</div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="ft">
    <div>
      <div class="flogo">Lumé<span>®</span></div>
      <p class="fdesc">Clean beauty crafted for the modern woman. Pure ingredients, proven results, sustainable future.</p>
      <div class="fsoc">
        <a href="#">in</a><a href="#">ig</a><a href="#">tk</a><a href="#">pt</a>
      </div>
    </div>
    <div class="fcol">
      <h4>Shop</h4>
      <ul><li>All Products</li><li>Serums</li><li>Moisturisers</li><li>Eye Care</li><li>Bundles</li><li>Gift Sets</li></ul>
    </div>
    <div class="fcol">
      <h4>Company</h4>
      <ul><li>Our Story</li><li>Ingredients</li><li>Sustainability</li><li>Press</li><li>Affiliates</li><li>Careers</li></ul>
    </div>
    <div class="fcol">
      <h4>Support</h4>
      <ul><li>FAQ</li><li>Shipping & Returns</li><li>Track My Order</li><li>Contact Us</li><li>Skin Quiz</li><li>Privacy Policy</li></ul>
    </div>
  </div>
  <div class="fb">
    <div class="fcopy">© 2026 Lumé Beauty. All rights reserved.</div>
    <div class="fpay">
      <span class="fp">Visa</span><span class="fp">Mastercard</span><span class="fp">PayPal</span><span class="fp">Apple Pay</span>
    </div>
  </div>
</footer>

<script>
const obs = new IntersectionObserver((entries) => {
  entries.forEach((e,i) => {
    if(e.isIntersecting) setTimeout(() => e.target.classList.add('vis'), i * 80);
  });
}, {threshold: 0.06});
document.querySelectorAll('.ani').forEach(el => obs.observe(el));

document.querySelectorAll('.filter-btn').forEach(btn => {
  btn.addEventListener('click', () => {
    document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
    btn.classList.add('active');
  });
});

document.querySelectorAll('.wish').forEach(btn => {
  btn.addEventListener('click', e => {
    e.stopPropagation();
    const on = btn.textContent === '♥';
    btn.textContent = on ? '♡' : '♥';
    btn.style.color = on ? '' : '#C8836A';
  });
});

document.querySelectorAll('.atb, .hero-card-add').forEach(btn => {
  btn.addEventListener('click', () => {
    const orig = btn.textContent;
    btn.textContent = btn.classList.contains('hero-card-add') ? '✓' : 'Added ✓';
    btn.style.background = '#5A7A56';
    setTimeout(() => { btn.textContent = orig; btn.style.background = ''; }, 1500);
  });
});

document.querySelector('.nl-btn').addEventListener('click', () => {
  const inp = document.querySelector('.nl-input');
  const btn = document.querySelector('.nl-btn');
  if(inp.value.includes('@')){
    btn.textContent = 'Joined ✓';
    btn.style.background = '#5A7A56';
    inp.value = '';
    setTimeout(() => { btn.textContent = 'Subscribe'; btn.style.background = ''; }, 2500);
  }
});
</script>
</body>
</html>
