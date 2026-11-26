A csatolt kep referencia

El tudnad kesziteni profibb premium webdesignnal az alabbi html weboldalt?

<!DOCTYPE html>
<html lang="en"><head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0, viewport-fit=cover" name="viewport"/>
<title>Furrow — Precision Agriculture Command Center</title>
<script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
<link href="https://fonts.googleapis.com" rel="preconnect"/>
<link crossorigin="" href="https://fonts.gstatic.com" rel="preconnect"/>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet"/>
<script data-purpose="tailwind-config">
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            sans: ['Inter', 'sans-serif'],
          },
          colors: {
            furrow: {
              lime: '#84cc16',
              limeGlow: '#a3e635',
              darkBg: '#090d0b',
              panel: 'rgba(16, 24, 20, 0.78)',
              panelBorder: 'rgba(255, 255, 255, 0.08)',
              hoverBorder: 'rgba(163, 230, 53, 0.35)',
            }
          }
        }
      }
    }
  </script>
<style>
:root{color-scheme:dark;--edge:clamp(12px,1.45vw,24px);--muted:#b4c1b8;--lime:#a3e635;--line:rgba(255,255,255,.12)}
body{margin:0;background:#080d0a;-webkit-font-smoothing:antialiased}
[hidden]{display:none!important}
::-webkit-scrollbar{width:6px;height:6px}::-webkit-scrollbar-thumb{background:#526358;border-radius:6px}
button,select{cursor:pointer}button:disabled{cursor:default;opacity:.5}
:where(button,a,input,select,[tabindex]):focus-visible{outline:2px solid #bef264!important;outline-offset:3px}
.glass-hud{background:rgba(13,20,16,.93);backdrop-filter:blur(20px);border:1px solid var(--line);box-shadow:0 16px 36px -8px #000a,0 0 1px 1px #ffffff0d inset}
.glass-pill{background:rgba(22,33,27,.92);backdrop-filter:blur(12px);border:1px solid var(--line)}
#app .text-slate-400{color:var(--muted)}
.skip-link{position:fixed;top:8px;left:8px;z-index:90;transform:translateY(-160%);background:#bef264;color:#101710;padding:10px 16px;border-radius:10px}.skip-link:focus{transform:none}
#app{min-height:100vh;min-height:100dvh;display:flex;flex-direction:column;isolation:isolate;gap:12px;padding:calc(var(--edge) + env(safe-area-inset-top,0px)) calc(var(--edge) + env(safe-area-inset-right,0px)) calc(var(--edge) + env(safe-area-inset-bottom,0px)) calc(var(--edge) + env(safe-area-inset-left,0px))}
.top-header{position:relative;z-index:8;display:grid;gap:10px;flex:none}.topbar,.nav-left,.nav-right,.subheader{display:flex;align-items:center}.topbar{position:relative;justify-content:space-between;gap:10px;padding:8px 12px}.nav-left,.nav-right{gap:clamp(8px,1vw,18px)}.nav-links{display:flex;gap:2px;padding:4px}.nav-item{padding:7px clamp(8px,1vw,14px);border:1px solid transparent;white-space:nowrap;color:#cbd5e1}.nav-item:hover,[data-dialog]:hover{color:#fff}.nav-item[aria-current]{border-color:var(--line);background:#ffffff26;color:#fff}
.inventory,.nav-search{display:none}.connection,.avatar{flex:none}.menu-toggle{display:none}.subheader{gap:12px;justify-content:space-between;padding-inline:4px}.page-title{font-size:clamp(1.25rem,2.3vw,2rem);line-height:1.15}.weather{flex:none}.search-icon{position:absolute;right:9px;top:50%;translate:0 -50%;pointer-events:none}.nav-search input{padding-right:28px}.search-results{position:absolute;top:calc(100% + 8px);inset-inline:0;z-index:15;min-width:160px}.search-results button{width:100%;text-align:left;padding:7px;border-radius:6px}.search-results button:hover{background:#ffffff14}
#content{position:relative;display:grid;grid-template-columns:minmax(0,1fr) auto;grid-template-rows:auto auto auto auto;gap:12px;min-width:0;min-height:0;isolation:isolate}
#map-view{position:relative;grid-area:1 / 1 / 2 / 3;overflow:hidden;border-radius:20px;background:radial-gradient(ellipse at 60% 45%,#263c25,#121d16 66%,#080d0a);min-height:clamp(370px,54dvh,550px);border:1px solid var(--line);touch-action:pan-y;user-select:none}
#map-stage{position:absolute;top:0;left:0;width:100%;height:100%;transform-origin:center;transition:transform .22s ease-out;--counter-angle:0deg;--counter-scale:1}#map-stage.dragging{transition:none}
.map-image,.map-vectors,.vignette{position:absolute;inset:0;width:100%;height:100%;pointer-events:none}.map-image{object-fit:cover;transition:filter .22s ease}.map-vectors{overflow:hidden}.vignette{z-index:1}.vignette-0{opacity:.68}.vignette-1,.vignette-2{opacity:.56}
#map-view[data-layer=ndvi] .map-image{filter:hue-rotate(32deg) saturate(1.9) contrast(1.18)}#map-view[data-layer=ndvi]{background-color:#304521}
#map-view[data-layer=soil] .map-image{filter:sepia(.8) saturate(1.45) contrast(1.1)}
#map-view[data-layer=ndvi]::after,#map-view[data-layer=soil]::after{content:"";position:absolute;inset:0;pointer-events:none;mix-blend-mode:soft-light;background:linear-gradient(144deg,#b13527,#e7b43a 44%,#63bc39 72%);opacity:.37}
#map-view[data-layer=soil]::after{background:linear-gradient(135deg,#7d4121,#eab260 64%,#6b4428);opacity:.42}
#map-view[data-layer=ndvi]::after,#map-view[data-layer=soil]::after{z-index:1}
.field-trigger{position:absolute;left:63%;top:48%;min-width:44px;min-height:44px;z-index:3;text-align:left;transform-origin:24px 50%;transform:translate(-24px,-50%) rotate(var(--counter-angle)) scale(var(--counter-scale));}
.radar-pin{width:48px;height:48px}.field-label{display:flex;white-space:nowrap}.field-label>span:first-child{display:grid;place-items:center}.field-label:hover,.field-trigger[aria-expanded=true] .field-label{border-color:var(--lime)}
.map-tools{grid-area:1 / 2 / 2 / 3;align-self:start;justify-self:end;z-index:4;display:grid;gap:8px;justify-items:end;margin:10px}.layer-choice{width:100%;border:1px solid transparent;color:#e2e8f0}.layer-choice:hover{background:#ffffff12}.layer-choice[aria-pressed=true]{border-color:#a3e635aa;background:#ffffff1a}.layer-caption{min-width:0}.layer-caption span{display:block;font-size:12px}.layer-description{color:var(--muted);font:11px ui-monospace,monospace}.layer-choice[aria-pressed=true] .layer-description{color:#bef264}
.map-caption{grid-area:1 / 1 / 2 / 3;align-self:end;justify-self:start;margin:10px;z-index:3;font-size:11px;color:#e2e8f0;pointer-events:none}
.map-detail,.view-panel{grid-area:1 / 1 / 2 / 3;align-self:end;justify-self:start;z-index:5;margin:0 12px 45px;width:min(300px,calc(100% - 24px))}.map-detail{z-index:6}
.analytics{grid-column:1/-1;grid-row:3;display:grid;gap:10px;min-width:0;align-content:start}.analytics article,.ops-card{min-width:0}.drawer-toggle{display:none}.operations{grid-column:1/-1;grid-row:4;display:grid;gap:10px;grid-template-columns:minmax(0,1fr)}
.period-select{font-size:12px;background:#17261c;color:#f1f5f9;border:1px solid #ffffff26;padding:5px 28px 5px 9px}.fleet-heading{display:flex;flex-wrap:wrap;align-items:center;column-gap:8px;row-gap:2px;min-width:0}.fleet-time,.matrix-legend{font-size:11px}.fleet-time{white-space:nowrap}.matrix-legend{margin:-3px 0 7px}
.cell-caution{background-image:repeating-linear-gradient(135deg,transparent 0 2px,#14141490 2px 3px)}.cell-stress{background-image:radial-gradient(circle,#171717 1px,transparent 1.4px);background-size:4px 4px}.polygon-glow{filter:drop-shadow(0 0 8px #84cc1690) drop-shadow(0 0 20px #84cc1640)}
[data-fleet-status].is-stale{color:#fda4af;border-color:#fb718580;background:#f43f5e22}[data-fleet-status].is-stale>span:first-child{background:#fb7185;animation:none}
#detail-dialog{margin:auto;width:min(440px,calc(100% - 32px))}#detail-dialog::backdrop{background:#030604bb}#detail-dialog button{min-height:44px}
@keyframes radarPulse{0%{transform:scale(.65);opacity:.9}50%{transform:scale(1.6);opacity:.25}100%{transform:scale(2.4);opacity:0}}.radar-ring-1,.radar-ring-2{animation:radarPulse 2.8s cubic-bezier(.215,.61,.355,1) infinite}.radar-ring-2{animation-delay:.9s}
@keyframes dronePulse{0%,100%{transform:scale(1);opacity:0.9}50%{transform:scale(1.25);opacity:1}}
.drone-anim{animation:dronePulse 1.8s ease-in-out infinite}
@media(max-width:767px){
 .brand{flex:none}.connection,.avatar,.weather{display:none!important}.menu-toggle{display:block}.nav-right{margin-left:auto}.nav-links{display:none;position:absolute;inset-inline:0;top:calc(100% + 6px);z-index:12;background:#111d16;padding:7px}.nav-links.is-open{display:grid}.nav-item{text-align:left}.map-tools{gap:5px;margin:7px}.map-tools>div{padding:3px;gap:0}.map-tools>div>*+*{margin-top:0!important}.layer-choice{padding:2px 6px}.layer-choice>div:first-child,.layer-description{display:none}.layer-choice{justify-content:center}.layer-caption span{font-size:11px}.map-tools>div:nth-child(2)>div{margin-block:2px!important}.field-label{padding:7px 9px}.field-label>span:first-child{display:none}.map-caption{max-width:92%}
 button:not(.skip-link),select{min-height:44px;min-width:44px}.analytics button svg,.operations button svg{margin-inline:auto}
}
@media(min-width:768px) and (max-width:1279px){
 .operations{grid-template-columns:repeat(2,minmax(0,1fr))}.drawer-toggle{display:block;grid-area:1 / 1 / 2 / 3;align-self:start;justify-self:start;margin:12px;z-index:7;min-height:44px}.analytics{display:none;grid-area:1 / 1 / 2 / 3;align-self:start;justify-self:start;margin:64px 12px 44px;width:min(325px,calc(100% - 175px));max-height:calc(clamp(370px,54dvh,550px) - 108px);overflow:auto;z-index:6;padding:2px;overscroll-behavior:contain}.analytics.is-open{display:grid}
}
@media(min-width:1150px){.nav-search{display:block;width:clamp(140px,13vw,205px)}}
@media(min-width:1280px){
 #app{height:100vh;height:100dvh;min-height:610px}#content{flex:1;grid-template-columns:minmax(255px,310px) minmax(0,1fr) auto;grid-template-rows:minmax(240px,1fr) auto;gap:12px}#map-view{grid-area:1 / 1 / 2 / 4;min-height:0}.analytics{display:grid;grid-area:1 / 1 / 2 / 2;z-index:4;align-content:start;align-self:stretch;overflow:auto;padding:12px 4px 12px 12px;scroll-padding:12px;overscroll-behavior:contain}.operations{grid-area:2 / 1 / 3 / 4;grid-template-columns:repeat(4,minmax(0,1fr))}.map-tools{grid-area:1 / 3 / 2 / 4}.map-caption{grid-area:1 / 2 / 2 / 4}.map-detail,.view-panel{grid-area:1 / 2 / 2 / 4}
}
@media(min-width:1500px){.inventory{display:flex}}
@media(pointer:coarse){button,select{min-height:44px;min-width:44px}}
@media(prefers-reduced-motion:reduce){*,*::before,*::after{animation:none!important;transition:none!important;scroll-behavior:auto!important}}
[aria-disabled=true]{opacity:.5;cursor:default}.map-image[hidden]{display:none!important}
@media(max-width:767px){.map-tools{grid-auto-flow:column;align-items:start}.map-tools>div:nth-child(2){grid-column:2}.map-tools>div:first-child{grid-column:1}}
@media(min-width:1280px) and (max-height:730px){.map-tools{grid-auto-flow:column;align-items:start}}
</style></head>
<body class="text-slate-100 font-sans antialiased"><a class="skip-link" href="#content">Skip to content</a><div id="app">
<!-- Dynamic Alert Banner for Irrigation Variance -->
<div id="irrigation-alert-banner" class="hidden transition-all duration-300 relative z-20 flex items-center justify-between px-4 py-2.5 rounded-2xl bg-rose-500/20 border border-rose-500/40 text-rose-200 text-xs shadow-lg backdrop-blur-md">
  <div class="flex items-center space-x-2.5">
    <span class="flex h-2.5 w-2.5 relative">
      <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-rose-400 opacity-75"></span>
      <span class="relative inline-flex rounded-full h-2.5 w-2.5 bg-rose-500"></span>
    </span>
    <span class="font-bold text-rose-300 tracking-wide uppercase text-[11px] bg-rose-950/60 px-2 py-0.5 rounded border border-rose-500/30">Irrigation Alert</span>
    <span id="alert-banner-text">Irrigation variance exceeded ±3.0 min threshold in Zone B (Current: -3.2 min).</span>
  </div>
  <button id="alert-dismiss-btn" type="button" class="text-rose-300 hover:text-white px-2 py-1 rounded-lg bg-rose-500/20 hover:bg-rose-500/30 transition text-[11px] font-semibold">Dismiss</button>
</div>

<header class="top-header" data-purpose="master-navigation-header">
<nav aria-label="Primary" class="glass-hud topbar rounded-2xl">
<div class="nav-left">
<div class="brand flex items-center gap-2">
<div class="w-9 h-9 rounded-xl bg-gradient-to-br from-lime-400 to-emerald-600 flex items-center justify-center shadow-lg shadow-lime-900/40">
<svg aria-hidden="true" class="w-5 h-5 text-zinc-950" fill="none" focusable="false" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" viewBox="0 0 24 24">
<path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"></path>
</svg>
</div>
<span class="text-lg font-bold tracking-tight text-white">Furrow</span>
</div>
<div class="nav-links rounded-xl bg-black/40 border border-white/5" id="primary-links">
<button aria-current="page" class="nav-item rounded-lg text-xs font-semibold" data-view="map" type="button">Live Map</button>
<button class="nav-item rounded-lg text-xs font-semibold" data-view="fields" type="button">Fields</button>
<button class="nav-item rounded-lg text-xs font-semibold" data-view="analytics" type="button">Analytics</button>
<button class="nav-item rounded-lg text-xs font-semibold" data-view="reports" type="button">Reports</button>
<button class="nav-item rounded-lg text-xs font-semibold" data-view="farmers" type="button">Farmers</button>
</div>
<div class="inventory items-center gap-1 text-xs text-slate-300">
<span class="px-2 py-1 rounded-lg bg-white/5 whitespace-nowrap">14 Fields</span>
<span class="px-2 py-1 rounded-lg bg-white/5 whitespace-nowrap">170 Sensors</span>
<span class="px-2 py-1 rounded-lg bg-white/5 whitespace-nowrap">13 Systems</span>
<span class="px-2 py-1 rounded-lg bg-white/5 whitespace-nowrap">12 Tractors</span>
</div>
</div>
<div class="nav-right">
<!-- Interactive Live Telemetry Pause/Resume Toggle -->
<button id="telemetry-toggle-btn" type="button" class="flex items-center space-x-1.5 px-3 py-1.5 bg-lime-500/15 border border-lime-400/40 hover:bg-lime-500/25 rounded-xl text-lime-300 text-xs font-semibold transition shadow-sm" title="Toggle Live Telemetry Simulation">
  <span id="telemetry-indicator" class="w-2 h-2 rounded-full bg-lime-400 animate-pulse"></span>
  <span id="telemetry-btn-text">Simulation: Live</span>
</button>

<div class="nav-search relative">
<input aria-label="Search parcels and equipment" autocomplete="off" class="w-full bg-white/5 border border-white/10 rounded-xl px-3.5 py-1.5 text-xs text-slate-200 placeholder-slate-400 focus:outline-none focus:ring-1 focus:ring-lime-400/50 focus:border-lime-400/50 transition" id="dashboard-search" placeholder="Search parcel, unit..." type="search"/>
<svg aria-hidden="true" class="search-icon w-4 h-4 text-slate-400" fill="none" focusable="false" stroke="currentColor" viewBox="0 0 24 24">
<path d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" stroke-linecap="round" stroke-linejoin="round" stroke-width="2.2"></path>
</svg>
<div class="search-results glass-hud rounded-xl p-2" hidden="" id="search-results"></div></div>
<div class="flex items-center space-x-1.5 px-2.5 py-1.5 bg-emerald-500/10 border border-emerald-500/25 rounded-xl text-emerald-400 text-[11px] font-semibold connection" role="status">
<span class="relative flex h-2 w-2">
<span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75"></span>
<span class="relative inline-flex rounded-full h-2 w-2 bg-emerald-500"></span>
</span>
<span>LTE Telemetry</span>
</div>
<button aria-label="Notifications" class="relative w-9 h-9 rounded-xl bg-white/5 hover:bg-white/10 border border-white/10 flex items-center justify-center text-slate-300 transition" data-dialog="notifications" type="button">
<svg aria-hidden="true" class="w-4 h-4" fill="none" focusable="false" stroke="currentColor" viewBox="0 0 24 24">
<path d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"></path>
</svg>
<span class="absolute top-2 right-2 w-2 h-2 bg-lime-400 rounded-full"></span>
</button>
<div class="w-8 h-8 rounded-xl bg-gradient-to-tr from-stone-800 to-stone-700 border border-white/20 flex items-center justify-center text-xs font-semibold text-lime-400 shadow-inner avatar">
            JD
          </div>
<button aria-controls="primary-links" aria-expanded="false" class="menu-toggle glass-pill rounded-xl px-3 text-xs font-semibold" id="menu-toggle" type="button">Menu</button></div>
</nav>
<div class="subheader">
<div>
<h1 class="page-title font-bold tracking-tight text-white" id="page-title">Field Management</h1>
<p class="text-xs text-slate-300" id="page-subtitle">Field health, fleet telemetry and operations · Live Simulation Active</p>
</div>
<div class="glass-pill px-4 py-2 rounded-2xl flex items-center space-x-4 text-xs font-medium text-slate-200 shadow-lg weather">
<div class="flex items-center space-x-2">
<svg aria-hidden="true" class="w-4 h-4 text-amber-400" fill="currentColor" focusable="false" viewBox="0 0 20 20">
<path clip-rule="evenodd" d="M10 2a1 1 0 011 1v1a1 1 0 11-2 0V3a1 1 0 011-1zm4 8a4 4 0 11-8 0 4 4 0 018 0zm-.464 4.95l.707.707a1 1 0 001.414-1.414l-.707-.707a1 1 0 00-1.414 1.414zm2.12-10.607a1 1 0 010 1.414l-.706.707a1 1 0 11-1.414-1.414l.707-.707a1 1 0 011.414 0zM17 11a1 1 0 100-2h-1a1 1 0 100 2h1zm-7 4a1 1 0 011 1v1a1 1 0 11-2 0v-1a1 1 0 011-1zM5.05 6.464A1 1 0 106.465 5.05l-.708-.707a1 1 0 00-1.414 1.414l.707.707zm1.414 8.486l-.707.707a1 1 0 01-1.414-1.414l.707-.707a1 1 0 011.414 1.414zM4 11a1 1 0 100-2H3a1 1 0 000 2h1z" fill-rule="evenodd"></path>
</svg>
<span class="text-white font-semibold">28°</span>
<span class="text-slate-400">Clear Sky</span>
</div>
<span class="w-px h-3.5 bg-white/15"></span>
<div class="flex items-center space-x-1.5">
<svg aria-hidden="true" class="w-3.5 h-3.5 text-sky-400" fill="none" focusable="false" stroke="currentColor" viewBox="0 0 24 24">
<path d="M14 5l7 7m0 0l-7 7m7-7H3" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"></path>
</svg>
<span id="weather-wind">12 km/h NE</span>
</div>
<span class="w-px h-3.5 bg-white/15"></span>
<div class="flex items-center space-x-1.5">
<span class="w-2 h-2 rounded-full bg-cyan-400"></span>
<span id="weather-humidity">62% Humidity</span>
</div>
</div>
</div>
</header><main aria-label="Farm workspace" id="content" tabindex="-1"><section aria-label="Interactive farm map preview" data-layer="satellite" id="map-view"><div id="map-stage"><img alt="High-resolution top-down aerial satellite photography of agricultural fields" class="map-image" draggable="false" fetchpriority="high" src="https://lh3.googleusercontent.com/aida-public/AB6AXuAfk4GGG4d7WPO-mRL3z-_8N9wP4qrwAR2GqYlskSqEuq0-eBQUR2WqTj9eYZfF7cdg8fpkXCqn7SLl5AWOEmhXs89uAOcVsqp5CRt0CYfR1GSxjkXkBC5I59uqzn0sWP6Y3Ox-yUZlyY4eHScjCgE0EhplPsvGZKl2U9tTI4vPTVMPYks7-u0QuGgxUBMxEncPJ_T8j8-Pd54VInSiObsDDkgsb7xN8qCyuIWwcz4"/><svg aria-hidden="true" class="map-vectors" fill="none" focusable="false" preserveAspectRatio="xMidYMid slice" viewBox="0 0 1920 1080" xmlns="http://www.w3.org/2000/svg">
<defs>
<linearGradient id="neonLimeGrad" x1="0%" x2="100%" y1="0%" y2="100%">
<stop offset="0%" stop-color="#bef264"></stop>
<stop offset="50%" stop-color="#84cc16"></stop>
<stop offset="100%" stop-color="#4d7c0f"></stop>
</linearGradient>
<pattern height="16" id="cropHatch" patternTransform="rotate(45 0 0)" patternUnits="userSpaceOnUse" width="16">
<line stroke="#a3e635" stroke-opacity="0.16" stroke-width="0.7" x1="0" x2="0" y1="0" y2="16"></line>
</pattern>
</defs>
<polygon class="field-scanlines" fill="url(#cropHatch)" points="954,342 1530,344 1532,714 1145,712 918,485 918,410"></polygon>
<polygon class="polygon-glow" points="954,342 1530,344 1532,714 1145,712 918,485 918,410" stroke="url(#neonLimeGrad)" stroke-linejoin="round" stroke-width="2.6"></polygon>
<circle cx="954" cy="342" fill="#facc15" r="3.5" stroke="#1c1917" stroke-width="1.5"></circle>
<circle cx="1530" cy="344" fill="#facc15" r="3.5" stroke="#1c1917" stroke-width="1.5"></circle>
<circle cx="1532" cy="714" fill="#facc15" r="3.5" stroke="#1c1917" stroke-width="1.5"></circle>
<circle cx="1145" cy="712" fill="#facc15" r="3.5" stroke="#1c1917" stroke-width="1.5"></circle>
<circle cx="918" cy="485" fill="#facc15" r="3.5" stroke="#1c1917" stroke-width="1.5"></circle>

<!-- Drone Flight Path Overlay (Interactive Simulation) -->
<g id="drone-path-group" class="cursor-pointer" opacity="0.9">
  <!-- Waypoint connecting flight line -->
  <path id="drone-flight-path" d="M 980 370 L 1490 375 L 1490 440 L 970 440 L 970 510 L 1480 510 L 1480 580 L 1020 580 L 1020 650 L 1450 650" stroke="#38bdf8" stroke-width="2" stroke-dasharray="6 6" fill="none" opacity="0.65"></path>
  
  <!-- Waypoints -->
  <circle cx="980" cy="370" r="4" fill="#38bdf8" stroke="#0f172a" stroke-width="1.5"></circle>
  <circle cx="1490" cy="375" r="4" fill="#38bdf8" stroke="#0f172a" stroke-width="1.5"></circle>
  <circle cx="1490" cy="440" r="4" fill="#38bdf8" stroke="#0f172a" stroke-width="1.5"></circle>
  <circle cx="970" cy="440" r="4" fill="#38bdf8" stroke="#0f172a" stroke-width="1.5"></circle>
  <circle cx="1480" cy="510" r="4" fill="#38bdf8" stroke="#0f172a" stroke-width="1.5"></circle>
  <circle cx="1020" cy="580" r="4" fill="#38bdf8" stroke="#0f172a" stroke-width="1.5"></circle>
  
  <!-- Live Animated Drone Marker -->
  <g id="drone-marker" transform="translate(980, 370)">
    <circle r="14" fill="#0284c7" opacity="0.25" class="drone-anim"></circle>
    <circle r="6" fill="#38bdf8" stroke="#ffffff" stroke-width="1.5"></circle>
    <polygon points="0,-10 6,4 0,1 -6,4" fill="#bae6fd"></polygon>
    <!-- Drone Label -->
    <rect x="10" y="-12" width="86" height="20" rx="6" fill="#0b1318cc" stroke="#38bdf8aa" stroke-width="1"></rect>
    <text x="16" y="2" fill="#38bdf8" font-size="10" font-weight="600" font-family="Inter, sans-serif">Drone Scan-03</text>
  </g>
</g>

<!-- Tractor T-04 GPS Route & Live Position -->
<g id="tractor-gps-group">
  <path id="tractor-trail" d="M 960 410 L 1080 410 L 1080 620 L 1150 620 L 1150 430 L 1220 430 L 1220 620" stroke="#84cc16" stroke-width="2.5" stroke-dasharray="4 4" fill="none" opacity="0.6"></path>
  <g id="tractor-marker" transform="translate(1080, 410)" class="cursor-pointer">
    <circle r="12" fill="#84cc16" opacity="0.25"></circle>
    <circle r="5" fill="#84cc16" stroke="#0f172a" stroke-width="1.5"></circle>
    <rect x="8" y="-10" width="76" height="18" rx="5" fill="#09140fdd" stroke="#84cc16aa" stroke-width="1"></rect>
    <text x="13" y="3" fill="#bef264" font-size="9" font-weight="bold" font-family="Inter, sans-serif">T-04 · 8km/h</text>
  </g>
</g>

<!-- Sprayer S-01 GPS Route & Live Position -->
<g id="sprayer-gps-group">
  <path id="sprayer-trail" d="M 1320 370 L 1320 680 L 1400 680 L 1400 370 L 1470 370 L 1470 660" stroke="#f59e0b" stroke-width="2.5" stroke-dasharray="4 4" fill="none" opacity="0.6"></path>
  <g id="sprayer-marker" transform="translate(1320, 450)" class="cursor-pointer">
    <circle r="12" fill="#f59e0b" opacity="0.25"></circle>
    <circle r="5" fill="#f59e0b" stroke="#0f172a" stroke-width="1.5"></circle>
    <rect x="8" y="-10" width="76" height="18" rx="5" fill="#140f09dd" stroke="#f59e0baa" stroke-width="1"></rect>
    <text x="13" y="3" fill="#fde68a" font-size="9" font-weight="bold" font-family="Inter, sans-serif">S-01 · 6km/h</text>
  </g>
</g>

</svg><button aria-controls="field-detail" aria-expanded="false" class="field-trigger flex items-center gap-2" data-purpose="field-target-callout" id="field-trigger" type="button">
<span class="radar-pin relative grid place-items-center shrink-0">
<span class="absolute w-12 h-12 rounded-full border border-lime-400/40 radar-ring-1"></span>
<span class="absolute w-8 h-8 rounded-full border border-lime-400/60 radar-ring-2"></span>
<span class="w-7 h-7 rounded-full bg-lime-500/20 backdrop-blur-md border border-lime-400 flex items-center justify-center shadow-[0_0_15px_rgba(132,204,22,0.8)] block">
<span class="w-2.5 h-2.5 bg-white rounded-full shadow-sm block"></span>
</span>
</span>
<span class="glass-hud py-2.5 px-4 rounded-2xl flex items-center space-x-3.5 border border-lime-500/30 hover:border-lime-400 transition-all duration-300 shadow-2xl cursor-pointer field-label">
<span class="w-8 h-8 rounded-xl bg-lime-500/20 border border-lime-400/40 flex items-center justify-center text-lime-400">
<svg aria-hidden="true" class="w-4 h-4" fill="currentColor" focusable="false" viewBox="0 0 20 20">
<path clip-rule="evenodd" d="M4.16 4.16C7.57.75 13.06.75 16.47 4.16s3.41 8.9 0 12.31c-1.4 1.4-3.2 2.2-5.1 2.37-.42.04-.8-.28-.84-.7-.04-.42.28-.8.7-.84 1.54-.14 3.01-.79 4.16-1.93 2.94-2.94 2.94-7.7 0-10.64S9.75 1.79 6.81 4.73c-.94.94-1.55 2.1-1.8 3.34l2.42 2.42c.31.31.31.82 0 1.13s-.82.31-1.13 0L3.82 9.14C3.76 10.15 4 11.2 4.54 12.1c.21.36.09.83-.27 1.04-.36.21-.83.09-1.04-.27C2.5 11.62 2.2 10.3 2.28 9c.1-1.57.85-3.09 2.04-4.28l-.16-.56z" fill-rule="evenodd"></path>
</svg>
</span>
<span class="text-left block">
<span class="flex items-center space-x-2">
<span class="text-sm font-semibold text-white tracking-wide">North Field</span>
<svg aria-hidden="true" class="w-3.5 h-3.5 text-white/50" fill="none" focusable="false" stroke="currentColor" viewBox="0 0 24 24">
<path d="M9 5l7 7-7 7" stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5"></path>
</svg>
</span>
<span class="flex items-center space-x-1.5 mt-0.5">
<span class="inline-block w-1.5 h-1.5 rounded-full bg-lime-400"></span>
<span class="text-xs font-semibold text-[#a3e635]">92% Health</span>
<span class="text-[11px] text-lime-300/80 font-medium">· +2%</span>
</span>
</span>
</span>
</button></div><div class="absolute pointer-events-none bg-gradient-to-r from-[#070c09]/95 via-[#070c09]/30 to-[#070c09]/85 mix-blend-multiply vignette vignette-0"></div><div class="absolute pointer-events-none bg-gradient-to-t from-[#050907] via-transparent to-[#050907]/75 vignette vignette-1"></div><div class="absolute pointer-events-none bg-[radial-gradient(ellipse_at_center,transparent_30%,rgba(4,7,5,0.75)_100%)] vignette vignette-2"></div></section><article aria-labelledby="field-title" class="glass-hud rounded-2xl p-4 map-detail" hidden="" id="field-detail"><h2 class="text-white font-semibold" id="field-title">North Field</h2><p class="mt-2 text-sm text-slate-300">92% crop health · 248 ha monitored across the farm</p><p class="mt-1 text-xs text-slate-300">Last scan: 09:42 (sample reading)</p><button class="mt-2 text-sm text-lime-300" id="field-close" type="button">Close details</button></article><aside aria-label="Map controls" class="map-tools" data-purpose="floating-map-controls">
<div class="glass-hud p-2 rounded-2xl flex flex-col space-y-2 shadow-2xl">
<button aria-pressed="true" class="layer-choice flex items-center gap-2 px-3 py-2 rounded-xl text-left" data-layer-choice="satellite" type="button">
<div aria-hidden="true" class="w-7 h-7 rounded-lg overflow-hidden border border-lime-400 relative">
<div class="w-full h-full bg-emerald-800 flex items-center justify-center">
<div class="w-3 h-3 rounded-full bg-lime-400/80"></div>
</div>
</div>
<div class="layer-caption">
<span class="block text-xs font-semibold text-white">Satellite</span>
<span class="layer-description">RGB High-Res</span>
</div>
</button>
<button aria-pressed="false" class="layer-choice flex items-center gap-2 px-3 py-2 rounded-xl text-left" data-layer-choice="ndvi" type="button">
<div aria-hidden="true" class="w-7 h-7 rounded-lg overflow-hidden border border-white/20 relative">
<div class="w-full h-full bg-gradient-to-tr from-amber-600 via-yellow-400 to-emerald-500"></div>
</div>
<div class="layer-caption">
<span class="block text-xs font-medium text-slate-300 group-hover:text-white">NDVI</span>
<span class="layer-description">Biomass Index</span>
</div>
</button>
<button aria-pressed="false" class="layer-choice flex items-center gap-2 px-3 py-2 rounded-xl text-left" data-layer-choice="soil" type="button">
<div aria-hidden="true" class="w-7 h-7 rounded-lg overflow-hidden border border-white/20 relative">
<div class="w-full h-full bg-amber-900/80 flex items-center justify-center">
<div class="w-3.5 h-3.5 rounded bg-amber-700"></div>
</div>
</div>
<div class="layer-caption">
<span class="block text-xs font-medium text-slate-300 group-hover:text-white">Soil</span>
<span class="layer-description">Moisture Profile</span>
</div>
</button>
<!-- Drone layer button -->
<button aria-pressed="true" id="drone-layer-toggle" class="layer-choice flex items-center gap-2 px-3 py-2 rounded-xl text-left" type="button">
<div aria-hidden="true" class="w-7 h-7 rounded-lg overflow-hidden border border-sky-400/60 relative bg-sky-950/80 flex items-center justify-center">
<svg class="w-4 h-4 text-sky-400" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 2v20M2 12h20M4.93 4.93l14.14 14.14M4.93 19.07l14.14-14.14"/></svg>
</div>
<div class="layer-caption">
<span class="block text-xs font-medium text-slate-300 group-hover:text-white">Drones</span>
<span class="layer-description text-sky-400">Flight Path</span>
</div>
</button>
</div>
<div class="glass-hud p-1.5 rounded-2xl flex flex-col space-y-1 items-center shadow-xl">
<button aria-label="Compass Orientation" class="w-9 h-9 rounded-xl flex items-center justify-center text-slate-300 hover:text-white hover:bg-white/10 transition" data-map-action="compass" title="Compass Orientation" type="button">
<svg aria-hidden="true" class="w-4 h-4 text-rose-400" fill="currentColor" focusable="false" viewBox="0 0 24 24">
<polygon points="12,2 15,10 12,8 9,10"></polygon>
<polygon fill="#94a3b8" points="12,22 9,14 12,16 15,14"></polygon>
</svg>
</button>
<div class="w-5 h-px bg-white/10"></div>
<button aria-label="Zoom In" class="w-9 h-9 rounded-xl flex items-center justify-center text-slate-300 hover:text-white hover:bg-white/10 transition text-sm font-semibold" data-map-action="in" title="Zoom In" type="button">+</button>
<button aria-label="Zoom Out" class="w-9 h-9 rounded-xl flex items-center justify-center text-slate-300 hover:text-white hover:bg-white/10 transition text-sm font-semibold" data-map-action="out" title="Zoom Out" type="button">−</button>
<div class="w-5 h-px bg-white/10"></div>
<button aria-label="Fit Bounds" class="w-9 h-9 rounded-xl flex items-center justify-center text-slate-300 hover:text-white hover:bg-white/10 transition" data-map-action="fit" title="Fit Bounds" type="button">
<svg aria-hidden="true" class="w-4 h-4" fill="none" focusable="false" stroke="currentColor" viewBox="0 0 24 24">
<path d="M4 8V4m0 0h4M4 4l5 5m11-5h-4m4 0v4m0 0l-5 5M4 16v4m0 0h4m-4 0l5-5m11 5l-5-5m5 5v-4m0 4h-4" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"></path>
</svg>
</button>
<button aria-label="Rotate map clockwise" class="w-9 h-9 rounded-xl text-slate-300 hover:text-white hover:bg-white/10" data-map-action="rotate" title="Rotate map clockwise" type="button">↻</button></div>
</aside><p class="map-caption glass-pill rounded-xl px-3 py-1" id="map-caption">Satellite imagery · Live telemetry & GPS tracking active</p><section aria-labelledby="analytics-title" class="analytics" data-purpose="left-analytics-stack" id="analytics"><h2 class="sr-only" id="analytics-title">Field analytics</h2>
<article aria-labelledby="crop-health-title" class="glass-hud p-4 rounded-2xl relative overflow-hidden" data-purpose="crop-health-card" data-value="92">
<div class="flex items-center justify-between mb-2">
<h3 class="text-xs font-semibold text-slate-300 uppercase tracking-wider" id="crop-health-title">Crop Health</h3>
<button aria-label="Crop health details" class="text-slate-400 hover:text-white" data-dialog="health" type="button">
<svg aria-hidden="true" class="w-3.5 h-3.5" fill="none" focusable="false" stroke="currentColor" viewBox="0 0 24 24">
<path d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"></path>
</svg>
</button>
</div>
<div class="flex items-center justify-between pt-1">
<div class="relative w-28 h-16 flex items-end justify-center">
<svg aria-label="Crop health: 92 percent" class="w-28 h-16 overflow-visible" focusable="false" id="crop-gauge" role="img" viewBox="0 0 100 55"><defs><linearGradient id="gaugeLimeGrad" x1="0%" x2="100%" y1="0%" y2="100%"><stop offset="0%" stop-color="#bef264"></stop><stop offset="50%" stop-color="#84cc16"></stop><stop offset="100%" stop-color="#4d7c0f"></stop></linearGradient></defs>
<path d="M 10 50 A 40 40 0 0 1 90 50" fill="none" stroke="rgba(255,255,255,0.12)" stroke-linecap="round" stroke-width="8"></path>
<path class="polygon-glow" d="M 10 50 A 40 40 0 0 1 90 50" fill="none" id="gauge-fill" pathLength="100" stroke="url(#gaugeLimeGrad)" stroke-dasharray="92 100" stroke-linecap="round" stroke-width="8"></path>
</svg>
<div class="absolute bottom-0 text-center">
<span class="text-2xl font-bold text-white tracking-tight"><span id="gauge-value">92</span><span class="text-sm font-semibold text-lime-400">%</span></span>
</div>
</div>
<div class="text-right">
<span class="text-2xl font-bold text-white tracking-tight">248 <span class="text-sm font-normal text-slate-300">ha</span></span>
<p class="text-[11px] text-slate-400 font-medium">Total monitored area</p>
<span class="inline-flex items-center text-[11px] text-emerald-400 bg-emerald-500/10 px-2 py-0.5 rounded mt-1">
                Optimal vigor index
              </span>
</div>
</div>
</article>
<article aria-labelledby="trend-title" class="glass-hud p-4 rounded-2xl" data-purpose="health-trend-card">
<div class="flex items-center justify-between mb-3">
<h3 class="text-xs font-semibold text-slate-300 uppercase tracking-wider" id="trend-title">Health Trend</h3>
<select aria-label="Health trend period" class="period-select rounded-lg" id="trend-range"><option value="24h">24 Hours</option><option selected="" value="7d">7 Days</option><option value="30d">30 Days</option></select>
</div>
<div class="w-full h-24 relative">
<svg aria-label="Seven-day crop health trend" class="w-full h-full" fill="none" focusable="false" id="trend-chart" role="img" viewBox="0 0 260 80">
<line stroke="rgba(255,255,255,0.1)" stroke-dasharray="3 3" x1="0" x2="260" y1="42" y2="42"></line>
<path d="M 0,58 Q 40,50 80,55 T 160,48 T 260,52" stroke="rgba(255,255,255,0.18)" stroke-dasharray="2 3" stroke-width="1.2"></path>
<defs>
<linearGradient id="trendGradient" x1="0" x2="0" y1="0" y2="1">
<stop offset="0%" stop-color="#84cc16" stop-opacity="0.35"></stop>
<stop offset="100%" stop-color="#84cc16" stop-opacity="0.0"></stop>
</linearGradient>
</defs>
<path d="M 0,55 L 20,53 L 50,46 L 85,22 L 120,44 L 160,35 L 200,48 L 240,40 L 260,42 L 260,78 L 0,78 Z" fill="url(#trendGradient)" id="trend-area"></path>
<path d="M 0,55 L 20,53 L 50,46 L 85,22 L 120,44 L 160,35 L 200,48 L 240,40 L 260,42" id="trend-line" stroke="#a3e635" stroke-linecap="round" stroke-linejoin="round" stroke-width="2.2"></path>
<circle cx="85" cy="22" fill="#facc15" id="trend-peak" r="4.5" stroke="#1c1917" stroke-width="2"></circle>
</svg>
</div>
<div class="flex items-center justify-between text-[11px] text-slate-400 font-medium px-1 mt-1" id="trend-labels">
<span>Mon</span>
<span>Tue</span>
<span class="text-lime-400 font-bold">Wed</span>
<span>Thu</span>
<span>Fri</span>
<span>Sat</span>
<span>Sun</span>
</div>
</article>
<article aria-labelledby="stress-title" class="glass-hud p-4 rounded-2xl" data-purpose="stress-zones-card">
<div class="flex items-center justify-between mb-2">
<div>
<h3 class="text-xs font-semibold text-slate-200" id="stress-title">Stress Zones</h3>
<p class="text-[11px] text-slate-400">Sensor Matrix Overview</p>
</div>
<div class="bg-lime-500/10 border border-lime-500/25 px-2.5 py-0.5 rounded-full text-[11px] font-semibold text-lime-400">
              Good for Planting
            </div>
</div>
<div aria-labelledby="matrix-summary" class="grid grid-cols-16 gap-1 my-3 bg-black/40 p-2 rounded-xl border border-white/5" role="img" style="grid-template-columns: repeat(16, minmax(0, 1fr));">
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-500 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-yellow-400 cell-caution"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-yellow-400 cell-caution"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-500 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-yellow-400 cell-caution"></span><span aria-hidden="true" class="h-2 rounded-sm bg-amber-500 cell-caution"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-amber-500 cell-caution"></span><span aria-hidden="true" class="h-2 rounded-sm bg-yellow-400 cell-caution"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-500 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-yellow-400 cell-caution"></span><span aria-hidden="true" class="h-2 rounded-sm bg-yellow-400 cell-caution"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-yellow-400 cell-caution"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-amber-500 cell-caution"></span><span aria-hidden="true" class="h-2 rounded-sm bg-rose-500 cell-stress"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-rose-500 cell-stress"></span><span aria-hidden="true" class="h-2 rounded-sm bg-amber-500 cell-caution"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-yellow-400 cell-caution"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-yellow-400 cell-caution"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-amber-500 cell-caution"></span><span aria-hidden="true" class="h-2 rounded-sm bg-yellow-400 cell-caution"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
<span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span><span aria-hidden="true" class="h-2 rounded-sm bg-lime-400 cell-healthy"></span>
</div><p class="matrix-legend text-slate-300" id="matrix-summary">47 Healthy · 15 Caution · 2 Stress</p>
<div class="flex items-center justify-between pt-1 border-t border-white/5">
<span class="text-[11px] text-slate-300 font-medium">12% yield increase projected</span>
<button class="flex items-center space-x-1.5 px-2.5 py-1 rounded-lg bg-lime-500/20 hover:bg-lime-500/30 text-lime-300 border border-lime-400/40 text-[11px] font-semibold transition" data-dialog="insights" type="button">
<svg aria-hidden="true" class="w-3 h-3" fill="none" focusable="false" stroke="currentColor" viewBox="0 0 24 24">
<path d="M13 10V3L4 14h7v7l9-11h-7z" stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5"></path>
</svg>
<span>+ AI Insights</span>
</button>
</div>
<div class="grid grid-cols-2 gap-2 mt-3 pt-2.5 border-t border-white/5">
<div class="bg-white/5 p-2 rounded-xl">
<div class="flex items-center justify-between text-[11px] text-slate-400">
<span>Avg. Humidity</span>
<span id="matrix-humidity" class="text-white font-semibold">62%</span>
</div>
<div class="text-[11px] text-slate-400 mt-0.5">Max 80% · Min 10%</div>
</div>
<div class="bg-white/5 p-2 rounded-xl">
<div class="flex items-center justify-between text-[11px] text-slate-400">
<span>Avg. Temp</span>
<span id="matrix-temp" class="text-white font-semibold">28°C</span>
</div>
<div class="text-[11px] text-slate-400 mt-0.5">Max 42° · Min 19°</div>
</div>
</div>
</article>
</section><button aria-controls="analytics" aria-expanded="false" class="drawer-toggle glass-hud rounded-xl px-4 text-sm font-semibold" id="drawer-toggle" type="button">Field analytics</button><section aria-labelledby="operations-title" class="operations" data-purpose="bottom-operations-dock" id="operations"><h2 class="sr-only" id="operations-title">Fleet and operations</h2>
<article aria-labelledby="tractor-title" class="glass-hud p-4 rounded-2xl flex flex-col justify-between group hover:border-lime-500/40 transition ops-card" id="tractor">
<div>
<div class="flex items-center justify-between">
<div class="fleet-heading">
<h3 class="text-sm font-bold text-white tracking-tight" id="tractor-title">Tractor T-04</h3>
<time class="fleet-time text-slate-300" data-offset-min="0" datetime="">Demo reading</time>
</div>
<button aria-label="Tractor T-04 details" class="text-slate-400 hover:text-white" data-dialog="tractor" type="button">
<svg aria-hidden="true" class="w-3.5 h-3.5" fill="none" focusable="false" stroke="currentColor" viewBox="0 0 24 24">
<path d="M7 17L17 7M17 7H7M17 7V17" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"></path>
</svg>
</button>
</div>
<div class="flex items-center justify-between mt-2.5">
<div class="flex items-center space-x-2">
<span class="inline-flex items-center space-x-1 px-2 py-0.5 rounded-full bg-emerald-500/15 text-emerald-400 text-[11px] font-semibold border border-emerald-500/30" data-fleet-status="" role="status">
<span class="w-1.5 h-1.5 rounded-full bg-emerald-400"></span>
<span data-status-text="">Online</span>
</span>
<span class="text-[11px] text-slate-400 font-mono">GPS · LTE</span>
</div>
<div class="w-10 h-7 text-lime-400/80">
<svg aria-hidden="true" fill="none" focusable="false" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.8" viewBox="0 0 48 32">
<circle cx="12" cy="24" r="6"></circle>
<circle cx="36" cy="22" r="8"></circle>
<path d="M12 24h16V10H16l-4 6v8z"></path>
<path d="M28 14h10v8"></path>
<path d="M16 10V6h4"></path>
</svg>
</div>
</div>
<div class="mt-2 bg-black/30 p-2 rounded-xl border border-white/5">
<svg aria-label="Sample tractor activity timeline, 6 AM to 11 PM" class="w-full h-8" fill="none" focusable="false" role="img" viewBox="0 0 200 30">
<path d="M 0,22 L 30,22 L 30,8 L 70,8 L 70,18 L 110,18 L 110,8 L 150,8 L 150,22 L 200,22" stroke="#84cc16" stroke-linejoin="bevel" stroke-width="1.8"></path>
</svg>
<div class="flex justify-between text-[11px] text-slate-400 mt-1 font-mono">
<span>06 AM</span>
<span>11 PM</span>
</div>
</div>
</div>
<div class="grid grid-cols-3 gap-2 mt-3 pt-2.5 border-t border-white/5 text-center">
<div>
<span class="block text-[11px] text-slate-400">Fuel</span>
<span id="tractor-fuel" class="text-xs font-bold text-white">64%</span>
</div>
<div>
<span class="block text-[11px] text-slate-400">Area</span>
<span id="tractor-area" class="text-xs font-bold text-white">12.4 ha</span>
</div>
<div>
<span class="block text-[11px] text-slate-400">Speed</span>
<span id="tractor-speed" class="text-xs font-bold text-lime-400">8 km/h</span>
</div>
</div>
</article>
<article aria-labelledby="sprayer-title" class="glass-hud p-4 rounded-2xl flex flex-col justify-between group hover:border-lime-500/40 transition ops-card" id="sprayer">
<div>
<div class="flex items-center justify-between">
<div class="fleet-heading">
<h3 class="text-sm font-bold text-white tracking-tight" id="sprayer-title">Sprayer S-01</h3>
<time class="fleet-time text-slate-300" data-offset-min="2" datetime="">Demo reading</time>
</div>
<button aria-label="Sprayer S-01 details" class="text-slate-400 hover:text-white" data-dialog="sprayer" type="button">
<svg aria-hidden="true" class="w-3.5 h-3.5" fill="none" focusable="false" stroke="currentColor" viewBox="0 0 24 24">
<path d="M7 17L17 7M17 7H7M17 7V17" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"></path>
</svg>
</button>
</div>
<div class="flex items-center justify-between mt-2.5">
<div class="flex items-center space-x-2">
<span class="inline-flex items-center space-x-1 px-2 py-0.5 rounded-full bg-amber-500/15 text-amber-400 text-[11px] font-semibold border border-amber-500/30" data-fleet-status="" role="status">
<span class="w-1.5 h-1.5 rounded-full bg-amber-400 animate-pulse"></span>
<span data-status-text="">Working</span>
</span>
<span class="text-[11px] text-slate-400 font-mono">GPS · LTE</span>
</div>
<div class="w-10 h-7 text-amber-400/80">
<svg aria-hidden="true" fill="none" focusable="false" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.8" viewBox="0 0 48 32">
<circle cx="14" cy="24" r="5"></circle>
<circle cx="34" cy="24" r="5"></circle>
<path d="M4 14h40"></path>
<path d="M14 24h20V14H14v10z"></path>
<path d="M8 14v4M24 14v4M40 14v4"></path>
</svg>
</div>
</div>
<div class="mt-2 bg-black/30 p-2 rounded-xl border border-white/5">
<svg aria-label="Sample sprayer activity timeline, 7 AM to 5 PM" class="w-full h-8" fill="none" focusable="false" role="img" viewBox="0 0 200 30">
<path d="M 0,16 L 45,16 L 45,6 L 90,6 L 90,24 L 140,24 L 140,10 L 200,10" stroke="#f59e0b" stroke-linejoin="bevel" stroke-width="1.8"></path>
</svg>
<div class="flex justify-between text-[11px] text-slate-400 mt-1 font-mono">
<span>07 AM</span>
<span>05 PM</span>
</div>
</div>
</div>
<div class="grid grid-cols-3 gap-2 mt-3 pt-2.5 border-t border-white/5 text-center">
<div>
<span class="block text-[11px] text-slate-400">Tank</span>
<span id="sprayer-tank" class="text-xs font-bold text-amber-400">41%</span>
</div>
<div>
<span class="block text-[11px] text-slate-400">Area</span>
<span id="sprayer-area" class="text-xs font-bold text-white">6.8 ha</span>
</div>
<div>
<span class="block text-[11px] text-slate-400">Speed</span>
<span id="sprayer-speed" class="text-xs font-bold text-white">6 km/h</span>
</div>
</div>
</article>
<article aria-labelledby="irrigation-title" class="glass-hud p-4 rounded-2xl flex flex-col justify-between group hover:border-lime-500/40 transition ops-card" id="irrigation">
<div>
<div class="flex items-center justify-between">
<h3 class="text-sm font-bold text-white tracking-tight" id="irrigation-title">Irrigation Offset</h3>
<div class="flex items-center space-x-1.5">
<span id="irrigation-global-variance" class="text-xs font-bold text-lime-400">± 2.5 <span class="text-[11px] text-slate-300 font-normal">min</span></span>
<button aria-label="Irrigation Offset details" class="text-slate-400 hover:text-white" data-dialog="irrigation" type="button">
<svg aria-hidden="true" class="w-3.5 h-3.5" fill="none" focusable="false" stroke="currentColor" viewBox="0 0 24 24">
<path d="M7 17L17 7M17 7H7M17 7V17" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"></path>
</svg>
</button>
</div>
</div>
<p class="text-[11px] text-slate-400 mt-0.5">Average system flow variance</p>
<div class="mt-3 overflow-hidden rounded-xl border border-white/5 bg-black/30">
<table aria-label="Sample irrigation offsets by zone" class="w-full text-center text-[11px]">
<thead class="bg-white/5 text-slate-400 border-b border-white/5">
<tr>
<th class="py-1 px-2 text-left font-medium" scope="col">Zone</th>
<th class="py-1 font-medium" scope="col">Z1</th>
<th class="py-1 font-medium" scope="col">Z2</th>
<th class="py-1 font-medium" scope="col">Z3</th>
<th class="py-1 font-medium" scope="col">Z4</th>
</tr>
</thead>
<tbody class="divide-y divide-white/5 font-mono">
<tr>
<th class="py-1.5 px-2 text-left font-sans text-slate-300 font-medium" scope="row">Zone A</th>
<td id="irrig-a1" class="text-slate-300">-2.0m</td>
<td id="irrig-a2" class="text-amber-400 font-semibold">+1.0m</td>
<td id="irrig-a3" class="text-amber-400 font-semibold">+1.5m</td>
<td id="irrig-a4" class="text-slate-300">-1.0m</td>
</tr>
<tr>
<th class="py-1.5 px-2 text-left font-sans text-slate-300 font-medium" scope="row">Zone B</th>
<td id="irrig-b1" class="text-slate-300">-1.0m</td>
<td id="irrig-b2" class="text-slate-300">-2.0m</td>
<td id="irrig-b3" class="text-amber-400 font-semibold">+2.0m</td>
<td id="irrig-b4" class="text-rose-400 font-semibold">-2.5m</td>
</tr>
</tbody>
</table>
</div>
</div>
<div class="flex items-center justify-between text-[11px] mt-2 pt-2 border-t border-white/5 text-slate-400">
<span>Main Pump Station 02</span>
<span id="pump-status" class="text-emerald-400 font-medium">Calibrated</span>
</div>
</article>
<article aria-labelledby="yield-title" class="glass-hud p-4 rounded-2xl flex flex-col justify-between group hover:border-lime-500/40 transition ops-card" id="yield">
<div>
<div class="flex items-center justify-between">
<h3 class="text-sm font-bold text-white tracking-tight" id="yield-title">Live Yield Volume</h3>
<button aria-label="Live Yield Volume details" class="text-slate-400 hover:text-white" data-dialog="yield" type="button">
<svg aria-hidden="true" class="w-3.5 h-3.5" fill="none" focusable="false" stroke="currentColor" viewBox="0 0 24 24">
<path d="M7 17L17 7M17 7H7M17 7V17" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"></path>
</svg>
</button>
</div>
<div class="mt-1">
<span id="yield-volume-val" class="text-2xl font-bold text-white tracking-tight">142,580</span>
<span class="text-xs text-slate-400 ml-1 font-medium">kg harvested today</span>
</div>
<!-- Live Histogram with Tooltips -->
<div id="yield-histogram-container" class="relative mt-3">
  <!-- Tooltip Floating Badge -->
  <div id="histogram-tooltip" class="absolute pointer-events-none -top-8 left-1/2 -translate-x-1/2 opacity-0 transition-opacity bg-black/90 text-lime-300 text-[10px] font-mono px-2 py-0.5 rounded border border-lime-400/40 shadow-lg whitespace-nowrap z-20">
    <span id="tooltip-text">14:00 · 18.4 tn/hr</span>
  </div>
  <div aria-label="Harvest activity histogram with interactive tooltips" class="flex items-end justify-between h-14 bg-black/30 p-2 rounded-xl border border-white/5 gap-1" role="img" id="yield-histogram">
    <div data-val="5.2" data-time="06:00" class="yield-bar flex-1 bg-slate-700/60 hover:bg-lime-400 transition-colors rounded-t h-[35%] cursor-pointer"></div>
    <div data-val="7.8" data-time="07:00" class="yield-bar flex-1 bg-slate-700/60 hover:bg-lime-400 transition-colors rounded-t h-[50%] cursor-pointer"></div>
    <div data-val="6.5" data-time="08:00" class="yield-bar flex-1 bg-slate-700/60 hover:bg-lime-400 transition-colors rounded-t h-[42%] cursor-pointer"></div>
    <div data-val="10.1" data-time="09:00" class="yield-bar flex-1 bg-slate-700/60 hover:bg-lime-400 transition-colors rounded-t h-[65%] cursor-pointer"></div>
    <div data-val="4.6" data-time="10:00" class="yield-bar flex-1 bg-slate-700/60 hover:bg-lime-400 transition-colors rounded-t h-[30%] cursor-pointer"></div>
    <div data-val="11.8" data-time="11:00" class="yield-bar flex-1 bg-slate-700/60 hover:bg-lime-400 transition-colors rounded-t h-[75%] cursor-pointer"></div>
    <div data-val="7.5" data-time="12:00" class="yield-bar flex-1 bg-slate-700/60 hover:bg-lime-400 transition-colors rounded-t h-[48%] cursor-pointer"></div>
    <div data-val="9.0" data-time="13:00" class="yield-bar flex-1 bg-slate-700/60 hover:bg-lime-400 transition-colors rounded-t h-[58%] cursor-pointer"></div>
    <div data-val="10.9" data-time="14:00" class="yield-bar flex-1 bg-slate-700/60 hover:bg-lime-400 transition-colors rounded-t h-[70%] cursor-pointer"></div>
    <div data-val="7.0" data-time="15:00" class="yield-bar flex-1 bg-slate-700/60 hover:bg-lime-400 transition-colors rounded-t h-[45%] cursor-pointer"></div>
    <div data-val="18.4" data-time="16:00 (Peak)" class="yield-bar flex-1 bg-gradient-to-t from-lime-500 to-lime-300 rounded-t h-[95%] shadow-[0_0_8px_rgba(132,204,22,0.8)] cursor-pointer"></div>
    <div data-val="17.1" data-time="17:00 (Peak)" class="yield-bar flex-1 bg-gradient-to-t from-lime-500 to-lime-300 rounded-t h-[88%] shadow-[0_0_8px_rgba(132,204,22,0.8)] cursor-pointer"></div>
    <div data-val="8.6" data-time="18:00" class="yield-bar flex-1 bg-slate-700/60 hover:bg-lime-400 transition-colors rounded-t h-[55%] cursor-pointer"></div>
    <div data-val="9.7" data-time="19:00" class="yield-bar flex-1 bg-slate-700/60 hover:bg-lime-400 transition-colors rounded-t h-[62%] cursor-pointer"></div>
    <div data-val="5.9" data-time="20:00" class="yield-bar flex-1 bg-slate-700/60 hover:bg-lime-400 transition-colors rounded-t h-[38%] cursor-pointer"></div>
    <div data-val="6.9" data-time="21:00" class="yield-bar flex-1 bg-slate-700/60 hover:bg-lime-400 transition-colors rounded-t h-[44%] cursor-pointer"></div>
  </div>
</div>
</div>
<div class="flex items-center justify-between text-[11px] mt-2 pt-2 border-t border-white/5">
<span class="text-slate-400">Peak Run Rate</span>
<span id="yield-runrate" class="text-lime-400 font-semibold">+18.4 tn/hr</span>
</div>
</article>
</section><section aria-labelledby="view-title" class="view-panel glass-hud rounded-2xl p-4" hidden="" id="view-panel"><h2 class="text-base font-semibold" id="view-title"></h2><p class="mt-2 text-sm text-slate-300" id="view-copy"></p></section><p class="sr-only" id="map-status" role="status"></p></main></div><dialog aria-labelledby="dialog-title" class="glass-hud rounded-2xl p-5 text-slate-100" id="detail-dialog"><h2 class="text-lg font-semibold" id="dialog-title"></h2><p class="mt-2 text-sm text-slate-300" id="dialog-copy"></p><form class="mt-4" method="dialog"><button autofocus="" class="glass-pill rounded-xl px-4 text-sm">Close</button></form></dialog><script>
(() => {
  'use strict';
  const $ = (q, scope = document) => scope.querySelector(q);
  const $$ = (q, scope = document) => [...scope.querySelectorAll(q)];
  const clamp = (n, lo, hi) => Math.min(hi, Math.max(lo, n));
  const map = $('#map-view'), stage = $('#map-stage'), image = $('.map-image'), vectors = $('.map-vectors');
  const trigger = $('#field-trigger'), field = $('#field-detail'), viewPanel = $('#view-panel');
  const mobile = matchMedia('(max-width: 767px)'), tablet = matchMedia('(min-width: 768px) and (max-width: 1279px)');
  const nav = $('#primary-links'), menu = $('#menu-toggle'), drawer = $('#drawer-toggle'), analytics = $('#analytics');
  const mapActions = Object.fromEntries($$('[data-map-action]').map(b => [b.dataset.mapAction, b]));
  let zoom = 1, angle = 0, panX = 0, panY = 0, drag = null;
  
  const parcel = vectors.querySelector('polygon').getAttribute('points').trim().split(/\s+/).map(p => p.split(',').map(Number));
  const centroid = (() => {
    let sum = 0, x = 0, y = 0;
    parcel.forEach(([a,b], i) => {
      const [c,d] = parcel[(i + 1) % parcel.length], cross = a*d - c*b;
      sum += cross; x += (a+c)*cross; y += (b+d)*cross;
    });
    return [x/(3*sum), y/(3*sum)];
  })();

  function renderMap() {
    const w = map.clientWidth, h = map.clientHeight;
    if (!w || !h) return;
    const iw = image.naturalWidth || 1920, ih = image.naturalHeight || 1080;
    const originalCover = Math.max(1920/iw, 1080/ih)*1.02;
    const rw = iw*originalCover, rh = ih*originalCover, rx = (1920-rw)/2, ry = (1080-rh)/2;
    vectors.setAttribute('viewBox', `${rx} ${ry} ${rw} ${rh}`);
    const ax = (centroid[0]-rx)/rw, ay = (centroid[1]-ry)/rh;
    const rad = angle*Math.PI/180, cos = Math.cos(rad), sin = Math.sin(rad);
    const cover = Math.max((w*Math.abs(cos)+h*Math.abs(sin))/iw, (w*Math.abs(sin)+h*Math.abs(cos))/ih);
    const bw = cover*iw, bh = cover*ih, zw = bw*zoom, zh = bh*zoom;
    const limX = (zw - w*Math.abs(cos) - h*Math.abs(sin))/2;
    const limY = (zh - w*Math.abs(sin) - h*Math.abs(cos))/2;
    const focusX = mobile.matches ? (.5-ax)*zw : 0;
    const focusY = mobile.matches ? (.5-ay)*zh : 0;
    const px = clamp(focusX + panX, -Math.max(0,limX), Math.max(0,limX));
    const py = clamp(focusY + panY, -Math.max(0,limY), Math.max(0,limY));
    const x = px*cos - py*sin, y = px*sin + py*cos;
    stage.style.width = `${bw}px`; stage.style.height = `${bh}px`;
    stage.style.left = `${(w-bw)/2}px`; stage.style.top = `${(h-bh)/2}px`;
    stage.style.transform = `translate(${x}px, ${y}px) rotate(${angle}deg) scale(${zoom})`;
    stage.style.setProperty('--counter-angle', `${-angle}deg`); stage.style.setProperty('--counter-scale', 1/zoom);
    trigger.style.left = `${ax*100}%`; trigger.style.top = `${ay*100}%`;
    mapActions.in.setAttribute('aria-disabled', String(zoom >= 3));
    mapActions.out.setAttribute('aria-disabled', String(zoom <= 1));
  }
  new ResizeObserver(renderMap).observe(map);
  image.addEventListener('load', renderMap);
  image.addEventListener('error', () => { image.hidden = true; $('#map-caption').textContent = 'Image unavailable · Demo field outline'; });
  if (image.complete && !image.naturalWidth) image.hidden = true;
  function announceMap(message) { $('#map-status').textContent = message; }
  function moveMap(action) {
    if (action === 'in' || action === 'out') zoom = clamp(zoom + (action === 'in' ? .25 : -.25), 1, 3);
    if (action === 'out' && zoom === 1) panX = panY = 0;
    if (action === 'rotate') angle = (angle+15)%360;
    if (action === 'compass') angle = 0;
    if (action === 'fit') { zoom = 1; panX = panY = 0; angle = 0; }
    renderMap();
    announceMap(action === 'fit' ? 'Map reset to fit bounds.' : action === 'compass' ? 'Map oriented north.' : `Map zoom ${zoom*100} percent, rotation ${angle} degrees.`);
  }
  for (const [action,b] of Object.entries(mapActions)) b.addEventListener('click', () => {
    if (b.getAttribute('aria-disabled') !== 'true') moveMap(action);
  });
  map.addEventListener('pointerdown', e => {
    if (zoom === 1 || e.button !== 0 || e.pointerType === 'touch' || e.target.closest('button')) return;
    drag = { id:e.pointerId, x:e.clientX, y:e.clientY };
    stage.classList.add('dragging'); map.setPointerCapture(e.pointerId);
  });
  map.addEventListener('pointermove', e => {
    if (!drag || drag.id !== e.pointerId) return;
    const x = e.clientX-drag.x, y = e.clientY-drag.y, a = angle*Math.PI/180;
    panX = clamp(panX + x*Math.cos(a) + y*Math.sin(a), -stage.clientWidth, stage.clientWidth);
    panY = clamp(panY - x*Math.sin(a) + y*Math.cos(a), -stage.clientHeight, stage.clientHeight);
    drag.x = e.clientX; drag.y = e.clientY; renderMap();
  });
  map.addEventListener('lostpointercapture', () => { drag = null; stage.classList.remove('dragging'); });
  
  const layers = { satellite:['RGB High-Res','Satellite imagery · Demo data'], ndvi:['Biomass preview','NDVI · Simulated color preview'], soil:['Moisture preview','Soil · Simulated color preview'] };
  $$('[data-layer-choice]').forEach(b => b.addEventListener('click', () => {
    const key = b.dataset.layerChoice;
    map.dataset.layer = key;
    $$('[data-layer-choice]').forEach(item => {
      const active = item === b;
      item.setAttribute('aria-pressed', String(active));
      $('.layer-description',item).textContent = active ? layers[key][0] : ({satellite:'RGB High-Res',ndvi:'Biomass Index',soil:'Moisture Profile'})[item.dataset.layerChoice];
    });
    $('#map-caption').textContent = layers[key][1] + (image.hidden ? ' · Image unavailable' : '');
    announceMap($('#map-caption').textContent);
  }));

  // Drone Layer Toggle button
  const droneToggleBtn = $('#drone-layer-toggle');
  const droneGroup = $('#drone-path-group');
  if (droneToggleBtn && droneGroup) {
    droneToggleBtn.addEventListener('click', () => {
      const isVisible = droneGroup.style.display !== 'none';
      droneGroup.style.display = isVisible ? 'none' : 'block';
      droneToggleBtn.setAttribute('aria-pressed', String(!isVisible));
      droneToggleBtn.querySelector('.layer-description').textContent = isVisible ? 'Hidden' : 'Flight Path';
      announceMap(isVisible ? 'Drone layer hidden' : 'Drone flight simulation visible');
    });
  }

  function fieldOpen(open, focus = false) {
    field.hidden = !open; trigger.setAttribute('aria-expanded', String(open));
    if (focus) (open ? $('#field-close') : trigger).focus();
  }
  trigger.addEventListener('click', () => fieldOpen(field.hidden, true));
  $('#field-close').addEventListener('click', () => fieldOpen(false,true));
  function menuOpen(open) { nav.classList.toggle('is-open',open); menu.setAttribute('aria-expanded',String(open)); }
  function drawerOpen(open) { analytics.classList.toggle('is-open',open); drawer.setAttribute('aria-expanded',String(open)); }
  menu.addEventListener('click', () => menuOpen(!nav.classList.contains('is-open')));
  drawer.addEventListener('click', () => drawerOpen(!analytics.classList.contains('is-open')));
  mobile.addEventListener('change', () => { menuOpen(false); renderMap(); });
  tablet.addEventListener('change', () => drawerOpen(false));
  
  const views = {
    map:['Field Management','Field health, fleet telemetry and operations · Live Simulation Active',''],
    fields:['Fields','Parcel monitoring · Demo','North Field: 92% crop health. Use the highlighted map marker to open field details.'],
    analytics:['Analytics','Crop health trends and stress zones · Demo','Use the Health Trend period selector to compare 24-hour, 7-day and 30-day sample readings.'],
    reports:['Reports','Irrigation and harvest summaries · Demo','The operations cards below show irrigation offsets and sample harvest volume.'],
    farmers:['Farmers','Farm team overview · Demo','This prototype has no connected team directory.']
  };
  $$('[data-view]').forEach(b => b.addEventListener('click', () => {
    const wasMobileMenu = mobile.matches && nav.classList.contains('is-open');
    $$('[data-view]').forEach(item => item === b ? item.setAttribute('aria-current','page') : item.removeAttribute('aria-current'));
    const key = b.dataset.view, [title, subtitle, copy] = views[key];
    $('#page-title').textContent = title; $('#page-subtitle').textContent = subtitle;
    $('#view-title').textContent = title + ' overview'; $('#view-copy').textContent = copy; viewPanel.hidden = key === 'map';
    fieldOpen(false); if (tablet.matches) drawerOpen(key === 'analytics'); menuOpen(false);
    if (wasMobileMenu) menu.focus();
  }));

  const health = $('[data-purpose=crop-health-card]');
  function renderGauge() {
    const p = clamp(Number(health.dataset.value) || 0,0,100);
    $('#gauge-fill').setAttribute('stroke-dasharray', `${p} 100`);
    $('#gauge-fill').style.visibility = p ? 'visible' : 'hidden';
    $('#gauge-value').textContent = p; $('#crop-gauge').setAttribute('aria-label', `Crop health: ${p} percent`);
  }
  new MutationObserver(renderGauge).observe(health,{attributes:true,attributeFilter:['data-value']}); renderGauge();
  
  const ranges = {
    '24h':{ name:'24-hour', y:[56,53,49,38,30,39,35], labels:['00:00','04:00','08:00','12:00','16:00','20:00','24:00'], peak:'16:00' },
    '7d':{ name:'seven-day', y:[55,53,22,44,35,48,42], labels:['Mon','Tue','Wed','Thu','Fri','Sat','Sun'], peak:'Wednesday' },
    '30d':{ name:'30-day', y:[62,56,59,43,48,34,26], labels:['Day 1','5','10','15','20','25','30'], peak:'day 30' }
  };
  function renderTrend() {
    const d = ranges[$('#trend-range').value], step = 260/(d.y.length-1);
    const path = d.y.map((y,i) => `${i?'L':'M'} ${i*step},${y}`).join(' ');
    $('#trend-line').setAttribute('d',path); $('#trend-area').setAttribute('d',path+' L 260,78 L 0,78 Z');
    const p = d.y.indexOf(Math.min(...d.y));
    $('#trend-peak').setAttribute('cx',p*step); $('#trend-peak').setAttribute('cy',d.y[p]);
    $('#trend-chart').setAttribute('aria-label', `Sample ${d.name} crop health trend. Highest point: ${d.peak}.`);
    $('#trend-labels').replaceChildren(...d.labels.map((label,i) => {
      const span = document.createElement('span'); span.textContent = label;
      if (i === p) span.className = 'text-lime-400 font-bold'; return span;
    }));
  }
  $('#trend-range').addEventListener('change',renderTrend); renderTrend();

  // Dialog handling
  const dialog = $('#detail-dialog');
  const detailCopy = {
    notifications:['Notifications','Alert history: Zone B irrigation variance exceeded threshold at 09:41.'],
    health:['Crop health',() => `The dashboard shows ${$('#gauge-value').textContent}% crop health over a monitored farm area of 248 ha.`],
    insights:['AI Insights','Soil moisture optimal across Zone A; Zone B requires schedule compensation to prevent root stress.'],
    tractor:['Tractor T-04 Telemetry',() => `Current telemetry: Speed ${$('#tractor-speed').textContent}, Fuel ${$('#tractor-fuel').textContent}, Area ${$('#tractor-area').textContent}. Autonomous GPS path tracking active.`],
    sprayer:['Sprayer S-01 Telemetry',() => `Current telemetry: Speed ${$('#sprayer-speed').textContent}, Tank ${$('#sprayer-tank').textContent}, Area ${$('#sprayer-area').textContent}. Variable-rate spraying active.`],
    irrigation:['Irrigation Offset Alert System','Real-time flow sensors evaluate deviation across all zones. If offset exceeds ±3.0 minutes, high-priority alert banners are triggered.'],
    yield:['Live Yield Volume Telemetry',() => `Total harvested today: ${$('#yield-volume-val').textContent} kg. Current run rate: ${$('#yield-runrate').textContent}.`]
  };
  function showDetails(key) {
    const item = detailCopy[key];
    if (!item) return;
    const [title,copy] = item;
    $('#dialog-title').textContent = title;
    $('#dialog-copy').textContent = typeof copy === 'function' ? copy() : copy;
    dialog.showModal();
  }
  $$('[data-dialog]').forEach(b => b.addEventListener('click', () => showDetails(b.dataset.dialog)));

  // Search feature
  const search = $('#dashboard-search'), results = $('#search-results');
  const searchable = [['North Field','field'],['Tractor T-04','tractor'],['Sprayer S-01','sprayer'],['Irrigation Station','irrigation'],['Yield Analysis','yield']];
  search.addEventListener('input', () => {
    const term = search.value.trim().toLowerCase(); results.replaceChildren(); results.hidden = !term;
    if (!term) return;
    for (const [name,key] of searchable.filter(([name]) => name.toLowerCase().includes(term))) {
      const b = document.createElement('button'); b.type = 'button'; b.textContent = name;
      b.addEventListener('click',() => { results.hidden = true; search.focus(); key === 'field' ? fieldOpen(true,true) : showDetails(key); }); results.append(b);
    }
    if (!results.childElementCount) results.textContent = 'No matching parcels or equipment.';
  });
  search.addEventListener('focus',() => { if (search.value.trim() && results.textContent.trim()) results.hidden = false; });
  search.parentElement.addEventListener('focusout',e => { if (!search.parentElement.contains(e.relatedTarget)) results.hidden = true; });

  // Yield Histogram Interactive Tooltip Connection
  const tooltip = $('#histogram-tooltip');
  const tooltipText = $('#tooltip-text');
  const histogramContainer = $('#yield-histogram-container');
  $$('.yield-bar').forEach(bar => {
    bar.addEventListener('mouseenter', e => {
      const val = bar.dataset.val;
      const time = bar.dataset.time;
      tooltipText.textContent = `${time} · ${val} tn/hr`;
      const rect = bar.getBoundingClientRect();
      const parentRect = histogramContainer.getBoundingClientRect();
      const leftOffset = rect.left - parentRect.left + (rect.width / 2);
      tooltip.style.left = `${leftOffset}px`;
      tooltip.style.opacity = '1';
    });
    bar.addEventListener('mouseleave', () => {
      tooltip.style.opacity = '0';
    });
    bar.addEventListener('click', () => {
      $('#yield-runrate').textContent = `+${bar.dataset.val} tn/hr`;
    });
  });

  // --- LIVE TELEMETRY & SIMULATION ENGINE ---
  let isSimulating = true;
  const toggleBtn = $('#telemetry-toggle-btn');
  const indicator = $('#telemetry-indicator');
  const btnText = $('#telemetry-btn-text');

  toggleBtn.addEventListener('click', () => {
    isSimulating = !isSimulating;
    if (isSimulating) {
      indicator.className = 'w-2 h-2 rounded-full bg-lime-400 animate-pulse';
      btnText.textContent = 'Simulation: Live';
      toggleBtn.classList.remove('bg-rose-500/20','border-rose-400/40','text-rose-300');
      toggleBtn.classList.add('bg-lime-500/15','border-lime-400/40','text-lime-300');
      announceMap('Live telemetry simulation resumed');
    } else {
      indicator.className = 'w-2 h-2 rounded-full bg-amber-400';
      btnText.textContent = 'Simulation: Paused';
      toggleBtn.classList.remove('bg-lime-500/15','border-lime-400/40','text-lime-300');
      toggleBtn.classList.add('bg-rose-500/20','border-rose-400/40','text-rose-300');
      announceMap('Live telemetry simulation paused');
    }
  });

  // GPS Waypoint movement loops
  const droneWaypoints = [
    [980, 370], [1490, 375], [1490, 440], [970, 440], 
    [970, 510], [1480, 510], [1480, 580], [1020, 580], [1020, 650], [1450, 650]
  ];
  let droneLeg = 0, droneT = 0;
  const droneMarker = $('#drone-marker');

  const tractorWaypoints = [
    [960, 410], [1080, 410], [1080, 620], [1150, 620], [1150, 430], [1220, 430], [1220, 620]
  ];
  let tractorLeg = 0, tractorT = 0;
  const tractorMarker = $('#tractor-marker');

  const sprayerWaypoints = [
    [1320, 370], [1320, 680], [1400, 680], [1400, 370], [1470, 370], [1470, 660]
  ];
  let sprayerLeg = 0, sprayerT = 0;
  const sprayerMarker = $('#sprayer-marker');

  // Irrigation alert elements
  const alertBanner = $('#irrigation-alert-banner');
  const alertText = $('#alert-banner-text');
  const alertDismiss = $('#alert-dismiss-btn');
  let alertDismissedManually = false;

  alertDismiss.addEventListener('click', () => {
    alertBanner.classList.add('hidden');
    alertDismissedManually = true;
  });

  // Clickable markers show dialogs
  tractorMarker.addEventListener('click', () => showDetails('tractor'));
  sprayerMarker.addEventListener('click', () => showDetails('sprayer'));
  $('#drone-marker').addEventListener('click', () => {
    $('#dialog-title').textContent = 'Drone Scan-03 Flight Status';
    $('#dialog-copy').textContent = 'Autonomous multi-spectral crop scan at 65m altitude. Battery: 78%. Coverage: 18.5 ha completed.';
    dialog.showModal();
  });

  // Main animation frame for smooth vehicle motions & telemetry updates
  let lastTick = performance.now();
  let telemetryCounter = 0;
  let harvestVolume = 142580;
  let tractorSpeedVal = 8;
  let sprayerSpeedVal = 6;
  let tractorFuelVal = 64;
  let sprayerTankVal = 41;
  let tractorAreaVal = 12.4;
  let sprayerAreaVal = 6.8;

  function interpolate(p1, p2, t) {
    return [p1[0] + (p2[0] - p1[0]) * t, p1[1] + (p2[1] - p1[1]) * t];
  }

  function tickSimulation(now) {
    requestAnimationFrame(tickSimulation);
    if (!isSimulating) return;
    const delta = (now - lastTick) / 1000;
    lastTick = now;

    // Move Drone
    droneT += delta * 0.35;
    if (droneT >= 1) {
      droneT = 0;
      droneLeg = (droneLeg + 1) % (droneWaypoints.length - 1);
    }
    const dPos = interpolate(droneWaypoints[droneLeg], droneWaypoints[droneLeg + 1], droneT);
    droneMarker.setAttribute('transform', `translate(${dPos[0]}, ${dPos[1]})`);

    // Move Tractor T-04
    tractorT += delta * 0.12;
    if (tractorT >= 1) {
      tractorT = 0;
      tractorLeg = (tractorLeg + 1) % (tractorWaypoints.length - 1);
    }
    const tPos = interpolate(tractorWaypoints[tractorLeg], tractorWaypoints[tractorLeg + 1], tractorT);
    tractorMarker.setAttribute('transform', `translate(${tPos[0]}, ${tPos[1]})`);

    // Move Sprayer S-01
    sprayerT += delta * 0.14;
    if (sprayerT >= 1) {
      sprayerT = 0;
      sprayerLeg = (sprayerLeg + 1) % (sprayerWaypoints.length - 1);
    }
    const sPos = interpolate(sprayerWaypoints[sprayerLeg], sprayerWaypoints[sprayerLeg + 1], sprayerT);
    sprayerMarker.setAttribute('transform', `translate(${sPos[0]}, ${sPos[1]})`);

    // Telemetry increments every ~1.5s
    telemetryCounter += delta;
    if (telemetryCounter >= 1.6) {
      telemetryCounter = 0;

      // Update Tractor telemetry
      tractorSpeedVal = clamp(tractorSpeedVal + (Math.random() * 0.8 - 0.4), 6.5, 9.5);
      tractorAreaVal += 0.02;
      tractorFuelVal = Math.max(10, tractorFuelVal - 0.03);
      $('#tractor-speed').textContent = `${tractorSpeedVal.toFixed(1)} km/h`;
      $('#tractor-area').textContent = `${tractorAreaVal.toFixed(1)} ha`;
      $('#tractor-fuel').textContent = `${Math.round(tractorFuelVal)}%`;

      // Update Sprayer telemetry
      sprayerSpeedVal = clamp(sprayerSpeedVal + (Math.random() * 0.6 - 0.3), 5.0, 7.5);
      sprayerAreaVal += 0.015;
      sprayerTankVal = Math.max(5, sprayerTankVal - 0.05);
      $('#sprayer-speed').textContent = `${sprayerSpeedVal.toFixed(1)} km/h`;
      $('#sprayer-area').textContent = `${sprayerAreaVal.toFixed(1)} ha`;
      $('#sprayer-tank').textContent = `${Math.round(sprayerTankVal)}%`;

      // Update Live Harvest Yield
      harvestVolume += Math.floor(Math.random() * 12 + 6);
      $('#yield-volume-val').textContent = harvestVolume.toLocaleString();

      // Fluctuate Irrigation variance & trigger Alert Banner when exceeding ±3.0 min
      const jitter = (Math.random() * 0.6 - 0.28);
      const b4Offset = -2.5 + jitter;
      $('#irrig-b4').textContent = `${b4Offset >= 0 ? '+' : ''}${b4Offset.toFixed(1)}m`;

      const globalVariance = Math.abs(b4Offset);
      $('#irrigation-global-variance').innerHTML = `± ${globalVariance.toFixed(1)} <span class="text-[11px] text-slate-300 font-normal">min</span>`;

      if (globalVariance > 3.0) {
        $('#irrig-b4').className = 'text-rose-400 font-bold animate-pulse';
        $('#pump-status').textContent = 'Variance Alert';
        $('#pump-status').className = 'text-rose-400 font-bold';
        if (!alertDismissedManually) {
          alertText.textContent = `Warning: Irrigation variance exceeded ±3.0 min threshold in Zone B (Current: ${b4Offset.toFixed(1)} min). Flow readjustment suggested.`;
          alertBanner.classList.remove('hidden');
        }
      } else {
        $('#irrig-b4').className = 'text-rose-400 font-semibold';
        $('#pump-status').textContent = 'Calibrated';
        $('#pump-status').className = 'text-emerald-400 font-medium';
        if (!alertDismissedManually && globalVariance <= 2.8) {
          alertBanner.classList.add('hidden');
        }
      }
    }
  }
  requestAnimationFrame(tickSimulation);

  // Keep times updated
  const sampleStart = Date.now(), staleAfter = 15*60_000;
  const fleetTimes = $$('time[data-offset-min]').map(t => ({ node:t, reading:sampleStart - Number(t.dataset.offsetMin)*60_000 }));
  const format = new Intl.DateTimeFormat('hu-HU',{day:'2-digit',month:'2-digit',year:'numeric',hour:'2-digit',minute:'2-digit',hour12:false});
  function renderTimes() {
    const now = Date.now();
    for (const {node,reading} of fleetTimes) {
      const date = new Date(reading), parts = Object.fromEntries(format.formatToParts(date).map(p => [p.type,p.value]));
      const label = `${parts.day}.${parts.month}.${parts.year}, ${parts.hour}:${parts.minute}`;
      node.dateTime = date.toISOString(); if (node.textContent !== label) node.textContent = label;
      const status = $('[data-fleet-status]',node.closest('article')), text = $('[data-status-text]',status);
      const stale = now-reading > staleAfter; status.classList.toggle('is-stale',stale);
      if (stale && text.textContent !== 'Stale') text.textContent = 'Stale';
    }
  }
  renderTimes(); setInterval(renderTimes,30_000);

  document.addEventListener('keydown', e => {
    if (e.key !== 'Escape' || dialog.open) return;
    if (!results.hidden) { results.hidden = true; search.focus(); }
    else if (nav.classList.contains('is-open')) { menuOpen(false); menu.focus(); }
    else if (!field.hidden) fieldOpen(false,true);
    else if (analytics.classList.contains('is-open')) { drawerOpen(false); drawer.focus(); }
  });
  renderMap();
})();
</script></body></html>
