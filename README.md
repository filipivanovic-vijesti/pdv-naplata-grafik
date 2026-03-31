[pdv-infographic.html](https://github.com/user-attachments/files/26375817/pdv-infographic.html)
<!DOCTYPE html>
<html lang="sr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:ital,wght@0,400;0,500;0,600;0,700;1,400&family=Source+Serif+4:ital,opsz,wght@0,8..60,400;0,8..60,700;0,8..60,900;1,8..60,400&display=swap" rel="stylesheet">
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  
  body {
    font-family: 'DM Sans', sans-serif;
    background: #FAFAFA;
    color: #1A1A2E;
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
  }

  .container {
    max-width: 680px;
    margin: 0 auto;
    padding: 0 20px;
  }

  /* ===== HERO ===== */
  .hero {
    background: linear-gradient(165deg, #0F0F23 0%, #1A1A3E 50%, #2D1B4E 100%);
    padding: 48px 20px 52px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute;
    top: -50%;
    left: -50%;
    width: 200%;
    height: 200%;
    background: radial-gradient(circle at 30% 70%, rgba(218,165,32,0.06) 0%, transparent 50%),
                radial-gradient(circle at 70% 30%, rgba(255,255,255,0.03) 0%, transparent 40%);
    pointer-events: none;
  }
  .hero-label {
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: #DAA520;
    margin-bottom: 20px;
    position: relative;
  }
  .hero h1 {
    font-family: 'Source Serif 4', serif;
    font-size: clamp(28px, 6vw, 40px);
    font-weight: 900;
    color: #FFFFFF;
    line-height: 1.15;
    margin-bottom: 12px;
    position: relative;
  }
  .hero h1 span {
    color: #DAA520;
  }
  .hero-sub {
    font-size: 15px;
    color: rgba(255,255,255,0.55);
    max-width: 480px;
    margin: 0 auto 28px;
    position: relative;
  }
  .hero-total {
    display: inline-flex;
    align-items: baseline;
    gap: 6px;
    position: relative;
  }
  .hero-total .num {
    font-family: 'Source Serif 4', serif;
    font-size: clamp(42px, 10vw, 64px);
    font-weight: 900;
    color: #FFFFFF;
    letter-spacing: -2px;
  }
  .hero-total .unit {
    font-size: 18px;
    font-weight: 600;
    color: rgba(255,255,255,0.5);
  }
  .hero-note {
    font-size: 12px;
    color: rgba(255,255,255,0.35);
    margin-top: 8px;
    position: relative;
  }

  /* ===== SECTION COMMON ===== */
  section {
    padding: 40px 0;
  }
  .section-divider {
    width: 40px;
    height: 3px;
    background: #DAA520;
    margin-bottom: 16px;
  }
  .section-title {
    font-family: 'Source Serif 4', serif;
    font-size: clamp(22px, 5vw, 28px);
    font-weight: 700;
    color: #1A1A2E;
    margin-bottom: 8px;
    line-height: 1.25;
  }
  .section-desc {
    font-size: 14px;
    color: #666;
    margin-bottom: 28px;
    max-width: 560px;
  }

  /* ===== PODGORICA DOMINANCE ===== */
  .pg-section {
    background: #FFFFFF;
    border-top: 1px solid #E8E8E8;
    border-bottom: 1px solid #E8E8E8;
  }
  .pg-visual {
    display: flex;
    align-items: center;
    gap: 28px;
    margin-bottom: 20px;
    flex-wrap: wrap;
  }
  .pg-circle-wrap {
    position: relative;
    width: 160px;
    height: 160px;
    flex-shrink: 0;
  }
  .pg-circle-wrap svg {
    width: 100%;
    height: 100%;
    transform: rotate(-90deg);
  }
  .pg-circle-wrap .track {
    fill: none;
    stroke: #E8E8E8;
    stroke-width: 14;
  }
  .pg-circle-wrap .fill {
    fill: none;
    stroke: #DAA520;
    stroke-width: 14;
    stroke-linecap: round;
    stroke-dasharray: 408;
    stroke-dashoffset: 179.5;
    animation: fillIn 1.5s ease-out forwards;
  }
  @keyframes fillIn {
    from { stroke-dashoffset: 408; }
    to { stroke-dashoffset: 179.5; }
  }
  .pg-center-label {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
  }
  .pg-center-label .pct {
    font-family: 'Source Serif 4', serif;
    font-size: 36px;
    font-weight: 900;
    color: #1A1A2E;
    line-height: 1;
  }
  .pg-center-label .pct-label {
    font-size: 10px;
    color: #999;
    text-transform: uppercase;
    letter-spacing: 1px;
  }
  .pg-stats {
    flex: 1;
    min-width: 200px;
  }
  .pg-stat-row {
    display: flex;
    justify-content: space-between;
    padding: 10px 0;
    border-bottom: 1px solid #F0F0F0;
    font-size: 14px;
  }
  .pg-stat-row:last-child { border-bottom: none; }
  .pg-stat-row .label { color: #888; }
  .pg-stat-row .val { font-weight: 700; color: #1A1A2E; }
  .pg-stat-row .val.gold { color: #B8860B; }

  /* ===== BAR CHART ===== */
  .bar-chart {
    margin-top: 8px;
  }
  .bar-row {
    display: flex;
    align-items: center;
    margin-bottom: 6px;
    font-size: 13px;
  }
  .bar-label {
    width: 110px;
    flex-shrink: 0;
    text-align: right;
    padding-right: 12px;
    color: #555;
    font-weight: 500;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }
  .bar-track {
    flex: 1;
    height: 26px;
    background: #F0F0F0;
    border-radius: 4px;
    position: relative;
    overflow: hidden;
  }
  .bar-fill {
    height: 100%;
    border-radius: 4px;
    transition: width 1s ease-out;
    display: flex;
    align-items: center;
    padding-left: 8px;
    min-width: 2px;
  }
  .bar-fill.tier1 { background: linear-gradient(90deg, #DAA520, #C4941C); }
  .bar-fill.tier2 { background: linear-gradient(90deg, #3A6B8C, #2D5470); }
  .bar-fill.tier3 { background: linear-gradient(90deg, #7A8B99, #6B7C8A); }
  .bar-fill.tier4 { background: linear-gradient(90deg, #B0B8C0, #A0A8B0); }
  .bar-amount {
    font-size: 11px;
    font-weight: 600;
    color: #FFFFFF;
    white-space: nowrap;
  }
  .bar-amount.outside {
    color: #888;
    position: absolute;
    left: calc(var(--bar-w) + 8px);
    top: 50%;
    transform: translateY(-50%);
    font-weight: 500;
  }

  .bar-row.highlight .bar-label { color: #B8860B; font-weight: 700; }

  /* ===== NORTH SECTION ===== */
  .north-section {
    background: #0F0F23;
    padding: 40px 20px;
    color: #FFFFFF;
  }
  .north-section .section-divider { background: #DAA520; }
  .north-section .section-title { color: #FFFFFF; }
  .north-section .section-desc { color: rgba(255,255,255,0.5); }

  .north-compare {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
    margin-bottom: 24px;
  }
  .north-card {
    background: rgba(255,255,255,0.06);
    border-radius: 10px;
    padding: 20px;
    text-align: center;
    border: 1px solid rgba(255,255,255,0.08);
  }
  .north-card .nc-num {
    font-family: 'Source Serif 4', serif;
    font-size: 28px;
    font-weight: 900;
    margin-bottom: 4px;
  }
  .north-card .nc-pct {
    font-size: 13px;
    color: rgba(255,255,255,0.4);
    margin-bottom: 8px;
  }
  .north-card .nc-label {
    font-size: 12px;
    color: rgba(255,255,255,0.55);
    line-height: 1.3;
  }
  .north-card.south .nc-num { color: #DAA520; }
  .north-card.north .nc-num { color: #5BA4CF; }

  .north-bar-wrap {
    height: 28px;
    display: flex;
    border-radius: 6px;
    overflow: hidden;
    margin-top: 16px;
  }
  .north-bar-seg {
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 11px;
    font-weight: 600;
  }
  .north-bar-seg.south-seg { background: #DAA520; color: #000; }
  .north-bar-seg.north-seg { background: #5BA4CF; color: #000; }

  /* ===== SPOTLIGHT: GUSINJE & PETNJICA ===== */
  .spotlight {
    background: #FFF;
    border-top: 1px solid #E8E8E8;
    border-bottom: 1px solid #E8E8E8;
  }
  .spot-cards {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 14px;
    margin-bottom: 24px;
  }
  @media (max-width: 480px) {
    .spot-cards { grid-template-columns: 1fr; }
    .north-compare { grid-template-columns: 1fr; }
  }
  .spot-card {
    border: 2px solid #E74C3C;
    border-radius: 10px;
    padding: 20px;
    text-align: center;
    background: #FFF9F8;
  }
  .spot-card .sc-name {
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: #E74C3C;
    margin-bottom: 10px;
  }
  .spot-card .sc-num {
    font-family: 'Source Serif 4', serif;
    font-size: 30px;
    font-weight: 900;
    color: #E74C3C;
    margin-bottom: 4px;
  }
  .spot-card .sc-label {
    font-size: 12px;
    color: #999;
  }
  .spot-card .sc-pop {
    margin-top: 14px;
    padding-top: 14px;
    border-top: 1px solid #F0E0DD;
    font-size: 13px;
    color: #666;
  }
  .spot-card .sc-pop strong { color: #1A1A2E; }

  .compare-box {
    background: #F5F5F0;
    border-radius: 10px;
    padding: 20px;
    margin-top: 16px;
  }
  .compare-box .cb-title {
    font-size: 12px;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 1.5px;
    color: #999;
    margin-bottom: 14px;
  }
  .compare-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 8px 0;
    border-bottom: 1px solid rgba(0,0,0,0.06);
    font-size: 14px;
  }
  .compare-row:last-child { border-bottom: none; }
  .compare-row .cr-name { color: #555; }
  .compare-row .cr-pop { color: #999; font-size: 12px; }
  .compare-row .cr-val { font-weight: 700; color: #1A1A2E; }

  /* ===== EGALIZACIONI FOND ===== */
  .fund-section {
    padding-bottom: 20px;
  }
  .fund-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 13px;
    margin-top: 8px;
  }
  .fund-table thead th {
    text-align: left;
    font-size: 10px;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 1px;
    color: #999;
    padding: 8px 6px;
    border-bottom: 2px solid #1A1A2E;
  }
  .fund-table thead th:not(:first-child) { text-align: right; }
  .fund-table tbody td {
    padding: 10px 6px;
    border-bottom: 1px solid #F0F0F0;
    vertical-align: middle;
  }
  .fund-table tbody td:not(:first-child) {
    text-align: right;
    font-variant-numeric: tabular-nums;
  }
  .fund-table .name-cell { font-weight: 600; color: #1A1A2E; }
  .fund-table .pdv-cell { color: #3A6B8C; font-weight: 500; }
  .fund-table .fund-cell { color: #B8860B; font-weight: 500; }
  .fund-table .ratio-cell { font-weight: 700; }
  .fund-table .ratio-cell.negative { color: #E74C3C; }
  .fund-table .ratio-cell.positive { color: #27AE60; }
  .fund-table tr.highlight-row { background: #FFF9F8; }
  .fund-table tr.highlight-row .name-cell { color: #E74C3C; }

  /* ===== FOOTER ===== */
  .footer {
    background: #F0F0F0;
    padding: 24px 20px;
    text-align: center;
  }
  .footer p {
    font-size: 11px;
    color: #999;
    line-height: 1.5;
  }
  .footer .src {
    font-weight: 600;
    color: #777;
  }

  /* ===== CALLOUT ===== */
  .callout {
    background: #F9F6EE;
    border-left: 4px solid #DAA520;
    padding: 16px 20px;
    margin: 20px 0;
    border-radius: 0 8px 8px 0;
  }
  .callout p {
    font-size: 14px;
    color: #555;
    line-height: 1.55;
  }
  .callout strong {
    color: #1A1A2E;
  }

  /* ===== ANIMATIONS ===== */
  .fade-in {
    opacity: 0;
    transform: translateY(16px);
    transition: opacity 0.6s ease, transform 0.6s ease;
  }
  .fade-in.visible {
    opacity: 1;
    transform: translateY(0);
  }
</style>
</head>
<body>

<!-- HERO -->
<div class="hero">
  <div class="container">
    <div class="hero-label">Analiza podataka</div>
    <h1>Koliko svaka opština<br>doprinosi budžetu <span>kroz PDV</span></h1>
    <p class="hero-sub">Naplata poreza na dodatu vrijednost po opštinama u Crnoj Gori za 2024. godinu</p>
    <div class="hero-total">
      <span class="num">479,5</span>
      <span class="unit">mil. €</span>
    </div>
    <p class="hero-note">Ukupna naplata PDV-a u domaćem prometu</p>
  </div>
</div>

<!-- PODGORICA DOMINANCE -->
<section class="pg-section">
  <div class="container" style="padding-top: 40px; padding-bottom: 40px;">
    <div class="fade-in">
      <div class="section-divider"></div>
      <h2 class="section-title">Podgorica — više od pola ukupnog PDV-a</h2>
      <p class="section-desc">Sa 28% ukupnog stanovništva, glavni grad generiše 56% naplate PDV-a u cijeloj državi.</p>
    </div>
    <div class="pg-visual fade-in">
      <div class="pg-circle-wrap">
        <svg viewBox="0 0 160 160">
          <circle class="track" cx="80" cy="80" r="65"/>
          <circle class="fill" cx="80" cy="80" r="65"/>
        </svg>
        <div class="pg-center-label">
          <div class="pct">56%</div>
          <div class="pct-label">PDV-a</div>
        </div>
      </div>
      <div class="pg-stats">
        <div class="pg-stat-row">
          <span class="label">Naplaćeno PDV-a</span>
          <span class="val gold">271 mil. €</span>
        </div>
        <div class="pg-stat-row">
          <span class="label">Stanovništvo</span>
          <span class="val">180.000</span>
        </div>
        <div class="pg-stat-row">
          <span class="label">% stanovništva</span>
          <span class="val">28%</span>
        </div>
        <div class="pg-stat-row">
          <span class="label">PDV po stanovniku</span>
          <span class="val gold">~1.506 €</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- FULL RANKING -->
<section>
  <div class="container">
    <div class="fade-in">
      <div class="section-divider"></div>
      <h2 class="section-title">Rang lista svih opština</h2>
      <p class="section-desc">Prvih sedam opština čini preko 93% ukupne naplate PDV-a u domaćem prometu.</p>
    </div>
    <div class="bar-chart fade-in">

      <div class="bar-row highlight">
        <div class="bar-label">Podgorica</div>
        <div class="bar-track">
          <div class="bar-fill tier1" style="width:100%; --bar-w:100%;">
            <span class="bar-amount">271 mil. €</span>
          </div>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Budva</div>
        <div class="bar-track">
          <div class="bar-fill tier2" style="width:15.3%; --bar-w:15.3%;">
            <span class="bar-amount" style="font-size:10px;">41,5M</span>
          </div>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Nikšić</div>
        <div class="bar-track">
          <div class="bar-fill tier2" style="width:11.4%; --bar-w:11.4%;">
            <span class="bar-amount" style="font-size:10px;">30,8M</span>
          </div>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Herceg Novi</div>
        <div class="bar-track">
          <div class="bar-fill tier2" style="width:9.5%; --bar-w:9.5%;">
          </div>
          <span class="bar-amount outside" style="left:calc(9.5% + 8px);">25,6M</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Tivat</div>
        <div class="bar-track">
          <div class="bar-fill tier2" style="width:9.2%; --bar-w:9.2%;">
          </div>
          <span class="bar-amount outside" style="left:calc(9.2% + 8px);">24,8M</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Kotor</div>
        <div class="bar-track">
          <div class="bar-fill tier3" style="width:7%; --bar-w:7%;">
          </div>
          <span class="bar-amount outside" style="left:calc(7% + 8px);">19M</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Bar</div>
        <div class="bar-track">
          <div class="bar-fill tier3" style="width:6%; --bar-w:6%;">
          </div>
          <span class="bar-amount outside" style="left:calc(6% + 8px);">16,3M</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Pljevlja</div>
        <div class="bar-track">
          <div class="bar-fill tier3" style="width:4.5%; --bar-w:4.5%;">
          </div>
          <span class="bar-amount outside" style="left:calc(4.5% + 8px);">12,2M</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Ulcinj</div>
        <div class="bar-track">
          <div class="bar-fill tier4" style="width:3%; --bar-w:3%;">
          </div>
          <span class="bar-amount outside" style="left:calc(3% + 8px);">8M</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Bijelo Polje</div>
        <div class="bar-track">
          <div class="bar-fill tier4" style="width:2.4%; --bar-w:2.4%;">
          </div>
          <span class="bar-amount outside" style="left:calc(2.4% + 8px);">6,6M</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Danilovgrad</div>
        <div class="bar-track">
          <div class="bar-fill tier4" style="width:2.2%; --bar-w:2.2%;">
          </div>
          <span class="bar-amount outside" style="left:calc(2.2% + 8px);">5,9M</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Cetinje</div>
        <div class="bar-track">
          <div class="bar-fill tier4" style="width:1.3%; --bar-w:1.3%;">
          </div>
          <span class="bar-amount outside" style="left:calc(1.3% + 8px);">3,4M</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Tuzi</div>
        <div class="bar-track">
          <div class="bar-fill tier4" style="width:1.2%; --bar-w:1.2%;">
          </div>
          <span class="bar-amount outside" style="left:calc(1.2% + 8px);">3,3M</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Zeta</div>
        <div class="bar-track">
          <div class="bar-fill tier4" style="width:0.85%; --bar-w:0.85%;">
          </div>
          <span class="bar-amount outside" style="left:calc(0.85% + 8px);">2,3M</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Berane</div>
        <div class="bar-track">
          <div class="bar-fill tier4" style="width:0.72%; --bar-w:0.72%;">
          </div>
          <span class="bar-amount outside" style="left:calc(0.72% + 8px);">1,9M</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Rožaje</div>
        <div class="bar-track">
          <div class="bar-fill tier4" style="width:0.7%; --bar-w:0.7%;">
          </div>
          <span class="bar-amount outside" style="left:calc(0.7% + 8px);">1,9M</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Kolašin</div>
        <div class="bar-track">
          <div class="bar-fill tier4" style="width:0.54%; --bar-w:0.54%;">
          </div>
          <span class="bar-amount outside" style="left:calc(0.54% + 8px);">1,5M</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Andrijevica</div>
        <div class="bar-track">
          <div class="bar-fill tier4" style="width:0.4%; --bar-w:0.4%;">
          </div>
          <span class="bar-amount outside" style="left:calc(0.4% + 8px);">1,1M</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Mojkovac</div>
        <div class="bar-track">
          <div class="bar-fill tier4" style="width:0.3%; --bar-w:0.3%;">
          </div>
          <span class="bar-amount outside" style="left:calc(0.3% + 8px);">829 hilj.</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Žabljak</div>
        <div class="bar-track">
          <div class="bar-fill tier4" style="width:0.17%; --bar-w:0.17%;">
          </div>
          <span class="bar-amount outside" style="left:calc(0.17% + 8px);">~400 hilj.</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Plav</div>
        <div class="bar-track">
          <div class="bar-fill tier4" style="width:0.13%; --bar-w:0.13%;">
          </div>
          <span class="bar-amount outside" style="left:calc(0.13% + 8px);">~305 hilj.</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Šavnik</div>
        <div class="bar-track">
          <div class="bar-fill tier4" style="width:0.07%; --bar-w:0.07%;">
          </div>
          <span class="bar-amount outside" style="left:calc(0.07% + 8px);">186 hilj.</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label">Plužine</div>
        <div class="bar-track">
          <div class="bar-fill tier4" style="width:0.05%; --bar-w:0.05%;">
          </div>
          <span class="bar-amount outside" style="left:calc(0.05% + 8px);">126 hilj.</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label" style="color:#E74C3C; font-weight:700;">Petnjica</div>
        <div class="bar-track" style="background:#FDECEA;">
          <div class="bar-fill" style="width:0.01%; --bar-w:0.01%; background:#E74C3C;">
          </div>
          <span class="bar-amount outside" style="left:8px; color:#E74C3C; font-weight:700;">27.988 €</span>
        </div>
      </div>

      <div class="bar-row">
        <div class="bar-label" style="color:#E74C3C; font-weight:700;">Gusinje</div>
        <div class="bar-track" style="background:#FDECEA;">
          <div class="bar-fill" style="width:0.009%; --bar-w:0.009%; background:#E74C3C;">
          </div>
          <span class="bar-amount outside" style="left:8px; color:#E74C3C; font-weight:700;">25.452 €</span>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- NORTH vs REST -->
<section class="north-section">
  <div class="container">
    <div class="fade-in">
      <div class="section-divider"></div>
      <h2 class="section-title">Sjever vs. ostatak Crne Gore</h2>
      <p class="section-desc">Svih 13 opština sjevernog regiona zajedno naplate manje PDV-a nego jedna Budva.</p>
    </div>
    <div class="north-compare fade-in">
      <div class="north-card south">
        <div class="nc-num">452,3M €</div>
        <div class="nc-pct">94,4% ukupnog PDV-a</div>
        <div class="nc-label">Centralni i primorski region<br>(12 opština)</div>
      </div>
      <div class="north-card north">
        <div class="nc-num">27,2M €</div>
        <div class="nc-pct">5,6% ukupnog PDV-a</div>
        <div class="nc-label">Sjever<br>(13 opština)</div>
      </div>
    </div>
    <div class="fade-in">
      <div class="north-bar-wrap">
        <div class="north-bar-seg south-seg" style="width:94.4%;">94,4%</div>
        <div class="north-bar-seg north-seg" style="width:5.6%;">5,6%</div>
      </div>
    </div>
  </div>
</section>

<!-- SPOTLIGHT -->
<section class="spotlight">
  <div class="container" style="padding-top:40px; padding-bottom:40px;">
    <div class="fade-in">
      <div class="section-divider" style="background:#E74C3C;"></div>
      <h2 class="section-title">Dno tabele: Gusinje i Petnjica</h2>
      <p class="section-desc">Ukupan godišnji PDV ovih opština odgovara prometu od svega 130 do 150 hiljada eura — koliko jedan manji kafić ostvari za godinu dana.</p>
    </div>

    <div class="spot-cards fade-in">
      <div class="spot-card">
        <div class="sc-name">Gusinje</div>
        <div class="sc-num">25.452 €</div>
        <div class="sc-label">naplaćeno PDV-a</div>
        <div class="sc-pop"><strong>4.600</strong> stanovnika</div>
      </div>
      <div class="spot-card">
        <div class="sc-name">Petnjica</div>
        <div class="sc-num">27.988 €</div>
        <div class="sc-label">naplaćeno PDV-a</div>
        <div class="sc-pop"><strong>5.500</strong> stanovnika</div>
      </div>
    </div>

    <div class="compare-box fade-in">
      <div class="cb-title">Poređenje sa manjim opštinama</div>
      <div class="compare-row">
        <div>
          <span class="cr-name">Šavnik</span>
          <span class="cr-pop"> · 1.600 stan.</span>
        </div>
        <span class="cr-val">186.000 €</span>
      </div>
      <div class="compare-row">
        <div>
          <span class="cr-name">Plužine</span>
          <span class="cr-pop"> · 2.200 stan.</span>
        </div>
        <span class="cr-val">126.000 €</span>
      </div>
      <div class="compare-row">
        <div>
          <span class="cr-name">Andrijevica</span>
          <span class="cr-pop"> · 3.700 stan.</span>
        </div>
        <span class="cr-val">1.096.494 €</span>
      </div>
    </div>

    <div class="callout fade-in" style="margin-top:24px;">
      <p>Andrijevica ima skoro hiljadu stanovnika <strong>manje</strong> od Gusinja, ali je njen prihod od PDV-a <strong>43 puta veći</strong>.</p>
    </div>
  </div>
</section>

<!-- EGALIZACIONI FOND -->
<section class="fund-section">
  <div class="container">
    <div class="fade-in">
      <div class="section-divider"></div>
      <h2 class="section-title">Koliko dobijaju iz Egalizacionog fonda?</h2>
      <p class="section-desc">Nerazvijene opštine dobijaju sredstva iz Egalizacionog fonda. Za neke, ta sredstva čine četvrtinu do trećinu ukupnog budžeta.</p>
    </div>

    <div class="fade-in" style="overflow-x:auto;">
      <table class="fund-table">
        <thead>
          <tr>
            <th>Opština</th>
            <th>Naplaćen PDV</th>
            <th>Dobijeno iz fonda</th>
            <th>Odnos</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="name-cell">Nikšić</td>
            <td class="pdv-cell">30,8M</td>
            <td class="fund-cell">5,9M</td>
            <td class="ratio-cell positive">+24,9M</td>
          </tr>
          <tr>
            <td class="name-cell">Bijelo Polje</td>
            <td class="pdv-cell">6,6M</td>
            <td class="fund-cell">4,8M</td>
            <td class="ratio-cell positive">+1,8M</td>
          </tr>
          <tr>
            <td class="name-cell">Bar</td>
            <td class="pdv-cell">16,3M</td>
            <td class="fund-cell">3,8M</td>
            <td class="ratio-cell positive">+12,5M</td>
          </tr>
          <tr>
            <td class="name-cell">Rožaje</td>
            <td class="pdv-cell">1,9M</td>
            <td class="fund-cell">4,1M</td>
            <td class="ratio-cell negative">-2,2M</td>
          </tr>
          <tr>
            <td class="name-cell">Berane</td>
            <td class="pdv-cell">1,9M</td>
            <td class="fund-cell">3,4M</td>
            <td class="ratio-cell negative">-1,5M</td>
          </tr>
          <tr>
            <td class="name-cell">Plav</td>
            <td class="pdv-cell">~305 hilj.</td>
            <td class="fund-cell">1,9M</td>
            <td class="ratio-cell negative">-1,6M</td>
          </tr>
          <tr>
            <td class="name-cell">Andrijevica</td>
            <td class="pdv-cell">1,1M</td>
            <td class="fund-cell">1,1M</td>
            <td class="ratio-cell" style="color:#DAA520;">≈ 0</td>
          </tr>
          <tr class="highlight-row">
            <td class="name-cell">Petnjica</td>
            <td class="pdv-cell">28 hilj.</td>
            <td class="fund-cell">992 hilj.</td>
            <td class="ratio-cell negative">-964 hilj.</td>
          </tr>
          <tr class="highlight-row">
            <td class="name-cell">Gusinje</td>
            <td class="pdv-cell">25 hilj.</td>
            <td class="fund-cell">828 hilj.</td>
            <td class="ratio-cell negative">-803 hilj.</td>
          </tr>
        </tbody>
      </table>
    </div>

    <div class="callout fade-in" style="margin-top:24px;">
      <p>Gusinje je od PDV-a doprinijelo budžetu <strong>25.452 €</strong>, a iz Egalizacionog fonda dobilo <strong>828.000 €</strong> — odnos 1 prema 32.</p>
    </div>
  </div>
</section>

<!-- FOOTER -->
<div class="footer">
  <div class="container">
    <p class="src">Izvor: Poreska uprava Crne Gore / Ministarstvo finansija</p>
    <p>Podaci se odnose na naplatu PDV-a u domaćem prometu za 2024. godinu.<br>Podaci o naplati PDV-a prilikom uvoza nisu uključeni jer se ne mogu raspodijeliti po opštinama.</p>
    <p style="margin-top:8px;">Infografik: Vijesti.me</p>
  </div>
</div>

<script>
// Scroll-triggered fade-in animations
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('visible');
    }
  });
}, { threshold: 0.15, rootMargin: '0px 0px -40px 0px' });

document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));
</script>

</body>
</html>
