<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Talk to Jaoka - Rainy.REN</title>
<style>
:root{
  --bg1:#010208; --panel:#060d24;
  --gold:#d4af37; --gold-l:#f6e27a; --gold-d:#8a6d1c;
  --text:#dfe6f7; --muted:#8a98bd;
  box-sizing:border-box;
  padding-top:env(safe-area-inset-top,0px);
  padding-bottom:env(safe-area-inset-bottom,0px);
}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
*{box-sizing:border-box;margin:0}
body{
  min-height:100vh;display:flex;align-items:center;justify-content:center;
  padding:20px;font-family:"Segoe UI",Tahoma,sans-serif;color:var(--text);
  background:
    radial-gradient(ellipse 60% 40% at 20% 10%,rgba(122,77,255,.28),transparent 70%),
    radial-gradient(ellipse 50% 40% at 85% 85%,rgba(40,120,255,.25),transparent 70%),
    var(--bg1);
  overflow-x:hidden;
}

/* ===== ดวงดาวพื้นหลัง ===== */
.stars,.stars::before,.stars::after{content:"";position:fixed;inset:0;pointer-events:none;background-repeat:repeat}
.stars{z-index:1;
  background-image:
    radial-gradient(1.2px 1.2px at 20px 30px,#fff,transparent),
    radial-gradient(1px 1px at 90px 80px,#cfe0ff,transparent),
    radial-gradient(1.5px 1.5px at 150px 20px,#fff,transparent),
    radial-gradient(1px 1px at 60px 140px,#f6e27a,transparent),
    radial-gradient(1.2px 1.2px at 180px 120px,#fff,transparent);
  background-size:200px 180px;animation:twinkle 4s ease-in-out infinite}
.stars::before{
  background-image:
    radial-gradient(1.5px 1.5px at 40px 60px,#fff,transparent),
    radial-gradient(1px 1px at 130px 110px,#b9c9ff,transparent),
    radial-gradient(2px 2px at 100px 20px,#f6e27a,transparent);
  background-size:260px 230px;animation:twinkle 6s ease-in-out infinite reverse}
.stars::after{
  inset:auto;top:8%;left:-20%;width:140px;height:2px;
  background:linear-gradient(90deg,transparent,#fff);
  transform:rotate(25deg);opacity:0;animation:shoot 7s ease-in infinite 2s}
@keyframes twinkle{50%{opacity:.35}}
@keyframes shoot{0%{opacity:0;transform:translate(0,0) rotate(25deg)}
  5%{opacity:1}20%{opacity:0;transform:translate(130vw,60vh) rotate(25deg)}100%{opacity:0}}

/* ===== หน้าต่างคอนโซลหลัก ===== */
.window{
  position:relative;z-index:2;width:100%;max-width:380px;
  padding:34px 24px 30px;border-radius:18px;overflow:hidden;
  background:linear-gradient(160deg,#0b1a40,var(--panel) 60%,#03060f);
  border:2px solid var(--gold);
  box-shadow:0 0 0 5px #050a1a,0 0 0 6px var(--gold-d),0 0 50px rgba(122,77,255,.3),0 0 30px rgba(212,175,55,.25),inset 0 0 40px rgba(0,0,0,.6);
}
.window::before{content:"";position:absolute;inset:8px;border:1px solid rgba(212,175,55,.45);border-radius:12px;pointer-events:none;z-index:1}
.corner{position:absolute;z-index:2;width:22px;height:22px;border:2px solid var(--gold-l)}
.tl{top:14px;left:14px;border-right:0;border-bottom:0}
.tr{top:14px;right:14px;border-left:0;border-bottom:0}
.bl{bottom:14px;left:14px;border-right:0;border-top:0}
.br{bottom:14px;right:14px;border-left:0;border-top:0}

h1{
  text-align:center;font-size:2.2rem;letter-spacing:2px;
  background:linear-gradient(180deg,var(--gold-l),var(--gold) 55%,var(--gold-d));
  -webkit-background-clip:text;background-clip:text;color:transparent;
  filter:drop-shadow(0 0 12px rgba(212,175,55,.45));
}
.sub{text-align:center;color:var(--muted);font-size:.8rem;margin-top:6px;letter-spacing:3px;text-transform:uppercase;}
.line{height:1px;margin:18px auto 20px;width:70%;background:linear-gradient(90deg,transparent,var(--gold),transparent)}

/* ===== วงเวียนเวทมนตร์ตรงกลาง ===== */
.sigil{display:block;width:140px;height:140px;margin:0 auto 24px;
  filter:drop-shadow(0 0 14px rgba(127,166,255,.7))}
.sigil .r1{transform-origin:100px 100px;animation:spin 28s linear infinite}
.sigil .r2{transform-origin:100px 100px;animation:spin 18s linear infinite reverse}
.sigil .core{transform-origin:100px 100px;animation:pulse 3.2s ease-in-out infinite}
@keyframes spin{to{transform:rotate(360deg)}}
@keyframes pulse{50%{transform:scale(1.15);opacity:.8}}

/* ===== ปุ่ม START TALKING ===== */
.btn-talk{
  display:flex;align-items:center;justify-content:center;gap:10px;text-decoration:none;
  width:100%;padding:15px;border-radius:12px;font-weight:700;letter-spacing:2px;
  color:#1a1303;background:linear-gradient(180deg,var(--gold-l),var(--gold) 60%,var(--gold-d));
  border:1px solid var(--gold-l);box-shadow:0 4px 22px rgba(212,175,55,.4);transition:transform .15s, box-shadow .15s;
}
.btn-talk:hover{transform:translateY(-2px);box-shadow:0 6px 26px rgba(212,175,55,.6)}
.btn-talk:active{transform:scale(.97)}
</style>
</head>
<body>
<div class="stars"></div>

<main class="window">
  <span class="corner tl"></span><span class="corner tr"></span>
  <span class="corner bl"></span><span class="corner br"></span>

  <header>
    <h1>Rainy.REN</h1>
    <p class="sub">Talk to Jaoka</p>
    <div class="line"></div>
  </header>

  <svg class="sigil" viewBox="0 0 200 200" aria-hidden="true">
    <defs>
      <radialGradient id="g" cx="50%" cy="50%" r="50%">
        <stop offset="0" stop-color="#fff"/><stop offset=".4" stop-color="#f6e27a"/><stop offset="1" stop-color="#7fa6ff" stop-opacity="0"/>
      </radialGradient>
    </defs>
    <g class="r1" fill="none" stroke="#d4af37" stroke-width="1.5">
      <circle cx="100" cy="100" r="92" stroke-dasharray="3 7"/>
      <circle cx="100" cy="100" r="80"/>
      <circle cx="100" cy="8" r="4" fill="#f6e27a"/><circle cx="192" cy="100" r="3" fill="#7fa6ff"/>
      <circle cx="20" cy="100" r="3" fill="#f6e27a"/>
    </g>
    <g class="r2" fill="none" stroke="#7fa6ff" stroke-width="1.2">
      <polygon points="100,28 172,100 100,172 28,100" stroke="#d4af37"/>
      <polygon points="100,28 172,100 100,172 28,100" transform="rotate(45 100 100)"/>
      <circle cx="100" cy="100" r="46" stroke-dasharray="2 5"/>
    </g>
    <g class="core">
      <circle cx="100" cy="100" r="34" fill="url(#g)"/>
      <path d="M100 70 L106 94 L130 100 L106 106 L100 130 L94 106 L70 100 L94 94 Z" fill="#fff"/>
    </g>
  </svg>

  <!-- ปุ่มกด Start Talking (สามารถเปลี่ยนลิงก์ตรง href="ใส่ลิงก์แชทตรงนี้" ได้เลย) -->
  <a href="#" class="btn-talk">START TALKING</a>
</main>
</body>
</html>
