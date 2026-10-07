
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>KHALIF — Africa's Business Marketplace</title>

<meta name="description"
content="KHALIF helps businesses sell online, reach customers and grow.">

<style>

:root{
  --bg:#f6f7fb;
  --card:#ffffff;
  --text:#101828;
  --muted:#667085;
  --border:#e4e7ec;
  --primary:#2563eb;
  --primary2:#1d4ed8;
  --dark:#0b1220;
  --success:#16a34a;
  --danger:#dc2626;
  --shadow:0 15px 40px rgba(16,24,40,.08);
}

*{
  box-sizing:border-box;
  margin:0;
  padding:0;
}

html{
  scroll-behavior:smooth;
}

body{
  font-family:Inter,Arial,sans-serif;
  background:var(--bg);
  color:var(--text);
  transition:.25s;
}

body.dark{
  --bg:#080d18;
  --card:#111827;
  --text:#f9fafb;
  --muted:#9ca3af;
  --border:#263244;
  --dark:#020617;
}

button,
input{
  font:inherit;
}

button{
  cursor:pointer;
}

a{
  text-decoration:none;
  color:inherit;
}

/* HEADER */

header{
  position:sticky;
  top:0;
  z-index:1000;
  background:rgba(255,255,255,.92);
  backdrop-filter:blur(15px);
  border-bottom:1px solid var(--border);
}

body.dark header{
  background:rgba(8,13,24,.92);
}

.nav{
  max-width:1250px;
  margin:auto;
  padding:15px 20px;
  display:flex;
  align-items:center;
  gap:25px;
}

.logo{
  font-size:28px;
  font-weight:1000;
  letter-spacing:-1px;
}

.logo span{
  color:var(--primary);
}

.search{
  flex:1;
  position:relative;
}

.search input{
  width:100%;
  padding:13px 18px 13px 45px;
  border:1px solid var(--border);
  border-radius:12px;
  outline:none;
  background:var(--bg);
  color:var(--text);
}

.search-icon{
  position:absolute;
  left:16px;
  top:12px;
}

.nav-actions{
  display:flex;
  gap:10px;
}

.icon-btn{
  width:43px;
  height:43px;
  border-radius:12px;
  border:1px solid var(--border);
  background:var(--card);
  color:var(--text);
  font-size:18px;
  position:relative;
}

.badge{
  position:absolute;
  top:-5px;
  right:-5px;
  min-width:18px;
  height:18px;
  padding:2px 5px;
  border-radius:20px;
  background:#ef4444;
  color:white;
  font-size:10px;
  font-weight:bold;
}

.menu{
  display:none;
}

/* HERO */

.hero{
  max-width:1250px;
  margin:30px auto;
  padding:70px 35px;
  border-radius:28px;
  overflow:hidden;
  position:relative;
  background:
    radial-gradient(circle at 80% 20%,#3b82f655,transparent 30%),
    linear-gradient(135deg,#0b1220,#172554);
  color:white;
}

.hero-content{
  max-width:650px;
  position:relative;
  z-index:2;
}

.hero small{
  display:inline-block;
  padding:7px 12px;
  border-radius:30px;
  background:#ffffff15;
  border:1px solid #ffffff22;
  margin-bottom:20px;
}

.hero h1{
  font-size:clamp(42px,7vw,75px);
  line-height:.98;
  letter-spacing:-3px;
  margin-bottom:25px;
}

.hero h1 span{
  color:#60a5fa;
}

.hero p{
  font-size:18px;
  line-height:1.7;
  color:#cbd5e1;
  max-width:580px;
}

.hero-buttons{
  display:flex;
  gap:12px;
  flex-wrap:wrap;
  margin-top:30px;
}

.btn{
  border:none;
  padding:14px 20px;
  border-radius:11px;
  font-weight:800;
  transition:.2s;
}

.btn:hover{
  transform:translateY(-2px);
}

.btn-primary{
  background:#2563eb;
  color:white;
}

.btn-white{
  background:white;
  color:#111827;
}

/* STATS */

.stats{
  max-width:1250px;
  margin:0 auto 45px;
  padding:0 20px;
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:15px;
}

.stat{
  background:var(--card);
  border:1px solid var(--border);
  padding:22px;
  border-radius:18px;
}

.stat strong{
  display:block;
  font-size:28px;
  margin-bottom:5px;
}

.stat span{
  color:var(--muted);
}

/* SECTIONS */

.section{
  max-width:1250px;
  margin:0 auto;
  padding:35px 20px;
}

.section-head{
  display:flex;
  align-items:end;
  justify-content:space-between;
  margin-bottom:25px;
}

.section-head h2{
  font-size:32px;
  letter-spacing:-1px;
}

.section-head p{
  color:var(--muted);
  margin-top:5px;
}

/* CATEGORIES */

.categories{
  display:flex;
  gap:12px;
  overflow-x:auto;
  padding-bottom:10px;
}

.category{
  flex:0 0 auto;
  border:1px solid var(--border);
  background:var(--card);
  color:var(--text);
  border-radius:14px;
  padding:13px 18px;
  font-weight:700;
}

.category.active{
  background:var(--primary);
  color:white;
  border-color:var(--primary);
}

/* PRODUCTS */

.products{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:20px;
}

.product{
  background:var(--card);
  border:1px solid var(--border);
  border-radius:18px;
  overflow:hidden;
  box-shadow:var(--shadow);
  transition:.25s;
}

.product:hover{
  transform:translateY(-5px);
}

.product-img{
  height:220px;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:80px;
  background:linear-gradient(135deg,#eef2ff,#e0f2fe);
  position:relative;
}

body.dark .product-img{
  background:#1e293b;
}

.heart{
  position:absolute;
  right:12px;
  top:12px;
  width:38px;
  height:38px;
  border-radius:50%;
  border:none;
  background:white;
  font-size:18px;
}

.product-body{
  padding:18px;
}

.seller{
  color:var(--muted);
  font-size:12px;
  margin-bottom:8px;
}

.product h3{
  font-size:17px;
  margin-bottom:8px;
}

.rating{
  color:#f59e0b;
  font-size:13px;
}

.price{
  font-size:21px;
  font-weight:900;
  margin:12px 0;
}

.product-bottom{
  display:flex;
  gap:8px;
}

.add{
  flex:1;
  border:none;
  border-radius:10px;
  background:var(--primary);
  color:white;
  font-weight:800;
  padding:12px;
}

.buy{
  width:45px;
  border:1px solid var(--border);
  border-radius:10px;
  background:var(--card);
  color:var(--text);
}

/* BUSINESS */

.business{
  margin-top:50px;
  border-radius:25px;
  padding:55px 30px;
  background:linear-gradient(135deg,#172554,#2563eb);
  color:white;
  text-align:center;
}

.business h2{
  font-size:40px;
  margin-bottom:15px;
}

.business p{
  color:#dbeafe;
  max-width:650px;
  margin:auto;
  line-height:1.7;
}

/* FEATURES */

.features{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:20px;
}

.feature{
  background:var(--card);
  border:1px solid var(--border);
  border-radius:18px;
  padding:28px;
}

.feature-icon{
  font-size:35px;
  margin-bottom:18px;
}

.feature p{
  color:var(--muted);
  line-height:1.6;
  margin-top:10px;
}

/* PRICING */

.pricing{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:20px;
}

.plan{
  background:var(--card);
  border:1px solid var(--border);
  padding:30px;
  border-radius:20px;
}

.plan.featured{
  border:2px solid var(--primary);
  position:relative;
}

.popular{
  position:absolute;
  right:20px;
  top:20px;
  color:white;
  background:var(--primary);
  padding:5px 10px;
  border-radius:20px;
  font-size:11px;
  font-weight:bold;
}

.plan-price{
  font-size:35px;
  font-weight:900;
  margin:20px 0;
}

.plan ul{
  list-style:none;
  color:var(--muted);
  line-height:2;
  margin-bottom:20px;
}

/* FOOTER */

footer{
  margin-top:60px;
  background:#050b16;
  color:white;
  padding:50px 20px;
}

.footer-inner{
  max-width:1250px;
  margin:auto;
  display:grid;
  grid-template-columns:2fr 1fr 1fr 1fr;
  gap:40px;
}

footer p{
  color:#94a3b8;
  line-height:1.7;
  margin-top:12px;
}

footer h4{
  margin-bottom:15px;
}

footer a{
  display:block;
  color:#94a3b8;
  margin:10px 0;
}

/* CART */

.overlay{
  display:none;
  position:fixed;
  inset:0;
  background:#0008;
  z-index:2000;
}

.cart-panel{
  position:absolute;
  right:0;
  top:0;
  height:100%;
  width:min(430px,100%);
  background:var(--card);
  color:var(--text);
  padding:25px;
  overflow:auto;
}

.cart-head{
  display:flex;
  justify-content:space-between;
  align-items:center;
  margin-bottom:25px;
}

.close{
  border:none;
  background:none;
  font-size:28px;
  color:var(--text);
}

.cart-item{
  display:flex;
  justify-content:space-between;
  gap:10px;
  padding:15px 0;
  border-bottom:1px solid var(--border);
}

.cart-total{
  margin-top:25px;
  font-size:23px;
  font-weight:900;
}

/* TOAST */

.toast{
  position:fixed;
  bottom:25px;
  left:50%;
  transform:translate(-50%,120px);
  background:#111827;
  color:white;
  padding:14px 20px;
  border-radius:12px;
  z-index:5000;
  transition:.3s;
}

.toast.show{
  transform:translate(-50%,0);
}

/* MOBILE */

@media(max-width:900px){

.products{
  grid-template-columns:repeat(2,1fr);
}

.stats{
  grid-template-columns:repeat(2,1fr);
}

.features{
  grid-template-columns:1fr;
}

.pricing{
  grid-template-columns:1fr;
}

.footer-inner{
  grid-template-columns:1fr 1fr;
}

}

@media(max-width:650px){

.nav{
  gap:10px;
}

.logo{
  font-size:23px;
}

.search{
  display:none;
}

.menu{
  display:block;
}

.hero{
  margin:15px;
  padding:55px 25px;
  border-radius:20px;
}

.hero h1{
  letter-spacing:-2px;
}

.stats{
  grid-template-columns:1fr 1fr;
  padding:0 15px;
}

.section{
  padding:30px 15px;
}

.products{
  grid-template-columns:1fr 1fr;
  gap:12px;
}

.product-img{
  height:150px;
  font-size:55px;
}

.product-body{
  padding:13px;
}

.product h3{
  font-size:14px;
}

.price{
  font-size:17px;
}

.section-head{
  display:block;
}

.footer-inner{
  grid-template-columns:1fr;
}

}

/* SMALL PHONE */

@media(max-width:390px){

.products{
  grid-template-columns:1fr;
}

}

</style>
</head>

<body>

<!-- HEADER -->

<header>

<div class="nav">

<a class="logo" href="#">
KHAL<span>IF</span>
</a>

<div class="search">
<span class="search-icon">🔎</span>
<input
id="searchInput"
type="text"
placeholder="Search products, stores..."
oninput="searchProducts()"
>
</div>

<div class="nav-actions">

<button class="icon-btn" onclick="toggleDark()">
🌙
</button>

<button class="icon-btn" onclick="showToast('Account system coming next!')">
👤
</button>

<button class="icon-btn" onclick="openCart()">
🛒
