# Theme-
Shopify t<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1.0"/>
<title>GlowPure – Natural Skincare</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,500;0,600;0,700;1,400;1,500&family=Jost:wght@300;400;500;600&display=swap" rel="stylesheet"/>
<style>
:root{
  --cream:#FAF7F2;--ivory:#F5EFE6;--blush:#E8C4A8;--rose:#C4705A;--deep:#2C1F1A;
  --sage:#7A9E7E;--gold:#B8955A;--muted:#8A7468;--white:#fff;--card:#FDF9F4;
  --border:rgba(196,112,90,.15);--shadow:rgba(44,31,26,.08);
}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;}
html{scroll-behavior:smooth;font-size:16px;}
body{font-family:'Jost',sans-serif;background:var(--cream);color:var(--deep);overflow-x:hidden;}
a{text-decoration:none;color:inherit;}
img{max-width:100%;}

/* ── SCROLLBAR ── */
::-webkit-scrollbar{width:6px;}
::-webkit-scrollbar-track{background:var(--cream);}
::-webkit-scrollbar-thumb{background:var(--blush);border-radius:3px;}

/* ── PAGE SYSTEM ── */
.page{display:none;}
.page.active{display:block;animation:pageIn .4s ease;}
@keyframes pageIn{from{opacity:0;transform:translateY(16px)}to{opacity:1;transform:translateY(0)}}

/* ── ANNOUNCEMENT ── */
.announce{background:var(--deep);color:var(--blush);text-align:center;padding:9px 20px;
  font-size:12px;letter-spacing:2.5px;text-transform:uppercase;position:relative;}
.announce strong{color:var(--white);}

/* ── NAV ── */
nav{position:sticky;top:0;z-index:200;background:rgba(250,247,242,.97);
  backdrop-filter:blur(14px);border-bottom:1px solid var(--border);
  padding:0 5%;display:flex;align-items:center;justify-content:space-between;height:72px;}
.nav-logo{font-family:'Playfair Display',serif;font-size:26px;font-weight:700;
  color:var(--deep);cursor:pointer;letter-spacing:.5px;}
.nav-logo span{color:var(--rose);}
.nav-links{display:flex;gap:30px;list-style:none;}
.nav-links a{font-size:12px;letter-spacing:1.5px;text-transform:uppercase;
  color:var(--muted);transition:color .2s;cursor:pointer;}
.nav-links a:hover{color:var(--rose);}
.nav-right{display:flex;gap:16px;align-items:center;}
.nav-icon-btn{background:none;border:none;cursor:pointer;font-size:18px;color:var(--deep);
  padding:6px;position:relative;transition:color .2s;}
.nav-icon-btn:hover{color:var(--rose);}
.cart-count{position:absolute;top:-4px;right:-4px;background:var(--rose);color:#fff;
  width:18px;height:18px;border-radius:50%;font-size:10px;display:flex;
  align-items:center;justify-content:center;font-weight:600;}
.nav-cta{background:var(--deep);color:var(--cream);padding:10px 22px;border-radius:2px;
  font-size:12px;letter-spacing:1.5px;text-transform:uppercase;cursor:pointer;
  transition:background .2s;border:none;font-family:'Jost',sans-serif;}
.nav-cta:hover{background:var(--rose);}
.hamburger{display:none;flex-direction:column;gap:5px;cursor:pointer;padding:4px;}
.hamburger span{width:24px;height:2px;background:var(--deep);border-radius:2px;transition:.3s;}
.mobile-nav{display:none;flex-direction:column;background:var(--cream);
  border-bottom:1px solid var(--border);padding:20px 5%;}
.mobile-nav.open{display:flex;}
.mobile-nav a{padding:12px 0;font-size:13px;letter-spacing:1px;text-transform:uppercase;
  color:var(--muted);border-bottom:1px solid var(--border);cursor:pointer;}

/* ── BUTTONS ── */
.btn{display:inline-block;font-family:'Jost',sans-serif;cursor:pointer;
  transition:all .25s;border-radius:2px;font-size:12px;letter-spacing:2px;text-transform:uppercase;}
.btn-dark{background:var(--deep);color:var(--cream);padding:15px 36px;border:none;}
.btn-dark:hover{background:var(--rose);}
.btn-outline{background:transparent;color:var(--deep);padding:14px 34px;
  border:1.5px solid var(--deep);}
.btn-outline:hover{background:var(--deep);color:var(--cream);}
.btn-rose{background:var(--rose);color:#fff;padding:15px 36px;border:none;}
.btn-rose:hover{background:#b05e4a;transform:translateY(-2px);}
.btn-sm{padding:10px 22px;font-size:11px;}
.btn-full{width:100%;text-align:center;padding:16px;}

/* ── SECTION HELPERS ── */
.section-tag{font-size:11px;letter-spacing:4px;text-transform:uppercase;
  color:var(--sage);display:block;margin-bottom:10px;}
.section-title{font-family:'Playfair Display',serif;font-size:clamp(30px,4vw,52px);
  font-weight:500;line-height:1.1;color:var(--deep);}
.section-title em{font-style:italic;color:var(--rose);}
.section-sub{font-size:16px;color:var(--muted);line-height:1.75;margin-top:14px;}
.divider{width:48px;height:2px;background:var(--blush);margin:20px 0;}

/* ═══════════════════════════════════════════════
   HOME PAGE
══════════════════════════════════════════════ */

/* HERO */
.hero{position:relative;min-height:92vh;display:flex;align-items:center;overflow:hidden;}
.hero-bg{position:absolute;inset:0;
  background:linear-gradient(140deg,#F7EAD8 0%,#EDD6BE 35%,#E2C8AD 65%,#D6B89B 100%);}
.hero-dots{position:absolute;inset:0;opacity:.25;
  background-image:radial-gradient(circle,#C4705A 1px,transparent 1px);
  background-size:32px 32px;}
.hero-blob{position:absolute;right:-100px;top:-60px;width:600px;height:600px;
  border-radius:50%;background:radial-gradient(circle,rgba(196,112,90,.2),transparent 70%);}
.hero-blob2{position:absolute;left:-150px;bottom:-100px;width:400px;height:400px;
  border-radius:50%;background:radial-gradient(circle,rgba(122,158,126,.15),transparent 70%);}
.hero-inner{position:relative;z-index:2;display:grid;grid-template-columns:1fr 1fr;
  gap:60px;align-items:center;padding:0 6%;width:100%;}
.hero-content{animation:heroIn .9s ease both;}
@keyframes heroIn{from{opacity:0;transform:translateX(-30px)}to{opacity:1;transform:translateX(0)}}
.hero-eyebrow{font-size:11px;letter-spacing:5px;text-transform:uppercase;
  color:var(--rose);display:block;margin-bottom:20px;}
.hero-h1{font-family:'Playfair Display',serif;font-size:clamp(44px,6vw,80px);
  font-weight:400;line-height:1.05;color:var(--deep);margin-bottom:22px;}
.hero-h1 em{font-style:italic;color:var(--rose);}
.hero-p{font-size:17px;color:var(--muted);line-height:1.75;margin-bottom:38px;max-width:450px;}
.hero-btns{display:flex;gap:14px;flex-wrap:wrap;}
.hero-stats{display:flex;gap:40px;margin-top:50px;padding-top:40px;
  border-top:1px solid rgba(196,112,90,.2);}
.hero-stat .num{font-family:'Playfair Display',serif;font-size:34px;font-weight:500;
  color:var(--deep);}
.hero-stat .lbl{font-size:11px;letter-spacing:2px;text-transform:uppercase;color:var(--muted);}
.hero-visual{animation:heroImgIn 1s ease .2s both;display:flex;align-items:center;justify-content:center;}
@keyframes heroImgIn{from{opacity:0;transform:translateX(30px)}to{opacity:1;transform:translateX(0)}}
.hero-img-wrap{position:relative;width:420px;height:520px;}
.hero-img-card{position:absolute;border-radius:6px;overflow:hidden;
  background:linear-gradient(145deg,#dfc8ad,#c9a97e);
  display:flex;align-items:center;justify-content:center;font-size:80px;}
.hero-img-card.main{inset:0;width:100%;height:100%;}
.hero-img-card.float1{width:160px;height:160px;bottom:-20px;left:-40px;font-size:40px;
  box-shadow:0 20px 50px var(--shadow);}
.hero-badge{position:absolute;top:20px;right:-20px;background:var(--deep);color:var(--cream);
  padding:14px 18px;border-radius:4px;text-align:center;}
.hero-badge .b-num{font-family:'Playfair Display',serif;font-size:26px;color:var(--gold);}
.hero-badge .b-txt{font-size:10px;letter-spacing:2px;text-transform:uppercase;display:block;}

/* TICKER */
.ticker-bar{background:var(--deep);padding:13px 0;overflow:hidden;}
.ticker-track{display:flex;white-space:nowrap;animation:ticker 25s linear infinite;}
.ticker-item{font-size:12px;letter-spacing:3px;text-transform:uppercase;
  color:var(--blush);padding:0 0 0 60px;}
.ticker-item::after{content:' ✦';color:var(--rose);margin-left:60px;}

/* CATEGORIES */
.categories{padding:80px 6%;}
.cats-header{text-align:center;margin-bottom:50px;}
.cats-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:20px;}
.cat-card{position:relative;border-radius:4px;overflow:hidden;cursor:pointer;
  height:260px;background:linear-gradient(145deg,#e8d4bc,#d4b89a);
  display:flex;align-items:flex-end;transition:transform .3s;group:true;}
.cat-card:hover{transform:translateY(-6px);}
.cat-card:hover .cat-overlay{opacity:1;}
.cat-emoji{position:absolute;top:50%;left:50%;transform:translate(-50%,-70%);
  font-size:70px;transition:transform .3s;}
.cat-card:hover .cat-emoji{transform:translate(-50%,-70%) scale(1.1);}
.cat-info{position:relative;z-index:2;padding:20px;width:100%;}
.cat-overlay{position:absolute;inset:0;background:rgba(44,31,26,.4);transition:opacity .3s;opacity:0;}
.cat-name{font-family:'Playfair Display',serif;font-size:20px;color:var(--white);
  position:relative;z-index:2;}
.cat-count{font-size:11px;letter-spacing:2px;text-transform:uppercase;
  color:rgba(255,255,255,.7);position:relative;z-index:2;}

/* PRODUCTS */
.products-sec{padding:80px 6%;background:var(--ivory);}
.prod-header{display:flex;justify-content:space-between;align-items:flex-end;margin-bottom:50px;}
.products-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(260px,1fr));gap:28px;}
.prod-card{background:var(--card);border:1px solid var(--border);border-radius:4px;
  overflow:hidden;transition:transform .3s,box-shadow .3s;position:relative;}
.prod-card:hover{transform:translateY(-8px);box-shadow:0 24px 60px var(--shadow);}
.prod-badge{position:absolute;top:14px;left:14px;z-index:2;padding:5px 12px;
  border-radius:2px;font-size:10px;letter-spacing:2px;text-transform:uppercase;font-weight:600;}
.badge-sale{background:var(--rose);color:#fff;}
.badge-new{background:var(--sage);color:#fff;}
.badge-best{background:var(--gold);color:#fff;}
.prod-img{height:280px;overflow:hidden;position:relative;cursor:pointer;
  background:linear-gradient(145deg,#f0e0cc,#e0ccb4);
  display:flex;align-items:center;justify-content:center;font-size:80px;}
.prod-img img{width:100%;height:100%;object-fit:cover;transition:transform .5s;}
.prod-card:hover .prod-img img{transform:scale(1.06);}
.prod-wishlist{position:absolute;top:12px;right:12px;background:rgba(255,255,255,.9);
  border:none;width:34px;height:34px;border-radius:50%;display:flex;align-items:center;
  justify-content:center;cursor:pointer;font-size:16px;transition:all .2s;}
.prod-wishlist:hover{background:var(--rose);color:#fff;}
.prod-body{padding:20px 20px 24px;}
.prod-category{font-size:10px;letter-spacing:2.5px;text-transform:uppercase;
  color:var(--sage);margin-bottom:6px;}
.prod-name{font-family:'Playfair Display',serif;font-size:19px;font-weight:500;
  color:var(--deep);margin-bottom:6px;cursor:pointer;}
.prod-name:hover{color:var(--rose);}
.prod-desc{font-size:13px;color:var(--muted);line-height:1.6;margin-bottom:14px;}
.prod-stars{color:var(--gold);font-size:13px;margin-bottom:14px;}
.prod-stars span{color:var(--muted);font-size:12px;margin-left:4px;}
.prod-price-row{display:flex;align-items:center;gap:10px;margin-bottom:16px;}
.price-now{font-size:22px;font-weight:600;color:var(--rose);}
.price-was{font-size:15px;text-decoration:line-through;color:var(--muted);}
.price-save{font-size:11px;background:#FFF0EB;color:var(--rose);
  padding:3px 8px;border-radius:2px;font-weight:600;}
.btn-cart-add{width:100%;background:var(--deep);color:var(--cream);border:none;
  padding:13px;font-size:11px;letter-spacing:2px;text-transform:uppercase;
  font-family:'Jost',sans-serif;cursor:pointer;border-radius:2px;transition:background .25s;}
.btn-cart-add:hover{background:var(--rose);}
.btn-cart-add.added{background:var(--sage);}

/* MARQUEE REVIEWS */
.reviews-sec{padding:80px 0;background:#F0E8DC;overflow:hidden;}
.reviews-header{text-align:center;padding:0 6%;margin-bottom:50px;}
.marquee-wrap{overflow:hidden;}
.marquee-row{display:flex;gap:18px;animation:ticker 32s linear infinite;}
.marquee-row.rev{animation-direction:reverse;}
.rev-card{flex-shrink:0;width:280px;background:var(--white);border-radius:4px;
  padding:22px 24px;box-shadow:0 4px 24px var(--shadow);}
.rev-stars{color:var(--gold);font-size:13px;letter-spacing:2px;margin-bottom:10px;}
.rev-text{font-size:14px;color:var(--deep);line-height:1.65;font-style:italic;margin-bottom:12px;}
.rev-author{font-size:11px;letter-spacing:2px;text-transform:uppercase;
  color:var(--muted);font-weight:600;}
.rev-verified{font-size:10px;color:var(--sage);margin-top:2px;}

/* WHY US */
.why-sec{padding:90px 6%;}
.why-grid{display:grid;grid-template-columns:1fr 1fr;gap:80px;align-items:center;}
.why-left .section-title{margin-bottom:20px;}
.why-points{display:flex;flex-direction:column;gap:22px;margin-top:30px;}
.why-point{display:flex;gap:18px;align-items:flex-start;}
.why-icon{width:48px;height:48px;border-radius:50%;background:var(--ivory);
  display:flex;align-items:center;justify-content:center;font-size:22px;flex-shrink:0;}
.why-text h4{font-size:16px;font-weight:600;color:var(--deep);margin-bottom:4px;}
.why-text p{font-size:14px;color:var(--muted);line-height:1.65;}
.why-right{display:grid;grid-template-columns:1fr 1fr;gap:16px;}
.why-stat-card{background:var(--card);border:1px solid var(--border);border-radius:4px;
  padding:30px 24px;text-align:center;transition:transform .3s;}
.why-stat-card:hover{transform:translateY(-5px);}
.why-stat-card .big{font-family:'Playfair Display',serif;font-size:44px;font-weight:500;color:var(--rose);}
.why-stat-card .lbl{font-size:11px;letter-spacing:2px;text-transform:uppercase;color:var(--muted);margin-top:6px;}
.why-stat-card.accent{background:var(--deep);}
.why-stat-card.accent .big{color:var(--gold);}
.why-stat-card.accent .lbl{color:var(--blush);}

/* INSTAGRAM */
.insta-sec{padding:80px 6%;background:var(--ivory);text-align:center;}
.insta-grid{display:grid;grid-template-columns:repeat(6,1fr);gap:8px;margin-top:40px;}
.insta-cell{aspect-ratio:1;border-radius:2px;overflow:hidden;cursor:pointer;position:relative;
  background:linear-gradient(145deg,#e8d0b8,#d4b898);
  display:flex;align-items:center;justify-content:center;font-size:36px;transition:transform .3s;}
.insta-cell:hover{transform:scale(.97);}
.insta-cell .insta-overlay{position:absolute;inset:0;background:rgba(44,31,26,.5);
  opacity:0;transition:opacity .3s;display:flex;align-items:center;justify-content:center;color:#fff;font-size:24px;}
.insta-cell:hover .insta-overlay{opacity:1;}

/* PRESS */
.press-sec{padding:60px 6%;border-top:1px solid var(--border);}
.press-inner{display:flex;align-items:center;gap:40px;flex-wrap:wrap;justify-content:center;}
.press-label{font-size:11px;letter-spacing:3px;text-transform:uppercase;color:var(--muted);white-space:nowrap;}
.press-divider{width:1px;height:28px;background:var(--border);}
.press-logos{display:flex;gap:40px;flex-wrap:wrap;align-items:center;justify-content:center;}
.press-logo{font-size:13px;letter-spacing:2px;text-transform:uppercase;color:var(--muted);
  opacity:.55;transition:opacity .2s;font-weight:500;}
.press-logo:hover{opacity:1;}

/* NEWSLETTER */
.newsletter-sec{padding:90px 6%;background:var(--deep);text-align:center;}
.newsletter-sec .section-title{color:var(--cream);}
.newsletter-sec .section-sub{color:var(--blush);opacity:.8;}
.nl-form{display:flex;gap:0;max-width:480px;margin:40px auto 0;border-radius:3px;overflow:hidden;}
.nl-form input{flex:1;padding:16px 22px;border:none;font-family:'Jost',sans-serif;
  font-size:14px;background:rgba(255,255,255,.1);color:var(--cream);outline:none;}
.nl-form input::placeholder{color:rgba(255,255,255,.45);}
.nl-form button{background:var(--rose);color:#fff;border:none;padding:0 28px;
  cursor:pointer;font-family:'Jost',sans-serif;font-size:12px;letter-spacing:2px;
  text-transform:uppercase;transition:background .2s;white-space:nowrap;}
.nl-form button:hover{background:#b05e4a;}

/* ═══════════════════════════════════════════════
   COLLECTION PAGE
══════════════════════════════════════════════ */
.page-hero{background:var(--ivory);padding:60px 6%;text-align:center;
  border-bottom:1px solid var(--border);}
.page-breadcrumb{font-size:12px;color:var(--muted);margin-bottom:16px;letter-spacing:.5px;}
.page-breadcrumb span{color:var(--rose);}
.collection-body{padding:50px 6%;}
.collection-top{display:flex;justify-content:space-between;align-items:center;
  margin-bottom:30px;flex-wrap:wrap;gap:14px;}
.filter-tags{display:flex;gap:8px;flex-wrap:wrap;}
.filter-tag{padding:8px 18px;border:1.5px solid var(--border);border-radius:2px;
  font-size:12px;letter-spacing:1px;text-transform:uppercase;color:var(--muted);
  cursor:pointer;transition:all .2s;background:transparent;}
.filter-tag.active,.filter-tag:hover{background:var(--deep);color:var(--cream);border-color:var(--deep);}
.sort-select{padding:10px 16px;border:1px solid var(--border);border-radius:2px;
  font-family:'Jost',sans-serif;font-size:13px;color:var(--deep);background:var(--white);
  outline:none;cursor:pointer;}

/* ═══════════════════════════════════════════════
   PRODUCT DETAIL
══════════════════════════════════════════════ */
.product-detail-wrap{padding:60px 6%;}
.product-detail-grid{display:grid;grid-template-columns:1fr 1fr;gap:70px;align-items:start;}
.pd-imgs{position:sticky;top:90px;}
.pd-main-img{border-radius:4px;background:linear-gradient(145deg,#f0e0cc,#dfc8ad);
  height:500px;display:flex;align-items:center;justify-content:center;font-size:120px;
  margin-bottom:12px;overflow:hidden;}
.pd-thumbs{display:flex;gap:10px;}
.pd-thumb{width:80px;height:80px;border-radius:3px;border:2px solid transparent;
  background:linear-gradient(145deg,#e8d4bc,#d4b89a);
  display:flex;align-items:center;justify-content:center;font-size:28px;
  cursor:pointer;transition:border-color .2s;}
.pd-thumb.active,.pd-thumb:hover{border-color:var(--rose);}
.pd-info{}
.pd-category{font-size:11px;letter-spacing:3px;text-transform:uppercase;color:var(--sage);margin-bottom:10px;}
.pd-title{font-family:'Playfair Display',serif;font-size:clamp(28px,3vw,42px);
  font-weight:500;line-height:1.1;margin-bottom:14px;}
.pd-stars{color:var(--gold);font-size:14px;margin-bottom:20px;}
.pd-stars span{color:var(--muted);font-size:13px;margin-left:6px;}
.pd-price-row{display:flex;align-items:center;gap:14px;margin-bottom:24px;}
.pd-price-now{font-size:34px;font-weight:600;color:var(--rose);}
.pd-price-was{font-size:20px;text-decoration:line-through;color:var(--muted);}
.pd-save{background:#FFF0EB;color:var(--rose);padding:6px 14px;border-radius:2px;
  font-size:13px;font-weight:600;}
.pd-desc{font-size:15px;color:var(--muted);line-height:1.8;margin-bottom:28px;}
.pd-variants h4{font-size:12px;letter-spacing:2px;text-transform:uppercase;
  color:var(--muted);margin-bottom:12px;}
.pd-variant-btns{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:26px;}
.pd-variant-btn{padding:10px 20px;border:1.5px solid var(--border);border-radius:2px;
  font-size:13px;cursor:pointer;transition:all .2s;background:transparent;
  font-family:'Jost',sans-serif;}
.pd-variant-btn.active,.pd-variant-btn:hover{border-color:var(--deep);background:var(--deep);color:var(--cream);}
.pd-qty{display:flex;align-items:center;gap:0;margin-bottom:26px;
  border:1px solid var(--border);border-radius:2px;width:fit-content;}
.pd-qty button{width:42px;height:46px;border:none;background:transparent;
  font-size:20px;cursor:pointer;transition:background .2s;}
.pd-qty button:hover{background:var(--ivory);}
.pd-qty input{width:60px;height:46px;border:none;border-left:1px solid var(--border);
  border-right:1px solid var(--border);text-align:center;font-size:16px;
  font-family:'Jost',sans-serif;outline:none;}
.pd-actions{display:flex;gap:12px;margin-bottom:28px;flex-wrap:wrap;}
.pd-actions .btn{flex:1;min-width:180px;text-align:center;}
.pd-perks{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-bottom:28px;}
.pd-perk{display:flex;gap:10px;align-items:center;font-size:13px;color:var(--muted);
  background:var(--ivory);padding:12px 16px;border-radius:3px;}
.pd-perk .icon{font-size:18px;}
.pd-accordion{border
