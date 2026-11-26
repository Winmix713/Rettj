<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<meta name="color-scheme" content="dark">
<title>Furrow — Precision Agriculture Command Center</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#050806;
  --ink:#f3f7ef; --ink-2:#c5cfc1; --ink-3:#8a968a; --ink-4:#5d695f;
  --lime:#bff24a; --lime-d:#8fd11a; --lime-deep:#4d7c0f;
  --amber:#f5b342; --rose:#fb7185; --sky:#5fc8ff; --emerald:#34d399;
  --glass:rgba(19,24,20,.56);
  --glass-hi:rgba(12,16,13,.86);
  --stroke:rgba(255,255,255,.07); --stroke-2:rgba(255,255,255,.13);
  --r-xl:30px; --r-lg:24px; --r-md:16px; --r-sm:11px;
  --blur:blur(28px) saturate(155%);
  --shadow:0 30px 60px -28px rgba(0,0,0,.85),0 8px 20px -12px rgba(0,0,0,.6);
  --ease:cubic-bezier(.22,.8,.24,1);
  --gap:14px; --pad:clamp(12px,1.6vw,28px);
  --mono:'JetBrains Mono',ui-monospace,SFMono-Regular,Menlo,monospace;
}
*{box-sizing:border-box}
html,body{margin:0;height:100%}
body{background:var(--bg);color:var(--ink);font:400 14px/1.45 Inter,system-ui,-apple-system,"Segoe UI",sans-serif;font-feature-settings:'cv11','ss03','tnum' 1;-webkit-font-smoothing:antialiased;text-rendering:optimizeLegibility;overflow-x:hidden}
body::after{content:"";position:fixed;inset:0;z-index:100;pointer-events:none;opacity:.045;mix-blend-mode:overlay;background-image:url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='160' height='160'><filter id='n'><feTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='2' stitchTiles='stitch'/></filter><rect width='100%' height='100%' filter='url(%23n)'/></svg>")}
button,select,input{font:inherit;color:inherit}
button{cursor:pointer;background:none;border:0;padding:0}
button:disabled,[aria-disabled=true]{opacity:.45;cursor:default}
[hidden]{display:none!important}
.sr-only{position:absolute;width:1px;height:1px;overflow:hidden;clip:rect(0 0 0 0);white-space:nowrap}
:where(button,a,input,select,[tabindex]):focus-visible{outline:2px solid var(--lime);outline-offset:3px;border-radius:10px}
::-webkit-scrollbar{width:6px;height:6px}::-webkit-scrollbar-thumb{background:rgba(255,255,255,.14);border-radius:6px}::-webkit-scrollbar-track{background:transparent}
.skip-link{position:fixed;top:10px;left:10px;z-index:200;transform:translateY(-200%);background:var(--lime);color:#10170a;padding:10px 16px;border-radius:12px;font-weight:600}
.skip-link:focus{transform:none}
.mono{font-family:var(--mono);font-feature-settings:normal}
.i{width:16px;height:16px;flex:none;fill:none;stroke:currentColor;stroke-width:1.7;stroke-linecap:round;stroke-linejoin:round}
.i.sm{width:13px;height:13px}

/* ---------- Glass primitive ---------- */
.glass{position:relative;border-radius:var(--r-lg);border:1px solid var(--stroke);
  background:linear-gradient(180deg,rgba(255,255,255,.05),rgba(255,255,255,0) 38%),var(--glass);
  -webkit-backdrop-filter:var(--blur);backdrop-filter:var(--blur);box-shadow:var(--shadow),inset 0 1px 0 rgba(255,255,255,.06)}
.glass::before{content:"";position:absolute;inset:0;border-radius:inherit;padding:1px;pointer-events:none;
  background:linear-gradient(155deg,rgba(255,255,255,.24),rgba(255,255,255,0) 32%,rgba(255,255,255,0) 68%,rgba(191,242,74,.16));
  -webkit-mask:linear-gradient(#000 0 0) content-box,linear-gradient(#000 0 0);-webkit-mask-composite:xor;mask-composite:exclude}
.glass.strong{background:linear-gradient(180deg,rgba(255,255,255,.05),rgba(255,255,255,0) 38%),var(--glass-hi)}
.card{padding:16px 18px}
.eyebrow{font-size:10.5px;font-weight:600;letter-spacing:.1em;text-transform:uppercase;color:var(--ink-3)}
.card-h{display:flex;align-items:center;justify-content:space-between;gap:10px;margin-bottom:12px;min-height:30px}
.card-title{margin:0;font-size:13.5px;font-weight:600;letter-spacing:-.01em;color:var(--ink)}
.meta{font-size:11px;color:var(--ink-3)}
.icon-btn{width:32px;height:32px;border-radius:11px;display:grid;place-items:center;color:var(--ink-3);border:1px solid transparent;transition:.2s var(--ease)}
.icon-btn:hover{color:#fff;background:rgba(255,255,255,.08);border-color:var(--stroke)}
.pill{display:inline-flex;align-items:center;gap:6px;padding:4px 10px;border-radius:999px;font-size:11px;font-weight:600;border:1px solid var(--stroke-2);white-space:nowrap;line-height:1.3}
.pill .dot{width:6px;height:6px;border-radius:50%;background:currentColor;box-shadow:0 0 8px currentColor}
.pill.ok{color:var(--lime);background:rgba(191,242,74,.09);border-color:rgba(191,242,74,.28)}
.pill.warn{color:var(--amber);background:rgba(245,179,66,.1);border-color:rgba(245,179,66,.3)}
.pill.warn .dot{animation:blink 1.6s ease-in-out infinite}
.pill.is-stale{color:#fda4af;background:rgba(244,63,94,.12);border-color:rgba(251,113,133,.4)}
.big{font-size:30px;font-weight:600;letter-spacing:-.035em;line-height:1;font-variant-numeric:tabular-nums}
.big small{font-size:13px;font-weight:500;letter-spacing:0;color:var(--ink-3);margin-left:4px}

/* ---------- App shell ---------- */
.app{position:relative;display:flex;flex-direction:column;gap:var(--gap);min-height:100dvh;padding:calc(var(--pad) + env(safe-area-inset-top,0px)) calc(var(--pad) + env(safe-area-inset-right,0px)) calc(var(--pad) + env(safe-area-inset-bottom,0px)) calc(var(--pad) + env(safe-area-inset-left,0px));isolation:isolate}
.topbar{position:relative;z-index:20;display:flex;align-items:center;justify-content:space-between;gap:12px;padding:8px 10px 8px 12px;border-radius:22px}
.nav-left,.nav-right{display:flex;align-items:center;gap:clamp(8px,1vw,16px)}
.brand{display:flex;align-items:center;gap:10px;font-weight:700;font-size:16.5px;letter-spacing:-.02em}
.brand-mark{width:34px;height:34px;border-radius:11px;display:grid;place-items:center;color:#0c1406;background:linear-gradient(145deg,#e4ff8a,#8fd11a 55%,#3f7d0b);box-shadow:0 6px 18px -4px rgba(143,209,26,.55),inset 0 1px 0 rgba(255,255,255,.55)}
.nav-links{display:flex;gap:2px;padding:3px;border-radius:14px;background:rgba(0,0,0,.34);border:1px solid var(--stroke)}
.nav-item{padding:7px clamp(9px,1vw,15px);border-radius:11px;font-size:12px;font-weight:550;color:var(--ink-3);white-space:nowrap;border:1px solid transparent;transition:.25s var(--ease)}
.nav-item:hover{color:#fff}
.nav-item[aria-current]{color:#fff;background:linear-gradient(180deg,rgba(255,255,255,.14),rgba(255,255,255,.07));border-color:var(--stroke-2);box-shadow:inset 0 1px 0 rgba(255,255,255,.12)}
.inventory{display:none;gap:4px;font-size:11.5px;color:var(--ink-2)}
.inventory span{padding:5px 9px;border-radius:9px;background:rgba(255,255,255,.05);white-space:nowrap}
.inventory b{color:#fff;font-weight:600}
.sim-toggle{display:flex;align-items:center;gap:8px;padding:7px 12px;border-radius:12px;font-size:11.5px;font-weight:600;color:var(--lime);background:rgba(191,242,74,.09);border:1px solid rgba(191,242,74,.28);transition:.25s var(--ease)}
.sim-toggle:hover{background:rgba(191,242,74,.16)}
.sim-toggle .pulse{width:7px;height:7px;border-radius:50%;background:var(--lime);box-shadow:0 0 0 0 rgba(191,242,74,.6);animation:ping 2s infinite}
.sim-toggle.paused{color:var(--amber);background:rgba(245,179,66,.09);border-color:rgba(245,179,66,.3)}
.sim-toggle.paused .pulse{background:var(--amber);animation:none;box-shadow:none}
.nav-search{display:none;position:relative;width:clamp(150px,14vw,220px)}
.nav-search input{width:100%;padding:8px 32px 8px 13px;border-radius:12px;font-size:12px;background:rgba(255,255,255,.05);border:1px solid var(--stroke);color:var(--ink);transition:.2s}
.nav-search input::placeholder{color:var(--ink-3)}
.nav-search input:focus{outline:0;border-color:rgba(191,242,74,.5);background:rgba(255,255,255,.08);box-shadow:0 0 0 4px rgba(191,242,74,.1)}
.nav-search .i{position:absolute;right:11px;top:50%;translate:0 -50%;color:var(--ink-3);pointer-events:none}
.search-results{position:absolute;top:calc(100% + 8px);inset-inline:0;z-index:30;padding:6px;min-width:190px;border-radius:16px;font-size:12px;color:var(--ink-3)}
.search-results button{display:block;width:100%;text-align:left;padding:8px 10px;border-radius:10px;color:var(--ink)}
.search-results button:hover,.search-results button:focus-visible{background:rgba(255,255,255,.08)}
.chip-status{display:none;align-items:center;gap:7px;padding:7px 11px;border-radius:12px;font-size:11px;font-weight:600;color:var(--emerald);background:rgba(52,211,153,.08);border:1px solid rgba(52,211,153,.24)}
.bell{position:relative}
.bell::after{content:"";position:absolute;top:7px;right:8px;width:7px;height:7px;border-radius:50%;background:var(--lime);box-shadow:0 0 0 2px #151a16,0 0 10px var(--lime)}
.avatar{width:34px;height:34px;border-radius:12px;display:grid;place-items:center;font-size:11.5px;font-weight:700;color:var(--lime);background:linear-gradient(145deg,#2b312c,#161a17);border:1px solid var(--stroke-2);flex:none}
.menu-toggle{display:none;padding:8px 13px;border-radius:12px;font-size:12px;font-weight:600;background:rgba(255,255,255,.07);border:1px solid var(--stroke-2)}

.subhead{position:relative;z-index:10;display:flex;align-items:flex-end;justify-content:space-between;gap:14px;flex-wrap:wrap;padding:2px 6px}
.page-title{margin:0;font-size:clamp(24px,2.6vw,38px);font-weight:650;letter-spacing:-.04em;line-height:1.05;text-shadow:0 2px 24px rgba(0,0,0,.5)}
.page-sub{margin:6px 0 0;font-size:12.5px;color:var(--ink-2);text-shadow:0 1px 12px rgba(0,0,0,.6)}
.weather{display:flex;gap:8px;flex-wrap:wrap}
.wchip{display:flex;align-items:center;gap:9px;padding:8px 14px;border-radius:999px;font-size:12px;font-weight:550;color:var(--ink);background:rgba(16,21,17,.5);-webkit-backdrop-filter:var(--blur);backdrop-filter:var(--blur);border:1px solid var(--stroke-2);box-shadow:inset 0 1px 0 rgba(255,255,255,.08)}
.wchip small{display:block;font-size:10.5px;color:var(--ink-3);font-weight:500;line-height:1.1}
.wchip .i{width:17px;height:17px}
.wchip b{font-weight:650;display:block;line-height:1.15}

/* ---------- Alert ---------- */
.alert{position:fixed;z-index:60;top:calc(14px + env(safe-area-inset-top,0px));left:50%;translate:-50% 0;width:min(680px,calc(100% - 24px));display:flex;align-items:center;justify-content:space-between;gap:14px;padding:11px 14px;border-radius:18px;font-size:12px;color:#ffd5db;background:linear-gradient(180deg,rgba(244,63,94,.26),rgba(244,63,94,.14));border:1px solid rgba(251,113,133,.45);-webkit-backdrop-filter:blur(22px);backdrop-filter:blur(22px);box-shadow:0 24px 50px -18px rgba(244,63,94,.5);transition:.4s var(--ease)}
.alert.hidden{opacity:0;translate:-50% -140%;pointer-events:none}
.alert-tag{font-weight:700;font-size:10.5px;letter-spacing:.08em;text-transform:uppercase;color:#fecdd3;background:rgba(76,5,25,.6);padding:3px 8px;border-radius:7px;border:1px solid rgba(251,113,133,.35);white-space:nowrap}
.alert-body{display:flex;align-items:center;gap:10px;min-width:0}
.alert-dismiss{padding:6px 12px;border-radius:10px;font-weight:600;font-size:11.5px;background:rgba(251,113,133,.2);color:#fff;border:1px solid rgba(251,113,133,.3);white-space:nowrap}
.alert-dismiss:hover{background:rgba(251,113,133,.35)}

/* ---------- Map ---------- */
.map{position:relative;z-index:1;height:clamp(400px,58dvh,600px);border-radius:var(--r-xl);overflow:hidden;border:1px solid var(--stroke);background:radial-gradient(ellipse at 60% 45%,#2a4328,#122017 66%,#070c09);touch-action:pan-y;user-select:none;box-shadow:var(--shadow)}
#map-stage{position:absolute;top:0;left:0;width:100%;height:100%;transform-origin:center;transition:transform .35s var(--ease);--counter-angle:0deg;--counter-scale:1;will-change:transform}
#map-stage.dragging{transition:none}
.map-image{position:absolute;inset:0;width:100%;height:100%;object-fit:cover;pointer-events:none;filter:saturate(.92) contrast(1.06) brightness(.82);transition:filter .4s ease}
.map-vectors{position:absolute;inset:0;width:100%;height:100%;pointer-events:none;overflow:visible}
.map-vectors g[id$="group"] .hit,.map-vectors .marker{pointer-events:all;cursor:pointer}
.map[data-layer=ndvi] .map-image{filter:hue-rotate(34deg) saturate(2) contrast(1.15) brightness(.85)}
.map[data-layer=soil] .map-image{filter:sepia(.85) saturate(1.5) contrast(1.1) brightness(.82)}
.map::after{content:"";position:absolute;inset:0;z-index:1;pointer-events:none;opacity:0;mix-blend-mode:soft-light;transition:opacity .4s;background:linear-gradient(144deg,#b13527,#e7b43a 44%,#63bc39 72%)}
.map[data-layer=ndvi]::after{opacity:.45}
.map[data-layer=soil]::after{opacity:.5;background:linear-gradient(135deg,#7d4121,#eab260 64%,#6b4428)}
.veil{position:absolute;inset:0;pointer-events:none;z-index:1}
.veil.a{background:linear-gradient(90deg,rgba(5,8,6,.88),rgba(5,8,6,.25) 42%,rgba(5,8,6,.55))}
.veil.b{background:linear-gradient(0deg,rgba(5,8,6,.92),rgba(5,8,6,0) 45%,rgba(5,8,6,.7))}
.veil.c{background:radial-gradient(ellipse at 58% 46%,transparent 28%,rgba(3,6,4,.7) 100%)}

.field-trigger{position:absolute;left:63%;top:48%;z-index:3;min-width:44px;min-height:44px;display:flex;align-items:center;gap:10px;text-align:left;transform-origin:24px 50%;transform:translate(-24px,-50%) rotate(var(--counter-angle)) scale(var(--counter-scale))}
.radar{position:relative;width:48px;height:48px;display:grid;place-items:center;flex:none}
.radar i{position:absolute;border-radius:50%;border:1px solid rgba(191,242,74,.55);animation:radar 2.8s cubic-bezier(.215,.61,.355,1) infinite}
.radar i:nth-child(1){width:48px;height:48px}
.radar i:nth-child(2){width:32px;height:32px;animation-delay:.9s}
.radar b{position:relative;width:28px;height:28px;border-radius:50%;display:grid;place-items:center;background:rgba(191,242,74,.18);border:1px solid var(--lime);box-shadow:0 0 22px rgba(191,242,74,.7),inset 0 0 8px rgba(191,242,74,.4);-webkit-backdrop-filter:blur(8px);backdrop-filter:blur(8px)}
.radar b::after{content:"";width:9px;height:9px;border-radius:50%;background:#fff;box-shadow:0 0 8px #fff}
.field-label{display:flex;align-items:center;gap:12px;padding:9px 14px 9px 10px;border-radius:18px;white-space:nowrap;background:linear-gradient(180deg,rgba(255,255,255,.07),rgba(255,255,255,0)),rgba(12,17,13,.78);-webkit-backdrop-filter:var(--blur);backdrop-filter:var(--blur);border:1px solid rgba(191,242,74,.32);box-shadow:var(--shadow),0 0 24px -6px rgba(191,242,74,.35);transition:.3s var(--ease)}
.field-trigger:hover .field-label,.field-trigger[aria-expanded=true] .field-label{border-color:var(--lime);box-shadow:var(--shadow),0 0 32px -4px rgba(191,242,74,.55)}
.field-ico{width:34px;height:34px;border-radius:11px;display:grid;place-items:center;color:var(--lime);background:rgba(191,242,74,.13);border:1px solid rgba(191,242,74,.32)}
.field-name{display:flex;align-items:center;gap:6px;font-size:13.5px;font-weight:650;letter-spacing:-.01em}
.field-name .i{color:var(--ink-3)}
.field-meta{display:flex;align-items:center;gap:6px;margin-top:2px;font-size:11.5px;font-weight:600;color:var(--lime)}
.field-meta .dot{width:6px;height:6px;border-radius:50%;background:var(--lime);box-shadow:0 0 8px var(--lime)}
.field-meta span:last-child{color:rgba(191,242,74,.72);font-weight:500}

.map-tools{position:absolute;z-index:6;top:12px;right:12px;display:flex;flex-direction:column;align-items:flex-end;gap:10px}
.layers{padding:6px;display:flex;flex-direction:column;gap:2px;border-radius:20px;width:168px}
.layer{display:flex;align-items:center;gap:10px;padding:6px 10px 6px 6px;border-radius:14px;text-align:left;border:1px solid transparent;color:var(--ink-2);transition:.2s var(--ease)}
.layer:hover{background:rgba(255,255,255,.07);color:#fff}
.layer[aria-pressed=true]{color:#fff;background:rgba(255,255,255,.1);border-color:rgba(191,242,74,.4)}
.thumb{width:32px;height:32px;border-radius:50%;flex:none;border:1.5px solid rgba(255,255,255,.22);box-shadow:inset 0 0 8px rgba(0,0,0,.5)}
.layer[aria-pressed=true] .thumb{border-color:var(--lime)}
.t-sat{background:radial-gradient(circle at 35% 30%,#8bc24a,#2f6a1c 55%,#173d12)}
.t-ndvi{background:linear-gradient(140deg,#c2410c,#facc15 50%,#16a34a)}
.t-soil{background:radial-gradient(circle at 40% 35%,#a5603a,#6b3a22 60%,#3b2113)}
.t-drone{background:radial-gradient(circle,#0c4a6e,#082f49);display:grid;place-items:center;color:var(--sky)}
.lc b{display:block;font-size:12px;font-weight:600}
.lc small{display:block;font-size:10.5px;color:var(--ink-3);font-family:var(--mono)}
.layer[aria-pressed=true] .lc small{color:var(--lime)}
#drone-layer-toggle[aria-pressed=true] .lc small{color:var(--sky)}
.ctrls{padding:5px;display:flex;flex-direction:column;align-items:center;gap:2px;border-radius:18px}
.ctrls button{width:36px;height:36px;border-radius:12px;display:grid;place-items:center;color:var(--ink-2);transition:.2s var(--ease)}
.ctrls button:hover{color:#fff;background:rgba(255,255,255,.1)}
.ctrls hr{width:18px;height:1px;border:0;background:var(--stroke-2);margin:2px 0}
.map-caption{position:absolute;z-index:3;left:12px;bottom:12px;margin:0;padding:6px 12px;border-radius:999px;font-size:11px;color:var(--ink-2);pointer-events:none;background:rgba(12,17,13,.6);-webkit-backdrop-filter:blur(14px);backdrop-filter:blur(14px);border:1px solid var(--stroke-2)}
.map-detail,.view-panel{position:absolute;z-index:7;left:12px;bottom:52px;width:min(310px,calc(100% - 200px));padding:16px 18px;min-width:230px}
.map-detail h2,.view-panel h2{margin:0;font-size:15px;font-weight:650;letter-spacing:-.01em}
.map-detail p,.view-panel p{margin:6px 0 0;font-size:12.5px;color:var(--ink-2)}
.link-btn{margin-top:10px;font-size:12.5px;font-weight:600;color:var(--lime)}
.link-btn:hover{text-decoration:underline}

/* ---------- Left rail ---------- */
.rail{position:relative;z-index:5;display:grid;grid-template-columns:repeat(auto-fit,minmax(290px,1fr));gap:12px;align-content:start}
.gauge-row{display:flex;align-items:flex-end;justify-content:space-between;gap:12px}
.gauge{position:relative;width:150px;height:88px;flex:none}
.gauge svg{width:100%;height:100%;overflow:visible}
.gauge .tick{stroke:rgba(255,255,255,.12);stroke-width:3.2;stroke-linecap:round;transition:stroke .5s,opacity .5s}
.gauge .tick.on{filter:drop-shadow(0 0 3px rgba(191,242,74,.55))}
.gauge-val{position:absolute;inset:auto 0 0 0;text-align:center;font-size:32px;font-weight:600;letter-spacing:-.04em;line-height:1}
.gauge-val span{font-size:14px;color:var(--lime);margin-left:2px;letter-spacing:0}
.area{text-align:right}
.area .big{font-size:34px}
.delta{display:inline-flex;align-items:center;gap:5px;margin-top:8px;padding:3px 9px;border-radius:999px;font-size:11px;font-weight:600;color:var(--emerald);background:rgba(52,211,153,.1);border:1px solid rgba(52,211,153,.22)}
.select-wrap{position:relative}
.select-wrap select{appearance:none;-webkit-appearance:none;padding:6px 28px 6px 12px;border-radius:999px;font-size:11.5px;font-weight:550;background:rgba(255,255,255,.07);border:1px solid var(--stroke-2);color:var(--ink);cursor:pointer}
.select-wrap select option{background:#131a15}
.select-wrap .i{position:absolute;right:9px;top:50%;translate:0 -50%;pointer-events:none;width:12px;height:12px;color:var(--ink-3)}
.trend{position:relative}
.trend svg{display:block;width:100%;height:auto;overflow:visible;touch-action:none}
.trend text{fill:var(--ink-4);font-size:8.5px;font-family:Inter,sans-serif}
.trend text.hl{fill:var(--lime);font-weight:700}
.tip{position:absolute;top:-6px;z-index:3;pointer-events:none;opacity:0;transform:translate(-50%,-100%);padding:4px 9px;border-radius:9px;font-size:10.5px;font-family:var(--mono);white-space:nowrap;color:var(--lime);background:rgba(5,8,6,.92);border:1px solid rgba(191,242,74,.35);transition:opacity .15s}
.matrix{display:grid;grid-template-columns:repeat(16,1fr);gap:4px;padding:11px;border-radius:16px;background:rgba(0,0,0,.34);border:1px solid var(--stroke)}
.matrix i{aspect-ratio:1;border-radius:5px;position:relative;transition:transform .2s var(--ease),filter .2s;box-shadow:inset 0 1px 0 rgba(255,255,255,.35),0 0 10px -2px var(--c)}
.matrix i:hover{transform:scale(1.35);z-index:2;filter:brightness(1.2)}
.matrix i.c::after,.matrix i.s::after{content:"";position:absolute;inset:0;border-radius:inherit}
.matrix i.c::after{background-image:repeating-linear-gradient(135deg,transparent 0 2px,rgba(20,20,20,.5) 2px 3px)}
.matrix i.s::after{background-image:radial-gradient(circle,rgba(20,10,10,.8) 1px,transparent 1.5px);background-size:4px 4px}
.matrix-legend{display:flex;gap:12px;margin:9px 2px 0;font-size:11px;color:var(--ink-2)}
.matrix-legend span{display:flex;align-items:center;gap:6px}
.matrix-legend i{width:8px;height:8px;border-radius:3px}
.foot-row{display:flex;align-items:center;justify-content:space-between;gap:10px;margin-top:12px;padding-top:12px;border-top:1px solid var(--stroke);font-size:11.5px;color:var(--ink-2)}
.ai-btn{display:inline-flex;align-items:center;gap:6px;padding:6px 12px;border-radius:999px;font-size:11.5px;font-weight:650;color:#142007;background:linear-gradient(180deg,#d4fa72,#a8e02a);box-shadow:0 8px 20px -6px rgba(168,224,42,.6),inset 0 1px 0 rgba(255,255,255,.55);transition:.25s var(--ease)}
.ai-btn:hover{transform:translateY(-1px);box-shadow:0 12px 26px -6px rgba(168,224,42,.75),inset 0 1px 0 rgba(255,255,255,.55)}
.mini-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-top:12px}
.mini{display:flex;align-items:center;gap:10px;padding:10px;border-radius:14px;background:rgba(255,255,255,.04);border:1px solid var(--stroke)}
.mini .ico{width:30px;height:30px;border-radius:50%;display:grid;place-items:center;flex:none;color:var(--lime);background:rgba(191,242,74,.1);border:1px solid rgba(191,242,74,.22)}
.mini small{display:block;font-size:10.5px;color:var(--ink-3)}
.mini b{display:block;font-size:17px;font-weight:600;letter-spacing:-.02em;line-height:1.15}
.mini em{display:block;font-style:normal;font-size:10px;color:var(--ink-4);font-family:var(--mono)}

/* ---------- Dock ---------- */
.dock{position:relative;z-index:5;display:grid;gap:12px;grid-template-columns:1fr}
.ops{display:flex;flex-direction:column;gap:12px;container-type:inline-size;transition:.3s var(--ease)}
.ops:hover{border-color:rgba(191,242,74,.28);transform:translateY(-2px)}
.ops-head{display:flex;align-items:flex-start;justify-content:space-between;gap:8px}
.ops-head h3{margin:0;font-size:14.5px;font-weight:650;letter-spacing:-.02em}
.ops-head time{display:block;margin-top:1px;font-size:10.5px;color:var(--ink-3);font-family:var(--mono)}
.ops-mid{display:flex;align-items:center;justify-content:space-between;gap:10px}
.ops-mid .col{display:flex;flex-direction:column;align-items:flex-start;gap:8px}
.vehicle{width:70px;height:44px;flex:none;fill:none;stroke:rgba(255,255,255,.62);stroke-width:1.2;stroke-linecap:round;stroke-linejoin:round}
.vehicle.amber{stroke:rgba(245,179,66,.8)}
.chart-box{padding:8px 10px 8px;border-radius:14px;background:rgba(0,0,0,.3);border:1px solid var(--stroke)}
.chart-box svg{display:block;width:100%;height:42px}
.chart-box .axis{display:flex;justify-content:space-between;margin-top:2px;font-size:10px;color:var(--ink-3);font-family:var(--mono)}
.track{position:relative;height:4px;border-radius:4px;margin-top:8px;background:rgba(255,255,255,.1)}
.track i{position:absolute;inset:0 auto 0 0;width:50%;border-radius:inherit;transition:width 1s var(--ease)}
.track i::after{content:"";position:absolute;right:-5px;top:50%;translate:0 -50%;width:10px;height:10px;border-radius:50%;background:#fff;box-shadow:0 0 0 3px rgba(255,255,255,.18),0 2px 6px rgba(0,0,0,.5)}
.track.lime i{background:linear-gradient(90deg,#4d7c0f,#bff24a)}
.track.amber i{background:linear-gradient(90deg,#b45309,#fcd34d)}
.stats{display:grid;grid-template-columns:repeat(3,1fr);gap:8px;padding-top:12px;margin-top:auto;border-top:1px solid var(--stroke)}
.stats small{display:block;font-size:10.5px;color:var(--ink-3)}
.stats b{display:block;font-size:14px;font-weight:650;letter-spacing:-.02em;font-variant-numeric:tabular-nums}
.stats > div:nth-child(2){text-align:center}.stats > div:nth-child(3){text-align:right}
.irr-top{display:flex;align-items:flex-end;justify-content:space-between;gap:10px}
.irr-top .meta{margin-top:5px}
.tbl-wrap{border-radius:14px;overflow:hidden;border:1px solid var(--stroke);background:rgba(0,0,0,.3)}
.tbl{width:100%;border-collapse:collapse;text-align:center;font-size:11.5px}
.tbl th{font-weight:500;color:var(--ink-3);padding:6px 4px;font-size:10.5px}
.tbl thead tr{background:rgba(255,255,255,.04)}
.tbl tbody tr+tr th,.tbl tbody tr+tr td{border-top:1px solid var(--stroke)}
.tbl tbody th{text-align:left;padding:8px 10px;color:var(--ink-2);font-size:11.5px}
.tbl td{font-family:var(--mono);color:var(--ink-2);padding:8px 4px}
.tbl td.up{color:var(--amber);font-weight:500}
.tbl td.up::before{content:"◔ ";font-size:10px}
.tbl td.bad{color:var(--rose);font-weight:600}
.tbl td.bad.pulse{animation:blink 1s infinite}
.irr-foot{display:flex;justify-content:space-between;font-size:11px;color:var(--ink-3);padding-top:10px;border-top:1px solid var(--stroke);margin-top:auto}
.yield-body{display:grid;gap:10px}
.yield-body .num{display:flex;align-items:baseline;gap:7px;flex-wrap:wrap}
.hist-wrap{position:relative}
.hist{display:flex;align-items:flex-end;gap:3px;height:68px;padding:8px 8px 6px;border-radius:14px;background:rgba(0,0,0,.3);border:1px solid var(--stroke)}
.hist b{flex:1;min-width:0;border-radius:3px 3px 1px 1px;background:linear-gradient(180deg,rgba(255,255,255,.2),rgba(255,255,255,.07));cursor:pointer;transition:.18s}
.hist b:hover{background:var(--lime)}
.hist b.peak{background:linear-gradient(180deg,#e2ff8c,#84cc16);box-shadow:0 0 14px rgba(191,242,74,.6)}
@container (min-width:330px){.yield-body{grid-template-columns:auto 1fr;align-items:end}}
.run{display:flex;justify-content:space-between;font-size:11px;padding-top:10px;margin-top:auto;border-top:1px solid var(--stroke);color:var(--ink-3)}
.run b{color:var(--lime);font-weight:650}

/* ---------- Dialog ---------- */
dialog{margin:auto;width:min(440px,calc(100% - 32px));padding:22px;color:var(--ink);border-radius:var(--r-lg);border:1px solid var(--stroke-2);background:linear-gradient(180deg,rgba(255,255,255,.06),transparent 40%),rgba(14,19,15,.94);-webkit-backdrop-filter:blur(30px);backdrop-filter:blur(30px);box-shadow:0 40px 90px -20px #000}
dialog::backdrop{background:rgba(2,5,3,.66);-webkit-backdrop-filter:blur(6px);backdrop-filter:blur(6px)}
dialog[open]{animation:pop .3s var(--ease)}
dialog h2{margin:0;font-size:18px;font-weight:650;letter-spacing:-.02em}
dialog p{margin:10px 0 0;font-size:13.5px;color:var(--ink-2);line-height:1.6}
dialog .close{margin-top:18px;padding:9px 18px;border-radius:12px;font-size:12.5px;font-weight:600;background:rgba(255,255,255,.09);border:1px solid var(--stroke-2)}
dialog .close:hover{background:rgba(255,255,255,.15)}

/* ---------- Motion ---------- */
@keyframes radar{0%{transform:scale(.65);opacity:.9}50%{transform:scale(1.6);opacity:.25}100%{transform:scale(2.4);opacity:0}}
@keyframes ping{0%{box-shadow:0 0 0 0 rgba(191,242,74,.55)}70%,100%{box-shadow:0 0 0 9px rgba(191,242,74,0)}}
@keyframes blink{50%{opacity:.35}}
@keyframes pop{from{opacity:0;transform:translateY(10px) scale(.97)}}
@keyframes rise{from{opacity:0;transform:translateY(14px)}}
@keyframes dronePulse{0%,100%{transform:scale(1);opacity:.9}50%{transform:scale(1.3);opacity:1}}
.drone-anim{animation:dronePulse 1.8s ease-in-out infinite;transform-box:fill-box;transform-origin:center}
.glass.card,.topbar,.subhead{animation:rise .7s var(--ease) both}
.rail .glass:nth-child(2){animation-delay:.08s}.rail .glass:nth-child(3){animation-delay:.16s}
.dock .glass:nth-child(2){animation-delay:.06s}.dock .glass:nth-child(3){animation-delay:.12s}.dock .glass:nth-child(4){animation-delay:.18s}

/* ---------- Breakpoints ---------- */
@media(min-width:700px){.dock{grid-template-columns:repeat(2,minmax(0,1fr))}}
@media(min-width:900px){.chip-status{display:flex}}
@media(min-width:1100px){.nav-search{display:block}}
@media(min-width:1500px){.inventory{display:flex}}
@media(max-width:899px){
  .menu-toggle{display:block}
  .nav-links{display:none;position:absolute;inset-inline:0;top:calc(100% + 8px);z-index:12;padding:6px;flex-direction:column;background:rgba(14,19,15,.96);border-radius:18px}
  .nav-links.is-open{display:flex}
  .nav-item{text-align:left;padding:10px 12px}
  .sim-toggle span:last-child{display:none}
  .sim-toggle{padding:10px}
  .avatar{display:none}
}
@media(max-width:767px){
  .weather .wchip:nth-child(n+3){display:none}
  .map{height:clamp(420px,66dvh,560px)}
  .map-tools{flex-direction:row;align-items:flex-start;top:8px;right:8px;gap:6px}
  .layers{width:auto;flex-direction:column}
  .layer{padding:4px}.lc,.layer .lc small{display:none}
  .lc{display:none}
  .map-detail,.view-panel{width:calc(100% - 24px);bottom:48px}
  button:not(.skip-link),select{min-height:44px}
  .icon-btn,.ctrls button{min-height:0}
  .field-label{padding:7px 10px}.field-ico{display:none}
}
@media(min-width:1180px){
  .app{height:100dvh;min-height:640px;display:grid;overflow:hidden;gap:12px 16px;
    grid-template-columns:minmax(300px,340px) minmax(0,1fr);grid-template-rows:auto auto minmax(0,1fr) auto}
  .map{position:absolute;inset:12px;height:auto;border-radius:34px;z-index:0}
  .topbar{grid-column:1/-1;grid-row:1}
  .subhead{grid-column:1/-1;grid-row:2}
  .rail{grid-column:1;grid-row:3/5;min-height:0;overflow-y:auto;display:flex;flex-direction:column;padding:2px 4px 2px 0;margin-right:-4px;
    -webkit-mask-image:linear-gradient(180deg,#000 calc(100% - 22px),transparent);mask-image:linear-gradient(180deg,#000 calc(100% - 22px),transparent);padding-bottom:20px}
  .rail>.glass{flex:none}
  .dock{grid-column:2;grid-row:4;grid-template-columns:1fr 1fr 1.3fr 1.3fr;align-self:end}
  .map-tools{top:calc(var(--pad) + 112px);right:calc(var(--pad) + 4px)}
  .map-caption{left:auto;bottom:auto;top:calc(var(--pad) + 112px);left:392px}
  .map-detail,.view-panel{left:392px;bottom:auto;top:calc(var(--pad) + 150px);width:310px}
}
@media(min-width:1180px) and (max-height:800px){
  .map-tools{flex-direction:row;align-items:flex-start}
  .layers{width:auto;flex-direction:column}
  .layer .lc{display:none}
  .layer{padding:5px}
}
@media(prefers-reduced-motion:reduce){*,*::before,*::after{animation:none!important;transition:none!important;scroll-behavior:auto!important}}
</style>
</head>
<body>
<a class="skip-link" href="#content">Skip to content</a>

<svg width="0" height="0" style="position:absolute" aria-hidden="true" focusable="false"><defs>
  <symbol id="i-logo" viewBox="0 0 24 24"><path d="M12 3 3 7.5l9 4.5 9-4.5zM3 12l9 4.5 9-4.5M3 16.5 12 21l9-4.5"/></symbol>
  <symbol id="i-search" viewBox="0 0 24 24"><circle cx="11" cy="11" r="6.5"/><path d="m20 20-4-4"/></symbol>
  <symbol id="i-bell" viewBox="0 0 24 24"><path d="M6 16v-5a6 6 0 0 1 12 0v5l1.5 2h-15z"/><path d="M10 21h4"/></symbol>
  <symbol id="i-wifi" viewBox="0 0 24 24"><path d="M3 9a14 14 0 0 1 18 0M6 12.5a9.5 9.5 0 0 1 12 0M9 16a5 5 0 0 1 6 0"/><circle cx="12" cy="19" r=".8"/></symbol>
  <symbol id="i-arrow" viewBox="0 0 24 24"><path d="M7 17 17 7M9 7h8v8"/></symbol>
  <symbol id="i-chev-d" viewBox="0 0 24 24"><path d="m6 9 6 6 6-6"/></symbol>
  <symbol id="i-chev-r" viewBox="0 0 24 24"><path d="m9 6 6 6-6 6"/></symbol>
  <symbol id="i-leaf" viewBox="0 0 24 24"><path d="M5 19C5 10 10 5 20 5c0 9-5 15-13 15"/><path d="M5 19c3-5 6-8 10-10"/></symbol>
  <symbol id="i-sun" viewBox="0 0 24 24"><circle cx="12" cy="12" r="4"/><path d="M12 2v2M12 20v2M2 12h2M20 12h2M5 5l1.5 1.5M17.5 17.5 19 19M19 5l-1.5 1.5M6.5 17.5 5 19"/></symbol>
  <symbol id="i-wind" viewBox="0 0 24 24"><path d="M3 9h11a3 3 0 1 0-3-3M3 15h15a3 3 0 1 1-3 3M3 12h7"/></symbol>
  <symbol id="i-drop" viewBox="0 0 24 24"><path d="M12 3c4 5 6 8 6 11a6 6 0 0 1-12 0c0-3 2-6 6-11z"/></symbol>
  <symbol id="i-therm" viewBox="0 0 24 24"><path d="M10 14V5a2 2 0 0 1 4 0v9a4 4 0 1 1-4 0z"/></symbol>
  <symbol id="i-spark" viewBox="0 0 24 24"><path d="m11 3 1.8 5.2L18 10l-5.2 1.8L11 17l-1.8-5.2L4 10l5.2-1.8z"/><path d="m19 15 .7 2 2 .7-2 .7-.7 2-.7-2-2-.7 2-.7z"/></symbol>
  <symbol id="i-compass" viewBox="0 0 24 24"><circle cx="12" cy="12" r="8.5"/><path d="m15.5 8.5-2 5-5 2 2-5z"/></symbol>
  <symbol id="i-plus" viewBox="0 0 24 24"><path d="M12 5v14M5 12h14"/></symbol>
  <symbol id="i-minus" viewBox="0 0 24 24"><path d="M5 12h14"/></symbol>
  <symbol id="i-fit" viewBox="0 0 24 24"><path d="M4 9V5h4M20 9V5h-4M4 15v4h4M20 15v4h-4"/></symbol>
  <symbol id="i-rotate" viewBox="0 0 24 24"><path d="M20 12a8 8 0 1 1-2.5-5.8M20 4v4h-4"/></symbol>
  <symbol id="i-drone" viewBox="0 0 24 24"><circle cx="12" cy="12" r="2"/><path d="M10.5 10.5 6 6M13.5 10.5 18 6M10.5 13.5 6 18M13.5 13.5 18 18"/><circle cx="5" cy="5" r="2"/><circle cx="19" cy="5" r="2"/><circle cx="5" cy="19" r="2"/><circle cx="19" cy="19" r="2"/></symbol>
</defs></svg>

<!-- Irrigation alert -->
<div class="alert hidden" id="irrigation-alert-banner" role="alert">
  <div class="alert-body">
    <span class="alert-tag">Irrigation Alert</span>
    <span id="alert-banner-text">Irrigation variance exceeded ±3.0 min threshold in Zone B.</span>
  </div>
  <button class="alert-dismiss" id="alert-dismiss-btn" type="button">Dismiss</button>
</div>

<div class="app" id="app">

  <header class="glass strong topbar" aria-label="Primary">
    <nav class="nav-left" aria-label="Primary">
      <div class="brand"><span class="brand-mark"><svg class="i" style="width:18px;height:18px;stroke-width:2.2"><use href="#i-logo"/></svg></span>Furrow</div>
      <div class="nav-links" id="primary-links">
        <button class="nav-item" aria-current="page" data-view="map" type="button">Live Map</button>
        <button class="nav-item" data-view="fields" type="button">Fields</button>
        <button class="nav-item" data-view="analytics" type="button">Analytics</button>
        <button class="nav-item" data-view="reports" type="button">Reports</button>
        <button class="nav-item" data-view="farmers" type="button">Farmers</button>
      </div>
      <div class="inventory" aria-label="Inventory"><span><b>14</b> Fields</span><span><b>170</b> Sensors</span><span><b>13</b> Systems</span><span><b>12</b> Tractors</span></div>
    </nav>
    <div class="nav-right">
      <button class="sim-toggle" id="telemetry-toggle-btn" type="button" aria-pressed="true" title="Toggle live telemetry simulation"><span class="pulse" id="telemetry-indicator"></span><span id="telemetry-btn-text">Simulation: Live</span></button>
      <div class="nav-search">
        <input id="dashboard-search" type="search" autocomplete="off" placeholder="Search parcel, unit…" aria-label="Search parcels and equipment">
        <svg class="i" aria-hidden="true"><use href="#i-search"/></svg>
        <div class="glass strong search-results" id="search-results" hidden></div>
      </div>
      <div class="chip-status" role="status"><svg class="i sm"><use href="#i-wifi"/></svg>LTE Telemetry</div>
      <button class="icon-btn bell" data-dialog="notifications" type="button" aria-label="Notifications"><svg class="i"><use href="#i-bell"/></svg></button>
      <div class="avatar" aria-hidden="true">JD</div>
      <button class="menu-toggle" id="menu-toggle" type="button" aria-controls="primary-links" aria-expanded="false">Menu</button>
    </div>
  </header>

  <div class="subhead">
    <div>
      <h1 class="page-title" id="page-title">Field Management</h1>
      <p class="page-sub" id="page-subtitle">Field health, fleet telemetry and operations · Live simulation active</p>
    </div>
    <div class="weather" aria-label="Weather">
      <div class="wchip"><svg class="i" style="color:#fbbf24"><use href="#i-sun"/></svg><div><b>28°</b><small>Clear Sky</small></div></div>
      <div class="wchip"><svg class="i" style="color:var(--emerald)"><use href="#i-wind"/></svg><div><b id="weather-wind">12 km/h</b><small>NE</small></div></div>
      <div class="wchip"><svg class="i" style="color:var(--sky)"><use href="#i-drop"/></svg><div><b id="weather-humidity">62%</b><small>Humidity</small></div></div>
    </div>
  </div>

  <main id="content" tabindex="-1" style="display:contents">

    <!-- MAP -->
    <section class="map" id="map-view" data-layer="satellite" aria-label="Interactive farm map">
      <div id="map-stage">
        <img class="map-image" alt="Top-down aerial satellite photograph of agricultural fields" draggable="false" fetchpriority="high"
          src="https://lh3.googleusercontent.com/aida-public/AB6AXuAfk4GGG4d7WPO-mRL3z-_8N9wP4qrwAR2GqYlskSqEuq0-eBQUR2WqTj9eYZfF7cdg8fpkXCqn7SLl5AWOEmhXs89uAOcVsqp5CRt0CYfR1GSxjkXkBC5I59uqzn0sWP6Y3Ox-yUZlyY4eHScjCgE0EhplPsvGZKl2U9tTI4vPTVMPYks7-u0QuGgxUBMxEncPJ_T8j8-Pd54VInSiObsDDkgsb7xN8qCyuIWwcz4">
        <svg class="map-vectors" aria-hidden="true" focusable="false" fill="none" preserveAspectRatio="xMidYMid slice" viewBox="0 0 1920 1080" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <linearGradient id="neon" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#e4ff8a"/><stop offset=".5" stop-color="#b7f03c"/><stop offset="1" stop-color="#6aa80f"/></linearGradient>
            <radialGradient id="fieldFill" cx=".5" cy=".5" r=".7"><stop offset="0" stop-color="#d9ff6b" stop-opacity=".32"/><stop offset="1" stop-color="#7fc41a" stop-opacity=".07"/></radialGradient>
            <pattern id="hatch" width="16" height="16" patternUnits="userSpaceOnUse" patternTransform="rotate(45)"><line x1="0" y1="0" x2="0" y2="16" stroke="#bff24a" stroke-opacity=".18" stroke-width=".8"/></pattern>
            <filter id="glow" x="-20%" y="-20%" width="140%" height="140%"><feGaussianBlur stdDeviation="7" result="b"/><feMerge><feMergeNode in="b"/><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge></filter>
          </defs>
          <polygon id="parcel" points="954,342 1530,344 1532,714 1145,712 918,485 918,410" fill="url(#fieldFill)"/>
          <polygon points="954,342 1530,344 1532,714 1145,712 918,485 918,410" fill="url(#hatch)"/>
          <polygon points="954,342 1530,344 1532,714 1145,712 918,485 918,410" stroke="url(#neon)" stroke-width="3" stroke-linejoin="round" filter="url(#glow)"/>
          <g fill="#facc15" stroke="#1c1917" stroke-width="1.5"><circle cx="954" cy="342" r="4"/><circle cx="1530" cy="344" r="4"/><circle cx="1532" cy="714" r="4"/><circle cx="1145" cy="712" r="4"/><circle cx="918" cy="485" r="4"/></g>

          <g id="drone-path-group">
            <path d="M 980 370 L 1490 375 L 1490 440 L 970 440 L 970 510 L 1480 510 L 1480 580 L 1020 580 L 1020 650 L 1450 650" stroke="#5fc8ff" stroke-width="2" stroke-dasharray="6 6" opacity=".6"/>
            <g fill="#5fc8ff" stroke="#0f172a" stroke-width="1.5"><circle cx="980" cy="370" r="4"/><circle cx="1490" cy="375" r="4"/><circle cx="1490" cy="440" r="4"/><circle cx="970" cy="440" r="4"/><circle cx="1480" cy="510" r="4"/><circle cx="1020" cy="580" r="4"/></g>
            <g id="drone-marker" class="marker" transform="translate(980,370)">
              <circle r="15" fill="#0284c7" opacity=".28" class="drone-anim"/><circle r="6" fill="#5fc8ff" stroke="#fff" stroke-width="1.5"/><polygon points="0,-10 6,4 0,1 -6,4" fill="#e0f2fe"/>
              <rect x="12" y="-12" width="96" height="22" rx="11" fill="#06121acc" stroke="#5fc8ff88"/><text x="22" y="3" fill="#7dd3fc" font-size="10.5" font-weight="600" font-family="Inter,sans-serif">Drone Scan-03</text>
            </g>
          </g>
          <g id="tractor-gps-group">
            <path d="M 960 410 L 1080 410 L 1080 620 L 1150 620 L 1150 430 L 1220 430 L 1220 620" stroke="#bff24a" stroke-width="2.5" stroke-dasharray="4 4" opacity=".55"/>
            <g id="tractor-marker" class="marker" transform="translate(1080,410)">
              <circle r="13" fill="#bff24a" opacity=".25"/><circle r="5" fill="#bff24a" stroke="#0f172a" stroke-width="1.5"/>
              <rect x="10" y="-11" width="88" height="22" rx="11" fill="#09140fcc" stroke="#bff24a88"/><text x="20" y="3.5" fill="#d9f99d" font-size="10" font-weight="700" font-family="Inter,sans-serif">T-04 · 8 km/h</text>
            </g>
          </g>
          <g id="sprayer-gps-group">
            <path d="M 1320 370 L 1320 680 L 1400 680 L 1400 370 L 1470 370 L 1470 660" stroke="#f5b342" stroke-width="2.5" stroke-dasharray="4 4" opacity=".55"/>
            <g id="sprayer-marker" class="marker" transform="translate(1320,450)">
              <circle r="13" fill="#f5b342" opacity=".25"/><circle r="5" fill="#f5b342" stroke="#0f172a" stroke-width="1.5"/>
              <rect x="10" y="-11" width="88" height="22" rx="11" fill="#140f09cc" stroke="#f5b34288"/><text x="20" y="3.5" fill="#fde68a" font-size="10" font-weight="700" font-family="Inter,sans-serif">S-01 · 6 km/h</text>
            </g>
          </g>
        </svg>
        <button class="field-trigger" id="field-trigger" type="button" aria-controls="field-detail" aria-expanded="false">
          <span class="radar" aria-hidden="true"><i></i><i></i><b></b></span>
          <span class="field-label">
            <span class="field-ico"><svg class="i"><use href="#i-leaf"/></svg></span>
            <span>
              <span class="field-name">North Field <svg class="i sm"><use href="#i-chev-r"/></svg></span>
              <span class="field-meta"><span class="dot"></span><span>92% Health</span><span>· +2%</span></span>
            </span>
          </span>
        </button>
      </div>
      <div class="veil a"></div><div class="veil b"></div><div class="veil c"></div>

      <aside class="map-tools" aria-label="Map controls">
        <div class="glass strong layers" role="group" aria-label="Map layers">
          <button class="layer" type="button" aria-pressed="true" data-layer-choice="satellite"><span class="thumb t-sat"></span><span class="lc"><b>Satellite</b><small class="layer-description">RGB High-Res</small></span></button>
          <button class="layer" type="button" aria-pressed="false" data-layer-choice="ndvi"><span class="thumb t-ndvi"></span><span class="lc"><b>NDVI</b><small class="layer-description">Biomass Index</small></span></button>
          <button class="layer" type="button" aria-pressed="false" data-layer-choice="soil"><span class="thumb t-soil"></span><span class="lc"><b>Soil</b><small class="layer-description">Moisture Profile</small></span></button>
          <button class="layer" type="button" aria-pressed="true" id="drone-layer-toggle"><span class="thumb t-drone"><svg class="i sm"><use href="#i-drone"/></svg></span><span class="lc"><b>Drones</b><small class="layer-description">Flight Path</small></span></button>
        </div>
        <div class="glass strong ctrls">
          <button type="button" data-map-action="compass" aria-label="Compass orientation" title="Compass orientation"><svg class="i"><use href="#i-compass"/></svg></button>
          <hr>
          <button type="button" data-map-action="in" aria-label="Zoom in" title="Zoom in"><svg class="i"><use href="#i-plus"/></svg></button>
          <button type="button" data-map-action="out" aria-label="Zoom out" title="Zoom out"><svg class="i"><use href="#i-minus"/></svg></button>
          <hr>
          <button type="button" data-map-action="fit" aria-label="Fit bounds" title="Fit bounds"><svg class="i"><use href="#i-fit"/></svg></button>
          <button type="button" data-map-action="rotate" aria-label="Rotate map clockwise" title="Rotate map clockwise"><svg class="i"><use href="#i-rotate"/></svg></button>
        </div>
      </aside>

      <p class="map-caption" id="map-caption">Satellite imagery · Live telemetry &amp; GPS tracking active</p>

      <article class="glass strong map-detail" id="field-detail" hidden aria-labelledby="field-title">
        <h2 id="field-title">North Field</h2>
        <p>92% crop health · 248 ha monitored across the farm</p>
        <p class="meta">Last scan: 09:42 (sample reading)</p>
        <button class="link-btn" id="field-close" type="button">Close details</button>
      </article>
      <section class="glass strong view-panel" id="view-panel" hidden aria-labelledby="view-title"><h2 id="view-title"></h2><p id="view-copy"></p></section>
      <p class="sr-only" id="map-status" role="status"></p>
    </section>

    <!-- LEFT RAIL -->
    <section class="rail" id="analytics" aria-labelledby="analytics-title">
      <h2 class="sr-only" id="analytics-title">Field analytics</h2>

      <article class="glass card" data-purpose="crop-health-card" data-value="92" aria-labelledby="crop-health-title">
        <div class="card-h"><h3 class="card-title" id="crop-health-title">Crop Health</h3>
          <button class="icon-btn" data-dialog="health" type="button" aria-label="Crop health details"><svg class="i"><use href="#i-arrow"/></svg></button></div>
        <div class="gauge-row">
          <div class="gauge">
            <svg id="crop-gauge" viewBox="0 0 200 108" role="img" aria-label="Crop health: 92 percent"><g id="gauge-ticks"></g></svg>
            <div class="gauge-val"><span style="color:#fff;font-size:inherit;margin:0" id="gauge-value">92</span><span>%</span></div>
          </div>
          <div class="area">
            <div class="big">248<small>ha</small></div>
            <div class="meta" style="margin-top:4px">Total monitored area</div>
            <span class="delta"><svg class="i sm"><use href="#i-arrow"/></svg>Optimal vigor</span>
          </div>
        </div>
      </article>

      <article class="glass card" data-purpose="health-trend-card" aria-labelledby="trend-title">
        <div class="card-h"><h3 class="card-title" id="trend-title">Health Trend</h3>
          <label class="select-wrap"><span class="sr-only">Health trend period</span>
            <select id="trend-range"><option value="24h">24 Hours</option><option value="7d" selected>7 Days</option><option value="30d">30 Days</option></select>
            <svg class="i"><use href="#i-chev-d"/></svg></label></div>
        <div class="trend" id="trend-box">
          <div class="tip" id="trend-tip"></div>
          <svg id="trend-chart" viewBox="0 0 320 140" role="img" aria-label="Seven-day crop health trend">
            <defs>
              <linearGradient id="trendFill" x1="0" y1="0" x2="0" y2="1"><stop offset="0" stop-color="#bff24a" stop-opacity=".32"/><stop offset="1" stop-color="#bff24a" stop-opacity="0"/></linearGradient>
              <linearGradient id="colFill" x1="0" y1="0" x2="0" y2="1"><stop offset="0" stop-color="#bff24a" stop-opacity=".22"/><stop offset="1" stop-color="#bff24a" stop-opacity="0"/></linearGradient>
            </defs>
            <g id="trend-grid"></g><g id="trend-cols"></g>
            <path id="trend-target" stroke="rgba(255,255,255,.28)" stroke-dasharray="3 4" stroke-width="1" fill="none"/>
            <path id="trend-area" fill="url(#trendFill)"/>
            <path id="trend-line" fill="none" stroke="#d4fa72" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/>
            <g id="trend-marks"></g>
            <g id="trend-hover" style="display:none"><line y1="8" y2="112" stroke="rgba(255,255,255,.35)" stroke-dasharray="2 3"/><circle r="4" fill="#0b1208" stroke="#d4fa72" stroke-width="2"/></g>
            <g id="trend-xlabels"></g>
          </svg>
        </div>
      </article>

      <article class="glass card" data-purpose="stress-zones-card" aria-labelledby="stress-title">
        <div class="card-h"><div><h3 class="card-title" id="stress-title">Stress Zones</h3><div class="meta">Sensor matrix overview</div></div>
          <span class="pill ok">Good for Planting</span></div>
        <div class="matrix" id="matrix" role="img" aria-labelledby="matrix-summary"></div>
        <div class="matrix-legend" id="matrix-summary"></div>
        <div class="foot-row"><span>12% yield increase projected</span>
          <button class="ai-btn" data-dialog="insights" type="button"><svg class="i sm"><use href="#i-spark"/></svg>AI Insights</button></div>
        <div class="mini-grid">
          <div class="mini"><span class="ico"><svg class="i sm"><use href="#i-drop"/></svg></span><div><small>Avg. Humidity</small><b id="matrix-humidity">62%</b><em>Max 80% · Min 10%</em></div></div>
          <div class="mini"><span class="ico"><svg class="i sm"><use href="#i-therm"/></svg></span><div><small>Avg. Temp</small><b id="matrix-temp">28°C</b><em>Max 42° · Min 19°</em></div></div>
        </div>
      </article>
    </section>

    <!-- DOCK -->
    <section class="dock" id="operations" aria-labelledby="operations-title">
      <h2 class="sr-only" id="operations-title">Fleet and operations</h2>

      <article class="glass card ops" id="tractor" aria-labelledby="tractor-title">
        <div class="ops-head"><div><h3 id="tractor-title">Tractor T-04</h3><time data-offset-min="0">—</time></div>
          <button class="icon-btn" data-dialog="tractor" type="button" aria-label="Tractor T-04 details"><svg class="i"><use href="#i-arrow"/></svg></button></div>
        <div class="ops-mid">
          <div class="col"><span class="pill ok" data-fleet-status role="status"><span class="dot"></span><span data-status-text>Online</span></span>
            <span class="meta mono"><svg class="i sm" style="vertical-align:-2px"><use href="#i-wifi"/></svg> GPS · LTE</span></div>
          <svg class="vehicle" viewBox="0 0 96 60" aria-hidden="true"><circle cx="26" cy="42" r="14"/><circle cx="26" cy="42" r="6"/><circle cx="74" cy="46" r="10"/><circle cx="74" cy="46" r="4"/><path d="M26 28V14h14l8 12h12l6 10M40 14l-4-6h-10"/><path d="M12 34H40V28M60 26v8M48 26v10H88"/><path d="M52 14h10l4 12"/></svg>
        </div>
        <div>
          <div class="chart-box">
            <svg viewBox="0 0 200 42" preserveAspectRatio="none" aria-label="Sample tractor activity timeline, 6 AM to 11 PM" role="img">
              <g stroke="rgba(255,255,255,.07)"><path d="M0 10.5H200M0 21H200M0 31.5H200"/><path d="M40 0V42M80 0V42M120 0V42M160 0V42"/></g>
              <path d="M0 32H30V10H70V26H110V10H150V32H196" stroke="#bff24a" stroke-width="1.8" fill="none" stroke-linejoin="bevel" vector-effect="non-scaling-stroke"/>
            </svg>
            <div class="axis"><span>06 AM</span><span>11 PM</span></div>
          </div>
          <div class="track lime"><i id="tractor-fuel-bar" style="width:64%"></i></div>
        </div>
        <div class="stats"><div><small>Fuel</small><b id="tractor-fuel">64%</b></div><div><small>Area</small><b id="tractor-area">12.4 ha</b></div><div><small>Speed</small><b id="tractor-speed" style="color:var(--lime)">8 km/h</b></div></div>
      </article>

      <article class="glass card ops" id="sprayer" aria-labelledby="sprayer-title">
        <div class="ops-head"><div><h3 id="sprayer-title">Sprayer S-01</h3><time data-offset-min="2">—</time></div>
          <button class="icon-btn" data-dialog="sprayer" type="button" aria-label="Sprayer S-01 details"><svg class="i"><use href="#i-arrow"/></svg></button></div>
        <div class="ops-mid">
          <div class="col"><span class="pill warn" data-fleet-status role="status"><span class="dot"></span><span data-status-text>Working</span></span>
            <span class="meta mono"><svg class="i sm" style="vertical-align:-2px"><use href="#i-wifi"/></svg> GPS · LTE</span></div>
          <svg class="vehicle amber" viewBox="0 0 96 60" aria-hidden="true"><circle cx="28" cy="46" r="9"/><circle cx="68" cy="46" r="9"/><circle cx="28" cy="46" r="3.5"/><circle cx="68" cy="46" r="3.5"/><path d="M20 36h56V22H40l-8-10H20z"/><path d="M4 24h88M8 24v8M24 24v8M48 24v8M72 24v8M88 24v8"/><path d="M44 10h18v12"/></svg>
        </div>
        <div>
          <div class="chart-box">
            <svg viewBox="0 0 200 42" preserveAspectRatio="none" aria-label="Sample sprayer activity timeline, 7 AM to 5 PM" role="img">
              <g stroke="rgba(255,255,255,.07)"><path d="M0 10.5H200M0 21H200M0 31.5H200"/><path d="M40 0V42M80 0V42M120 0V42M160 0V42"/></g>
              <path d="M0 18H45V8H90V34H140V14H196" stroke="#f5b342" stroke-width="1.8" fill="none" stroke-linejoin="bevel" vector-effect="non-scaling-stroke"/>
            </svg>
            <div class="axis"><span>07 AM</span><span>05 PM</span></div>
          </div>
          <div class="track amber"><i id="sprayer-tank-bar" style="width:41%"></i></div>
        </div>
        <div class="stats"><div><small>Tank</small><b id="sprayer-tank" style="color:var(--amber)">41%</b></div><div><small>Area</small><b id="sprayer-area">6.8 ha</b></div><div><small>Speed</small><b id="sprayer-speed">6 km/h</b></div></div>
      </article>

      <article class="glass card ops" id="irrigation" aria-labelledby="irrigation-title">
        <div class="ops-head"><h3 id="irrigation-title">Irrigation Offset</h3>
          <button class="icon-btn" data-dialog="irrigation" type="button" aria-label="Irrigation Offset details"><svg class="i"><use href="#i-arrow"/></svg></button></div>
        <div class="irr-top"><div><div class="big" id="irrigation-global-variance">± 2.5<small>min</small></div><div class="meta">Peak zone variance</div></div></div>
        <div class="tbl-wrap">
          <table class="tbl" aria-label="Sample irrigation offsets by zone">
            <thead><tr><th scope="col" style="text-align:left;padding-left:10px">Zone</th><th scope="col">Z1</th><th scope="col">Z2</th><th scope="col">Z3</th><th scope="col">Z4</th></tr></thead>
            <tbody>
              <tr><th scope="row">Zone A</th><td id="irrig-a1">-2.0m</td><td id="irrig-a2" class="up">+1.0m</td><td id="irrig-a3" class="up">+1.5m</td><td id="irrig-a4">-1.0m</td></tr>
              <tr><th scope="row">Zone B</th><td id="irrig-b1">-1.0m</td><td id="irrig-b2">-2.0m</td><td id="irrig-b3" class="up">+2.0m</td><td id="irrig-b4" class="bad">-2.5m</td></tr>
            </tbody>
          </table>
        </div>
        <div class="irr-foot"><span>Main Pump Station 02</span><span id="pump-status" style="color:var(--emerald);font-weight:600">Calibrated</span></div>
      </article>

      <article class="glass card ops" id="yield" aria-labelledby="yield-title">
        <div class="ops-head"><h3 id="yield-title">Live Yield Volume</h3>
          <button class="icon-btn" data-dialog="yield" type="button" aria-label="Live Yield Volume details"><svg class="i"><use href="#i-arrow"/></svg></button></div>
        <div class="yield-body">
          <div class="num"><span class="big" id="yield-volume-val">142,580</span><span class="meta">kg harvested today</span></div>
          <div class="hist-wrap" id="yield-histogram-container">
            <div class="tip" id="histogram-tooltip"><span id="tooltip-text"></span></div>
            <div class="hist" id="yield-histogram" role="img" aria-label="Harvest activity histogram with interactive tooltips"></div>
          </div>
        </div>
        <div class="run"><span>Peak run rate</span><b id="yield-runrate">+18.4 tn/hr</b></div>
      </article>
    </section>
  </main>
</div>

<dialog id="detail-dialog" aria-labelledby="dialog-title">
  <h2 id="dialog-title"></h2><p id="dialog-copy"></p>
  <form method="dialog"><button class="close" autofocus>Close</button></form>
</dialog>

<script>
(() => {
  'use strict';
  const $ = (q, s = document) => s.querySelector(q);
  const $$ = (q, s = document) => [...s.querySelectorAll(q)];
  const clamp = (n, lo, hi) => Math.min(hi, Math.max(lo, n));
  const rng = seed => () => (seed = (seed * 1664525 + 1013904223) >>> 0) / 4294967296;
  const NS = 'http://www.w3.org/2000/svg';
  const el = (tag, attrs = {}, parent) => { const n = document.createElementNS(NS, tag); for (const k in attrs) n.setAttribute(k, attrs[k]); parent && parent.append(n); return n; };

  /* ================= MAP ================= */
  const map = $('#map-view'), stage = $('#map-stage'), image = $('.map-image'), vectors = $('.map-vectors');
  const trigger = $('#field-trigger'), field = $('#field-detail'), viewPanel = $('#view-panel');
  const mobile = matchMedia('(max-width: 767px)');
  const nav = $('#primary-links'), menu = $('#menu-toggle');
  const mapActions = Object.fromEntries($$('[data-map-action]').map(b => [b.dataset.mapAction, b]));
  let zoom = 1, angle = 0, panX = 0, panY = 0, drag = null;

  const parcel = $('#parcel').getAttribute('points').trim().split(/\s+/).map(p => p.split(',').map(Number));
  const centroid = (() => {
    let sum = 0, x = 0, y = 0;
    parcel.forEach(([a, b], i) => { const [c, d] = parcel[(i + 1) % parcel.length], cr = a * d - c * b; sum += cr; x += (a + c) * cr; y += (b + d) * cr; });
    return [x / (3 * sum), y / (3 * sum)];
  })();

  function renderMap() {
    const w = map.clientWidth, h = map.clientHeight;
    if (!w || !h) return;
    const iw = image.naturalWidth || 1920, ih = image.naturalHeight || 1080;
    const oc = Math.max(1920 / iw, 1080 / ih) * 1.02;
    const rw = iw * oc, rh = ih * oc, rx = (1920 - rw) / 2, ry = (1080 - rh) / 2;
    vectors.setAttribute('viewBox', `${rx} ${ry} ${rw} ${rh}`);
    const ax = (centroid[0] - rx) / rw, ay = (centroid[1] - ry) / rh;
    const rad = angle * Math.PI / 180, cos = Math.cos(rad), sin = Math.sin(rad);
    const cover = Math.max((w * Math.abs(cos) + h * Math.abs(sin)) / iw, (w * Math.abs(sin) + h * Math.abs(cos)) / ih);
    const bw = cover * iw, bh = cover * ih, zw = bw * zoom, zh = bh * zoom;
    const limX = (zw - w * Math.abs(cos) - h * Math.abs(sin)) / 2;
    const limY = (zh - w * Math.abs(sin) - h * Math.abs(cos)) / 2;
    const fx = mobile.matches ? (.5 - ax) * zw : 0, fy = mobile.matches ? (.5 - ay) * zh : 0;
    const px = clamp(fx + panX, -Math.max(0, limX), Math.max(0, limX));
    const py = clamp(fy + panY, -Math.max(0, limY), Math.max(0, limY));
    const x = px * cos - py * sin, y = px * sin + py * cos;
    stage.style.width = bw + 'px'; stage.style.height = bh + 'px';
    stage.style.left = (w - bw) / 2 + 'px'; stage.style.top = (h - bh) / 2 + 'px';
    stage.style.transform = `translate(${x}px, ${y}px) rotate(${angle}deg) scale(${zoom})`;
    stage.style.setProperty('--counter-angle', -angle + 'deg');
    stage.style.setProperty('--counter-scale', 1 / zoom);
    trigger.style.left = ax * 100 + '%'; trigger.style.top = ay * 100 + '%';
    mapActions.in.setAttribute('aria-disabled', String(zoom >= 3));
    mapActions.out.setAttribute('aria-disabled', String(zoom <= 1));
  }
  new ResizeObserver(renderMap).observe(map);
  image.addEventListener('load', renderMap);
  image.addEventListener('error', () => { image.hidden = true; $('#map-caption').textContent = 'Image unavailable · Demo field outline'; });
  if (image.complete && !image.naturalWidth) image.hidden = true;
  const announce = m => { $('#map-status').textContent = m; };
  function moveMap(a) {
    if (a === 'in' || a === 'out') zoom = clamp(zoom + (a === 'in' ? .25 : -.25), 1, 3);
    if (a === 'out' && zoom === 1) panX = panY = 0;
    if (a === 'rotate') angle = (angle + 15) % 360;
    if (a === 'compass') angle = 0;
    if (a === 'fit') { zoom = 1; panX = panY = 0; angle = 0; }
    renderMap();
    announce(a === 'fit' ? 'Map reset to fit bounds.' : a === 'compass' ? 'Map oriented north.' : `Map zoom ${zoom * 100} percent, rotation ${angle} degrees.`);
  }
  for (const [a, b] of Object.entries(mapActions)) b.addEventListener('click', () => { if (b.getAttribute('aria-disabled') !== 'true') moveMap(a); });
  map.addEventListener('pointerdown', e => {
    if (zoom === 1 || e.button !== 0 || e.pointerType === 'touch' || e.target.closest('button')) return;
    drag = { id: e.pointerId, x: e.clientX, y: e.clientY };
    stage.classList.add('dragging'); map.setPointerCapture(e.pointerId);
  });
  map.addEventListener('pointermove', e => {
    if (!drag || drag.id !== e.pointerId) return;
    const dx = e.clientX - drag.x, dy = e.clientY - drag.y, a = angle * Math.PI / 180;
    panX = clamp(panX + dx * Math.cos(a) + dy * Math.sin(a), -stage.clientWidth, stage.clientWidth);
    panY = clamp(panY - dx * Math.sin(a) + dy * Math.cos(a), -stage.clientHeight, stage.clientHeight);
    drag.x = e.clientX; drag.y = e.clientY; renderMap();
  });
  map.addEventListener('lostpointercapture', () => { drag = null; stage.classList.remove('dragging'); });

  const layers = { satellite: ['RGB High-Res', 'Satellite imagery · Demo data'], ndvi: ['Biomass preview', 'NDVI · Simulated color preview'], soil: ['Moisture preview', 'Soil · Simulated color preview'] };
  const layerIdle = { satellite: 'RGB High-Res', ndvi: 'Biomass Index', soil: 'Moisture Profile' };
  $$('[data-layer-choice]').forEach(b => b.addEventListener('click', () => {
    const key = b.dataset.layerChoice; map.dataset.layer = key;
    $$('[data-layer-choice]').forEach(item => {
      const on = item === b; item.setAttribute('aria-pressed', String(on));
      $('.layer-description', item).textContent = on ? layers[key][0] : layerIdle[item.dataset.layerChoice];
    });
    $('#map-caption').textContent = layers[key][1] + (image.hidden ? ' · Image unavailable' : '');
    announce($('#map-caption').textContent);
  }));

  const droneBtn = $('#drone-layer-toggle'), droneGroup = $('#drone-path-group');
  droneBtn.addEventListener('click', () => {
    const vis = droneGroup.style.display !== 'none';
    droneGroup.style.display = vis ? 'none' : '';
    droneBtn.setAttribute('aria-pressed', String(!vis));
    $('.layer-description', droneBtn).textContent = vis ? 'Hidden' : 'Flight Path';
    announce(vis ? 'Drone layer hidden' : 'Drone flight simulation visible');
  });

  function fieldOpen(open, focus = false) {
    field.hidden = !open; trigger.setAttribute('aria-expanded', String(open));
    if (focus) (open ? $('#field-close') : trigger).focus();
  }
  trigger.addEventListener('click', () => fieldOpen(field.hidden, true));
  $('#field-close').addEventListener('click', () => fieldOpen(false, true));
  function menuOpen(o) { nav.classList.toggle('is-open', o); menu.setAttribute('aria-expanded', String(o)); }
  menu.addEventListener('click', () => menuOpen(!nav.classList.contains('is-open')));
  mobile.addEventListener('change', () => { menuOpen(false); renderMap(); });

  const views = {
    map: ['Field Management', 'Field health, fleet telemetry and operations · Live simulation active', ''],
    fields: ['Fields', 'Parcel monitoring · Demo', 'North Field: 92% crop health. Use the highlighted map marker to open field details.'],
    analytics: ['Analytics', 'Crop health trends and stress zones · Demo', 'Use the Health Trend period selector to compare 24-hour, 7-day and 30-day sample readings.'],
    reports: ['Reports', 'Irrigation and harvest summaries · Demo', 'The operations cards below show irrigation offsets and sample harvest volume.'],
    farmers: ['Farmers', 'Farm team overview · Demo', 'This prototype has no connected team directory.']
  };
  $$('[data-view]').forEach(b => b.addEventListener('click', () => {
    const wasMenu = mobile.matches && nav.classList.contains('is-open');
    $$('[data-view]').forEach(i => i === b ? i.setAttribute('aria-current', 'page') : i.removeAttribute('aria-current'));
    const key = b.dataset.view, [t, s, c] = views[key];
    $('#page-title').textContent = t; $('#page-subtitle').textContent = s;
    $('#view-title').textContent = t + ' overview'; $('#view-copy').textContent = c; viewPanel.hidden = key === 'map';
    fieldOpen(false); menuOpen(false);
    if (wasMenu) menu.focus();
  }));

  /* ================= GAUGE ================= */
  const health = $('[data-purpose=crop-health-card]');
  const gaugeTicks = $('#gauge-ticks'), TICKS = 46;
  for (let i = 0; i < TICKS; i++) {
    const a = Math.PI + i / (TICKS - 1) * Math.PI, c = Math.cos(a), s = Math.sin(a);
    el('line', { class: 'tick', x1: 100 + 64 * c, y1: 100 + 64 * s, x2: 100 + 84 * c, y2: 100 + 84 * s }, gaugeTicks);
  }
  function renderGauge() {
    const p = clamp(Number(health.dataset.value) || 0, 0, 100);
    [...gaugeTicks.children].forEach((t, i) => {
      const f = i / (TICKS - 1), on = f * 100 <= p;
      t.classList.toggle('on', on);
      t.style.stroke = on ? `hsl(${74 + f * 16} 85% ${44 + f * 24}%)` : '';
    });
    $('#gauge-value').textContent = p; $('#crop-gauge').setAttribute('aria-label', `Crop health: ${p} percent`);
  }
  new MutationObserver(renderGauge).observe(health, { attributes: true, attributeFilter: ['data-value'] }); renderGauge();

  /* ================= TREND ================= */
  const ranges = {
    '24h': { name: '24-hour', n: 48, key: [90, 89, 88, 85, 83, 87, 91, 93, 92, 90], labels: ['00:00', '04:00', '08:00', '12:00', '16:00', '20:00', '24:00'], seed: 11, noise: 2.2 },
    '7d':  { name: 'seven-day', n: 84, key: [88, 90, 95, 90, 85, 91, 92], labels: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun'], seed: 7, noise: 2.6 },
    '30d': { name: '30-day', n: 90, key: [84, 87, 90, 86, 91, 94, 92], labels: ['Day 1', '5', '10', '15', '20', '25', '30'], seed: 3, noise: 2.4 }
  };
  const G = { W: 320, L: 26, R: 316, T: 10, B: 112, MIN: 70 };
  let tSeries = [], tCfg = ranges['7d'], tPeak = 0;
  const tx = i => G.L + i * (G.R - G.L) / (tSeries.length - 1);
  const ty = v => G.T + (100 - v) / (100 - G.MIN) * (G.B - G.T);
  function buildSeries(d) {
    const r = rng(d.seed), out = [];
    for (let i = 0; i < d.n; i++) {
      const t = i / (d.n - 1) * (d.key.length - 1), a = Math.min(Math.floor(t), d.key.length - 2);
      let f = t - a; f = f * f * (3 - 2 * f);
      out.push(clamp(d.key[a] * (1 - f) + d.key[a + 1] * f + (r() - .5) * d.noise, G.MIN + 2, 99.5));
    }
    return out;
  }
  const smooth = pts => {
    let d = `M${pts[0][0]},${pts[0][1]}`;
    for (let i = 1; i < pts.length; i++) { const [x0, y0] = pts[i - 1], [x1, y1] = pts[i]; d += ` Q${x0},${y0} ${(x0 + x1) / 2},${(y0 + y1) / 2}`; }
    return d + ` L${pts[pts.length - 1][0]},${pts[pts.length - 1][1]}`;
  };
  function labelAt(i) {
    const f = i / (tSeries.length - 1);
    if (tCfg === ranges['24h']) { const m = Math.round(f * 24 * 60); return `${String(Math.floor(m / 60) % 24).padStart(2, '0')}:${String(m % 60).padStart(2, '0')}`; }
    if (tCfg === ranges['7d']) return tCfg.labels[Math.min(6, Math.round(f * 6))];
    return `Day ${Math.round(1 + f * 29)}`;
  }
  function renderTrend() {
    tCfg = ranges[$('#trend-range').value]; tSeries = buildSeries(tCfg);
    const pts = tSeries.map((v, i) => [tx(i), ty(v)]), line = smooth(pts);
    $('#trend-line').setAttribute('d', line);
    $('#trend-area').setAttribute('d', `${line} L${G.R},${G.B} L${G.L},${G.B} Z`);
    $('#trend-target').setAttribute('d', `M${G.L},${ty(90)} L${G.R},${ty(90)}`);
    const grid = $('#trend-grid'); grid.replaceChildren();
    [100, 90, 80, 70].forEach(v => {
      el('line', { x1: G.L, x2: G.R, y1: ty(v), y2: ty(v), stroke: 'rgba(255,255,255,.07)', 'stroke-dasharray': v === 100 || v === 70 ? '' : '2 4' }, grid);
      const t = el('text', { x: 0, y: ty(v) + 3 }, grid); t.textContent = v;
    });
    tPeak = tSeries.indexOf(Math.max(...tSeries));
    let low = tPeak; for (let i = tPeak + 1; i < tSeries.length; i++) if (tSeries[i] < tSeries[low] || low === tPeak) low = i;
    const cols = $('#trend-cols'); cols.replaceChildren();
    [tPeak, low].forEach(i => el('rect', { x: tx(i) - 8, y: ty(tSeries[i]), width: 16, height: G.B - ty(tSeries[i]), rx: 4, fill: 'url(#colFill)' }, cols));
    const marks = $('#trend-marks'); marks.replaceChildren();
    el('circle', { cx: tx(tPeak), cy: ty(tSeries[tPeak]), r: 4.5, fill: '#facc15', stroke: '#1c1917', 'stroke-width': 2 }, marks);
    el('circle', { cx: tx(low), cy: ty(tSeries[low]), r: 3.5, fill: '#fff', stroke: '#1c1917', 'stroke-width': 1.5 }, marks);
    const xl = $('#trend-xlabels'); xl.replaceChildren();
    tCfg.labels.forEach((l, i) => {
      const x = G.L + i * (G.R - G.L) / (tCfg.labels.length - 1);
      const t = el('text', { x, y: 130, 'text-anchor': i === 0 ? 'start' : i === tCfg.labels.length - 1 ? 'end' : 'middle' }, xl);
      t.textContent = l;
      if (Math.abs(x - tx(tPeak)) < 24) t.setAttribute('class', 'hl');
    });
    $('#trend-chart').setAttribute('aria-label', `Sample ${tCfg.name} crop health trend. Highest point: ${labelAt(tPeak)}, ${tSeries[tPeak].toFixed(0)} percent.`);
  }
  $('#trend-range').addEventListener('change', renderTrend); renderTrend();
  (() => {
    const svg = $('#trend-chart'), hov = $('#trend-hover'), tip = $('#trend-tip'), box = $('#trend-box');
    svg.addEventListener('pointermove', e => {
      const r = svg.getBoundingClientRect(), x = (e.clientX - r.left) / r.width * G.W;
      const i = clamp(Math.round((x - G.L) / (G.R - G.L) * (tSeries.length - 1)), 0, tSeries.length - 1);
      hov.style.display = ''; $('line', hov).setAttribute('x1', tx(i)); $('line', hov).setAttribute('x2', tx(i));
      $('circle', hov).setAttribute('cx', tx(i)); $('circle', hov).setAttribute('cy', ty(tSeries[i]));
      tip.textContent = `${labelAt(i)} · ${tSeries[i].toFixed(1)}%`;
      tip.style.left = clamp(tx(i) / G.W * box.clientWidth, 50, box.clientWidth - 50) + 'px'; tip.style.opacity = 1;
    });
    svg.addEventListener('pointerleave', () => { hov.style.display = 'none'; tip.style.opacity = 0; });
  })();

  /* ================= STRESS MATRIX ================= */
  (() => {
    const layout = ['HHHHHCCHHHHHHHHH', 'HHHHCCCCHHHHHHHH', 'HHHHHCCSSCCHHHHH', 'HHCCCCCHHHHHHHHH'];
    const m = $('#matrix'), count = { H: 0, C: 0, S: 0 };
    layout.forEach((row, r) => [...row].forEach((k, c) => {
      count[k]++;
      const i = document.createElement('i');
      const col = k === 'H' ? `hsl(${84 - c * .7} 78% ${58 + ((r + c) % 3) * 3}%)` : k === 'C' ? `hsl(${42 - c * .4} 92% 58%)` : 'hsl(4 80% 58%)';
      i.style.background = col; i.style.setProperty('--c', col);
      i.className = k.toLowerCase(); i.title = `Sensor R${r + 1}·C${c + 1} — ${{ H: 'Healthy', C: 'Caution', S: 'Stress' }[k]}`;
      m.append(i);
    }));
    $('#matrix-summary').innerHTML = `<span><i style="background:hsl(80 78% 60%)"></i>${count.H} Healthy</span><span><i style="background:hsl(40 92% 58%)"></i>${count.C} Caution</span><span><i style="background:hsl(4 80% 58%)"></i>${count.S} Stress</span>`;
  })();

  /* ================= YIELD HISTOGRAM ================= */
  (() => {
    const hourly = [5.2, 7.8, 6.5, 10.1, 4.6, 11.8, 7.5, 9.0, 10.9, 7.0, 18.4, 17.1, 8.6, 9.7, 5.9, 6.9];
    const r = rng(21), box = $('#yield-histogram'), tip = $('#histogram-tooltip'), wrap = $('#yield-histogram-container');
    hourly.forEach((v, h) => [0, 1].forEach(half => {
      const val = v * (.9 + r() * .2), b = document.createElement('b');
      b.dataset.val = val.toFixed(1); b.dataset.time = `${String(6 + h).padStart(2, '0')}:${half ? '30' : '00'}`;
      b.style.height = clamp(val / 19 * 100, 12, 100) + '%';
      if (v > 16) b.classList.add('peak');
      box.append(b);
    }));
    box.addEventListener('pointerover', e => {
      const b = e.target.closest('b'); if (!b) return;
      $('#tooltip-text').textContent = `${b.dataset.time} · ${b.dataset.val} tn/hr`;
      const br = b.getBoundingClientRect(), wr = wrap.getBoundingClientRect();
      tip.style.left = clamp(br.left - wr.left + br.width / 2, 55, wr.width - 55) + 'px'; tip.style.opacity = 1;
    });
    box.addEventListener('pointerleave', () => { tip.style.opacity = 0; });
    box.addEventListener('click', e => { const b = e.target.closest('b'); if (b) $('#yield-runrate').textContent = `+${b.dataset.val} tn/hr`; });
  })();

  /* ================= DIALOGS & SEARCH ================= */
  const dialog = $('#detail-dialog');
  const detailCopy = {
    notifications: ['Notifications', 'Alert history: Zone B irrigation variance exceeded threshold at 09:41.'],
    health: ['Crop health', () => `The dashboard shows ${$('#gauge-value').textContent}% crop health over a monitored farm area of 248 ha.`],
    insights: ['AI Insights', 'Soil moisture optimal across Zone A; Zone B requires schedule compensation to prevent root stress.'],
    tractor: ['Tractor T-04 Telemetry', () => `Current telemetry: speed ${$('#tractor-speed').textContent}, fuel ${$('#tractor-fuel').textContent}, area ${$('#tractor-area').textContent}. Autonomous GPS path tracking active.`],
    sprayer: ['Sprayer S-01 Telemetry', () => `Current telemetry: speed ${$('#sprayer-speed').textContent}, tank ${$('#sprayer-tank').textContent}, area ${$('#sprayer-area').textContent}. Variable-rate spraying active.`],
    irrigation: ['Irrigation Offset Alert System', 'Real-time flow sensors evaluate deviation across all zones. If the offset exceeds ±3.0 minutes, a high-priority alert banner is triggered.'],
    yield: ['Live Yield Volume Telemetry', () => `Total harvested today: ${$('#yield-volume-val').textContent} kg. Current run rate: ${$('#yield-runrate').textContent}.`],
    drone: ['Drone Scan-03 Flight Status', 'Autonomous multi-spectral crop scan at 65 m altitude. Battery: 78%. Coverage: 18.5 ha completed.']
  };
  function showDetails(key) {
    const item = detailCopy[key]; if (!item) return;
    $('#dialog-title').textContent = item[0];
    $('#dialog-copy').textContent = typeof item[1] === 'function' ? item[1]() : item[1];
    dialog.showModal();
  }
  $$('[data-dialog]').forEach(b => b.addEventListener('click', () => showDetails(b.dataset.dialog)));

  const search = $('#dashboard-search'), results = $('#search-results');
  const searchable = [['North Field', 'field'], ['Tractor T-04', 'tractor'], ['Sprayer S-01', 'sprayer'], ['Drone Scan-03', 'drone'], ['Irrigation Station', 'irrigation'], ['Yield Analysis', 'yield']];
  search.addEventListener('input', () => {
    const term = search.value.trim().toLowerCase(); results.replaceChildren(); results.hidden = !term;
    if (!term) return;
    for (const [name, key] of searchable.filter(([n]) => n.toLowerCase().includes(term))) {
      const b = document.createElement('button'); b.type = 'button'; b.textContent = name;
      b.addEventListener('click', () => { results.hidden = true; search.focus(); key === 'field' ? fieldOpen(true, true) : showDetails(key); });
      results.append(b);
    }
    if (!results.childElementCount) results.textContent = 'No matching parcels or equipment.';
  });
  search.addEventListener('focus', () => { if (search.value.trim() && results.textContent.trim()) results.hidden = false; });
  search.parentElement.addEventListener('focusout', e => { if (!search.parentElement.contains(e.relatedTarget)) results.hidden = true; });

  /* ================= LIVE SIMULATION ================= */
  let sim = true;
  const toggle = $('#telemetry-toggle-btn');
  toggle.addEventListener('click', () => {
    sim = !sim; lastTick = performance.now();
    toggle.classList.toggle('paused', !sim); toggle.setAttribute('aria-pressed', String(sim));
    $('#telemetry-btn-text').textContent = sim ? 'Simulation: Live' : 'Simulation: Paused';
    announce(sim ? 'Live telemetry simulation resumed' : 'Live telemetry simulation paused');
  });

  const droneWp = [[980, 370], [1490, 375], [1490, 440], [970, 440], [970, 510], [1480, 510], [1480, 580], [1020, 580], [1020, 650], [1450, 650]];
  const tractorWp = [[960, 410], [1080, 410], [1080, 620], [1150, 620], [1150, 430], [1220, 430], [1220, 620]];
  const sprayerWp = [[1320, 370], [1320, 680], [1400, 680], [1400, 370], [1470, 370], [1470, 660]];
  const agents = [
    { wp: droneWp, el: $('#drone-marker'), leg: 0, t: 0, speed: .35 },
    { wp: tractorWp, el: $('#tractor-marker'), leg: 0, t: 0, speed: .12 },
    { wp: sprayerWp, el: $('#sprayer-marker'), leg: 0, t: 0, speed: .14 }
  ];
  agents[1].el.addEventListener('click', () => showDetails('tractor'));
  agents[2].el.addEventListener('click', () => showDetails('sprayer'));
  agents[0].el.addEventListener('click', () => showDetails('drone'));

  const banner = $('#irrigation-alert-banner'), bannerText = $('#alert-banner-text');
  let dismissed = false;
  $('#alert-dismiss-btn').addEventListener('click', () => { banner.classList.add('hidden'); dismissed = true; });

  let lastTick = performance.now(), acc = 0, clock = 0, harvest = 142580, tSpeed = 8, sSpeed = 6, fuel = 64, tank = 41, tArea = 12.4, sArea = 6.8;
  const lerp = (a, b, t) => [a[0] + (b[0] - a[0]) * t, a[1] + (b[1] - a[1]) * t];

  function tick(now) {
    requestAnimationFrame(tick);
    if (!sim) return;
    const dt = Math.min((now - lastTick) / 1000, .25); lastTick = now;
    for (const a of agents) {
      a.t += dt * a.speed;
      if (a.t >= 1) { a.t = 0; a.leg = (a.leg + 1) % (a.wp.length - 1); }
      const p = lerp(a.wp[a.leg], a.wp[a.leg + 1], a.t);
      a.el.setAttribute('transform', `translate(${p[0]}, ${p[1]})`);
    }
    acc += dt; clock += dt;
    if (acc < 1.6) return;
    acc = 0;

    tSpeed = clamp(tSpeed + Math.random() * .8 - .4, 6.5, 9.5); tArea += .02; fuel = Math.max(10, fuel - .03);
    $('#tractor-speed').textContent = `${tSpeed.toFixed(1)} km/h`; $('#tractor-area').textContent = `${tArea.toFixed(1)} ha`;
    $('#tractor-fuel').textContent = `${Math.round(fuel)}%`; $('#tractor-fuel-bar').style.width = fuel + '%';

    sSpeed = clamp(sSpeed + Math.random() * .6 - .3, 5, 7.5); sArea += .015; tank = Math.max(5, tank - .05);
    $('#sprayer-speed').textContent = `${sSpeed.toFixed(1)} km/h`; $('#sprayer-area').textContent = `${sArea.toFixed(1)} ha`;
    $('#sprayer-tank').textContent = `${Math.round(tank)}%`; $('#sprayer-tank-bar').style.width = tank + '%';

    harvest += Math.floor(Math.random() * 12 + 6); $('#yield-volume-val').textContent = harvest.toLocaleString('en-US');

    const b4 = -2.5 - .85 * Math.sin(clock / 9) + (Math.random() * .4 - .2), v = Math.abs(b4), cell = $('#irrig-b4');
    cell.textContent = `${b4 >= 0 ? '+' : ''}${b4.toFixed(1)}m`;
    $('#irrigation-global-variance').innerHTML = `± ${v.toFixed(1)}<small>min</small>`;
    if (v > 3) {
      cell.classList.add('pulse');
      $('#pump-status').textContent = 'Variance Alert'; $('#pump-status').style.color = 'var(--rose)';
      if (!dismissed) { bannerText.textContent = `Variance exceeded ±3.0 min threshold in Zone B (current: ${b4.toFixed(1)} min). Flow readjustment suggested.`; banner.classList.remove('hidden'); }
    } else {
      cell.classList.remove('pulse');
      $('#pump-status').textContent = 'Calibrated'; $('#pump-status').style.color = 'var(--emerald)';
      if (v <= 2.8) { banner.classList.add('hidden'); dismissed = false; }
    }
  }
  requestAnimationFrame(tick);

  /* ================= TIMESTAMPS ================= */
  const start = Date.now(), staleAfter = 15 * 60000;
  const times = $$('time[data-offset-min]').map(t => ({ node: t, reading: start - Number(t.dataset.offsetMin) * 60000 }));
  const fmt = new Intl.DateTimeFormat('hu-HU', { day: '2-digit', month: '2-digit', year: 'numeric', hour: '2-digit', minute: '2-digit', hour12: false });
  function renderTimes() {
    const now = Date.now();
    for (const { node, reading } of times) {
      const d = new Date(reading), p = Object.fromEntries(fmt.formatToParts(d).map(x => [x.type, x.value]));
      const label = `${p.day}.${p.month}.${p.year}, ${p.hour}:${p.minute}`;
      node.dateTime = d.toISOString(); if (node.textContent !== label) node.textContent = label;
      const status = $('[data-fleet-status]', node.closest('article')), text = $('[data-status-text]', status);
      const stale = now - reading > staleAfter; status.classList.toggle('is-stale', stale);
      if (stale && text.textContent !== 'Stale') text.textContent = 'Stale';
    }
  }
  renderTimes(); setInterval(renderTimes, 30000);

  document.addEventListener('keydown', e => {
    if (e.key !== 'Escape' || dialog.open) return;
    if (!results.hidden) { results.hidden = true; search.focus(); }
    else if (nav.classList.contains('is-open')) { menuOpen(false); menu.focus(); }
    else if (!field.hidden) fieldOpen(false, true);
  });
  renderMap();
})();
</script>
</body>
</html>
