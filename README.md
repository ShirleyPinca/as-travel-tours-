# as-travel-tours-<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>A&S Travel & Tours — Facebook Page</title>
<link href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800;900&family=Playfair+Display:wght@800;900&display=swap" rel="stylesheet"/>
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --fb:#1877F2;--fb-dark:#0d5fd4;--fb-light:#E7F3FF;
  --red:#E53935;--gold:#F5A623;--gold2:#FFD166;
  --night:#0B1D3A;--ink:#1C1C1E;--gray:#6B7A99;
  --line:#E4E6EB;--bg:#F0F2F5;--white:#fff;
  --green:#22C55E;--teal:#0EA5E9;--purple:#8B5CF6;
}
body{font-family:'Nunito',sans-serif;background:var(--bg);color:var(--ink);min-height:100vh}

/* ─── FB TOPBAR ─── */
.fb-topbar{
  position:sticky;top:0;z-index:100;
  background:var(--fb);
  display:flex;align-items:center;justify-content:space-between;
  padding:0 16px;height:56px;
  box-shadow:0 2px 8px rgba(0,0,0,.2);
}
.fb-logo{font-size:28px;font-weight:900;color:#fff;letter-spacing:-1px}
.fb-logo span{font-size:14px;font-weight:600;opacity:.8;margin-left:6px}
.fb-nav{display:flex;gap:6px}
.fb-nav-btn{
  background:rgba(255,255,255,.15);border:none;cursor:pointer;
  color:#fff;font-size:12px;font-weight:700;
  padding:6px 14px;border-radius:6px;
  transition:background .15s;
}
.fb-nav-btn:hover{background:rgba(255,255,255,.25)}
.fb-nav-btn.active{background:rgba(255,255,255,.3)}

/* ─── COVER ─── */
.cover-wrap{position:relative;background:var(--night);overflow:hidden}
.cover-gradient{
  width:100%;height:320px;
  background:linear-gradient(135deg,#0B1D3A 0%,#1A3460 40%,#1877F2 70%,#F5A623 100%);
  display:flex;align-items:center;justify-content:center;
  position:relative;overflow:hidden;
}
.cover-pattern{
  position:absolute;inset:0;
  background-image:radial-gradient(circle at 20% 50%,rgba(245,166,35,.15) 0%,transparent 50%),
    radial-gradient(circle at 80% 20%,rgba(24,119,242,.2) 0%,transparent 50%);
}
.cover-text{
  position:relative;z-index:2;text-align:center;color:#fff;padding:20px;
}
.cover-text h1{
  font-family:'Playfair Display',serif;
  font-size:clamp(24px,5vw,52px);font-weight:900;
  line-height:1.1;text-shadow:0 2px 12px rgba(0,0,0,.4);
}
.cover-text h1 em{color:var(--gold);font-style:normal}
.cover-text p{font-size:15px;margin-top:8px;opacity:.85;font-weight:600}
.cover-badges{display:flex;gap:8px;justify-content:center;margin-top:14px;flex-wrap:wrap}
.cover-badge{
  background:rgba(255,255,255,.18);backdrop-filter:blur(4px);
  border:1px solid rgba(255,255,255,.3);
  color:#fff;font-size:12px;font-weight:700;
  padding:5px 14px;border-radius:20px;
}
.cover-bottom{position:relative;background:var(--white)}
.profile-row{
  max-width:900px;margin:0 auto;
  display:flex;align-items:flex-end;gap:16px;
  padding:0 20px;position:relative;top:-36px;
}
.profile-pic{
  width:120px;height:120px;border-radius:50%;
  border:4px solid var(--white);
  background:var(--white);
  display:flex;align-items:center;justify-content:center;
  box-shadow:0 4px 20px rgba(0,0,0,.2);
  flex-shrink:0;overflow:hidden;font-size:52px;
}
.profile-info{flex:1;padding-bottom:8px}
.profile-info h2{font-size:22px;font-weight:900;color:var(--night);line-height:1.2}
.profile-info p{font-size:13px;color:var(--gray);font-weight:600;margin-top:2px}
.profile-btns{display:flex;gap:8px;margin-top:10px;flex-wrap:wrap}
.btn-primary{
  background:var(--fb);color:#fff;
  border:none;cursor:pointer;
  padding:8px 20px;border-radius:8px;
  font-size:14px;font-weight:800;
  display:flex;align-items:center;gap:6px;
  transition:background .15s;
}
.btn-primary:hover{background:var(--fb-dark)}
.btn-outline{
  background:var(--line);color:var(--night);
  border:none;cursor:pointer;
  padding:8px 20px;border-radius:8px;
  font-size:14px;font-weight:700;
  transition:background .15s;
}
.btn-outline:hover{background:#d8dadf}

/* ─── PAGE TABS ─── */
.page-tabs{
  background:var(--white);border-top:1px solid var(--line);
  border-bottom:1px solid var(--line);
  position:sticky;top:56px;z-index:90;
}
.page-tabs-inner{
  max-width:900px;margin:0 auto;
  display:flex;gap:2px;padding:0 16px;overflow-x:auto;
}
.page-tab{
  padding:14px 16px;
  font-size:14px;font-weight:700;color:var(--gray);
  border:none;background:none;cursor:pointer;
  border-bottom:3px solid transparent;
  white-space:nowrap;transition:all .15s;
}
.page-tab:hover{color:var(--fb)}
.page-tab.active{color:var(--fb);border-bottom-color:var(--fb)}

/* ─── LAYOUT ─── */
.page-body{max-width:900px;margin:0 auto;padding:20px 16px 60px;display:grid;grid-template-columns:1fr 340px;gap:20px}
@media(max-width:720px){.page-body{grid-template-columns:1fr}}

/* ─── ABOUT CARD ─── */
.sidebar{}
.card{background:var(--white);border-radius:12px;border:1px solid var(--line);overflow:hidden;margin-bottom:16px}
.card-head{padding:16px 16px 10px;font-size:17px;font-weight:800;color:var(--night);border-bottom:1px solid var(--line)}
.card-body{padding:14px 16px}
.about-item{display:flex;align-items:flex-start;gap:10px;padding:6px 0;font-size:14px;color:var(--ink)}
.about-icon{font-size:18px;flex-shrink:0;width:24px;text-align:center;margin-top:1px}
.about-label{font-weight:700;color:var(--gray);font-size:12px;display:block}
.stats-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px;padding:14px 16px}
.stat-box{background:var(--fb-light);border-radius:10px;padding:14px;text-align:center}
.stat-box .num{font-size:24px;font-weight:900;color:var(--fb);font-family:'Playfair Display',serif}
.stat-box .lbl{font-size:11px;font-weight:700;color:var(--gray);text-transform:uppercase;letter-spacing:.5px}

/* ─── POSTS ─── */
.main-feed{}
.post-box{
  background:var(--white);border-radius:12px;border:1px solid var(--line);
  padding:16px;margin-bottom:16px;
}
.post-header{display:flex;align-items:center;gap:10px;margin-bottom:12px}
.post-avatar{
  width:42px;height:42px;border-radius:50%;
  background:linear-gradient(135deg,var(--fb),var(--gold));
  display:flex;align-items:center;justify-content:center;
  font-size:15px;font-weight:900;color:#fff;flex-shrink:0;font-family:'Playfair Display',serif;
}
.post-meta h4{font-size:15px;font-weight:800;color:var(--night)}
.post-meta p{font-size:12px;color:var(--gray);font-weight:600}
.post-text{font-size:14px;line-height:1.65;color:var(--ink);margin-bottom:14px;white-space:pre-wrap}
.post-actions{
  display:flex;gap:0;border-top:1px solid var(--line);margin-top:12px;padding-top:10px;
}
.post-action-btn{
  flex:1;display:flex;align-items:center;justify-content:center;gap:6px;
  padding:8px;border-radius:8px;cursor:pointer;
  font-size:13px;font-weight:700;color:var(--gray);
  border:none;background:none;transition:background .15s;
}
.post-action-btn:hover{background:var(--bg)}

/* ─── TOUR PACKAGE SECTION ─── */
.section-title{
  font-size:20px;font-weight:900;color:var(--night);
  margin-bottom:14px;padding-bottom:10px;
  border-bottom:3px solid var(--fb);
  display:flex;align-items:center;gap:8px;
}
.pkg-grid{display:grid;grid-template-columns:1fr 1fr;gap:14px}
@media(max-width:500px){.pkg-grid{grid-template-columns:1fr}}
.pkg-card{
  background:var(--white);border:1px solid var(--line);border-radius:14px;
  overflow:hidden;cursor:pointer;
  transition:box-shadow .2s,transform .2s;
}
.pkg-card:hover{box-shadow:0 8px 28px rgba(0,0,0,.12);transform:translateY(-2px)}
.pkg-banner{
  height:110px;display:flex;align-items:center;justify-content:center;
  position:relative;overflow:hidden;
}
.pkg-banner-emoji{font-size:48px;z-index:1}
.pkg-tag{
  position:absolute;top:8px;right:8px;
  background:var(--red);color:#fff;
  font-size:10px;font-weight:800;padding:3px 8px;border-radius:12px;
  text-transform:uppercase;letter-spacing:.5px;
}
.pkg-tag.green{background:var(--green)}
.pkg-tag.gold{background:var(--gold);color:var(--night)}
.pkg-info{padding:12px}
.pkg-dest{font-size:15px;font-weight:900;color:var(--night);line-height:1.2}
.pkg-name{font-size:12px;color:var(--gray);font-weight:600;margin-top:2px}
.pkg-price{
  font-size:17px;font-weight:900;color:var(--red);margin-top:6px;
}
.pkg-price span{font-size:11px;font-weight:700;color:var(--gray)}
.pkg-pills{display:flex;gap:5px;flex-wrap:wrap;margin-top:6px}
.pkg-pill{
  background:var(--fb-light);color:var(--fb);
  font-size:10px;font-weight:700;padding:2px 8px;border-radius:10px;
}
.pkg-btn{
  width:100%;background:var(--fb);color:#fff;
  border:none;cursor:pointer;padding:9px;
  font-size:13px;font-weight:800;
  border-radius:0 0 14px 14px;
  transition:background .15s;
  margin-top:10px;
}
.pkg-btn:hover{background:var(--fb-dark)}

/* ─── MODAL ─── */
.modal-overlay{
  display:none;position:fixed;inset:0;
  background:rgba(0,0,0,.65);z-index:200;
  align-items:center;justify-content:center;
  padding:20px;backdrop-filter:blur(4px);
}
.modal-overlay.open{display:flex}
.modal{
  background:var(--white);border-radius:16px;
  width:100%;max-width:620px;max-height:90vh;
  overflow:hidden;display:flex;flex-direction:column;
  box-shadow:0 24px 80px rgba(0,0,0,.3);
}
.modal-hdr{
  padding:18px 20px;
  display:flex;align-items:center;gap:12px;
  border-bottom:1px solid var(--line);
  position:relative;
}
.modal-hdr-banner{
  width:54px;height:54px;border-radius:12px;
  display:flex;align-items:center;justify-content:center;
  font-size:26px;flex-shrink:0;
}
.modal-hdr h3{font-size:18px;font-weight:900;color:var(--night);line-height:1.2}
.modal-hdr p{font-size:13px;color:var(--gray);font-weight:600}
.modal-close{
  position:absolute;top:14px;right:14px;
  width:32px;height:32px;border-radius:50%;
  background:var(--line);border:none;cursor:pointer;
  font-size:17px;display:flex;align-items:center;justify-content:center;
  color:var(--gray);
}
.modal-close:hover{background:#fca5a5;color:var(--red)}
.modal-body{padding:20px;overflow-y:auto;flex:1}
.modal-price-box{
  background:linear-gradient(135deg,var(--red),#ff6b6b);
  border-radius:12px;padding:16px;color:#fff;
  text-align:center;margin-bottom:18px;
}
.modal-price-box .big-price{font-size:36px;font-weight:900;font-family:'Playfair Display',serif}
.modal-price-box .per{font-size:13px;opacity:.85;font-weight:700}
.section-hdr{font-size:14px;font-weight:800;color:var(--night);margin:14px 0 8px;text-transform:uppercase;letter-spacing:.5px}
.inc-list{list-style:none;display:flex;flex-direction:column;gap:6px}
.inc-list li{font-size:13px;display:flex;gap:8px;align-items:flex-start;line-height:1.5}
.inc-list li::before{content:'✅';flex-shrink:0;font-size:12px;margin-top:1px}
.exc-list li::before{content:'❌'}
.dates-wrap{display:flex;flex-wrap:wrap;gap:6px}
.date-chip{
  background:var(--fb-light);color:var(--fb);
  font-size:11px;font-weight:700;padding:4px 10px;border-radius:12px;
}
.days-grid{display:grid;grid-template-columns:1fr;gap:8px}
.day-row{
  background:var(--bg);border-radius:10px;padding:12px;
  display:flex;gap:10px;align-items:flex-start;
}
.day-num{
  background:var(--fb);color:#fff;
  font-size:11px;font-weight:900;padding:3px 8px;border-radius:8px;
  white-space:nowrap;flex-shrink:0;
}
.day-text{font-size:12px;line-height:1.6;color:var(--ink)}
.modal-footer{
  padding:14px 20px;border-top:1px solid var(--line);
  display:flex;gap:10px;
}
.mftr-btn{
  flex:1;padding:12px;border-radius:10px;border:none;
  font-size:14px;font-weight:800;cursor:pointer;
  transition:all .15s;
}
.mftr-btn-book{background:var(--fb);color:#fff}
.mftr-btn-book:hover{background:var(--fb-dark)}
.mftr-btn-msg{background:var(--line);color:var(--night)}
.mftr-btn-msg:hover{background:#d8dadf}

/* ─── STORIES ─── */
.stories-wrap{
  display:flex;gap:10px;overflow-x:auto;padding-bottom:4px;
  margin-bottom:18px;
}
.stories-wrap::-webkit-scrollbar{height:4px}
.stories-wrap::-webkit-scrollbar-thumb{background:var(--line);border-radius:4px}
.story{
  flex-shrink:0;width:100px;height:130px;border-radius:14px;
  overflow:hidden;cursor:pointer;position:relative;
  border:3px solid var(--fb);
  display:flex;align-items:flex-end;
  transition:transform .15s;
}
.story:hover{transform:scale(1.03)}
.story-bg{
  position:absolute;inset:0;
  display:flex;align-items:center;justify-content:center;
  font-size:40px;
}
.story-label{
  position:relative;z-index:1;width:100%;
  background:linear-gradient(transparent,rgba(0,0,0,.7));
  color:#fff;font-size:10px;font-weight:800;
  padding:20px 6px 6px;text-align:center;line-height:1.2;
}

/* ─── PHOTO GALLERY ─── */
.photo-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:4px;border-radius:12px;overflow:hidden;margin-bottom:18px}
.photo-item{
  aspect-ratio:1;background:var(--line);
  display:flex;align-items:center;justify-content:center;
  font-size:32px;cursor:pointer;transition:opacity .15s;
  overflow:hidden;
}
.photo-item:hover{opacity:.85}

/* ─── CONTACT CARD ─── */
.contact-card{
  background:linear-gradient(135deg,var(--night),var(--fb));
  border-radius:14px;padding:20px;color:#fff;margin-bottom:16px;
}
.contact-card h3{font-size:17px;font-weight:900;margin-bottom:12px}
.contact-item{display:flex;align-items:center;gap:8px;padding:5px 0;font-size:13px;font-weight:600}
.contact-icon{font-size:16px;width:22px}
.msg-btn-big{
  width:100%;background:var(--gold);color:var(--night);
  border:none;cursor:pointer;padding:13px;border-radius:10px;
  font-size:15px;font-weight:900;margin-top:12px;
  transition:background .15s;display:flex;align-items:center;justify-content:center;gap:6px;
}
.msg-btn-big:hover{background:var(--gold2)}

/* ─── SCROLL TOAST ─── */
.toast{
  position:fixed;bottom:24px;left:50%;transform:translateX(-50%) translateY(60px);
  background:var(--night);color:#fff;
  padding:12px 24px;border-radius:30px;
  font-size:14px;font-weight:700;
  box-shadow:0 8px 24px rgba(0,0,0,.25);
  opacity:0;transition:all .3s;z-index:300;
  display:flex;align-items:center;gap:8px;
  white-space:nowrap;
}
.toast.show{opacity:1;transform:translateX(-50%) translateY(0)}

/* scrollbar */
::-webkit-scrollbar{width:6px}
::-webkit-scrollbar-thumb{background:var(--line);border-radius:4px}
</style>
</head>
<body>

<!-- FB TOPBAR -->
<div class="fb-topbar">
  <div>
    <div class="fb-logo">f <span>A&S Travel & Tours</span></div>
  </div>
  <div class="fb-nav">
    <button class="fb-nav-btn active">🏠 Home</button>
    <button class="fb-nav-btn">✈️ Tours</button>
    <button class="fb-nav-btn">📞 Contact</button>
    <button class="fb-nav-btn" onclick="showToast('💬 Opening Messenger…')">💬 Message</button>
  </div>
</div>

<!-- COVER -->
<div class="cover-wrap">
  <div class="cover-gradient">
    <div class="cover-pattern"></div>
    <div class="cover-text">
      <h1>A&S Travel <em>&</em> Tours<br/>Tourist Transport Services</h1>
      <p>✈️ Philippines · Vietnam · China · Europe · Africa and Beyond!</p>
      <div class="cover-badges">
        <span class="cover-badge">🇵🇭 Domestic Tours</span>
        <span class="cover-badge">🌏 International Tours</span>
        <span class="cover-badge">🚐 Transport Services</span>
        <span class="cover-badge">⭐ Trusted & Reliable</span>
      </div>
    </div>
  </div>
  <div class="cover-bottom">
    <div class="profile-row">
      <div class="profile-pic" style="background:#fff">
        <img src="/mnt/user-data/uploads/1000001406.jpg" style="width:100%;height:100%;object-fit:cover;border-radius:50%" onerror="this.parentElement.innerHTML='❤️'"/>
      </div>
      <div class="profile-info">
        <h2>A&S Travel & Tours Tourist Transport Services</h2>
        <p>🏢 Travel Agency · Transportation Service · Tour Operator</p>
        <div class="profile-btns">
          <button class="btn-primary" onclick="showToast('📩 Opening message box…')">✉️ Send Message</button>
          <button class="btn-primary" style="background:var(--green)" onclick="showToast('📞 Calling A&S Travel…')">📞 Call Now</button>
          <button class="btn-outline" onclick="showToast('👍 You liked A&S Travel & Tours!')">👍 Like Page</button>
          <button class="btn-outline">⋯ More</button>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- PAGE TABS -->
<div class="page-tabs">
  <div class="page-tabs-inner">
    <button class="page-tab active">Posts</button>
    <button class="page-tab">About</button>
    <button class="page-tab">Photos</button>
    <button class="page-tab">Tour Packages</button>
    <button class="page-tab">Reviews</button>
    <button class="page-tab">Videos</button>
  </div>
</div>

<!-- BODY -->
<div class="page-body">

  <!-- ─── MAIN FEED ─── -->
  <div class="main-feed">

    <!-- STORIES -->
    <div class="stories-wrap">
      <div class="story" style="background:linear-gradient(135deg,#0B1D3A,#1877F2)">
        <div class="story-bg">🏖️</div>
        <div class="story-label">Boracay</div>
      </div>
      <div class="story" style="background:linear-gradient(135deg,#b91c1c,#f97316)">
        <div class="story-bg">🇻🇳</div>
        <div class="story-label">Vietnam</div>
      </div>
      <div class="story" style="background:linear-gradient(135deg,#065f46,#10b981)">
        <div class="story-bg">🌴</div>
        <div class="story-label">El Nido</div>
      </div>
      <div class="story" style="background:linear-gradient(135deg,#7c3aed,#a78bfa)">
        <div class="story-bg">🏯</div>
        <div class="story-label">China</div>
      </div>
      <div class="story" style="background:linear-gradient(135deg,#92400e,#f59e0b)">
        <div class="story-bg">🦁</div>
        <div class="story-label">Africa</div>
      </div>
      <div class="story" style="background:linear-gradient(135deg,#1e3a5f,#3b82f6)">
        <div class="story-bg">⛪</div>
        <div class="story-label">Europe</div>
      </div>
      <div class="story" style="background:linear-gradient(135deg,#134e4a,#0d9488)">
        <div class="story-bg">🏝️</div>
        <div class="story-label">Batanes</div>
      </div>
      <div class="story" style="background:linear-gradient(135deg,#7f1d1d,#ef4444)">
        <div class="story-bg">🥭</div>
        <div class="story-label">Iloilo</div>
      </div>
    </div>

    <!-- PINNED POST -->
    <div class="post-box" style="border-left:4px solid var(--gold)">
      <div class="post-header">
        <div class="post-avatar">A&S</div>
        <div class="post-meta">
          <h4>A&S Travel & Tours Tourist Transport Services</h4>
          <p>📌 Pinned Post · 🌐 Public</p>
        </div>
      </div>
      <div class="post-text">📌 WELCOME TO A&S TRAVEL & TOURS TOURIST TRANSPORT SERVICES! 📌

Thank you for visiting our official Facebook page! 🙏✈️

We are your TRUSTED travel and transportation partner — offering safe, comfortable, and affordable travel experiences for individuals, families, and groups across the Philippines and beyond! 🌏

📋 OUR SERVICES:
✅ Airport Transfers & Pick-up
✅ Domestic Tour Packages (Boracay, El Nido, Batanes, Iloilo-Guimaras & more!)
✅ International Tours (Vietnam, China, Europe, Africa & more!)
✅ Group Transportation & Corporate Outings
✅ Custom Tour Packages & Itineraries
✅ Hotel & Accommodation Bookings

💬 Message us on Facebook — we respond FAST!
📲 Available 7 days a week

We look forward to traveling WITH YOU! 🌍❤️

#ASTravelTours #TransportationService #TravelAndTours #BookNow #TrustedTravel</div>
      <div class="post-actions">
        <button class="post-action-btn" onclick="showToast('👍 You liked this post!')">👍 Like</button>
        <button class="post-action-btn" onclick="showToast('💬 Opening comments…')">💬 Comment</button>
        <button class="post-action-btn" onclick="showToast('↗️ Post link copied!')">↗️ Share</button>
      </div>
    </div>

    <!-- TOUR PACKAGES HEADER -->
    <div class="section-title">✈️ Our Tour Packages 2026–2027</div>

    <!-- DOMESTIC -->
    <div style="font-size:13px;font-weight:800;color:var(--gray);text-transform:uppercase;letter-spacing:1px;margin-bottom:10px">🇵🇭 Domestic Packages</div>
    <div class="pkg-grid" style="margin-bottom:20px">

      <div class="pkg-card" onclick="openModal('boracay')">
        <div class="pkg-banner" style="background:linear-gradient(135deg,#0ea5e9,#38bdf8,#7dd3fc)">
          <div class="pkg-banner-emoji">🏖️</div>
          <span class="pkg-tag gold">ALL IN</span>
        </div>
        <div class="pkg-info">
          <div class="pkg-dest">GO BORACAY</div>
          <div class="pkg-name">2026–2027 · 3N4D</div>
          <div class="pkg-price">₱12,888 <span>/ pax</span></div>
          <div class="pkg-pills"><span class="pkg-pill">Roundtrip Air</span><span class="pkg-pill">Hotel</span><span class="pkg-pill">Transfers</span></div>
        </div>
        <button class="pkg-btn">View Package →</button>
      </div>

      <div class="pkg-card" onclick="openModal('elnido')">
        <div class="pkg-banner" style="background:linear-gradient(135deg,#059669,#10b981,#6ee7b7)">
          <div class="pkg-banner-emoji">🌊</div>
          <span class="pkg-tag">2 Island Hop</span>
        </div>
        <div class="pkg-info">
          <div class="pkg-dest">GO EL NIDO</div>
          <div class="pkg-name">2026–2027 · 3N4D</div>
          <div class="pkg-price">₱14,888 <span>/ pax</span></div>
          <div class="pkg-pills"><span class="pkg-pill">Roundtrip Air</span><span class="pkg-pill">Hotel</span><span class="pkg-pill">Tour A&C</span></div>
        </div>
        <button class="pkg-btn">View Package →</button>
      </div>

      <div class="pkg-card" onclick="openModal('iloilo')">
        <div class="pkg-banner" style="background:linear-gradient(135deg,#d97706,#f59e0b,#fcd34d)">
          <div class="pkg-banner-emoji">🥭</div>
          <span class="pkg-tag green">Island Hop</span>
        </div>
        <div class="pkg-info">
          <div class="pkg-dest">ILOILO–GUIMARAS</div>
          <div class="pkg-name">2026–2027 · 4D3N</div>
          <div class="pkg-price">₱15,888 <span>/ pax</span></div>
          <div class="pkg-pills"><span class="pkg-pill">Roundtrip Air</span><span class="pkg-pill">Pumpboat</span><span class="pkg-pill">Meals</span></div>
        </div>
        <button class="pkg-btn">View Package →</button>
      </div>

      <div class="pkg-card" onclick="openModal('batanes')">
        <div class="pkg-banner" style="background:linear-gradient(135deg,#16a34a,#22c55e,#86efac)">
          <div class="pkg-banner-emoji">🏔️</div>
          <span class="pkg-tag gold">ALL IN!</span>
        </div>
        <div class="pkg-info">
          <div class="pkg-dest">GO BATANES</div>
          <div class="pkg-name">2026–2027 · 4D3N via Clark</div>
          <div class="pkg-price">₱28,888 <span>/ pax</span></div>
          <div class="pkg-pills"><span class="pkg-pill">PAL Airlines</span><span class="pkg-pill">Ins. Incl.</span><span class="pkg-pill">No Excl.</span></div>
        </div>
        <button class="pkg-btn">View Package →</button>
      </div>

    </div>

    <!-- INTERNATIONAL -->
    <div style="font-size:13px;font-weight:800;color:var(--gray);text-transform:uppercase;letter-spacing:1px;margin-bottom:10px">🌏 International Packages</div>
    <div class="pkg-grid" style="margin-bottom:20px">

      <div class="pkg-card" onclick="openModal('vnrose')">
        <div class="pkg-banner" style="background:linear-gradient(135deg,#be123c,#f43f5e,#fb7185)">
          <div class="pkg-banner-emoji">🌹</div>
          <span class="pkg-tag">Premium</span>
        </div>
        <div class="pkg-info">
          <div class="pkg-dest">VIETNAM ROSE RELOADED</div>
          <div class="pkg-name">Hanoi·Sapa·Ha Long Bay · 6D5N</div>
          <div class="pkg-price">₱58,888 <span>/ pax</span></div>
          <div class="pkg-pills"><span class="pkg-pill">5★ Cruise</span><span class="pkg-pill">No Shopping</span></div>
        </div>
        <button class="pkg-btn">View Package →</button>
      </div>

      <div class="pkg-card" onclick="openModal('vnrose2')">
        <div class="pkg-banner" style="background:linear-gradient(135deg,#b45309,#f97316,#fdba74)">
          <div class="pkg-banner-emoji">🏮</div>
          <span class="pkg-tag">Premium</span>
        </div>
        <div class="pkg-info">
          <div class="pkg-dest">VIETNAM ROSE 2.0</div>
          <div class="pkg-name">Da Nang·Hoi An·Hue · 4D3N</div>
          <div class="pkg-price">₱38,888 <span>/ pax</span></div>
          <div class="pkg-pills"><span class="pkg-pill">5★ Hoi An Hotel</span><span class="pkg-pill">Full Board</span></div>
        </div>
        <button class="pkg-btn">View Package →</button>
      </div>

      <div class="pkg-card" onclick="openModal('vnrose3')">
        <div class="pkg-banner" style="background:linear-gradient(135deg,#7c3aed,#a78bfa,#c4b5fd)">
          <div class="pkg-banner-emoji">⛩️</div>
          <span class="pkg-tag">Premium</span>
        </div>
        <div class="pkg-info">
          <div class="pkg-dest">VIETNAM ROSE 3.0</div>
          <div class="pkg-name">Hanoi·Sapa·Ninh Binh · 5D4N</div>
          <div class="pkg-price">₱38,888 <span>/ pax</span></div>
          <div class="pkg-pills"><span class="pkg-pill">Silk Path 5★</span><span class="pkg-pill">No Detours</span></div>
        </div>
        <button class="pkg-btn">View Package →</button>
      </div>

      <div class="pkg-card" onclick="openModal('danang')">
        <div class="pkg-banner" style="background:linear-gradient(135deg,#0369a1,#0ea5e9,#7dd3fc)">
          <div class="pkg-banner-emoji">🌉</div>
          <span class="pkg-tag green">Special Offer</span>
        </div>
        <div class="pkg-info">
          <div class="pkg-dest">VIETNAM DA NANG</div>
          <div class="pkg-name">4D3N via AirAsia</div>
          <div class="pkg-price">₱21,888 <span>/ pax</span></div>
          <div class="pkg-pills"><span class="pkg-pill">Golden Bridge</span><span class="pkg-pill">Ba Na Hills</span></div>
        </div>
        <button class="pkg-btn">View Package →</button>
      </div>

      <div class="pkg-card" onclick="openModal('danang2')">
        <div class="pkg-banner" style="background:linear-gradient(135deg,#9d174d,#ec4899,#f9a8d4)">
          <div class="pkg-banner-emoji">🚡</div>
          <span class="pkg-tag">Charter</span>
        </div>
        <div class="pkg-info">
          <div class="pkg-dest">DA NANG CHARTER</div>
          <div class="pkg-name">6D4N via VietJet ALL IN</div>
          <div class="pkg-price">₱23,888 <span>/ pax</span></div>
          <div class="pkg-pills"><span class="pkg-pill">Charter Flight</span><span class="pkg-pill">7 Meals</span></div>
        </div>
        <button class="pkg-btn">View Package →</button>
      </div>

      <div class="pkg-card" onclick="openModal('chongqing')">
        <div class="pkg-banner" style="background:linear-gradient(135deg,#92400e,#d97706,#fbbf24)">
          <div class="pkg-banner-emoji">🏮</div>
          <span class="pkg-tag">Wo Ai Ni</span>
        </div>
        <div class="pkg-info">
          <div class="pkg-dest">CHONGQING CHINA</div>
          <div class="pkg-name">5D4N via Xiamen Air</div>
          <div class="pkg-price">$888 <span>/ pax</span></div>
          <div class="pkg-pills"><span class="pkg-pill">23kg Baggage</span><span class="pkg-pill">No Tourist Traps</span></div>
        </div>
        <button class="pkg-btn">View Package →</button>
      </div>

      <div class="pkg-card" onclick="openModal('avatar')">
        <div class="pkg-banner" style="background:linear-gradient(135deg,#064e3b,#059669,#34d399)">
          <div class="pkg-banner-emoji">🗻</div>
          <span class="pkg-tag">Charter</span>
        </div>
        <div class="pkg-info">
          <div class="pkg-dest">AVATAR FURONG</div>
          <div class="pkg-name">Mini Venice · 5D4N Charter</div>
          <div class="pkg-price">$369 <span>/ pax</span></div>
          <div class="pkg-pills"><span class="pkg-pill">Direct Flight</span><span class="pkg-pill">5★ Hotels</span></div>
        </div>
        <button class="pkg-btn">View Package →</button>
      </div>

      <div class="pkg-card" onclick="openModal('beijing')">
        <div class="pkg-banner" style="background:linear-gradient(135deg,#1e3a5f,#1877F2,#60a5fa)">
          <div class="pkg-banner-emoji">🏯</div>
          <span class="pkg-tag gold">ALL IN</span>
        </div>
        <div class="pkg-info">
          <div class="pkg-dest">BEIJING AVATAR</div>
          <div class="pkg-name">8D7N · Great Wall + Zhangjiajie</div>
          <div class="pkg-price">$699 <span>/ pax</span></div>
          <div class="pkg-pills"><span class="pkg-pill">Air China</span><span class="pkg-pill">5★ Hotels</span><span class="pkg-pill">Visa Incl.</span></div>
        </div>
        <button class="pkg-btn">View Package →</button>
      </div>

      <div class="pkg-card" onclick="openModal('europe')">
        <div class="pkg-banner" style="background:linear-gradient(135deg,#312e81,#4338ca,#818cf8)">
          <div class="pkg-banner-emoji">⛪</div>
          <span class="pkg-tag">Pilgrimage</span>
        </div>
        <div class="pkg-info">
          <div class="pkg-dest">HAIL HOLY QUEEN</div>
          <div class="pkg-name">Italy·France·Spain·Portugal · 17D</div>
          <div class="pkg-price">$4,588 <span>/ pax</span></div>
          <div class="pkg-pills"><span class="pkg-pill">Emirates</span><span class="pkg-pill">15 Nights Hotel</span></div>
        </div>
        <button class="pkg-btn">View Package →</button>
      </div>

      <div class="pkg-card" onclick="openModal('africa')">
        <div class="pkg-banner" style="background:linear-gradient(135deg,#78350f,#b45309,#f59e0b)">
          <div class="pkg-banner-emoji">🦁</div>
          <span class="pkg-tag">Safari</span>
        </div>
        <div class="pkg-info">
          <div class="pkg-dest">WAKANDA AFRICA</div>
          <div class="pkg-name">South Africa · 10D9N</div>
          <div class="pkg-price">$3,488 <span>/ pax</span></div>
          <div class="pkg-pills"><span class="pkg-pill">Safari Drives</span><span class="pkg-pill">Luxury Lodge</span></div>
        </div>
        <button class="pkg-btn">View Package →</button>
      </div>

    </div>

    <!-- PROMO POST -->
    <div class="post-box">
      <div class="post-header">
        <div class="post-avatar">A&S</div>
        <div class="post-meta">
          <h4>A&S Travel & Tours Tourist Transport Services</h4>
          <p>🔥 Promo · 🌐 Public</p>
        </div>
      </div>
      <div class="post-text">🔥 BOOK NOW AND SAVE BIG! 🔥

Whether you dream of the white sands of Boracay 🏖️, the limestone cliffs of El Nido 🌊, the mango paradise of Guimaras 🥭, the wild landscapes of Batanes 🏔️, or the magical cities of Vietnam 🇻🇳, China 🇨🇳, Europe 🇪🇺, and Africa 🦁 — A&S Travel & Tours has the PERFECT package for you!

✅ Affordable Rates
✅ Flexible Payment Options
✅ Licensed & Professional Drivers & Guides
✅ Safe & Comfortable Travel
✅ Fully Loaded Inclusions

📩 Message us NOW to inquire and book your dream trip!
👇 TAG a friend you want to travel with! 👇

#ASTravelTours #BookNow #TravelPH #InternationalTours #AffordableTravel #TransportServices</div>
      <div class="post-actions">
        <button class="post-action-btn" onclick="showToast('👍 You liked this post!')">👍 Like</button>
        <button class="post-action-btn" onclick="showToast('💬 Opening comments…')">💬 Comment</button>
        <button class="post-action-btn" onclick="showToast('↗️ Link copied!')">↗️ Share</button>
      </div>
    </div>

  </div><!-- end main-feed -->

  <!-- ─── SIDEBAR ─── -->
  <div class="sidebar">

    <!-- CONTACT -->
    <div class="contact-card">
      <h3>📞 Contact & Book Now</h3>
      <div class="contact-item"><span class="contact-icon">💬</span> Facebook Messenger</div>
      <div class="contact-item"><span class="contact-icon">📍</span> Philippines</div>
      <div class="contact-item"><span class="contact-icon">🕒</span> Open 7 Days a Week</div>
      <div class="contact-item"><span class="contact-icon">✈️</span> Domestic & International</div>
      <button class="msg-btn-big" onclick="showToast('💬 Opening Messenger…')">💬 Send Message Now</button>
    </div>

    <!-- ABOUT -->
    <div class="card">
      <div class="card-head">About A&S Travel & Tours</div>
      <div class="card-body">
        <div class="about-item"><span class="about-icon">🏢</span><div><span class="about-label">Category</span>Travel Agency · Tourist Transport</div></div>
        <div class="about-item"><span class="about-icon">🌏</span><div><span class="about-label">Service Area</span>Philippines & International</div></div>
        <div class="about-item"><span class="about-icon">✈️</span><div><span class="about-label">Specialties</span>Tours, Transport, Airport Transfers, Custom Packages</div></div>
        <div class="about-item"><span class="about-icon">🛡️</span><div><span class="about-label">Promise</span>Safe · Comfortable · Affordable · Reliable</div></div>
        <div class="about-item"><span class="about-icon">⭐</span><div><span class="about-label">Rating</span>5.0 ★ — Highly Recommended</div></div>
      </div>
    </div>

    <!-- STATS -->
    <div class="card">
      <div class="card-head">Page Stats</div>
      <div class="stats-grid">
        <div class="stat-box"><div class="num">10+</div><div class="lbl">Tour Packages</div></div>
        <div class="stat-box"><div class="num">5★</div><div class="lbl">Client Rating</div></div>
        <div class="stat-box"><div class="num">7/7</div><div class="lbl">Days Open</div></div>
        <div class="stat-box"><div class="num">2027</div><div class="lbl">Dates Available</div></div>
      </div>
    </div>

    <!-- PHOTO GRID -->
    <div class="card">
      <div class="card-head">Photos & Packages</div>
      <div class="card-body" style="padding:10px">
        <div class="photo-grid">
          <div class="photo-item" style="background:linear-gradient(135deg,#0ea5e9,#7dd3fc)" onclick="showToast('🏖️ Boracay Package')">🏖️</div>
          <div class="photo-item" style="background:linear-gradient(135deg,#059669,#6ee7b7)" onclick="showToast('🌊 El Nido Package')">🌊</div>
          <div class="photo-item" style="background:linear-gradient(135deg,#d97706,#fcd34d)" onclick="showToast('🥭 Iloilo-Guimaras Package')">🥭</div>
          <div class="photo-item" style="background:linear-gradient(135deg,#be123c,#fb7185)" onclick="showToast('🌹 Vietnam Rose Package')">🌹</div>
          <div class="photo-item" style="background:linear-gradient(135deg,#78350f,#f59e0b)" onclick="showToast('🦁 Africa Safari Package')">🦁</div>
          <div class="photo-item" style="background:linear-gradient(135deg,#312e81,#818cf8)" onclick="showToast('⛪ Europe Package')">⛪</div>
          <div class="photo-item" style="background:linear-gradient(135deg,#064e3b,#34d399)" onclick="showToast('🗻 Avatar Furong Package')">🗻</div>
          <div class="photo-item" style="background:linear-gradient(135deg,#16a34a,#86efac)" onclick="showToast('🏔️ Batanes Package')">🏔️</div>
          <div class="photo-item" style="background:linear-gradient(135deg,#1e3a5f,#60a5fa)" onclick="showToast('🏯 Beijing Package')">🏯</div>
        </div>
      </div>
    </div>

    <!-- REVIEWS -->
    <div class="card">
      <div class="card-head">⭐ Reviews</div>
      <div class="card-body">
        <div style="font-size:13px;margin-bottom:10px;padding-bottom:10px;border-bottom:1px solid var(--line)">
          <div style="font-weight:800;color:var(--night)">Maria Santos ⭐⭐⭐⭐⭐</div>
          <div style="font-size:12px;color:var(--gray);margin:3px 0">Boracay Package · June 2026</div>
          <div style="color:var(--ink)">Napakaganda ng experience! Very smooth ang lahat from booking to hotel. Highly recommend A&S Travel!</div>
        </div>
        <div style="font-size:13px;margin-bottom:10px;padding-bottom:10px;border-bottom:1px solid var(--line)">
          <div style="font-weight:800;color:var(--night)">John dela Cruz ⭐⭐⭐⭐⭐</div>
          <div style="font-size:12px;color:var(--gray);margin:3px 0">Vietnam Rose · May 2026</div>
          <div style="color:var(--ink)">Best Vietnam tour ever! No compulsory shopping, no detours. Pure travel experience! 👏</div>
        </div>
        <div style="font-size:13px">
          <div style="font-weight:800;color:var(--night)">Reyes Family ⭐⭐⭐⭐⭐</div>
          <div style="font-size:12px;color:var(--gray);margin:3px 0">El Nido Package · April 2026</div>
          <div style="color:var(--ink)">The island hopping was AMAZING! Safe, on-time, and the driver was very professional. Will book again!</div>
        </div>
      </div>
    </div>

  </div><!-- end sidebar -->
</div><!-- end page-body -->

<!-- ─── MODAL ─── -->
<div class="modal-overlay" id="modalOverlay" onclick="closeModal(event)">
  <div class="modal">
    <div class="modal-hdr">
      <div class="modal-hdr-banner" id="mIcon" style="background:#EAF2FF"></div>
      <div><h3 id="mTitle"></h3><p id="mSub"></p></div>
      <button class="modal-close" onclick="closeModalBtn()">✕</button>
    </div>
    <div class="modal-body">
      <div class="modal-price-box">
        <div style="font-size:13px;opacity:.85;margin-bottom:4px;font-weight:700">STARTING PRICE</div>
        <div class="big-price" id="mPrice"></div>
        <div class="per" id="mPer">per person</div>
      </div>
      <div id="mDates"></div>
      <div id="mDays"></div>
      <div id="mInc"></div>
      <div id="mExc"></div>
    </div>
    <div class="modal-footer">
      <button class="mftr-btn mftr-btn-msg" onclick="showToast('💬 Opening Messenger to inquire…');closeModalBtn()">💬 Inquire</button>
      <button class="mftr-btn mftr-btn-book" onclick="showToast('✅ Booking request sent! We will message you shortly.');closeModalBtn()">✈️ Book Now</button>
    </div>
  </div>
</div>

<!-- TOAST -->
<div class="toast" id="toast"></div>

<script>
const packages = {
  boracay:{
    icon:'🏖️',bg:'linear-gradient(135deg,#0ea5e9,#38bdf8)',
    title:'GO BORACAY 2026–2027',sub:'3 Nights 4 Days · Roundtrip via Cebu Pacific',
    price:'₱12,888',per:'per person (twin sharing)',
    dates:['Jun 11–14','Jul 2–5','Aug 20–23','Sep 24–27','Oct 28–31','Nov 27–30','Dec 5–8','Dec 23–26','Jan 13–16 2027','Feb 13–16 2027','Mar 24–27 2027','Apr 9–12 2027','May 1–4 2027'],
    days:[
      {d:'Day 1',t:'Arrival · Transfer to hotel · Free time at beach'},
      {d:'Day 2',t:'Breakfast · Beach activities · Island hopping'},
      {d:'Day 3',t:'Breakfast · D\'Mall shopping · Sunset cruise'},
      {d:'Day 4',t:'Breakfast · Hotel checkout · Transfer to airport · Fly home'}
    ],
    inc:['Roundtrip Airfare via Cebu Pacific (via Caticlan)','7KG Hand Carry','3 Nights Hotel Accommodation','Daily Hotel Breakfast','Roundtrip Airport Transfers via Private Company','Terminal Fee','Environmental Fee'],
    exc:['Check-in Baggage','Travel Insurance','P400 Fuel Surcharge']
  },
  elnido:{
    icon:'🌊',bg:'linear-gradient(135deg,#059669,#10b981)',
    title:'GO EL NIDO 2026–2027',sub:'3 Nights 4 Days · 2 Island Hopping Tours',
    price:'₱14,888',per:'per person (Rovic\'s Tourist Hotel)',
    dates:['Jun 11–14','Jul 2–5','Aug 28–31','Sep 17–20','Oct 28–31','Nov 28–Dec 1','Dec 24–27','Jan 27–30 2027','Feb 11–14 2027','Mar 24–27 2027','Apr 7–10 2027','May 5–8 2027'],
    days:[
      {d:'Day 1',t:'Departure from Manila · Arrival at Puerto Princesa · Transfer to El Nido · Check-in'},
      {d:'Day 2',t:'Breakfast · TOUR A: Island Hopping — Big/Small Lagoon, Shimizu Island, Seven Commando Beach, Payong-Payong Beach, Secret Lagoon'},
      {d:'Day 3',t:'Breakfast · TOUR C: Island Hopping — Helicopter Island, Hidden Beach, Talisay Beach, Matinloc Straight (Snorkeling), Secret Beach'},
      {d:'Day 4',t:'Breakfast · Free time · Check out · Transfer to Puerto Princesa · Fly back to Manila'}
    ],
    inc:['Roundtrip Airfare via Cebu Pacific','7KG Hand Carry','3 Nights Hotel Accommodation','Daily Breakfast','Tour A & Tour C Island Hopping','Roundtrip Airport Van Transfers','Lagoon User Fee','Environmental Fee'],
    exc:['Check-in Baggage','Travel Insurance']
  },
  iloilo:{
    icon:'🥭',bg:'linear-gradient(135deg,#d97706,#f59e0b)',
    title:'ILOILO–GUIMARAS 2026–2027',sub:'4 Days 3 Nights · Island Hopping Included',
    price:'₱15,888',per:'per person',
    dates:['Jul 22–25','Aug 20–23','Sep 10–13','Oct 29–Nov 1','Nov 27–30','Mar 24–27 2027','Apr 7–10 2027','Apr 14–17 2027','May 5–8 2027'],
    days:[
      {d:'Day 1',t:'Departure from Manila · Breakfast at La Paz Batchoy · Transfer to Parola Wharf · Boat to Guimaras · Visit San Lorenzo Wind Farm, Guimaras Landmark · Lunch at seafood restaurant · Visit Trappist Monastery · Check-in resort · Overnight'},
      {d:'Day 2',t:'Breakfast · ISLAND HOPPING TOUR: Natago Beach Resort, La Murawan, Baras Cave, Ave Maria Islet · Lunch at resort · Free & Easy (Swim/Dive) · Dinner · Overnight at resort'},
      {d:'Day 3',t:'Breakfast · Free time · Check out · Lunch (own) · Transfer: Jordan Wharf to Parola Wharf · Check-in Iloilo City Hotel · Dinner (own) · Overnight'},
      {d:'Day 4',t:'Breakfast · Garin Farm · Miag-ao Church · Molo Church · Brandy Museum · Calle Real Rolling Tour · Philippine Maritime Museum, Iloilo Economic History Museum, Prison Jail Museum · Biscocho Haus · Jaro Cathedral · Transfer to airport · Fly home'}
    ],
    inc:['Roundtrip Airfare (7KG Hand Carry)','2 Nights Hotel in Guimaras (Beach Resort)','1 Night Hotel in Iloilo City','Tourist Van','Roundtrip Airport Transfers','Licensed Tour Guide','Roundtrip Pumpboat (Iloilo–Guimaras–Iloilo)','3-Breakfast 2-Lunch 2-Dinner','Sweet Guimaras Mango','Fully Loaded Tours with Entrances','Island Hopping','All Taxes and Fees'],
    exc:['Check-in Baggage','Travel Insurance']
  },
  batanes:{
    icon:'🏔️',bg:'linear-gradient(135deg,#16a34a,#22c55e)',
    title:'GO BATANES 2026–2027',sub:'4 Days 3 Nights · Out Clark via Philippine Airlines',
    price:'₱28,888',per:'per person — ALL IN! No Exclusions!',
    dates:['Jun 26–29','Jul 10–13','Aug 21–24','Sep 4–7','Oct 30–Nov 2','Nov 20–23','Dec 23–26','Jan 22–25 2027'],
    days:[
      {d:'Day 1',t:'Departure from Clark · Arrival in Basco · Transfer to hotel · Batan North Tour: Valugan Boulder Bay, Japanese Tunnel, Basco Cathedral, Tukon Chapel, Basco Lighthouse, Radar Station, Casa Real, Amandangat, Kilometer Zero · Lunch · Free time'},
      {d:'Day 2',t:'Breakfast + Lunch · Sabtang Island Tour via Faluwa · Transfer to Ivana Port · Sabtang Island: San Vicente Ferrer Church, Savidug Community, Savidug Idjang Fortress, Tinyan, Chavayan Vernacular Houses, Ahaw Arc, Morong Beach, Souvenir Shops'},
      {d:'Day 3',t:'Breakfast + Lunch · Batan South Tour: Racuh A Payaman, Mahatao Church Complex, Chawa View Deck, Maydangeb White Beach, San Jose Spanish Bridge, House of Dakay, Honesty Coffee Shop, Ivana Church, Mutchong Viewpoint, Itbud Church, Madangay Hills · Transfer to hotel'},
      {d:'Day 4',t:'Breakfast · Transfer to airport · Departure for Clark'}
    ],
    inc:['Roundtrip Airfare via Philippine Airlines','7kg Hand Carry','10kg Check-in Baggage','3 Nights Hotel Accommodation','Roundtrip Airport Transfers (Private)','Roundtrip Boat Transfers','Meals as per itinerary (4B-3L)','Daily Hotel Breakfast','Fully Loaded Tours','Licensed Tour Guide','Bottled Water','LGU Fees','Environmental Fee','Travel Insurance'],
    exc:['P400 Fuel Surcharge (subject to change)']
  },
  vnrose:{
    icon:'🌹',bg:'linear-gradient(135deg,#be123c,#f43f5e)',
    title:'VIETNAM ROSE RELOADED 2026–2027',sub:'Hanoi · Sapa · Ha Long Bay · 6 Days 5 Nights',
    price:'₱58,888',per:'per person — Premium Luxury',
    dates:['Jul 2–7','Aug 17–22','Sep 10–15','Nov 26–Dec 1','Jan 14–19 2027'],
    days:[
      {d:'Day 1',t:'Departure from Manila · Arrival in Hanoi · Proceed to Sapa · Visit Moana Cafe · Sightsee Hoang Lien Son Mountain & Fansipan Peak Clouds · Visit Cat Cat Village · Check-in hotel'},
      {d:'Day 2',t:'Breakfast + Lunch · Visit Fansipan Mountain — Roof of Indochina (Train & Cable Car) · Transfer back to Sapa Town · Proceed to Hanoi'},
      {d:'Day 3',t:'Breakfast + Lunch + Dinner · Visit Tran Quoc Pagoda & St. Joseph Cathedral · Proceed to Ha Long City · Enjoy dinner at Dragon Pearl Cave · Overnight in Ha Long City'},
      {d:'Day 4',t:'Breakfast + Lunch + Dinner · Proceed to Ha Long Bay · Embark Ambassador Signature Cruise · Excursion to Viet Hai Fishing Village · Happy Hour & Cooking Demonstration with Canapes · Premium Michelin-standard Dinner · Party on board!'},
      {d:'Day 5',t:'Breakfast + Lunch + Dinner · Taichi on Sundeck / Piano Lounge · Explore Dark & Bright Cave · Disembark Ambassador Cruise · Transfer to Hanoi · Mega Grand World · Shopping: Dong Xuan Market, Hoan Kiem Lake, Lotte Mall · Transfer to airport'},
      {d:'Day 6',t:'Departure from Hanoi · Arrival in Manila'}
    ],
    inc:['Roundtrip International Airfare','7KG Hand Carry','23KG Check-in Baggage (Vietnam Airlines)','1 Night in Sapa (5-Star)','1 Night in Hanoi (4-Star)','1 Night in Ha Long City (5-Star)','Overnight Ambassador Cruise (5-Star Luxury)','Cave Dinner in Ha Long City','Meals as per itinerary (5B-5L-4D)','Private Coach','Fully Loaded Tours','English-Speaking Guide','Filipino Tour Escort'],
    exc:['PH Travel Tax (Cebu Pacific)','Airline Tax (Vietnam Airlines)','Tipping','Travel Insurance','Check-in Baggage (Cebu Pacific)']
  },
  vnrose2:{
    icon:'🏮',bg:'linear-gradient(135deg,#b45309,#f97316)',
    title:'VIETNAM ROSE 2.0 · 2026–2027',sub:'Da Nang · Hoi An · Hue · Incense Village · 4D3N',
    price:'₱38,888',per:'per person — Premium',
    dates:['Jun 10–13','Jul 23–26','Aug 19–22','Oct 29–Nov 1','Nov 27–30','Dec 25–28','Jan 2–5 2027','Feb 11–14 2027','Feb 23–27 2027'],
    days:[
      {d:'Day 1',t:'Departure from Manila · Arrival in Da Nang · Meet & greet at airport · Proceed to Da Nang City Center'},
      {d:'Day 2',t:'Breakfast + Lunch + Dinner · Han Market · Cross High Mountain Pass of Hai Van · Thuy Xuan Incense Village · Hue Ancient Citadel · Noan Gate · Thai Hoa Palace · Proceed back to Da Nang'},
      {d:'Day 3',t:'Breakfast + Lunch + Dinner · Linh Ung Pagoda & Lady Buddha Statue · Ba Na Hills by Cable Car · Debay Wine Cellar, Loc Uyen Garden, Golden Bridge, Quan Am Pavilion, Monkey Garden, French Village, Fantasy Park · Drive to Hoi An · Hoi An Lantern Boat along Thu Bon River'},
      {d:'Day 4',t:'Breakfast + Lunch + Dinner · Hoi An Ancient Town · Ecological Village of Cam Thanh · Bay Mau Coconut Forest · Basket Boat Race · Japanese Covered Bridge · Phuc Kien Chinese Assembly Hall · Last-minute shopping · Arrival in Manila'}
    ],
    inc:['Roundtrip Airfare via Cebu Pacific','7KG Hand Carry','2 Nights in Da Nang (4-Star Deluxe Beachfront)','1 Night in Hoi An (#1 Rated 5-Star Hotel)','Full Board Meals (3B-3L-3D)','Private Coach','Fully Loaded Tours','English-Speaking Guide','Filipino Tour Escort'],
    exc:['PH Travel Tax','Tipping','Travel Insurance','Check-in Baggage']
  },
  vnrose3:{
    icon:'⛩️',bg:'linear-gradient(135deg,#7c3aed,#a78bfa)',
    title:'VIETNAM ROSE 3.0 · 2026–2027',sub:'Hanoi · Sapa · Ninh Binh · Trang An · 5D4N',
    price:'₱38,888',per:'per person',
    dates:['Jul 10–14','Aug 30–Sep 3','Sep 15–19','Nov 29–Dec 3','Dec 22–26','Jan 5–9 2027','Jan 12–16 2027','Feb 23–27 2027'],
    days:[
      {d:'Day 1',t:'Departure from Manila · Arrival in Hanoi · Proceed to Sapa · Visit Cat Cat Village and Sapa Church'},
      {d:'Day 2',t:'Breakfast + Lunch + Dinner · Visit Fansipan Mountain (Train & Cable Car) · Transfer back to Sapa Town · Proceed to Hanoi · Train Track Experience with Egg Coffee'},
      {d:'Day 3',t:'Breakfast · Free & Easy! · Discover scenic views · Walk around nearby spots · Shopping at nearby markets'},
      {d:'Day 4',t:'Breakfast + Lunch · Visit Quang Phu Cau Incense Village · Visit Trang An Scenic Landscape · Boat Ride to Cave Complex of Trang An (Sang Cave, Toi Cave, Ba Glot Cave, Nau Ruou) · Transfer to Hanoi · Shopping at Old Quarter, Dong Xuan Market, Hoan Kiem Lake · Transfer to airport'},
      {d:'Day 5',t:'Departure from Hanoi · Arrival in Manila'}
    ],
    inc:['Roundtrip Airfare via Cebu Pacific','7KG Hand Carry','2 Nights in Hanoi (4-Star)','1 Night in Sapa (5-Star Silk Path Grand Resort)','Meals as per itinerary (4B-3L-2D)','Private Coach','Fully Loaded Tours','English-Speaking Guide','Filipino Tour Escort'],
    exc:['PH Travel Tax','Tipping','Travel Insurance','Check-in Baggage']
  },
  danang:{
    icon:'🌉',bg:'linear-gradient(135deg,#0369a1,#0ea5e9)',
    title:'VIETNAM DA NANG 4D3N',sub:'Via AirAsia · Special Offer',
    price:'₱21,888',per:'per person (Special Price)',
    dates:['Aug 7–10','Aug 14–17','Aug 21–24','Aug 28–31','Sep 4–7','Sep 11–14','Sep 18–21','Sep 25–28','Oct 9–12','Oct 16–19'],
    days:[
      {d:'Day 1',t:'Arrive Da Nang · Meet tour guide · Da Nang Cathedral (Pink Church) · Nguyen Van Thoai Street · Son Tra Peninsula/Linh Ung Pagoda · Ba Na Hills (longest cable car) · Walking on Golden Bridge · Fantasy Park · French Village · Linh Ung Pagoda · Mini super market · Transfer to hotel & check in'},
      {d:'Day 2',t:'Hotel breakfast · Latex Shop · Jewelry Shop · Transfer to Camnam Island Coconut Village · Bamboo basket boat + crab fishing · Transfer to Hoi An Ancient Town · Fujian Guild Hall, Cantonese Assembly Hall, Tan Ky Old House, Japanese Covered Bridge, Lotus Lanterns · Transfer to hotel'},
      {d:'Day 3',t:'Hotel breakfast · Dragon Bridge & Love Bridge & Dragon head fountain · APEC Park · Marble Mountains (upward lift) · Silk shop · My Khe Beach (Vietnamese drip coffee/specialty drink) · Transfer to hotel'},
      {d:'Day 4',t:'Hotel breakfast · Transfer to airport · Fly back home'}
    ],
    inc:['Economy Airfare via AirAsia (Round Trip)','1PC 20KG Baggage Allowance','3 Nights Hotel (4-Star, Twin Sharing)','Daily Hotel Breakfast','Private Coach with English-Speaking Tour Guide','Sightseeing tours (first-way entrance fees included)','Meals as listed'],
    exc:['Personal expenses (calls, mini bar)','Extra Baggage','Travel Insurance','Philippines Travel Tax','Visa USD40/PAX','Tips USD5/DAY/PAX','Single Supplement USD99/PAX','Taxes & Fees']
  },
  danang2:{
    icon:'🚡',bg:'linear-gradient(135deg,#9d174d,#ec4899)',
    title:'DA NANG CHARTER FLIGHT 6D4N',sub:'Via VietJet · ALL IN per person',
    price:'₱23,888',per:'per person ALL IN',
    dates:['Mar 30–Apr 3','Apr 4–8','Apr 13–17','Apr 18–22','Apr 27–May 1','May 2–6','May 11–15','May 16–20','May 25–29'],
    days:[
      {d:'Day 1',t:'Arrival Airport · Meet tour guide · Breakfast upon arrival · Son Tra Peninsula (67m Lady Buddha) · Canaan Island Coconut Boat Ride · Hoi An Ancient Town · Transfer to hotel & check in'},
      {d:'Day 2',t:'After breakfast · Transfer to Ba Na Hills (ancient French architecture) · French Village · Walking on Golden Bridge (Buddha hand bridge) · Visit Local Mini Supermarket · Transfer to hotel & check in'},
      {d:'Day 3',t:'After breakfast · Visit Latex Shop · APEC Park · Jewelry Shop · Da Nang Cathedral (Pink Church) · After dinner transfer to hotel'},
      {d:'Day 4',t:'After breakfast · Cham Museum · Dragon Bridge "Lovers Bridge" · Visit Silk Shop · After dinner transfer to hotel'},
      {d:'Day 5/6',t:'After breakfast · HAI VAN Pass and LANG CO Coastal Road · "Baili Gallery" · Treasure Shop · Transfer to airport · Fly back home'}
    ],
    inc:['Charter Flight Manila–Da Nang–Manila via VietJet','Baggage Allowance 20kg per pax + 7KG carry on','4 Nights Hotel (Local 4-Star, Twin Sharing)','7 Meals included','Sightseeing as specified (first-way entrance fees)','Air-conditioned Tourist Bus','English-Speaking Tour Guide Service'],
    exc:['Visa (if needed)','Extra Baggage','Single Supplement USD80/PAX','PH Tax 1620PHP/PAX','Terminal Fees USD42/pax','Tips USD5/PAX/day','Personal expenses','Han River Cruise (Night View) + 1 drink (optional)']
  },
  chongqing:{
    icon:'🏮',bg:'linear-gradient(135deg,#92400e,#d97706)',
    title:'WO AI NI CHONGQING 2026',sub:'5 Days 4 Nights via Xiamen Airlines',
    price:'$888',per:'per person (from 20+ pax)',
    dates:['Aug 25–29','Sep 15–19','Oct 20–24'],
    days:[
      {d:'Day 1',t:'Departure from Manila · Arrival at Chongqing'},
      {d:'Day 2',t:'Breakfast + Lunch + Dinner · Transfer to Nanchuan · Jinfo Mountain · Cable Car Transfer · Go back to Chongqing'},
      {d:'Day 3',t:'Breakfast + Lunch + Dinner · Shibati Scenic Area · Mountain City Trail · Jiefangbei Street & Bayi Food Street · Kuixing Building · Hongya Cave Night View'},
      {d:'Day 4',t:'Breakfast + Lunch + Dinner · Chongqing Zoo (Panda House) · Yangtze River Cableway (one-way) · Liziba Light Rail Through-the-Building Experience · Ciqikou Ancient Town'},
      {d:'Day 5',t:'Breakfast + Lunch + Meals on Board · Guanyinqiao Pedestrian Street · Shopping at Halo Mall · Transfer to airport · Departure from Chongqing · Arrival in Manila'}
    ],
    inc:['Roundtrip Airfare via Xiamen Airlines','23KG Check-in Baggage + 7KG Hand Carry','Private Coach','Daily Breakfast + Meals as specified','Fully Loaded Tours','4 Nights Hotel Accommodation (Twin Sharing)','English-Speaking Guide','Filipino Tour Escort'],
    exc:['PH Travel Tax','China Visa','Tipping','Travel Insurance']
  },
  avatar:{
    icon:'🗻',bg:'linear-gradient(135deg,#064e3b,#059669)',
    title:'AVATAR FURONG — MINI VENICE',sub:'Charter Flight 5D4N via Qingdao Airlines',
    price:'$369',per:'per person (22 yrs and above)',
    dates:['May 16–20','May 21–25','May 30–Jun 3','Jun 4–8','Jun 13–17','Jun 18–22','Jun 27–Jul 1','Sep 5–9','Sep 10–14','Sep 19–23'],
    days:[
      {d:'Day 1',t:'Arrive Changsha · Meet tour guide · Hotel buffet breakfast · Visit Orange Isle · Taiping Old Street · Huangxing Road Walking Street · Dinner by own · Transfer to hotel'},
      {d:'Day 2',t:'Breakfast + Check out · Proceed to Zhangjiajie · Optional Tour –USD85/Pax (Tianmen Mountain: cable cart, glass skywalk, Tianmen cave) · Proceed to Furong Town (ancient town hanging on waterfall) · Night view of Furong Town · Transfer to hotel'},
      {d:'Day 3',t:'Breakfast + Check out · Proceed to Zhangjiajie Avatar Scenic Area (Bailong Lift or Tianzishan cable car) · No.1 Bridge · Avatar Hallelujah Mountain · Breath-taking Platform · West Sea Clouds · Optional –USD70/PAX Tianmen Fox-Lady Show · After dinner transfer to hotel'},
      {d:'Day 4',t:'Breakfast · Compulsory shopping (Latex, Golden Whip Stream, water around four gates, Silk shop) · Visit Huangshi Village (cable cart included) · Optional –USD60/PAX Baofeng Lake (incl cruise) · After dinner transfer to hotel'},
      {d:'Day 5',t:'Breakfast + Check out · Compulsory shopping (Jewelry, Grand Canyon Glass Bridge +VR, Tea shop) · Transfer back to Changsha · Fly back to Manila'}
    ],
    inc:['Charter Flight Manila–Changsha–Manila (Qingdao Airlines)','Baggage Allowance 20KG per passenger','4 Nights Accommodation (5-Star Hotels, Twin Sharing)','Daily Hotel Breakfast','Private Coach with English-Speaking Tour Guide','Sightseeing as specified (first-way entrance fees)','Meals as listed'],
    exc:['Personal expenses','Travel Insurance','Airport Tax USD40/PAX','China Group Visa USD40/PAX','Tips for driver & guide USD25/PAX','Philippines Travel Tax 1620PHP/PAX','Single Supplement USD90/PAX']
  },
  beijing:{
    icon:'🏯',bg:'linear-gradient(135deg,#1e3a5f,#1877F2)',
    title:'BEIJING AVATAR — ALL IN 8D7N',sub:'Beijing + Zhangjiajie via Air China · Group Visa Guaranteed',
    price:'$699',per:'per person ALL IN',
    dates:['Apr 12–19','Apr 14–21','Apr 17–24','Apr 24–May 1','May 8–15','May 15–22','May 22–29','May 29–Jun 5','Jun 5–12','Jun 19–26','Jun 26–Jul 3'],
    days:[
      {d:'Day 1',t:'Arrival at PEK Airport · Temple of Heaven · Wangfuiing Walking Street · Transfer to hotel · Lunch: Peking Duck · Local 5★ Hotel Beijing (XLX)'},
      {d:'Day 2',t:'Juyongguan Great Wall · Hanfu Experience · Lunch: BBQ Buffet · Local 5★ Hotel Beijing (BLX)'},
      {d:'Day 3',t:'Free and easy day, no service · Optional: Universal Beijing Resort (USD135/pax, min 4pax) · Local 5★ Hotel Beijing (BXX)'},
      {d:'Day 4',t:'CA1953 PEK-DYG 18:30–21:00 · Tiananmen Square · Forbidden City · Transfer to PEK airport · Arrival at DYG airport · Transfer to hotel · Lunch: Mini Rotating Hot Pot Buffet · Local 5★ Hotel Zhangjiajie (BLX)'},
      {d:'Day 5',t:'No.1 Bridge · Avatar Hallelujah Mountain · Breath-taking Platform · West Sea Clouds (up and down by Bailong Lift) · Golden Whip Stream water around four gates · Optional: $70/pax Tianmen Fox Lady Show · Local 5★ Hotel Zhangjiajie (BLD)'},
      {d:'Day 6',t:'Junsheng Sandstone Painting Museum · Optional $85/pax Tianmen Mountain (cable car, glass skywalk, Tianmen cave) · Local 5★ Hotel Zhangjiajie (BLD)'},
      {d:'Day 7',t:'CA1954 DYG-PEK 21:45 · Grand Canyon C Line · Glass Bridge · 72 odd buildings (outside view) · Transfer to DYG airport · Local 5★ Hotel Beijing (BLD)'},
      {d:'Day 8',t:'CA179 PEK-MNL 19:15 · Summer Palace · Bird\'s Nest and Water Cube (outside view) · Transfer to PEK airport · Lunch: Hand Sliced Beef and Mutton Hot Pot Buffet · Fly home (BLX)'}
    ],
    inc:['7 Nights Accommodation at 5-Star Hotels (Twin Sharing, Daily Breakfast)','Private Coach with English-Speaking Tour Guide','Sightseeing (first-way entrance fees)','Meal as listed + 1 bottle water/day','RT Airfare via Air China (23kg check-in + 5kg carry-on)'],
    exc:['Personal expenses','PH Travel Tax (USD32/pax)','Travel Insurance','China Group Visa Fee (USD50/pax)','Tip (USD40/pax)','Single Supplement (USD210/pax)']
  },
  europe:{
    icon:'⛪',bg:'linear-gradient(135deg,#312e81,#4338ca)',
    title:'HAIL HOLY QUEEN — TALES OF EUROPE',sub:'Italy · France · Spain · Portugal · 17 Days via Emirates',
    price:'$4,588',per:'per person (from 40+ pax)',
    dates:['Sep 8–24, 2026'],
    days:[
      {d:'Day 1',t:'Departure from Manila · Arrival in Rome · Rome City Tour'},
      {d:'Day 2',t:'Breakfast + Dinner · Transfer to Vatican City · Attend a Papal Audience · Visit St. John in Lateran, Basilica of St. Mary Major, Chapel of St. Paul outside the Walls, Domus Sanctae Mariae, Quo Vadis'},
      {d:'Day 3',t:'Breakfast + Dinner · Proceed to San Giovanni Rotondo · Visit Sanctuary of Saint Mary Our Lady of Grace'},
      {d:'Day 4',t:'Breakfast + Dinner · Transfer to Lanciano · Visit Sanctuary of Il Miracolo Eucharístico · Proceed to Assisi'},
      {d:'Day 5',t:'Breakfast + Dinner · Assisi City Tour · Visit Basilica of St. Francis · Attend a Private Mass · Proceed to Florence'},
      {d:'Day 6',t:'Breakfast + Dinner · Transfer to Pisa · Leaning Tower of Pisa & Piazza dei Miracoli · Proceed to Genoa'},
      {d:'Days 7–17',t:'Monaco · Nice · Cannes → Avignon → Lourdes → Zaragoza, Basilica Notre Dame de la Garde → Nevers, Convent of Saint Gildard → Paris City Tour → Transfer to Montparnasse Station, TGV to Lourdes, enjoy free time → Lourdes City Tour, Sanctuary of Our Lady of Lourdes, Grotto of the Apparitions, Candlelight procession → Fatima City Tour → Transfer to airport, Arrival in Manila'}
    ],
    inc:['Roundtrip Airfare via Emirates','Check-in Baggage + Hand Carry','15 Nights Hotel Accommodation','Meals as specified','Fully Loaded Tours','Private Coach','Sightseeing & Entrances as specified','English-Speaking Tour Guide','European Tour Manager','Filipino Tour Escort'],
    exc:['Travel Insurance (up to 18 yrs only)','Tipping','Airline Taxes','Hotel/City Taxes','Visa Fee']
  },
  africa:{
    icon:'🦁',bg:'linear-gradient(135deg,#78350f,#b45309)',
    title:'WAKANDA AFRICA RELOADED 2026',sub:'South Africa — Johannesburg & Cape Town · 10 Days',
    price:'$3,488',per:'per person (from 35+ pax)',
    dates:['May 28–Jun 5','Jul 8–17','Jul 21–30','Aug 13–22'],
    days:[
      {d:'Day 1',t:'Assembly at airport · Departure from Manila'},
      {d:'Day 2',t:'Meals on Board + Lunch + Dinner · Arrival in Pretoria · Photo stop at The Union Buildings · "Beast of a Feast" dinner at The Carnivore Restaurant'},
      {d:'Day 3',t:'Breakfast + Lunch + Dinner · Transfer to Ukutula Conservancy · Guided Enrichment Walk with Lions in the African Bush · Predator Encounter Experience · Transfer to Luxury Game Lodge · 4x4 Safari Game Drive'},
      {d:'Day 4',t:'Breakfast + Lunch + Dinner · 4x4 Safari/Game Drive · Morning Private Guided 4x4 Safari Game Drive · Afternoon Private Guided 4x4 Safari Game Drive · BOMA Dinner with Live Entertainment'},
      {d:'Day 5',t:'Breakfast + Lunch + Dinner · Morning Private Guided 4x4 Safari Game Drive · Domestic Flight to Cape Town · Arrival in Cape Town'},
      {d:'Day 6',t:'Breakfast + Lunch + Dinner · Aerial Cableway to Table Mountain · Signal Hill · Great Constantia Wine Estate · Manor House & Cloete\'s Cellar · V&A Waterfront · 12-Minute Hopper Helicopter Ride over Cape Town · Catamaran Champagne Sunset Cruise'},
      {d:'Day 7',t:'Breakfast + Lunch + Dinner · Visit Hout Bay Harbour · Photo stops at Maiden\'s Cove & Duiker Island · Coffee viewing Fur Seals at Duiker Island at Mariner\'s Wharf · Transfer to V&A Waterfront · Flying Dutchman Funicular to the Lighthouse · Photo stop at "Cape of Good Hope"'},
      {d:'Day 8',t:'Breakfast + Lunch + Dinner · Visit Boulders Beach, Foxy Beach, Penguin Colony · Transfer to Cape Point Nature Reserve'},
      {d:'Day 9',t:'Breakfast + Lunch + Meals on Board · Photo stop & free time in Bo-Kaap · Guided City Tour of The 5 Tasting Experience · Transfer to airport'},
      {d:'Day 10',t:'Meals on Board · Flight back to Manila · Arrival in Manila'}
    ],
    inc:['Roundtrip Airfare via Emirates/Ethiopian Airlines','Check-in Baggage + Hand Carry','Domestic Flight to Cape Town','4.5-Star Hotel Accommodation','Private Coach','Full Board High-End Meals','Fully Loaded Tours','English-Speaking Guide','Filipino Tour Escort','Sightseeing & Entrances as per itinerary'],
    exc:['Travel Insurance','Visa Fee','Tipping','Airline Taxes']
  }
};

function openModal(id){
  const p=packages[id];if(!p)return;
  document.getElementById('mIcon').textContent=p.icon;
  document.getElementById('mIcon').style.background=p.bg;
  document.getElementById('mTitle').textContent=p.title;
  document.getElementById('mSub').textContent=p.sub;
  document.getElementById('mPrice').textContent=p.price;
  document.getElementById('mPer').textContent=p.per;
  // Dates
  let datesHTML=`<div class="section-hdr">📅 Available Dates</div><div class="dates-wrap">`;
  p.dates.forEach(d=>datesHTML+=`<span class="date-chip">${d}</span>`);
  datesHTML+='</div>';
  document.getElementById('mDates').innerHTML=datesHTML;
  // Days
  let daysHTML=`<div class="section-hdr">🗺️ Day-by-Day Itinerary</div><div class="days-grid">`;
  p.days.forEach(d=>daysHTML+=`<div class="day-row"><span class="day-num">${d.d}</span><div class="day-text">${d.t}</div></div>`);
  daysHTML+='</div>';
  document.getElementById('mDays').innerHTML=daysHTML;
  // Inclusions
  let incHTML=`<div class="section-hdr">✅ Inclusions</div><ul class="inc-list">`;
  p.inc.forEach(i=>incHTML+=`<li>${i}</li>`);
  incHTML+='</ul>';
  document.getElementById('mInc').innerHTML=incHTML;
  // Exclusions
  let excHTML=`<div class="section-hdr">❌ Exclusions</div><ul class="inc-list exc-list">`;
  p.exc.forEach(e=>excHTML+=`<li>${e}</li>`);
  excHTML+='</ul>';
  document.getElementById('mExc').innerHTML=excHTML;
  document.getElementById('modalOverlay').classList.add('open');
  document.getElementById('modalOverlay').querySelector('.modal-body').scrollTop=0;
}
function closeModal(e){if(e.target===document.getElementById('modalOverlay'))closeModalBtn()}
function closeModalBtn(){document.getElementById('modalOverlay').classList.remove('open')}

let toastTimer;
function showToast(msg){
  const t=document.getElementById('toast');
  t.textContent=msg;t.classList.add('show');
  clearTimeout(toastTimer);
  toastTimer=setTimeout(()=>t.classList.remove('show'),2800);
}
</script>
</body>
</html>
