# Acte-necesare-in-functie-de-domeniul-de-activitate
aplicatie informativa
[index.html](https://github.com/user-attachments/files/25587955/index.html)
<!DOCTYPE html>
<html lang="ro">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ghid Avize & Autorizații — Constanța</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=IBM+Plex+Mono:wght@400;500&family=IBM+Plex+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --navy: #0a1628;
    --deep: #0d1f3c;
    --blue: #1a3a6b;
    --accent: #c8922a;
    --gold: #e8b84b;
    --light: #f4f1eb;
    --cream: #faf8f3;
    --text: #2c2c2c;
    --muted: #7a7a7a;
    --border: #d4c9b0;
    --success: #2d7a4f;
    --warn: #b85c00;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--cream);
    color: var(--text);
    font-family: 'IBM Plex Sans', sans-serif;
    font-weight: 300;
    min-height: 100vh;
  }

  /* HEADER */
  header {
    background: var(--navy);
    color: var(--light);
    padding: 0;
    position: relative;
    overflow: hidden;
  }

  header::before {
    content: '';
    position: absolute;
    top: -50%;
    right: -10%;
    width: 600px;
    height: 600px;
    border-radius: 50%;
    border: 1px solid rgba(200,146,42,0.15);
    pointer-events: none;
  }

  header::after {
    content: '';
    position: absolute;
    top: -30%;
    right: 5%;
    width: 400px;
    height: 400px;
    border-radius: 50%;
    border: 1px solid rgba(200,146,42,0.08);
    pointer-events: none;
  }

  .header-inner {
    max-width: 1100px;
    margin: 0 auto;
    padding: 48px 32px 40px;
    position: relative;
    z-index: 1;
  }

  .header-badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(200,146,42,0.15);
    border: 1px solid rgba(200,146,42,0.3);
    color: var(--gold);
    font-family: 'IBM Plex Mono', monospace;
    font-size: 11px;
    letter-spacing: 2px;
    text-transform: uppercase;
    padding: 6px 14px;
    border-radius: 2px;
    margin-bottom: 20px;
  }

  header h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 5vw, 3.2rem);
    font-weight: 900;
    line-height: 1.1;
    letter-spacing: -0.5px;
    margin-bottom: 12px;
  }

  header h1 span { color: var(--gold); }

  .header-sub {
    font-size: 15px;
    color: rgba(244,241,235,0.65);
    max-width: 560px;
    line-height: 1.6;
    margin-bottom: 32px;
  }

  .disclaimer {
    background: rgba(200,146,42,0.1);
    border-left: 3px solid var(--accent);
    padding: 12px 16px;
    font-size: 12.5px;
    color: rgba(244,241,235,0.75);
    line-height: 1.5;
    max-width: 700px;
    border-radius: 0 4px 4px 0;
  }

  /* SEARCH SECTION */
  .search-section {
    background: var(--deep);
    padding: 32px;
    border-bottom: 1px solid rgba(200,146,42,0.2);
  }

  .search-inner {
    max-width: 1100px;
    margin: 0 auto;
  }

  .search-label {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 11px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 10px;
    display: block;
  }

  .search-row {
    display: flex;
    gap: 12px;
    align-items: stretch;
  }

  .search-input-wrap {
    flex: 1;
    position: relative;
  }

  .search-input-wrap input {
    width: 100%;
    padding: 14px 20px;
    font-family: 'IBM Plex Sans', sans-serif;
    font-size: 16px;
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(200,146,42,0.3);
    color: var(--light);
    border-radius: 4px;
    outline: none;
    transition: border-color 0.2s;
  }

  .search-input-wrap input::placeholder { color: rgba(244,241,235,0.4); }
  .search-input-wrap input:focus { border-color: var(--gold); }

  .search-btn {
    background: var(--accent);
    color: var(--navy);
    border: none;
    padding: 14px 28px;
    font-family: 'IBM Plex Mono', monospace;
    font-size: 13px;
    font-weight: 500;
    letter-spacing: 1px;
    text-transform: uppercase;
    border-radius: 4px;
    cursor: pointer;
    transition: background 0.2s, transform 0.1s;
    white-space: nowrap;
  }

  .search-btn:hover { background: var(--gold); }
  .search-btn:active { transform: scale(0.98); }

  /* DROPDOWN */
  .caen-dropdown {
    position: absolute;
    top: calc(100% + 4px);
    left: 0;
    right: 0;
    background: var(--navy);
    border: 1px solid rgba(200,146,42,0.3);
    border-radius: 4px;
    max-height: 300px;
    overflow-y: auto;
    z-index: 100;
    display: none;
  }

  .caen-dropdown.show { display: block; }

  .caen-item {
    padding: 12px 16px;
    cursor: pointer;
    border-bottom: 1px solid rgba(255,255,255,0.05);
    transition: background 0.15s;
    display: flex;
    gap: 12px;
    align-items: flex-start;
  }

  .caen-item:hover { background: rgba(200,146,42,0.1); }

  .caen-code-tag {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 12px;
    background: rgba(200,146,42,0.2);
    color: var(--gold);
    padding: 2px 8px;
    border-radius: 2px;
    white-space: nowrap;
    flex-shrink: 0;
  }

  .caen-name {
    font-size: 13.5px;
    color: rgba(244,241,235,0.85);
    line-height: 1.4;
  }

  /* MAIN */
  main {
    max-width: 1100px;
    margin: 0 auto;
    padding: 40px 32px;
  }

  .placeholder-state {
    text-align: center;
    padding: 80px 20px;
    color: var(--muted);
  }

  .placeholder-state .icon {
    font-size: 48px;
    margin-bottom: 16px;
    opacity: 0.4;
  }

  .placeholder-state h3 {
    font-family: 'Playfair Display', serif;
    font-size: 22px;
    color: var(--text);
    margin-bottom: 8px;
    font-weight: 400;
  }

  .placeholder-state p {
    font-size: 14px;
    max-width: 400px;
    margin: 0 auto;
    line-height: 1.6;
  }

  /* RESULT */
  .result-header {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    margin-bottom: 32px;
    padding-bottom: 24px;
    border-bottom: 1px solid var(--border);
    gap: 16px;
    flex-wrap: wrap;
  }

  .result-title h2 {
    font-family: 'Playfair Display', serif;
    font-size: 26px;
    font-weight: 700;
    color: var(--navy);
    margin-bottom: 4px;
  }

  .result-title p {
    font-size: 14px;
    color: var(--muted);
  }

  .caen-badge {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 22px;
    font-weight: 500;
    color: var(--accent);
    background: rgba(200,146,42,0.08);
    border: 1px solid rgba(200,146,42,0.25);
    padding: 8px 20px;
    border-radius: 4px;
    flex-shrink: 0;
  }

  /* SUMMARY CARDS */
  .summary-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
    gap: 12px;
    margin-bottom: 40px;
  }

  .summary-card {
    background: white;
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 16px;
    text-align: center;
  }

  .summary-card .num {
    font-family: 'Playfair Display', serif;
    font-size: 32px;
    font-weight: 700;
    color: var(--navy);
    line-height: 1;
    margin-bottom: 4px;
  }

  .summary-card .lbl {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 10px;
    letter-spacing: 1px;
    text-transform: uppercase;
    color: var(--muted);
  }

  /* STEPS */
  .steps-title {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 11px;
    letter-spacing: 2.5px;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 20px;
  }

  .step-card {
    background: white;
    border: 1px solid var(--border);
    border-radius: 8px;
    margin-bottom: 16px;
    overflow: hidden;
    transition: box-shadow 0.2s;
  }

  .step-card:hover { box-shadow: 0 4px 20px rgba(0,0,0,0.07); }

  .step-header {
    display: flex;
    align-items: center;
    gap: 16px;
    padding: 20px 24px;
    cursor: pointer;
    user-select: none;
  }

  .step-num {
    width: 36px;
    height: 36px;
    border-radius: 50%;
    background: var(--navy);
    color: var(--gold);
    font-family: 'IBM Plex Mono', monospace;
    font-size: 14px;
    font-weight: 500;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
  }

  .step-info { flex: 1 }

  .step-name {
    font-family: 'Playfair Display', serif;
    font-size: 17px;
    font-weight: 700;
    color: var(--navy);
    margin-bottom: 2px;
  }

  .step-inst {
    font-size: 12.5px;
    color: var(--muted);
    font-family: 'IBM Plex Mono', monospace;
  }

  .step-tags {
    display: flex;
    gap: 8px;
    align-items: center;
    flex-wrap: wrap;
  }

  .tag {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 11px;
    padding: 3px 10px;
    border-radius: 20px;
    white-space: nowrap;
  }

  .tag-cost {
    background: rgba(45,122,79,0.1);
    color: var(--success);
    border: 1px solid rgba(45,122,79,0.2);
  }

  .tag-time {
    background: rgba(26,58,107,0.08);
    color: var(--blue);
    border: 1px solid rgba(26,58,107,0.15);
  }

  .tag-required {
    background: rgba(184,92,0,0.08);
    color: var(--warn);
    border: 1px solid rgba(184,92,0,0.2);
  }

  .chevron {
    color: var(--muted);
    font-size: 18px;
    transition: transform 0.2s;
    flex-shrink: 0;
  }

  .step-card.open .chevron { transform: rotate(180deg); }

  .step-body {
    display: none;
    padding: 0 24px 24px;
    border-top: 1px solid var(--border);
  }

  .step-card.open .step-body { display: block; }

  .step-body-inner {
    padding-top: 20px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 24px;
  }

  @media (max-width: 640px) {
    .step-body-inner { grid-template-columns: 1fr; }
    .search-row { flex-direction: column; }
    header h1 { font-size: 1.8rem; }
  }

  .docs-section h4, .notes-section h4 {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 10.5px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 12px;
  }

  .doc-list {
    list-style: none;
  }

  .doc-list li {
    display: flex;
    gap: 8px;
    align-items: flex-start;
    font-size: 13.5px;
    line-height: 1.5;
    padding: 5px 0;
    border-bottom: 1px dashed rgba(212,201,176,0.5);
    color: var(--text);
  }

  .doc-list li:last-child { border-bottom: none; }

  .doc-list li::before {
    content: '▸';
    color: var(--accent);
    flex-shrink: 0;
    margin-top: 1px;
  }

  .notes-section {
    grid-column: 1 / -1;
  }

  .note-box {
    background: var(--light);
    border-left: 3px solid var(--gold);
    padding: 14px 16px;
    font-size: 13px;
    line-height: 1.6;
    color: var(--text);
    border-radius: 0 4px 4px 0;
    margin-bottom: 10px;
  }

  .note-box.law {
    border-left-color: var(--blue);
    background: rgba(26,58,107,0.04);
  }

  .link-row {
    margin-top: 14px;
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
  }

  .link-btn {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    font-family: 'IBM Plex Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.5px;
    color: var(--blue);
    background: rgba(26,58,107,0.07);
    border: 1px solid rgba(26,58,107,0.15);
    padding: 5px 12px;
    border-radius: 3px;
    text-decoration: none;
    cursor: pointer;
    transition: background 0.15s;
  }

  .link-btn:hover { background: rgba(26,58,107,0.14); }

  /* LEGEND */
  .legend {
    margin-top: 48px;
    padding-top: 32px;
    border-top: 1px solid var(--border);
  }

  .legend h3 {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 10.5px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 16px;
  }

  .institutions-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 10px;
  }

  .inst-item {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 13px;
    padding: 10px 14px;
    background: white;
    border: 1px solid var(--border);
    border-radius: 4px;
  }

  .inst-dot {
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background: var(--accent);
    flex-shrink: 0;
  }

  .inst-name { font-weight: 500; color: var(--navy); }
  .inst-desc { font-size: 12px; color: var(--muted); }

  footer {
    text-align: center;
    padding: 32px;
    font-family: 'IBM Plex Mono', monospace;
    font-size: 11px;
    color: var(--muted);
    border-top: 1px solid var(--border);
    margin-top: 40px;
  }

  /* Scrollbar */
  .caen-dropdown::-webkit-scrollbar { width: 4px; }
  .caen-dropdown::-webkit-scrollbar-track { background: var(--navy); }
  .caen-dropdown::-webkit-scrollbar-thumb { background: rgba(200,146,42,0.4); border-radius: 2px; }

  .fade-in {
    animation: fadeIn 0.3s ease;
  }

  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(8px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* Print */
  @media print {
    header { background: white !important; color: black !important; }
    .search-section { display: none; }
    .step-body { display: block !important; }
    .chevron { display: none; }
  }
</style>
</head>
<body>

<header>
  <div class="header-inner">
    <div class="header-badge">⚓ Constanța · Ghid Oficial 2025</div>
    <h1>Avize & Autorizații<br>pentru <span>Activități CAEN</span></h1>
    <p class="header-sub">Identificați toate avizele, autorizațiile, actele necesare și costurile aferente exercitării legale a activității dvs. în municipiul Constanța.</p>
    <div class="disclaimer">
      ⚠ Informațiile prezentate sunt orientative, bazate pe legislația în vigoare și pe cerințele instituțiilor publice. Verificați întotdeauna pe site-urile oficiale ale instituțiilor (ONRC, Primăria Constanța, ISU, DSP, DVS, ANPC etc.) pentru informații actualizate. Costurile pot varia.
    </div>
  </div>
</header>

<div class="search-section">
  <div class="search-inner">
    <label class="search-label">Introduceți codul CAEN sau denumirea activității</label>
    <div class="search-row">
      <div class="search-input-wrap">
        <input type="text" id="searchInput" placeholder="ex: 5610 — Restaurante, sau 4711 — Comerț cu amănuntul..." autocomplete="off">
        <div class="caen-dropdown" id="dropdown"></div>
      </div>
      <button class="search-btn" onclick="clearSearch()">✕ Resetează</button>
    </div>
  </div>
</div>

<main id="mainContent">
  <div class="placeholder-state">
    <div class="icon">🏛</div>
    <h3>Selectați o activitate CAEN</h3>
    <p>Căutați codul CAEN sau denumirea activității pentru a vedea lista completă de avize și autorizații necesare în Constanța.</p>
  </div>
</main>

<footer>
  Ghid orientativ generat pe baza legislației române în vigoare și a cerințelor instituțiilor publice din Constanța · 2025<br>
  Surse: ONRC · Primăria Constanța · ISU Dobrogea · DSP Constanța · DVS Constanța · ANPC · APM Constanța · DSVSA
</footer>

<script>
// =============================================
// BAZA DE DATE CAEN + AVIZE
// =============================================

const CAEN_DB = {
  "5610": {
    name: "Restaurante",
    sectiune: "HoReCa / Alimentație Publică",
    steps: [
      {
        id: 1,
        titlu: "Înregistrare la ONRC",
        institutie: "ONRC — Oficiul Național al Registrului Comerțului",
        institutie_url: "https://www.onrc.ro",
        cost: "200–400 RON (taxe înregistrare SRL)",
        durata: "3–5 zile lucrătoare",
        obligatoriu: true,
        documente: [
          "Cerere de înregistrare (formular tip)",
          "Actul constitutiv / Statut societate (2 exemplare originale)",
          "Dovada sediului social (contract de închiriere sau act proprietate)",
          "Specimen de semnătură al administratorului",
          "Declarație pe propria răspundere privind autorizarea funcționării",
          "Dovada achitării taxelor de înregistrare",
          "Cazier fiscal al asociaților și administratorilor",
          "Copii CI/pașaport asociați/administratori"
        ],
        note: [
          "Se poate face online pe portalul ONRC (onrc.ro) sau la ghișeu.",
          "Codul CAEN 5610 se înscrie în obiectul de activitate al firmei.",
          "Certificatul de înregistrare și CUI vor fi emise la finalizare."
        ],
        lege: "Legea nr. 31/1990 privind societățile comerciale; Legea nr. 26/1990 privind registrul comerțului; OUG nr. 44/2008 pentru PFA/II"
      },
      {
        id: 2,
        titlu: "Autorizația de construire / Acordul de funcționare (schimbare destinație)",
        institutie: "Primăria Municipiului Constanța — Direcția Urbanism",
        institutie_url: "https://www.primaria-constanta.ro",
        cost: "0,5% din valoarea lucrărilor (min. 50 RON) + taxe avize",
        durata: "30–60 zile calendaristice",
        obligatoriu: true,
        documente: [
          "Cerere tip pentru autorizație de construire/schimbare destinație",
          "Titlul de proprietate / Contract de închiriere / Comodat",
          "Proiect tehnic (arhitectură, instalații) întocmit de arhitect autorizat",
          "Certificat de urbanism (obținut anterior)",
          "Aviz ISU (dacă suprafața > 100 mp sau este loc public)",
          "Aviz DSP privind igiena (pentru restaurante)",
          "Aviz Protecția Mediului (APM) — dacă e cazul",
          "Fișa tehnică pentru avizul de securitate la incendiu",
          "Dovada achitării taxelor"
        ],
        note: [
          "Dacă spațiul are deja destinație alimentație publică, se solicită doar Acordul de funcționare.",
          "Certificatul de urbanism se obține în prealabil de la Primărie — 5–10 zile, taxă 5–30 RON.",
          "Proiectul trebuie semnat de arhitect cu drept de semnătură (RUR)."
        ],
        lege: "Legea nr. 50/1991 privind autorizarea executării lucrărilor de construcții; Legea nr. 350/2001 privind amenajarea teritoriului"
      },
      {
        id: 3,
        titlu: "Avizul / Autorizația de Securitate la Incendiu (ISU)",
        institutie: "ISU Dobrogea — Inspectoratul pentru Situații de Urgență",
        institutie_url: "https://isudobrogea.ro",
        cost: "Gratuit (serviciu public)",
        durata: "30 zile calendaristice",
        obligatoriu: true,
        documente: [
          "Cerere pentru emiterea avizului/autorizației PSI",
          "Documentație tehnică (planuri, memoriu tehnic) semnată de proiectant atestat IGSU",
          "Scenariul de securitate la incendiu (pentru autorizație)",
          "Planuri de arhitectură (releveu la scara 1:100 sau 1:50)",
          "Declarație privind respectarea cerințelor de securitate la incendiu",
          "Dovada achitării tarifului (dacă se aplică)",
          "Proiect PSI semnat de expert atestat"
        ],
        note: [
          "Avizul ISU este obligatoriu înainte de autorizația de construire pentru spații > 100 mp sau cu mai mult de 50 persoane simultan.",
          "Autorizația de securitate la incendiu se obține DUPĂ finalizarea lucrărilor, înainte de deschidere.",
          "ISU poate efectua inspecție la fața locului.",
          "Restaurantele sunt clasificate ca 'construcții cu risc mediu de incendiu'."
        ],
        lege: "Legea nr. 307/2006 privind apărarea împotriva incendiilor; Ordinul MAI nr. 129/2016 privind avizarea și autorizarea PSI"
      },
      {
        id: 4,
        titlu: "Avizul Direcției de Sănătate Publică (DSP)",
        institutie: "DSP Constanța — Direcția de Sănătate Publică",
        institutie_url: "https://dspct.ro",
        cost: "400–500 lei — conform OMS nr. 1030/2009 mod. OMS nr. 458/2023: 400 lei (asistență de specialitate + certificarea conformității) sau 500 lei (autorizație în baza referatului de evaluare). Viză anuală: 400 lei",
        durata: "15–30 zile calendaristice",
        obligatoriu: true,
        documente: [
          "Dovada achitării tarifului (400 lei sau 500 lei) — virament bancar în contul Trezoreriei Constanța (DSP Constanța, CIF: 2952688)",
          "Cerere pentru aviz sanitar",
          "Schița/planul spațiului cu destinația fiecărei încăperi (scara 1:50/1:100)",
          "Memoriu tehnico-sanitar (flux tehnologic, materiale folosite)",
          "Dovada sursei de apă potabilă (racord la rețea sau buletin de analiză)",
          "Contract de salubritate cu firmă autorizată",
          "Contract deratizare/dezinsecție/dezinfecție",
          "Contract de eliminare a deșeurilor menajere și a uleiurilor uzate",
          "Fișa de post a personalului cu mențiuni medicale",
          "Dovada instruirii personalului în igiena alimentelor (cursuri HACCP)"
        ],
        note: [
          "⚠ TARIFE REALE DSP Constanța (OMS nr. 1030/2009 mod. OMS nr. 458/2023): 400 lei — asistență specialitate/certificare conformitate; 500 lei — autorizație sanitară în baza referatului de evaluare.",
          "Plata se face EXCLUSIV prin virament bancar în contul DSP Constanța la Trezoreria Constanța.",
          "DSP efectuează inspecție la fața locului pentru verificarea condițiilor sanitare.",
          "Personalul care manipulează alimente trebuie să dețină carnet de sănătate actualizat.",
          "Se va implementa sistemul HACCP conform Regulamentului (CE) nr. 852/2004.",
          "Avizul sanitar este condiție pentru deschiderea unității.",
          "DSP Constanța: Aleea Lăcrămioarei nr. 1 / Str. Nicolae Iorga nr. 89 | secretariat@dspct.ro | Tel: 0241.838.330"
        ],
        lege: "Legea nr. 95/2006 privind reforma în domeniul sănătății; Regulamentul CE 852/2004; OMS nr. 1030/2009 privind procedurile de reglementare sanitară; OMS nr. 458/2023 (modificare OMS 1030/2009)"
      },
      {
        id: 5,
        titlu: "Autorizația Sanitar-Veterinară (DSVSA)",
        institutie: "DSVSA Constanța — Direcția Sanitar-Veterinară și Siguranța Alimentelor",
        institutie_url: "https://dsvsa-constanta.ro",
        cost: "200–500 RON (taxe de înregistrare/autorizare)",
        durata: "30 zile calendaristice",
        obligatoriu: true,
        documente: [
          "Cerere de înregistrare/autorizare sanitar-veterinară",
          "Planul spațiului cu fluxul produselor alimentare",
          "Lista produselor/preparatelor comercializate",
          "Proceduri HACCP documentate",
          "Contracte de aprovizionare cu furnizori autorizați",
          "Dovada echipamentelor frigorifice și temperaturile de depozitare",
          "Contracte de eliminare a deșeurilor alimentare",
          "Registrul de intrare-ieșire a produselor de origine animală"
        ],
        note: [
          "Obligatorie pentru unitățile care manipulează produse de origine animală.",
          "DSVSA efectuează inspecție și poate solicita probe de laborator.",
          "Numărul de autorizare se menționează pe toate documentele comerciale.",
          "Înregistrarea sanitară-veterinară este diferită de autorizare — în funcție de categoriile de produse."
        ],
        lege: "Regulamentul CE nr. 853/2004; Regulamentul CE nr. 854/2004; Legea nr. 150/2004; Ordinul ANSVSA nr. 111/2008"
      },
      {
        id: 6,
        titlu: "Certificatul de Clasificare Alimentație Publică — Ministerul Economiei, Antreprenoriatului și Turismului",
        institutie: "MEAT — Ministerul Economiei, Antreprenoriatului și Turismului (Direcția Generală Turism)",
        institutie_url: "https://se.situr.gov.ro/cms/",
        cost: "Fără taxă administrativă (procedura gratuită)",
        durata: "30 zile (autorizație provizorie) + 30–60 zile (certificat definitiv după inspecție)",
        obligatoriu: false,
        documente: [
          "Cerere standardizată (Anexa nr. 3 la Ordinul nr. 65/2013 cu modificările ulterioare)",
          "Certificat constatator extins ONRC — cu CAEN 5610 autorizat la punctul de lucru",
          "Fișă standardizată privind structura spațiilor de alimentație publică (Anexa nr. 5)",
          "Dovada proprietății sau dreptului de folosință a imobilului",
          "Aviz ISU — copie (dacă există)",
          "Autorizație sanitară DSP — copie",
          "Fotografii reprezentative (sala de mese, bucătărie, bar dacă există)"
        ],
        note: [
          "ℹ Clasificarea alimentației publice este FACULTATIVĂ pentru restaurantele standalone (art. 25, Ordinul ANT nr. 65/2013).",
          "⚠ Devine OBLIGATORIE dacă restaurantul face parte dintr-o structură de primire turistică (hotel, pensiune, motel, vilă turistică etc.).",
          "Clasificarea conferă categorie (furculițe: 1–5) și crește credibilitatea față de clienți și platformele de rezervare.",
          "Procedura se poate face ONLINE pe se.situr.gov.ro (platforma SITUR — Ministerul Economiei, Antreprenoriatului și Turismului).",
          "AMENZI: Funcționarea ca restaurant în structuri turistice fără clasificare: 10.000–20.000 lei (HG nr. 709/2009)."
        ],
        lege: "OG nr. 58/1998 privind organizarea și desfășurarea activității de turism; Ordinul ANT nr. 65/2013 (norme metodologice, art. 24–26); HG nr. 709/2009; Ordinul nr. 985/2024"
      },
      {
        id: 7,
        titlu: "Autorizația de funcționare — Primăria Constanța (DASOEC)",
        institutie: "Primăria Municipiului Constanța — Direcția Autorizare și Sprijin Operatori Economici",
        institutie_url: "https://www.primaria-constanta.ro",
        cost: "1.060–7.418 RON/an (în funcție de suprafață și program orar) — conform HCLM nr. 412/2024",
        durata: "15–30 zile calendaristice",
        obligatoriu: true,
        documente: [
          "Cerere tip pentru autorizație de funcționare",
          "Certificat de înregistrare ONRC + Certificat constatator",
          "Autorizația de securitate la incendiu (ISU)",
          "Avizul sanitar (DSP) sau dovada înregistrării DSVSA",
          "Contractul de închiriere / titlu proprietate",
          "Acordul asociației de proprietari (dacă e în bloc de locuințe)",
          "Dovada plății taxei de autorizare",
          "Plan de situație cu amplasamentul unității"
        ],
        note: [
          "⚠ TAXE REALE conform Anexei nr. 9 la HCLM nr. 412/2024 (în vigoare de la 01.01.2025):",
          "▸ Restaurante (gr. 561) program până la 01:00 — sub 100 mp: 1.060 lei/an; 100–500 mp: 2.650 lei/an; peste 500 mp: 5.298 lei/an",
          "▸ Restaurante (gr. 561) program PESTE 01:00 — sub 500 mp: 3.710 lei/an; peste 500 mp: 7.418 lei/an",
          "▸ Restaurante în Stațiunea Mamaia — sub 500 mp: 3.710 lei/an; peste 500 mp: 7.418 lei/an",
          "▸ Baruri (gr. 563) program până la 01:00 — sub 100 mp: 1.060 lei; 100–500 mp: 2.650 lei; peste 500 mp: 5.298 lei/an",
          "▸ Baruri (gr. 563) program PESTE 01:00 — sub 500 mp: 3.710 lei; peste 500 mp: 7.418 lei/an",
          "▸ Taxă sanitară de funcționare: 22 lei/an (suplimentar)",
          "Terasa exterioară necesită autorizare separată (taxă domeniului public: 1,59 lei/mp/zi în mai–septembrie).",
          "Vizarea (reînnoirea) anuală a autorizației implică aceeași taxă.",
          "Autorizația se afișează obligatoriu la loc vizibil în unitate."
        ],
        lege: "HCLM nr. 412/2024 — Anexa nr. 9, Art. 3 (taxe DASOEC); OG nr. 99/2000 privind comercializarea produselor și serviciilor de piață; HG nr. 843/1999"
      },
      {
        id: 8,
        titlu: "Înregistrare la ANPC / Conformitate Protecția Consumatorilor",
        institutie: "ANPC — Autoritatea Națională pentru Protecția Consumatorilor (Comisariatul Județean Constanța)",
        institutie_url: "https://anpc.ro",
        cost: "Gratuit",
        durata: "Notificare prealabilă (fără termen)",
        obligatoriu: true,
        documente: [
          "Meniuri cu prețuri afișate (inclusiv TVA)",
          "Afișarea vizibilă a prețurilor (conform OG 21/1992)",
          "Registrul de reclamații la dispoziția clienților",
          "Etichetare corectă a produselor alimentare",
          "Dovada originii și compoziției preparatelor (la cererea ANPC)"
        ],
        note: [
          "Nu există autorizare ANPC separată — conformitatea se verifică la inspecție.",
          "Meniurile trebuie să conțină declarații privind alergenii (Regulamentul UE 1169/2011).",
          "Bonul fiscal este obligatoriu pentru fiecare tranzacție (casă de marcat fiscalizată)."
        ],
        lege: "OG nr. 21/1992 privind protecția consumatorilor; Regulamentul UE 1169/2011; OUG nr. 28/1999 privind casele de marcat"
      },
      {
        id: 9,
        titlu: "Autorizație-Licență Neexclusivă UCMR-ADA (drepturi de autor muzică)",
        institutie: "UCMR-ADA — Asociația pentru Drepturi de Autor a Compozitorilor",
        institutie_url: "https://ucmr-ada.ro",
        cost: "Variabil lunar: ~100–500 lei/lună (ambiental, în funcție de suprafață și tip unitate) — conform Decizia ORDA nr. 68/2025 (în vigoare 01.05.2025)",
        durata: "7 zile de la depunerea cererii",
        obligatoriu: true,
        documente: [
          "Cerere de autorizare (model de pe ucmr-ada.ro sau portal.ucmr-ada.ro)",
          "Copie CUI societate",
          "Împuternicire reprezentant societate (dacă e cazul)",
          "Date complete punct de lucru: suprafață, clasificare turistică, program"
        ],
        note: [
          "OBLIGATORIE înainte de orice utilizare de muzică (ambientală sau cu artiști live).",
          "Remunerația se plătește LUNAR până pe data de 15 a lunii curente.",
          "Restaurante urban, scop ambiental (muzică fără interpreți): tarif calculat pe baza suprafeței — consultați tabelul de tarife actualizat pe ucmr-ada.ro (Decizia ORDA 68/2025, în vigoare 01.05.2025).",
          "Restaurante cu artiști interpreți/formații live: tarife mai ridicate (consultați metodologia spectacole).",
          "Autorizația se obține ONLINE pe portal.ucmr-ada.ro sau direct la sediu/inspector zonal.",
          "Lipsa autorizației atrage penalități de 0,5%/zi de întârziere + acțiune în instanță."
        ],
        lege: "Legea nr. 8/1996 privind dreptul de autor; Decizia ORDA nr. 68/31.03.2025; Decizia ORDA nr. 75/2023; Hotărârea arbitrală din 30.09.2011"
      },
      {
        id: 10,
        titlu: "Autorizație-Licență Neexclusivă UPFR (drepturi conexe producători fonograme)",
        institutie: "UPFR — Uniunea Producătorilor de Fonograme din România",
        institutie_url: "https://upfr.ro",
        cost: "Variabil lunar: ~100–300 lei/lună (ambiental, în funcție de suprafață și locație) — conform Decizia ORDA nr. 43/2025 (în vigoare 17.03.2025)",
        durata: "7–14 zile",
        obligatoriu: true,
        documente: [
          "Cerere de autorizare (formular de pe upfr.ro)",
          "Copie CUI societate",
          "Date punct de lucru: suprafață, tip activitate, localizare (urban/stațiune/rural)"
        ],
        note: [
          "OBLIGATORIE separat de UCMR-ADA — reprezintă drepturile producătorilor de fonograme (case de discuri).",
          "Restaurante, baruri, fast-food urban (201–300 mp): ~168 lei/lună (tarif de referință Decizia ORDA 43/2025).",
          "Licența se acordă per punct de lucru și este netransferabilă.",
          "Reînnoibilă pentru perioade de până la 12 luni.",
          "Deținerea doar a licenței UCMR-ADA NU exonerează de obligația față de UPFR și viceversa.",
          "Consultați tabelul complet de tarife actualizat la upfr.ro (Decizia ORDA nr. 43/2025, MO nr. 232/17.03.2025)."
        ],
        lege: "Legea nr. 8/1996 privind dreptul de autor; Decizia ORDA nr. 43/2025; Metodologia privind comunicarea publică (MO 146/25.02.2016)"
      },
      {
        id: 11,
        titlu: "Autorizație-Licență Neexclusivă CREDIDAM (drepturi conexe artiști interpreți)",
        institutie: "CREDIDAM — Centrul Român pentru Administrarea Drepturilor Artiștilor Interpreți",
        institutie_url: "https://credidam.ro",
        cost: "Variabil: calculat pe baza suprafeței și tipului de activitate — conform Decizia ORDA nr. 43/2025",
        durata: "7–14 zile",
        obligatoriu: true,
        documente: [
          "Declarație utilizator (model de pe credidam.ro — actualizat dec. 2025)",
          "Convenție utilizator (2 exemplare semnate și ștampilate)",
          "Se transmit la sediu (Str. C.A. Rosetti nr. 34, București) sau pe e-mail: office@credidam.ro"
        ],
        note: [
          "OBLIGATORIE separat de UCMR-ADA și UPFR — reprezintă drepturile artiștilor interpreți și executanți.",
          "Autorizația se emite DUPĂ confirmarea plății; factura (e-factura) se emite la înregistrare.",
          "Plata se poate face trimestrial (fără reducere), semestrial (reducere 3%) sau anual (reducere 5%).",
          "Cont IBAN: RO23INGB0001000152938958 (ING Bank) sau prin aplicația BCR Touch 24.",
          "Decizia ORDA nr. 43/2025 este actul în vigoare la data de 17.03.2025.",
          "Dacă difuzați și TV (televizoare în local), pot fi necesare și autorizații DACIN-SARA/UPFAR-ARGOA (colectate de UPFR)."
        ],
        lege: "Legea nr. 8/1996 privind dreptul de autor; Decizia ORDA nr. 43/2025; Decizia ORDA nr. 99/2015; Decizia ORDA nr. 10/2016"
      },
      {
        id: 12,
        titlu: "Autorizația de Mediu — APM Constanța",
        institutie: "APM Constanța — Agenția pentru Protecția Mediului Constanța",
        institutie_url: "http://apmct.anpm.ro",
        cost: "500 lei (tarif emitere autorizație de mediu — conform OM nr. 865/2014 + 1.500 lei analiză documentație, dacă e cazul)",
        durata: "30–60 zile calendaristice",
        obligatoriu: false,
        documente: [
          "Fișa de prezentare și declarație (Anexa 2 din OM nr. 1798/2007)",
          "Dovada publicității solicitării (anunț public — model Anexa 3 OM 1798/2007)",
          "Plan de situație și plan de încadrare în zonă",
          "Certificat constatator ONRC (emis conform art. 17 Legea 359/2004)",
          "Dovada achitării tarifului de 500 lei (IBAN: RO03TREZ2315032XXX005043, Trezoreria Constanța, CIF: 1863832)",
          "Contracte de gestionare deșeuri (inclusiv uleiuri alimentare uzate — firmă autorizată ANPM)",
          "Dovada separării selective a deșeurilor"
        ],
        note: [
          "⚠ Autorizația de mediu este OBLIGATORIE pentru activitățile din Anexa 1 la OM nr. 1798/2007.",
          "Restaurante cu suprafețe mari, cu instalații de ventilație/filtrare, sau situate în zone sensibile de mediu pot fi incluse în Anexa 1.",
          "Restaurantele mici (<200 mp, fără impact semnificativ) pot fi exceptate — verificați cu APM Constanța.",
          "Tarifele se plătesc EXCLUSIV prin virament bancar (nu la casierie).",
          "Autorizația de mediu este valabilă 5 ani, după care se revizuiește.",
          "APM Constanța: Str. Unirii nr. 23, Constanța | Tel: 0241.546.696 | office@apmct.anpm.ro"
        ],
        lege: "OUG nr. 195/2005 privind protecția mediului; OM nr. 1798/2007 privind procedura de emitere a autorizației de mediu; OM nr. 865/2014 privind tarifele; Legea nr. 211/2011 privind deșeurile"
      }
    ]
  },

  "4711": {
    name: "Comerț cu amănuntul în magazine nespecializate, cu vânzare predominantă de produse alimentare",
    sectiune: "Comerț cu Amănuntul — Alimentar",
    steps: [
      {
        id: 1,
        titlu: "Înregistrare la ONRC",
        institutie: "ONRC — Oficiul Național al Registrului Comerțului",
        institutie_url: "https://www.onrc.ro",
        cost: "200–400 RON",
        durata: "3–5 zile lucrătoare",
        obligatoriu: true,
        documente: [
          "Cerere de înregistrare (formular tip ONRC)",
          "Actul constitutiv / Statut",
          "Dovada sediului social",
          "Specimen de semnătură administrator",
          "Declarație pe propria răspundere",
          "Cazier fiscal asociați/administratori",
          "Dovada achitării taxelor de înregistrare"
        ],
        note: ["Codul CAEN 4711 trebuie inclus în obiectul de activitate. Înregistrarea se face la ONRC Constanța sau online."],
        lege: "Legea nr. 31/1990; Legea nr. 26/1990"
      },
      {
        id: 2,
        titlu: "Avizul / Autorizația de Securitate la Incendiu",
        institutie: "ISU Dobrogea",
        institutie_url: "https://isudobrogea.ro",
        cost: "Gratuit",
        durata: "30 zile",
        obligatoriu: true,
        documente: [
          "Cerere aviz/autorizație PSI",
          "Documentație tehnică PSI (proiectant atestat)",
          "Scenariul de securitate la incendiu",
          "Planuri de arhitectură",
          "Declarație de conformitate"
        ],
        note: ["Obligatoriu pentru magazine > 100 mp sau cu mai mult de 50 persoane. Verificați pragurile pe site-ul ISU Dobrogea."],
        lege: "Legea nr. 307/2006; Ordinul MAI nr. 129/2016"
      },
      {
        id: 3,
        titlu: "Avizul Sanitar (DSP)",
        institutie: "DSP Constanța",
        institutie_url: "https://dspct.ro",
        cost: "Gratuit",
        durata: "15–30 zile",
        obligatoriu: true,
        documente: [
          "Cerere aviz sanitar",
          "Schița spațiului comercial",
          "Memoriu tehnico-sanitar",
          "Contract salubritate",
          "Contract deratizare/dezinsecție",
          "Dovada sursei de apă potabilă"
        ],
        note: ["Necesară pentru orice spațiu în care se comercializează produse alimentare."],
        lege: "Legea nr. 95/2006; Ordinul MS nr. 976/1998"
      },
      {
        id: 4,
        titlu: "Înregistrare/Autorizare DSVSA",
        institutie: "DSVSA Constanța",
        institutie_url: "https://dsvsa-constanta.ro",
        cost: "100–300 RON",
        durata: "30 zile",
        obligatoriu: true,
        documente: [
          "Cerere înregistrare sanitară-veterinară",
          "Lista produselor comercializate",
          "Planul spațiului de depozitare frigorific",
          "Proceduri HACCP",
          "Contracte furnizori autorizați"
        ],
        note: ["Obligatorie pentru produse de origine animală (carne, lactate, ouă etc.)"],
        lege: "Regulamentul CE 853/2004; Ordinul ANSVSA 111/2008"
      },
      {
        id: 5,
        titlu: "Autorizația / Avizul Program de Funcționare — Primăria Constanța",
        institutie: "Primăria Municipiului Constanța — Direcția Autorizare și Sprijin Operatori Economici",
        institutie_url: "https://www.primaria-constanta.ro",
        cost: "107 RON/an (aviz program funcționare comerț alimentar) — conform HCLM nr. 412/2024 Anexa 9, Art. 1",
        durata: "15–30 zile",
        obligatoriu: true,
        documente: ["Cerere tip", "Certificat ONRC", "Contract închiriere/proprietate", "Aviz ISU (dacă e cazul)", "Dovada plății taxei"],
        note: [
          "⚠ TAXE REALE conform HCLM nr. 412/2024, Anexa 9, Art. 1 (în vigoare 01.01.2025):",
          "▸ Magazin alimentar (CAEN 4711, grup 472 cu excepția 4726) în orașul Constanța: 107 lei/an",
          "▸ Magazin alimentar (CAEN 4711, grup 472 exclusiv 4726) în Stațiunea Mamaia / Sat Vacanță: 8.477 lei/an",
          "Programul de funcționare se stabilește și se afișează obligatoriu.",
          "Vizarea anuală implică aceeași taxă."
        ],
        lege: "HCLM nr. 412/2024, Anexa nr. 9, Art. 1; OG nr. 99/2000"
      },
      {
        id: 6,
        titlu: "Înregistrare Casa de Marcat (ANAF)",
        institutie: "ANAF — Agenția Națională de Administrare Fiscală (Administrația Financiară Constanța)",
        institutie_url: "https://www.anaf.ro",
        cost: "Cost echipament: 1.500–4.000 RON + taxă fiscalizare",
        durata: "5–10 zile lucrătoare",
        obligatoriu: true,
        documente: [
          "Cerere de înregistrare a aparatelor de marcat electronice fiscale",
          "Cartea de intervenție a aparatului de marcat",
          "Procesul-verbal de sigilare emis de distribuitorul autorizat",
          "Copia certificatului de înregistrare fiscală (CIF)",
          "Dovada adresei punctului de lucru"
        ],
        note: [
          "Casa de marcat trebuie să fie de model omologat ANAF.",
          "Fiscalizarea se face prin distribuitorul autorizat, care transmite datele la ANAF.",
          "Se poate folosi și sistem POS cu facturare electronică ca alternativă."
        ],
        lege: "OUG nr. 28/1999 privind obligația agenților economici de a utiliza aparate de marcat electronice fiscale"
      }
    ]
  },

  "4120": {
    name: "Lucrări de construcție a clădirilor rezidențiale și nerezidențiale",
    sectiune: "Construcții",
    steps: [
      {
        id: 1,
        titlu: "Înregistrare ONRC + Autorizarea ca firmă de construcții",
        institutie: "ONRC",
        institutie_url: "https://www.onrc.ro",
        cost: "200–500 RON",
        durata: "3–5 zile",
        obligatoriu: true,
        documente: [
          "Cerere înregistrare",
          "Actul constitutiv",
          "Dovada sediului social",
          "Declarație pe propria răspundere",
          "Cazier fiscal"
        ],
        note: ["Codul CAEN 4120 se înscrie în obiectul de activitate."],
        lege: "Legea nr. 31/1990"
      },
      {
        id: 2,
        titlu: "Atestare ISC — Inspectoratul de Stat în Construcții",
        institutie: "ISC — Inspectoratul de Stat în Construcții",
        institutie_url: "https://www.isc.gov.ro",
        cost: "Variabil (tarife ISC)",
        durata: "30–60 zile",
        obligatoriu: true,
        documente: [
          "Cerere de atestare",
          "Dovada calificării profesionale a personalului tehnic (ingineri, arhitecți)",
          "Lista dotărilor tehnice (utilaje, echipamente)",
          "Dovada experienței anterioare în construcții",
          "Asigurare de răspundere civilă profesională",
          "CV-urile responsabililor tehnici cu execuția (RTE) atestați"
        ],
        note: [
          "Firma de construcții trebuie să aibă cel puțin un Responsabil Tehnic cu Execuția (RTE) atestat ISC.",
          "Atestarea se face pe categorii și specialități de lucrări.",
          "Fără atestare ISC, firma NU poate executa legal lucrări de construcții."
        ],
        lege: "Legea nr. 10/1995 privind calitatea în construcții; HG nr. 925/1995; Ordinul MLPAT nr. 777/2003"
      },
      {
        id: 3,
        titlu: "Autorizarea Responsabililor Tehnici (RTE) — ISC",
        institutie: "ISC — Inspectoratul de Stat în Construcții",
        institutie_url: "https://www.isc.gov.ro",
        cost: "Tarife examen atestare ISC",
        durata: "60–90 zile (depinde de sesiunile de examinare)",
        obligatoriu: true,
        documente: [
          "Cerere de atestare RTE",
          "Diplomă de inginer/arhitect (copie legalizată)",
          "Carnet de muncă / Adeverință vechime minim 5 ani în specialitate",
          "Recomandare de la angajator",
          "Cazier judiciar",
          "Dovada plății tarifului de examinare"
        ],
        note: ["RTE trebuie atestat pe specialitățile corespunzătoare lucrărilor executate."],
        lege: "Legea nr. 10/1995; HG nr. 925/1995"
      },
      {
        id: 4,
        titlu: "Autorizația de Construire (pentru fiecare proiect)",
        institutie: "Primăria Municipiului Constanța — Direcția Urbanism",
        institutie_url: "https://www.primaria-constanta.ro",
        cost: "0,5% din valoarea lucrărilor + avize",
        durata: "30–60 zile",
        obligatoriu: true,
        documente: [
          "Cerere autorizație de construire",
          "Certificat de urbanism",
          "Proiect pentru autorizarea executării lucrărilor (PAC)",
          "Aviz ISU",
          "Aviz Mediu (dacă e cazul)",
          "Aviz Utilități (apă, gaz, electricitate)",
          "Titlul de proprietate asupra terenului"
        ],
        note: ["Autorizația de construire se obține PENTRU FIECARE ȘANTIER în parte, nu pentru firmă."],
        lege: "Legea nr. 50/1991"
      },
      {
        id: 5,
        titlu: "Înregistrare la Inspecția Muncii (șantier)",
        institutie: "ITM Constanța — Inspectoratul Teritorial de Muncă",
        institutie_url: "https://itm-constanta.ro",
        cost: "Gratuit",
        durata: "Înainte de începerea lucrărilor",
        obligatoriu: true,
        documente: [
          "Declarație prealabilă de deschidere a șantierului",
          "Planul de securitate și sănătate (PSS)",
          "Dovada desemnării Coordonatorului de securitate",
          "Lista subcontractorilor"
        ],
        note: ["Declarația prealabilă se depune cu cel puțin 30 de zile înainte de deschiderea șantierului."],
        lege: "HG nr. 300/2006 privind cerințele minime de securitate și sănătate pe șantiere"
      },
      {
        id: 6,
        titlu: "Autorizația de Mediu — APM Constanța",
        institutie: "APM Constanța — Agenția pentru Protecția Mediului",
        institutie_url: "http://apmct.anpm.ro",
        cost: "500 lei (tarif emitere autorizație) — OM nr. 865/2014",
        durata: "30–60 zile calendaristice",
        obligatoriu: true,
        documente: [
          "Fișa de prezentare și declarație (Anexa 2, OM nr. 1798/2007)",
          "Dovada publicității solicitării (anunț public — Anexa 3)",
          "Plan de situație și plan de încadrare în zonă",
          "Certificat constatator ONRC",
          "Dovada plății 500 lei (IBAN: RO03TREZ2315032XXX005043, Trezoreria Constanța, CIF: 1863832)",
          "Contracte de gestionare a deșeurilor de construcție și demolare",
          "Plan de gestionare a deșeurilor de șantier"
        ],
        note: [
          "⚠ OBLIGATORIE pentru activitatea de construcții (CAEN 4120) conform Anexei 1 la OM 1798/2007.",
          "Firmele de construcții trebuie să dețină autorizație de mediu pentru activitatea lor generală.",
          "Pe fiecare șantier: se respectă planul de gestionare a deșeurilor de construcție (Legea 292/2018).",
          "Deșeurile de construcție se predau exclusiv operatorilor autorizați ANPM.",
          "Autorizația este valabilă 5 ani de la emitere.",
          "APM Constanța: Str. Unirii nr. 23 | office@apmct.anpm.ro | 0241.546.696"
        ],
        lege: "OUG nr. 195/2005; OM nr. 1798/2007; OM nr. 865/2014; Legea nr. 292/2018 privind deșeurile; HG nr. 1061/2008"
      }
    ]
  },

  "5630": {
    name: "Baruri și alte activități de servire a băuturilor",
    sectiune: "HoReCa / Bar",
    steps: [
      {
        id: 1,
        titlu: "Înregistrare la ONRC",
        institutie: "ONRC — Oficiul Național al Registrului Comerțului",
        institutie_url: "https://www.onrc.ro",
        cost: "200–400 RON",
        durata: "3–5 zile lucrătoare",
        obligatoriu: true,
        documente: ["Cerere de înregistrare (formular tip ONRC)", "Actul constitutiv", "Dovada sediului social", "Specimen de semnătură administrator", "Cazier fiscal", "Dovada achitării taxelor"],
        note: ["Codul CAEN 5630 se înscrie în obiectul de activitate."],
        lege: "Legea nr. 31/1990; Legea nr. 26/1990"
      },
      {
        id: 2,
        titlu: "Autorizația de Securitate la Incendiu (ISU)",
        institutie: "ISU Dobrogea",
        institutie_url: "https://isudobrogea.ro",
        cost: "Gratuit",
        durata: "30 zile",
        obligatoriu: true,
        documente: ["Cerere aviz/autorizație PSI", "Documentație tehnică PSI semnată de proiectant atestat", "Scenariu securitate incendiu", "Planuri arhitecturale"],
        note: ["Obligatoriu pentru baruri cu acces public, indiferent de suprafață."],
        lege: "Legea nr. 307/2006; Ordinul MAI nr. 129/2016"
      },
      {
        id: 3,
        titlu: "Avizul Sanitar (DSP)",
        institutie: "DSP Constanța",
        institutie_url: "https://dspct.ro",
        cost: "400–500 lei — conform OMS nr. 1030/2009 mod. OMS nr. 458/2023: 400 lei (asistență specialitate/certificarea conformității) sau 500 lei (autorizație baza referatului). Viză anuală: 400 lei",
        durata: "15–30 zile",
        obligatoriu: true,
        documente: ["Dovada achitării tarifului — virament bancar în contul DSP Constanța la Trezorerie (CIF: 2952688)", "Cerere aviz sanitar", "Schița spațiului", "Memoriu tehnico-sanitar", "Contract salubritate", "Contract deratizare", "Dovada sursei de apă"],
        note: ["Avizul sanitar este condiție pentru deschidere."],
        lege: "Legea nr. 95/2006; Ordinul MS nr. 976/1998"
      },
      {
        id: 4,
        titlu: "Autorizația de funcționare — Primăria Constanța (DASOEC)",
        institutie: "Primăria Municipiului Constanța — Direcția Autorizare și Sprijin Operatori Economici",
        institutie_url: "https://www.primaria-constanta.ro",
        cost: "1.060–7.418 RON/an — conform HCLM nr. 412/2024, Anexa 9, Art. 3",
        durata: "15–30 zile",
        obligatoriu: true,
        documente: [
          "Cerere tip autorizație de funcționare",
          "Certificat de înregistrare ONRC",
          "Autorizație ISU",
          "Aviz DSP",
          "Contract închiriere / titlu proprietate",
          "Acordul asociației de proprietari (dacă e cazul)",
          "Dovada plății taxei"
        ],
        note: [
          "⚠ TAXE REALE conform HCLM nr. 412/2024, Anexa 9, Art. 3 lit. c) și d):",
          "▸ Bar (gr. 563) program până la 01:00 în Constanța — sub 100 mp: 1.060 lei/an; 100–500 mp: 2.650 lei/an; peste 500 mp: 5.298 lei/an",
          "▸ Bar (gr. 563) program PESTE 01:00 în Constanța — sub 500 mp: 3.710 lei/an; peste 500 mp: 7.418 lei/an",
          "▸ Bar în Stațiunea Mamaia / Sat Vacanță — sub 500 mp: 3.710 lei/an; peste 500 mp: 7.418 lei/an",
          "▸ Taxă sanitară suplimentară: 22 lei/an (Art. 13)",
          "Vizarea anuală implică aceeași taxă. Programul de funcționare se menționează în autorizație."
        ],
        lege: "HCLM nr. 412/2024, Anexa nr. 9, Art. 3 lit. c), d), f) și Art. 13; OG nr. 99/2000"
      },
      {
        id: 5,
        titlu: "Înregistrare Casa de Marcat (ANAF)",
        institutie: "ANAF — Administrația Financiară Constanța",
        institutie_url: "https://www.anaf.ro",
        cost: "Cost echipament: 1.500–4.000 RON",
        durata: "5–10 zile",
        obligatoriu: true,
        documente: ["Cerere înregistrare aparat marcat", "Cartea de intervenție", "Procesul-verbal de sigilare", "CIF", "Dovada adresei punctului de lucru"],
        note: ["Casă de marcat fiscalizată obligatorie pentru orice bar/local cu vânzări către public."],
        lege: "OUG nr. 28/1999"
      },
      {
        id: 6,
        titlu: "Autorizație-Licență Neexclusivă UCMR-ADA",
        institutie: "UCMR-ADA — Asociația pentru Drepturi de Autor a Compozitorilor",
        institutie_url: "https://ucmr-ada.ro",
        cost: "Variabil lunar (ambiental/lucrativ, în funcție de suprafață) — Decizia ORDA nr. 68/2025 (01.05.2025)",
        durata: "7 zile",
        obligatoriu: true,
        documente: ["Cerere autorizare (portal.ucmr-ada.ro)", "Copie CUI", "Date punct de lucru: suprafață, program, tip activitate"],
        note: [
          "Obligatorie pentru orice bar/club care difuzează muzică (ambiental sau cu DJ/artiști live).",
          "Plata lunară până pe data de 15 a lunii. Penalități 0,5%/zi întârziere.",
          "Baruri tip club/discotecă cu muzică în scop lucrativ au tarife mai mari — consultați metodologia spectacole/club."
        ],
        lege: "Legea nr. 8/1996; Decizia ORDA nr. 68/31.03.2025"
      },
      {
        id: 7,
        titlu: "Autorizație-Licență Neexclusivă UPFR",
        institutie: "UPFR — Uniunea Producătorilor de Fonograme din România",
        institutie_url: "https://upfr.ro",
        cost: "Variabil lunar — conform Decizia ORDA nr. 43/2025 (MO nr. 232/17.03.2025)",
        durata: "7–14 zile",
        obligatoriu: true,
        documente: ["Cerere autorizare (upfr.ro)", "Copie CUI", "Date punct de lucru"],
        note: [
          "Obligatorie separat de UCMR-ADA. Reprezintă producătorii de fonograme (case de discuri).",
          "Club/bar cu muzică în scop lucrativ: tarife specifice (Decizia ORDA 43/2025).",
          "Licența per punct de lucru, netransferabilă, până la 12 luni."
        ],
        lege: "Legea nr. 8/1996; Decizia ORDA nr. 43/2025"
      },
      {
        id: 8,
        titlu: "Autorizație-Licență Neexclusivă CREDIDAM",
        institutie: "CREDIDAM — Centrul Român pentru Administrarea Drepturilor Artiștilor Interpreți",
        institutie_url: "https://credidam.ro",
        cost: "Variabil — conform Decizia ORDA nr. 43/2025",
        durata: "7–14 zile",
        obligatoriu: true,
        documente: ["Declarație utilizator + Convenție (2 ex.) — modele pe credidam.ro", "Transmitere la office@credidam.ro"],
        note: [
          "Obligatorie separat de UCMR-ADA și UPFR. Reprezintă artiștii interpreți și executanți.",
          "Factură emisă la înregistrare; autorizație eliberată după confirmarea plății.",
          "Plată: trimestrial / semestrial (-3%) / anual (-5%). IBAN: RO23INGB0001000152938958."
        ],
        lege: "Legea nr. 8/1996; Decizia ORDA nr. 43/2025; Decizia ORDA nr. 10/2016"
      }
    ]
  },

  "8610": {
    name: "Activități de asistență spitalicească",
    sectiune: "Sănătate",
    steps: [
      {
        id: 1,
        titlu: "Înregistrare ONRC (dacă este unitate privată)",
        institutie: "ONRC",
        institutie_url: "https://www.onrc.ro",
        cost: "200–400 RON",
        durata: "3–5 zile",
        obligatoriu: true,
        documente: ["Cerere înregistrare", "Act constitutiv", "Dovada sediului", "Cazier fiscal"],
        note: ["Pentru spitale private — SRL sau SA. Spitalele publice sunt înregistrate altfel."],
        lege: "Legea nr. 31/1990"
      },
      {
        id: 2,
        titlu: "Autorizarea unității medicale — MS și DSP",
        institutie: "DSP Constanța + Ministerul Sănătății",
        institutie_url: "https://dspct.ro",
        cost: "Variabil",
        durata: "60–120 zile",
        obligatoriu: true,
        documente: [
          "Cerere de autorizare sanitară",
          "Proiectul de funcționare al unității medicale",
          "Dovada personalului medical calificat (diplome, autorizații exercitare)",
          "Lista dotărilor medicale",
          "Planul spațiilor cu destinație medicală",
          "Aviz ISU",
          "Contracte de sterilizare și gestionare deșeuri medicale",
          "Acord de funcționare Primărie"
        ],
        note: [
          "Autorizarea se face de către MS prin DSP.",
          "Tot personalul medical trebuie să aibă autorizație de liberă practică de la Colegiile profesionale (CMR, OAMGMAMR etc.)."
        ],
        lege: "Legea nr. 95/2006 privind reforma în domeniul sănătății; Ordinul MS nr. 914/2006"
      },
      {
        id: 3,
        titlu: "Autorizația de Securitate la Incendiu",
        institutie: "ISU Dobrogea",
        institutie_url: "https://isudobrogea.ro",
        cost: "Gratuit",
        durata: "30 zile",
        obligatoriu: true,
        documente: ["Documentație PSI completă", "Scenariu securitate incendiu", "Planuri arhitecturale"],
        note: ["Obligatoriu pentru orice unitate medicală, indiferent de dimensiune."],
        lege: "Legea nr. 307/2006; Ordinul MAI nr. 129/2016"
      },
      {
        id: 4,
        titlu: "Acreditarea ANMCS",
        institutie: "ANMCS — Autoritatea Națională de Management al Calității în Sănătate",
        institutie_url: "https://anmcs.gov.ro",
        cost: "Tarife ANMCS",
        durata: "6–12 luni",
        obligatoriu: true,
        documente: [
          "Dosarul de autoevaluare pe standardele ANMCS",
          "Politici și proceduri interne",
          "Dovada implementării sistemului de calitate",
          "Rapoarte de audit intern"
        ],
        note: ["Acreditarea ANMCS este obligatorie pentru intrare în sistemul de asigurări de sănătate."],
        lege: "Legea nr. 95/2006; OMS nr. 446/2017"
      }
    ]
  },

  "5510": {
    name: "Hoteluri și alte facilități de cazare similare",
    sectiune: "HoReCa / Cazare",
    steps: [
      {
        id: 1,
        titlu: "Înregistrare ONRC",
        institutie: "ONRC",
        institutie_url: "https://www.onrc.ro",
        cost: "200–400 RON",
        durata: "3–5 zile",
        obligatoriu: true,
        documente: ["Cerere înregistrare", "Act constitutiv", "Dovada sediului", "Cazier fiscal"],
        note: ["Codul CAEN 5510 se înscrie în obiectul de activitate."],
        lege: "Legea nr. 31/1990"
      },
      {
        id: 2,
        titlu: "Autorizația de Construire / Schimbare destinație",
        institutie: "Primăria Constanța — Direcția Urbanism",
        institutie_url: "https://www.primaria-constanta.ro",
        cost: "0,5% din valoarea lucrărilor",
        durata: "30–60 zile",
        obligatoriu: true,
        documente: ["PAC semnat de arhitect RUR", "Certificate urbanism", "Avize tehnice (utilități)", "Aviz ISU", "Aviz DSP"],
        note: ["Obligatorie dacă clădirea se construiește sau se reabilitează pentru cazare."],
        lege: "Legea nr. 50/1991"
      },
      {
        id: 3,
        titlu: "Certificatul de Clasificare — Ministerul Economiei, Antreprenoriatului și Turismului (MEAT)",
        institutie: "Ministerul Economiei, Antreprenoriatului și Turismului (MEAT) — Direcția Generală Turism",
        institutie_url: "https://se.situr.gov.ro/cms/",
        cost: "Fără taxă administrativă de clasificare (procedura este gratuită) — costurile sunt cele ale pregătirii documentației și eventualelor lucrări de conformare",
        durata: "30 zile (certificat provizoriu) + 30–60 zile (certificat definitiv după inspecție la fața locului)",
        obligatoriu: true,
        documente: [
          "Cerere standardizată (Anexa nr. 3 la Ordinul nr. 65/2013 cu modificările ulterioare)",
          "Certificat constatator extins ONRC — cu activitățile CAEN autorizate la punctul de lucru",
          "Fișă standardizată privind încadrarea nominală a spațiilor de cazare (Anexa nr. 4)",
          "Fișă standardizată privind structura spațiilor de alimentație publică, dacă există restaurant (Anexa nr. 5)",
          "Dovada proprietății sau a dreptului de folosință a imobilului (act proprietate, contract chirie, comodat)",
          "Planul clădirii cu numerotarea camerelor și destinația spațiilor",
          "Brevet de turism pentru directorul/managerul unității (conf. OG 58/1998, art. 15)",
          "Avizul de amplasament și funcționalitate MEAT (doar pentru construcții noi)",
          "Autorizație ISU — copie",
          "Fotografii reprezentative ale unității (recepție, camere, băi, restaurant dacă există)"
        ],
        note: [
          "⚠ OBLIGATORIU ÎNAINTE DE DESCHIDERE — hotelul nu poate funcționa legal fără certificat de clasificare (OG 58/1998, art. 30).",
          "În 30 de zile de la depunerea documentației complete se emite Autorizația Provizorie de Funcționare.",
          "Certificatul definitiv se emite după inspecția la fața locului a inspectorilor MEAT.",
          "Clasificarea se face pe stele: 1★ – 5★ (hotel) conform Ordinului MT nr. 65/2013 actualizat prin Ordinul nr. 985/2024.",
          "Dacă restaurantul/barul din hotel are CAEN 561/563 autorizat, clasificarea alimentației publice se include în aceeași procedură.",
          "Documentele se depun: ONLINE pe se.situr.gov.ro, prin poștă (Calea Victoriei nr. 152, sector 1, București) sau prin e-mail la clasificare.turism@economie.gov.ro.",
          "Reclasificarea se solicită la modificarea structurii sau la schimbarea operatorului economic.",
          "AMENZI: Funcționarea fără certificat de clasificare se sancționează cu amenzi între 10.000–20.000 lei (HG nr. 709/2009)."
        ],
        lege: "OG nr. 58/1998 privind organizarea și desfășurarea activității de turism; HG nr. 1267/2010 privind eliberarea certificatelor de clasificare; Ordinul ANT nr. 65/2013 (norme metodologice) modificat prin Ordinul MT nr. 1179/2018 și Ordinul nr. 985/2024; HG nr. 709/2009 privind sancțiunile"
      },
      {
        id: 4,
        titlu: "Autorizația de Securitate la Incendiu (ISU)",
        institutie: "ISU Dobrogea",
        institutie_url: "https://isudobrogea.ro",
        cost: "Gratuit",
        durata: "30 zile",
        obligatoriu: true,
        documente: ["Documentație PSI", "Scenariu securitate incendiu", "Planuri arhitecturale", "Declarație conformitate"],
        note: ["Obligatoriu pentru toate hotelurile. Condiție pentru clasificare."],
        lege: "Legea nr. 307/2006"
      },
      {
        id: 5,
        titlu: "Autorizația Sanitară de Funcționare (DSP)",
        institutie: "DSP Constanța — Direcția de Sănătate Publică",
        institutie_url: "https://dspct.ro",
        cost: "500 lei (autorizație sanitară în baza referatului de evaluare) — conform OMS nr. 1030/2009 mod. OMS nr. 458/2023. Viză anuală: 400 lei",
        durata: "15–30 zile",
        obligatoriu: true,
        documente: ["Cerere aviz sanitar", "Schița spațiilor", "Memoriu tehnico-sanitar", "Contract salubritate", "Contract deratizare"],
        note: ["⚠ TARIFE: 400 lei (asistență specialitate/certificare conformitate) sau 500 lei (autorizație în baza referatului de evaluare). Viză anuală: 400 lei.", "Plata prin virament bancar la Trezoreria Constanța.", "Vizează condițiile igienico-sanitare ale camerelor, bucătăriei, piscinei (dacă există).", "DSP Constanța: Aleea Lăcrămioarei nr. 1 / Str. Nicolae Iorga nr. 89 | secretariat@dspct.ro | Tel: 0241.838.330"],
        lege: "Legea nr. 95/2006; OMS nr. 1030/2009; OMS nr. 458/2023"
      },
      {
        id: 6,
        titlu: "Autorizația de Funcționare — Primăria Constanța",
        institutie: "Primăria Municipiului Constanța — Direcția Autorizare și Sprijin Operatori Economici",
        institutie_url: "https://www.primaria-constanta.ro",
        cost: "107 RON/an (aviz program funcționare hotel fără restaurant) + taxe separate pentru restaurantele din complex",
        durata: "15–30 zile",
        obligatoriu: true,
        documente: ["Cerere tip", "Certificat ONRC", "Autorizație ISU", "Aviz DSP", "Certificat clasificare MT", "Contract închiriere/proprietate"],
        note: [
          "⚠ TAXE REALE conform HCLM nr. 412/2024, Anexa 9, Art. 4 (complexuri hoteliere):",
          "▸ Aviz program funcționare hotel (structuri fără restaurant/bar în CAEN 561/563): 107 lei/an",
          "▸ Restaurant/bar în cadrul complexului hotelier — suprafață totală sub 100 mp: 1.060 lei; 100–250 mp: 2.120 lei; 250–500 mp: 4.239 lei; peste 500 mp: 8.477 lei/an",
          "▸ Activități recreative (gr. 932) în complex hotelier: 1.060–7.418 lei/an (după suprafață)",
          "Autorizația de funcționare se eliberează după obținerea clasificării Ministerului Turismului."
        ],
        lege: "HCLM nr. 412/2024, Anexa nr. 9, Art. 1 și Art. 4; OG nr. 99/2000"
      },
      {
        id: 7,
        titlu: "Înregistrare Turism la nivel local",
        institutie: "Primăria Constanța / Consiliul Județean Constanța",
        institutie_url: "https://www.primaria-constanta.ro",
        cost: "Taxă de promovare turistică variabilă",
        durata: "Odată cu autorizația de funcționare",
        obligatoriu: false,
        documente: ["Certificat de clasificare", "Certificat ONRC", "Cerere înregistrare"],
        note: ["Unitățile turistice din Constanța (zonă turistică) pot fi supuse taxei de promovare turistică."],
        lege: "Legea nr. 571/2003 (Codul Fiscal) — taxe locale"
      },
      {
        id: 8,
        titlu: "Autorizație-Licență Neexclusivă UCMR-ADA (muzică ambientală)",
        institutie: "UCMR-ADA — Asociația pentru Drepturi de Autor a Compozitorilor",
        institutie_url: "https://ucmr-ada.ro",
        cost: "Variabil lunar per cameră/suprafață — hoteluri: tarif calculat pe număr de camere + suprafețe comune — Decizia ORDA nr. 68/2025",
        durata: "7 zile",
        obligatoriu: true,
        documente: ["Cerere autorizare (portal.ucmr-ada.ro)", "CUI societate", "Date punct de lucru: nr. camere, clasificare turistică, suprafețe comune"],
        note: [
          "Obligatorie pentru orice hotel cu muzică în recepție, lobby, restaurant, lift, camere (TV/radio).",
          "Tariful pentru hoteluri se calculează separat față de restaurantul din cadrul hotelului.",
          "Consultați tabelul de tarife pentru unități de cazare pe ucmr-ada.ro (Decizia ORDA 68/2025, în vigoare 01.05.2025)."
        ],
        lege: "Legea nr. 8/1996; Decizia ORDA nr. 68/31.03.2025"
      },
      {
        id: 9,
        titlu: "Autorizație-Licență Neexclusivă UPFR (drepturi conexe fonograme — hotel)",
        institutie: "UPFR — Uniunea Producătorilor de Fonograme din România",
        institutie_url: "https://upfr.ro",
        cost: "Variabil lunar — unități de cazare: tarif per cameră sau global — Decizia ORDA nr. 43/2025",
        durata: "7–14 zile",
        obligatoriu: true,
        documente: ["Cerere autorizare (upfr.ro)", "CUI", "Nr. camere, clasificare, suprafețe"],
        note: [
          "Obligatorie separat de UCMR-ADA pentru fonogramele difuzate în spațiile hotelului.",
          "Dacă există restaurant/bar în hotel, acestea necesită autorizații UPFR separate."
        ],
        lege: "Legea nr. 8/1996; Decizia ORDA nr. 43/2025"
      },
      {
        id: 10,
        titlu: "Autorizație-Licență Neexclusivă CREDIDAM (drepturi artiști interpreți — hotel)",
        institutie: "CREDIDAM",
        institutie_url: "https://credidam.ro",
        cost: "Variabil — conform Decizia ORDA nr. 43/2025",
        durata: "7–14 zile",
        obligatoriu: true,
        documente: ["Declarație + Convenție utilizator (credidam.ro)", "Transmitere la office@credidam.ro"],
        note: [
          "A treia licență obligatorie pentru muzică — separat de UCMR-ADA și UPFR.",
          "Plată trimestrial/semestrial/anual. Autorizație emisă după confirmare plată."
        ],
        lege: "Legea nr. 8/1996; Decizia ORDA nr. 43/2025"
      },
      {
        id: 11,
        titlu: "Autorizația de Mediu — APM Constanța",
        institutie: "APM Constanța",
        institutie_url: "http://apmct.anpm.ro",
        cost: "500 lei (tarif emitere autorizație) — OM nr. 865/2014",
        durata: "30–60 zile",
        obligatoriu: false,
        documente: [
          "Fișa de prezentare și declarație (Anexa 2, OM 1798/2007)",
          "Dovada publicității solicitării",
          "Plan de situație și încadrare în zonă",
          "Certificat constatator ONRC",
          "Dovada plății 500 lei (IBAN: RO03TREZ2315032XXX005043, Trezoreria Constanța)"
        ],
        note: [
          "Hotelurile cu suprafețe mari, piscine, centrale termice proprii pot fi incluse în Anexa 1 OM 1798/2007.",
          "Autorizația este valabilă 5 ani.",
          "APM Constanța: Str. Unirii nr. 23 | office@apmct.anpm.ro | 0241.546.696"
        ],
        lege: "OUG nr. 195/2005; OM nr. 1798/2007; OM nr. 865/2014"
      }
    ]
  },

  "8531": {
    name: "Învățământ secundar, tehnic sau profesional",
    sectiune: "Educație",
    steps: [
      {
        id: 1,
        titlu: "Înregistrare ONRC (pentru unități private)",
        institutie: "ONRC",
        institutie_url: "https://www.onrc.ro",
        cost: "200–400 RON",
        durata: "3–5 zile",
        obligatoriu: true,
        documente: ["Cerere înregistrare", "Act constitutiv", "Dovada sediului", "Cazier fiscal"],
        note: [],
        lege: "Legea nr. 31/1990"
      },
      {
        id: 2,
        titlu: "Autorizarea / Acreditarea de la ARACIP sau MEN",
        institutie: "ARACIP — Agenția Română de Asigurare a Calității în Învățământul Preuniversitar",
        institutie_url: "https://www.aracip.eu",
        cost: "Variabil — tarife ARACIP",
        durata: "6–18 luni",
        obligatoriu: true,
        documente: [
          "Cerere de autorizare provizorie de funcționare",
          "Proiectul de dezvoltare instituțională",
          "Planul de școlarizare",
          "Dovada bazei materiale (clădiri, laboratoare, ateliere)",
          "Lista personalului didactic calificat",
          "Avizul ISU",
          "Avizul DSP",
          "Avizul Primăriei",
          "Regulamentul de organizare și funcționare"
        ],
        note: [
          "Prima etapă: autorizare provizorie (3 ani).",
          "A doua etapă: acreditare (evaluare completă ARACIP).",
          "Acreditarea este necesară pentru emiterea diplomelor recunoscute de stat."
        ],
        lege: "Legea Educației Naționale nr. 1/2011; OG nr. 75/2005; HG nr. 1534/2008"
      },
      {
        id: 3,
        titlu: "Avizul ISU",
        institutie: "ISU Dobrogea",
        institutie_url: "https://isudobrogea.ro",
        cost: "Gratuit",
        durata: "30 zile",
        obligatoriu: true,
        documente: ["Documentație PSI", "Planuri arhitecturale", "Scenariu securitate incendiu"],
        note: ["Obligatoriu pentru orice instituție educațională."],
        lege: "Legea nr. 307/2006"
      }
    ]
  },

  "4941": {
    name: "Transporturi rutiere de mărfuri",
    sectiune: "Transport",
    steps: [
      {
        id: 1,
        titlu: "Înregistrare ONRC",
        institutie: "ONRC",
        institutie_url: "https://www.onrc.ro",
        cost: "200–400 RON",
        durata: "3–5 zile",
        obligatoriu: true,
        documente: ["Cerere înregistrare", "Act constitutiv", "Dovada sediului", "Cazier fiscal"],
        note: [],
        lege: "Legea nr. 31/1990"
      },
      {
        id: 2,
        titlu: "Licența de transport / Copie conformă — ARR",
        institutie: "ARR — Autoritatea Rutieră Română (Agenția Constanța)",
        institutie_url: "https://www.arr.ro",
        cost: "Taxe ARR: 500–2.000 RON (variabil)",
        durata: "30–60 zile",
        obligatoriu: true,
        documente: [
          "Cerere eliberare licență de transport",
          "Certificat de competență profesională al managerului de transport (CPC)",
          "Cazier judiciar manager transport",
          "Dovada situației financiare (capital minim 9.000 EUR pentru primul vehicul)",
          "Extras de cont bancar sau garanție bancară",
          "Dovada sediului/garajului",
          "Copia conformă pentru fiecare vehicul (certificat de înmatriculare, ITP valabil, asigurare RCA)"
        ],
        note: [
          "Managerul de transport trebuie să aibă Certificat de Competență Profesională (CPC) pentru transport rutier de mărfuri.",
          "Capacitatea financiară: min. 9.000 EUR pentru primul vehicul + 5.000 EUR pentru fiecare vehicul suplimentar.",
          "Licența de transport se eliberează de ARR și este valabilă 10 ani.",
          "Copia conformă se obține pentru fiecare vehicul."
        ],
        lege: "Regulamentul CE nr. 1071/2009; OG nr. 27/2011 privind transporturile rutiere"
      },
      {
        id: 3,
        titlu: "Inspecția Tehnică Periodică (ITP) și omologarea vehiculelor",
        institutie: "RAR — Registrul Auto Român / Stații ITP autorizate",
        institutie_url: "https://www.rarom.ro",
        cost: "100–500 RON/vehicul",
        durata: "1 zi",
        obligatoriu: true,
        documente: ["Certificat de înmatriculare", "Talonul vehiculului", "Asigurare RCA valabilă"],
        note: ["ITP obligatoriu anual pentru vehicule comerciale >3,5 t.", "Tahograful trebuie verificat periodic."],
        lege: "OUG nr. 195/2002 privind circulația pe drumurile publice; Directiva 2014/45/UE"
      },
      {
        id: 4,
        titlu: "Autorizare activitate ADR (transport mărfuri periculoase — dacă e cazul)",
        institutie: "ARR + Inspectoratul General al Poliției Române",
        institutie_url: "https://www.arr.ro",
        cost: "Variabil",
        durata: "30–60 zile",
        obligatoriu: false,
        documente: ["Certificat de pregătire ADR al șoferilor", "Certificat de conformitate vehicul ADR"],
        note: ["Obligatoriu DOAR dacă transportați mărfuri periculoase (chimice, inflamabile etc.)."],
        lege: "ADR 2023 (Acordul european privind transportul rutier internațional de mărfuri periculoase)"
      },
      {
        id: 5,
        titlu: "Autorizația de Mediu — APM Constanța",
        institutie: "APM Constanța — Agenția pentru Protecția Mediului",
        institutie_url: "http://apmct.anpm.ro",
        cost: "500 lei (tarif emitere autorizație) — OM nr. 865/2014",
        durata: "30–60 zile calendaristice",
        obligatoriu: true,
        documente: [
          "Fișa de prezentare și declarație (Anexa 2, OM nr. 1798/2007)",
          "Dovada publicității solicitării",
          "Plan de situație (sediu/garaj/punct de lucru)",
          "Certificat constatator ONRC",
          "Dovada plății 500 lei (IBAN: RO03TREZ2315032XXX005043, Trezoreria Constanța, CIF: 1863832)",
          "Contracte gestionare deșeuri (uleiuri uzate, anvelope, acumulatori — firme autorizate)"
        ],
        note: [
          "CAEN 4941 (transport rutier mărfuri) este inclus în Anexa 1 la OM 1798/2007 — autorizație de mediu obligatorie.",
          "Firmele de transport trebuie să gestioneze corect deșeurile generate: uleiuri uzate, filtre, anvelope uzate.",
          "Contracte obligatorii cu firme autorizate ANPM pentru colectarea deșeurilor specifice.",
          "Autorizația este valabilă 5 ani.",
          "APM Constanța: Str. Unirii nr. 23 | office@apmct.anpm.ro | 0241.546.696"
        ],
        lege: "OUG nr. 195/2005; OM nr. 1798/2007; OM nr. 865/2014; Legea nr. 211/2011 privind deșeurile"
      }
    ]
  },

  "8621": {
    name: "Activități de asistență medicală generală",
    sectiune: "Sănătate — Cabinet Medical",
    steps: [
      {
        id: 1,
        titlu: "Înregistrare ONRC (Cabinet Medical Individual sau Asociat)",
        institutie: "ONRC",
        institutie_url: "https://www.onrc.ro",
        cost: "100–300 RON",
        durata: "3–5 zile",
        obligatoriu: true,
        documente: ["Cerere înregistrare cabinet medical", "Statut CMI/SMP", "Dovada sediului", "Autorizație exercitare CMR"],
        note: ["Cabinetele medicale individuale (CMI) se înregistrează conform OG 124/1998."],
        lege: "OG nr. 124/1998 privind organizarea și funcționarea cabinetelor medicale"
      },
      {
        id: 2,
        titlu: "Autorizația de liberă practică — CMR",
        institutie: "CMR — Colegiul Medicilor din România (Filiala Constanța)",
        institutie_url: "https://cmr.ro",
        cost: "Taxe CMR",
        durata: "30 zile",
        obligatoriu: true,
        documente: [
          "Diploma de medic (copie legalizată)",
          "Certificat de rezidențiat sau specializare",
          "Certificat de sănătate",
          "Cazier judiciar",
          "Dovada asigurării de malpraxis",
          "Fotografie tip buletin"
        ],
        note: ["Fără autorizație de liberă practică de la CMR, medicul nu poate funcționa legal."],
        lege: "Legea nr. 95/2006; Statutul CMR"
      },
      {
        id: 3,
        titlu: "Autorizația Sanitară de Funcționare (DSP)",
        institutie: "DSP Constanța — Direcția de Sănătate Publică",
        institutie_url: "https://dspct.ro",
        cost: "500 lei (autorizație sanitară în baza referatului de evaluare, obligatorie pentru cabinete medicale) — conform OMS nr. 1030/2009 mod. OMS nr. 458/2023. Viză anuală: 400 lei",
        durata: "15–30 zile",
        obligatoriu: true,
        documente: [
          "Cerere aviz cabinet medical",
          "Schița spațiului (cameră consultații, sală de așteptare, grup sanitar)",
          "Lista echipamentelor medicale",
          "Autorizație CMR a medicului",
          "Contract gestionare deșeuri medicale (firmă autorizată)"
        ],
        note: [
          "⚠ TARIF: 500 lei (autorizație sanitară în baza referatului de evaluare — obligatorie pentru cabinete medicale). Viză anuală: 400 lei.",
          "Plata prin virament bancar la Trezoreria Constanța.",
          "DSP verifică condițiile de igienă, suprafețele minime, circuitele funcționale.",
          "Suprafața minimă a sălii de consultații: 12 mp (conform normelor în vigoare).",
          "DSP Constanța: Aleea Lăcrămioarei nr. 1 | secretariat@dspct.ro | Tel: 0241.838.330"
        ],
        lege: "Ordinul MS nr. 914/2006; Ordinul MS nr. 975/1998; OMS nr. 1030/2009; OMS nr. 458/2023"
      },
      {
        id: 4,
        titlu: "Autorizația de Securitate la Incendiu (ISU) — dacă e cazul",
        institutie: "ISU Dobrogea",
        institutie_url: "https://isudobrogea.ro",
        cost: "Gratuit",
        durata: "30 zile",
        obligatoriu: false,
        documente: ["Documentație PSI", "Planuri spații"],
        note: ["Obligatoriu pentru cabinete cu >50 mp sau internare. Cabinetele mici pot fi exceptate."],
        lege: "Legea nr. 307/2006"
      }
    ]
  },

  "6201": {
    name: "Activități de realizare a soft-ului la comandă (software orientat client)",
    sectiune: "IT — Servicii Software",
    steps: [
      {
        id: 1,
        titlu: "Înregistrare ONRC",
        institutie: "ONRC",
        institutie_url: "https://www.onrc.ro",
        cost: "200–400 RON",
        durata: "3–5 zile",
        obligatoriu: true,
        documente: ["Cerere înregistrare", "Act constitutiv", "Dovada sediului", "Cazier fiscal"],
        note: ["IT-ul are avantajul că nu necesită avize speciale pentru activitate de birou."],
        lege: "Legea nr. 31/1990"
      },
      {
        id: 2,
        titlu: "Scutire de impozit pe venit pentru angajați IT (opțional)",
        institutie: "ANAF + Ministerul Comunicațiilor",
        institutie_url: "https://www.anaf.ro",
        cost: "Gratuit",
        durata: "10–15 zile",
        obligatoriu: false,
        documente: [
          "Cerere înregistrare pentru scutire IT",
          "Lista angajaților programatori",
          "Dovada că activitatea principală este în domeniul IT",
          "Contractele de muncă ale programatorilor"
        ],
        note: [
          "Angajații IT (programatori) beneficiază de scutire de impozit pe venit conform Codului Fiscal.",
          "Condiție: angajatorul trebuie să aibă CAEN principal în IT și să realizeze efectiv activitate IT.",
          "Verificați condițiile actualizate pe site-ul ANAF."
        ],
        lege: "Art. 60 pct. 2 din Codul Fiscal; Legea nr. 227/2015"
      },
      {
        id: 3,
        titlu: "Înregistrare GDPR la ANSPDCP",
        institutie: "ANSPDCP — Autoritatea Națională de Supraveghere a Prelucrării Datelor cu Caracter Personal",
        institutie_url: "https://www.dataprotection.ro",
        cost: "Gratuit",
        durata: "Online, imediat",
        obligatoriu: true,
        documente: [
          "Înregistrare operator de date pe platforma ANSPDCP",
          "Politica de confidențialitate documentată",
          "Registrul activităților de prelucrare",
          "Evaluarea impactului (DPIA) — dacă se prelucrează date sensibile",
          "Desemnare DPO (Responsabil cu Protecția Datelor) — dacă e cazul"
        ],
        note: [
          "Orice firmă IT care procesează date personale trebuie să respecte GDPR.",
          "DPO obligatoriu dacă prelucrați date la scară largă sau date sensibile.",
          "Amenzile pentru neconformare pot ajunge la 20 milioane EUR sau 4% din cifra de afaceri globală."
        ],
        lege: "Regulamentul UE 679/2016 (GDPR); Legea nr. 190/2018"
      },
      {
        id: 4,
        titlu: "Autorizație de funcționare la Primăria Constanța (pentru sediu/punct de lucru)",
        institutie: "Primăria Municipiului Constanța",
        institutie_url: "https://www.primaria-constanta.ro",
        cost: "50–200 RON/an",
        durata: "15–30 zile",
        obligatoriu: true,
        documente: ["Cerere tip", "Certificat ONRC", "Contract spațiu", "Aviz ISU (dacă e cazul)"],
        note: ["Pentru birouri mici în clădiri de birouri, de regulă nu e necesară autorizație ISU separată."],
        lege: "OG nr. 99/2000"
      }
    ]
  }
};

// CAEN list for search
const CAEN_LIST = [
  { cod: "5610", nume: "Restaurante" },
  { cod: "5621", nume: "Activități de alimentație (catering) pentru evenimente" },
  { cod: "5629", nume: "Alte servicii de alimentație n.c.a." },
  { cod: "5630", nume: "Baruri și alte activități de servire a băuturilor" },
  { cod: "5510", nume: "Hoteluri și alte facilități de cazare similare" },
  { cod: "5520", nume: "Facilități de cazare pentru vacanțe și perioade de scurtă durată" },
  { cod: "5530", nume: "Parcuri pentru rulote, campinguri și tabere" },
  { cod: "4711", nume: "Comerț cu amănuntul — alimentar (magazine nespecializate)" },
  { cod: "4712", nume: "Comerț cu amănuntul în magazine nespecializate, cu vânzare predominantă de produse nealimentare" },
  { cod: "4721", nume: "Comerț cu amănuntul al fructelor și legumelor proaspete" },
  { cod: "4722", nume: "Comerț cu amănuntul al cărnii și al produselor din carne" },
  { cod: "4724", nume: "Comerț cu amănuntul al pâinii, produselor de patiserie și zaharoaselor" },
  { cod: "4730", nume: "Comerț cu amănuntul al carburanților pentru autovehicule" },
  { cod: "4741", nume: "Comerț cu amănuntul al calculatoarelor, echipamentelor periferice și software-ului" },
  { cod: "4751", nume: "Comerț cu amănuntul al textilelor" },
  { cod: "4761", nume: "Comerț cu amănuntul al cărților" },
  { cod: "4771", nume: "Comerț cu amănuntul al îmbrăcămintei" },
  { cod: "4775", nume: "Comerț cu amănuntul al produselor cosmetice și de toaletă" },
  { cod: "4776", nume: "Comerț cu amănuntul al florilor, plantelor și semințelor" },
  { cod: "4779", nume: "Comerț cu amănuntul al bunurilor de ocazie vândute prin magazine" },
  { cod: "4120", nume: "Lucrări de construcție a clădirilor rezidențiale și nerezidențiale" },
  { cod: "4211", nume: "Lucrări de construcție a drumurilor și autostrăzilor" },
  { cod: "4321", nume: "Lucrări de instalații electrice" },
  { cod: "4322", nume: "Lucrări de instalații sanitare, de încălzire și de aer condiționat" },
  { cod: "4331", nume: "Lucrări de ipsoserie" },
  { cod: "4332", nume: "Tâmplărie și dulgherie" },
  { cod: "4339", nume: "Alte lucrări de finisare" },
  { cod: "4941", nume: "Transporturi rutiere de mărfuri" },
  { cod: "4950", nume: "Transporturi prin conducte" },
  { cod: "5221", nume: "Activități de servicii anexe transporturilor terestre" },
  { cod: "4932", nume: "Transporturi cu taxiuri" },
  { cod: "4931", nume: "Transporturi urbane și suburbane de călători" },
  { cod: "8610", nume: "Activități de asistență spitalicească" },
  { cod: "8621", nume: "Activități de asistență medicală generală" },
  { cod: "8622", nume: "Activități de asistență medicală specializată" },
  { cod: "8623", nume: "Activități de asistență stomatologică" },
  { cod: "8690", nume: "Alte activități referitoare la sănătatea umană" },
  { cod: "8531", nume: "Învățământ secundar, tehnic sau profesional" },
  { cod: "8551", nume: "Cursuri sportive și recreative" },
  { cod: "8553", nume: "Școli de conducere (pilotaj)" },
  { cod: "8559", nume: "Alte forme de învățământ" },
  { cod: "6201", nume: "Activități de realizare a soft-ului la comandă" },
  { cod: "6202", nume: "Activități de consultanță în tehnologia informației" },
  { cod: "6209", nume: "Alte activități de servicii privind tehnologia informației" },
  { cod: "6311", nume: "Prelucrarea datelor, administrarea paginilor web și activități conexe" },
  { cod: "7111", nume: "Activități de arhitectură" },
  { cod: "7112", nume: "Activități de inginerie și consultanță tehnică" },
  { cod: "6910", nume: "Activități juridice" },
  { cod: "6920", nume: "Activități de contabilitate și audit financiar" },
  { cod: "7021", nume: "Activități de consultanță în domeniul relațiilor publice și al comunicării" },
  { cod: "7022", nume: "Activități de consultanță pentru afaceri și management" },
  { cod: "9601", nume: "Spălarea și curățarea (uscată) a articolelor textile și a blănurilor" },
  { cod: "9602", nume: "Coafură și alte activități de înfrumusețare" },
  { cod: "9604", nume: "Activități de întreținere corporală" },
  { cod: "9311", nume: "Activități ale bazelor sportive" },
  { cod: "9313", nume: "Activități ale centrelor de fitness" },
  { cod: "9321", nume: "Bâlciuri și parcuri de distracții" },
  { cod: "9329", nume: "Alte activități recreative și distractive n.c.a." },
  { cod: "4520", nume: "Întreținerea și repararea autovehiculelor" },
  { cod: "4531", nume: "Comerț cu ridicata de piese și accesorii pentru autovehicule" },
  { cod: "4711", nume: "Comerț cu amănuntul în magazine nespecializate cu produse alimentare" },
  { cod: "0111", nume: "Cultivarea cerealelor (exclusiv orez), plantelor leguminoase și a plantelor producătoare de semințe oleaginoase" },
  { cod: "1011", nume: "Prelucrarea și conservarea cărnii" },
  { cod: "1050", nume: "Fabricarea produselor lactate" },
  { cod: "1071", nume: "Fabricarea pâinii; fabricarea prăjiturilor și produselor proaspete de patiserie" }
];

// Generic fallback for codes not in CAEN_DB
function getGenericSteps(cod, name) {
  return {
    name,
    sectiune: "Activitate Generală",
    steps: [
      {
        id: 1,
        titlu: "Înregistrare la ONRC",
        institutie: "ONRC — Oficiul Național al Registrului Comerțului",
        institutie_url: "https://www.onrc.ro",
        cost: "200–400 RON",
        durata: "3–5 zile lucrătoare",
        obligatoriu: true,
        documente: [
          "Cerere de înregistrare (formular tip ONRC)",
          "Actul constitutiv / Statut societate",
          "Dovada sediului social",
          "Specimen de semnătură administrator",
          "Declarație pe propria răspundere privind autorizarea funcționării",
          "Cazier fiscal al asociaților și administratorilor",
          "Dovada achitării taxelor"
        ],
        note: ["Înregistrarea se poate efectua online pe portalul ONRC sau la ghișeu."],
        lege: "Legea nr. 31/1990 privind societățile comerciale; Legea nr. 26/1990"
      },
      {
        id: 2,
        titlu: "Autorizația de Securitate la Incendiu — ISU Dobrogea",
        institutie: "ISU Dobrogea — Inspectoratul pentru Situații de Urgență",
        institutie_url: "https://isudobrogea.ro",
        cost: "Gratuit",
        durata: "30 zile calendaristice",
        obligatoriu: true,
        documente: [
          "Cerere aviz/autorizație PSI",
          "Documentație tehnică PSI semnată de proiectant atestat",
          "Scenariul de securitate la incendiu",
          "Planuri de arhitectură ale spațiului"
        ],
        note: ["Necesară pentru spații > 100 mp sau unde accesul publicului este permis."],
        lege: "Legea nr. 307/2006; Ordinul MAI nr. 129/2016"
      },
      {
        id: 3,
        titlu: "Autorizația / Avizul Program de Funcționare — Primăria Constanța",
        institutie: "Primăria Municipiului Constanța — Direcția Autorizare și Sprijin Operatori Economici",
        institutie_url: "https://www.primaria-constanta.ro",
        cost: "107 RON/an (comerț/servicii generale) | 1.060–7.418 RON/an (HoReCa: restaurante gr.561, baruri gr.563, recreere gr.932) — HCLM nr. 412/2024",
        durata: "15–30 zile",
        obligatoriu: true,
        documente: [
          "Cerere tip",
          "Certificat de înregistrare ONRC",
          "Avizele obținute anterior (ISU, DSP etc.)",
          "Contract de închiriere / titlu proprietate",
          "Dovada plății taxei de autorizare"
        ],
        note: [
          "⚠ TAXE REALE conform HCLM nr. 412/2024, Anexa nr. 9 (în vigoare 01.01.2025):",
          "▸ Comerț și servicii generale (altele decât gr. 561/563/932): 107 lei/an (Art. 1 alin. 1)",
          "▸ Restaurante gr. 561, program până la 01:00: 1.060 lei (sub 100 mp) / 2.650 lei (100–500 mp) / 5.298 lei (peste 500 mp)",
          "▸ Restaurante gr. 561, program PESTE 01:00: 3.710 lei (sub 500 mp) / 7.418 lei (peste 500 mp)",
          "▸ Baruri gr. 563, program până la 01:00: 1.060–5.298 lei; program PESTE 01:00: 3.710–7.418 lei",
          "▸ Activități recreative gr. 932: 1.060–7.418 lei (după suprafață)",
          "▸ Taxă sanitară de funcționare: 22 lei/an (suplimentar, Art. 13)",
          "Verificați Anexa 9 la HCLM nr. 412/2024 pe primaria-constanta.ro pentru situația dvs. specifică."
        ],
        lege: "HCLM nr. 412/2024, Anexa nr. 9; OG nr. 99/2000 privind comercializarea produselor și serviciilor de piață"
      },
      {
        id: 4,
        titlu: "Verificare cerințe specifice domeniului de activitate",
        institutie: "Instituții specifice domeniului (DSP, DSVSA, ARR, ISC etc.)",
        institutie_url: "https://www.primaria-constanta.ro",
        cost: "Variabil",
        durata: "Variabil",
        obligatoriu: true,
        documente: [
          "Verificați pe site-urile instituțiilor de specialitate documentele necesare",
          "DSP — pentru activități cu impact sanitar",
          "DSVSA — pentru activități cu produse alimentare de origine animală",
          "ARR — pentru transport rutier",
          "ISC — pentru construcții"
        ],
        note: [
          `Codul CAEN ${cod} (${name}) poate necesita autorizații specifice în funcție de natura exactă a activității.`,
          "Consultați ghidul ONRC și site-urile instituțiilor relevante pentru lista completă.",
          "Recomandăm consultarea unui avocat sau consultant specializat pentru activități complexe."
        ],
        lege: "Verificați legislația specifică domeniului pe site-ul gov.ro sau legislatie.just.ro"
      }
    ]
  };
}

// =============================================
// UI LOGIC
// =============================================

let currentCaen = null;

const searchInput = document.getElementById('searchInput');
const dropdown = document.getElementById('dropdown');
const mainContent = document.getElementById('mainContent');

searchInput.addEventListener('input', function() {
  const val = this.value.trim().toLowerCase();
  if (!val || val.length < 1) {
    dropdown.classList.remove('show');
    return;
  }
  const filtered = CAEN_LIST.filter(c =>
    c.cod.includes(val) || c.nume.toLowerCase().includes(val)
  ).slice(0, 12);

  if (filtered.length === 0) {
    dropdown.classList.remove('show');
    return;
  }

  dropdown.innerHTML = filtered.map(c => `
    <div class="caen-item" onclick="selectCaen('${c.cod}', '${c.nume.replace(/'/g, "\\'")}')">
      <span class="caen-code-tag">${c.cod}</span>
      <span class="caen-name">${c.nume}</span>
    </div>
  `).join('');
  dropdown.classList.add('show');
});

document.addEventListener('click', function(e) {
  if (!e.target.closest('.search-input-wrap')) {
    dropdown.classList.remove('show');
  }
});

function selectCaen(cod, name) {
  searchInput.value = `${cod} — ${name}`;
  dropdown.classList.remove('show');
  renderResult(cod, name);
}

function clearSearch() {
  searchInput.value = '';
  dropdown.classList.remove('show');
  mainContent.innerHTML = `
    <div class="placeholder-state">
      <div class="icon">🏛</div>
      <h3>Selectați o activitate CAEN</h3>
      <p>Căutați codul CAEN sau denumirea activității pentru a vedea lista completă de avize și autorizații necesare în Constanța.</p>
    </div>`;
}

function renderResult(cod, name) {
  const data = CAEN_DB[cod] || getGenericSteps(cod, name);
  
  const totalCost = estimateTotalCost(data.steps);
  const totalDays = estimateTotalDays(data.steps);
  const required = data.steps.filter(s => s.obligatoriu).length;
  const optional = data.steps.filter(s => !s.obligatoriu).length;

  const stepsHTML = data.steps.map((step, i) => `
    <div class="step-card" id="step-${i}">
      <div class="step-header" onclick="toggleStep(${i})">
        <div class="step-num">${step.id}</div>
        <div class="step-info">
          <div class="step-name">${step.titlu}</div>
          <div class="step-inst">${step.institutie}</div>
        </div>
        <div class="step-tags">
          <span class="tag tag-cost">💰 ${step.cost}</span>
          <span class="tag tag-time">⏱ ${step.durata}</span>
          ${step.obligatoriu ? '<span class="tag tag-required">OBLIGATORIU</span>' : '<span class="tag" style="background:rgba(100,100,100,0.08);color:#666;border:1px solid #ccc;">OPȚIONAL</span>'}
        </div>
        <span class="chevron">▾</span>
      </div>
      <div class="step-body">
        <div class="step-body-inner">
          <div class="docs-section">
            <h4>Acte Necesare</h4>
            <ul class="doc-list">
              ${step.documente.map(d => `<li>${d}</li>`).join('')}
            </ul>
          </div>
          <div class="docs-section">
            <h4>Informații Suplimentare</h4>
            ${step.note.map(n => `<div class="note-box">${n}</div>`).join('')}
            <div class="note-box law">
              <strong>Temei legal:</strong><br>${step.lege}
            </div>
            <div class="link-row">
              <a class="link-btn" href="${step.institutie_url}" target="_blank" rel="noopener">↗ ${step.institutie_url.replace('https://','').replace('http://','')}</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  `).join('');

  mainContent.innerHTML = `
    <div class="fade-in">
      <div class="result-header">
        <div class="result-title">
          <h2>${data.name}</h2>
          <p>Sectiune: ${data.sectiune} · Municipiul Constanța</p>
        </div>
        <div class="caen-badge">CAEN ${cod}</div>
      </div>

      <div class="summary-grid">
        <div class="summary-card">
          <div class="num">${data.steps.length}</div>
          <div class="lbl">Etape Totale</div>
        </div>
        <div class="summary-card">
          <div class="num">${required}</div>
          <div class="lbl">Obligatorii</div>
        </div>
        <div class="summary-card">
          <div class="num">${optional}</div>
          <div class="lbl">Opționale</div>
        </div>
        <div class="summary-card">
          <div class="num" style="font-size:15px;padding-top:6px;line-height:1.3">${totalCost}</div>
          <div class="lbl">Cost Inițial Estimat</div>
        </div>
        <div class="summary-card">
          <div class="num" style="font-size:14px;padding-top:6px;line-height:1.3">${totalDays}</div>
          <div class="lbl">Durată Obținere</div>
        </div>
      </div>

      <div class="steps-title">Etape în ordinea obținerii</div>
      ${stepsHTML}

      <div class="legend">
        <h3>Instituții implicate · Contacte utile Constanța</h3>
        <div class="institutions-grid">
          <div class="inst-item"><div class="inst-dot"></div><div><div class="inst-name">ONRC Constanța</div><div class="inst-desc">onrc.ro · B-dul Tomis 101</div></div></div>
          <div class="inst-item"><div class="inst-dot"></div><div><div class="inst-name">Primăria Constanța</div><div class="inst-desc">primaria-constanta.ro · Bd. Tomis 51</div></div></div>
          <div class="inst-item"><div class="inst-dot"></div><div><div class="inst-name">ISU Dobrogea</div><div class="inst-desc">isudobrogea.ro · Str. Cuza Vodă 29</div></div></div>
          <div class="inst-item"><div class="inst-dot"></div><div><div class="inst-name">DSP Constanța</div><div class="inst-desc">dspct.ro · Aleea Lăcrămioarei 1, Str. Nicolae Iorga 89</div></div></div>
          <div class="inst-item"><div class="inst-dot"></div><div><div class="inst-name">DSVSA Constanța</div><div class="inst-desc">dsvsa-constanta.ro · Str. Eliberării 77</div></div></div>
          <div class="inst-item"><div class="inst-dot"></div><div><div class="inst-name">APM Constanța</div><div class="inst-desc">apmct.anpm.ro · Str. Unirii 23 · 0241.546.696</div></div></div>
          <div class="inst-item"><div class="inst-dot"></div><div><div class="inst-name">ARR Constanța</div><div class="inst-desc">arr.ro · Agenția Regională Constanța</div></div></div>
          <div class="inst-item"><div class="inst-dot"></div><div><div class="inst-name">ITM Constanța</div><div class="inst-desc">itm-constanta.ro · Str. Mihai Eminescu 58</div></div></div>
          <div class="inst-item"><div class="inst-dot"></div><div><div class="inst-name">ANAF / Finanțe Publice CT</div><div class="inst-desc">anaf.ro · Str. Mircea cel Bătrân 66</div></div></div>
          <div class="inst-item"><div class="inst-dot"></div><div><div class="inst-name">ANPC Constanța</div><div class="inst-desc">anpc.ro · Comisariatul Județean CT</div></div></div>
          <div class="inst-item"><div class="inst-dot"></div><div><div class="inst-name">UCMR-ADA (Drepturi Autor Muzică)</div><div class="inst-desc">ucmr-ada.ro · portal.ucmr-ada.ro</div></div></div>
          <div class="inst-item"><div class="inst-dot"></div><div><div class="inst-name">UPFR (Producători Fonograme)</div><div class="inst-desc">upfr.ro · Decizia ORDA nr. 43/2025</div></div></div>
          <div class="inst-item"><div class="inst-dot"></div><div><div class="inst-name">CREDIDAM (Artiști Interpreți)</div><div class="inst-desc">credidam.ro · office@credidam.ro</div></div></div>
        </div>
      </div>

      <div style="margin-top:24px;padding:16px;background:rgba(200,146,42,0.06);border:1px solid rgba(200,146,42,0.2);border-radius:6px;font-size:12.5px;color:#666;line-height:1.6;">
        ⚠ <strong>Atenție:</strong> Informațiile prezentate sunt orientative și bazate pe legislația în vigoare la data elaborării. Cerințele se pot modifica. Verificați întotdeauna pe site-urile oficiale ale instituțiilor enumerate și consultați un specialist (avocat, consultant ONRC) pentru situația dvs. specifică. Costurile indicate sunt estimate și pot varia în funcție de specificul activității, dimensiunea spațiului și alte criterii stabilite de fiecare instituție. <strong>Costul inițial estimat include taxele de înregistrare/autorizare, dar NU include costurile recurente lunare (UCMR-ADA, UPFR, CREDIDAM, vize anuale), onorariile proiectanților sau costul echipamentelor.</strong>
      </div>
    </div>
  `;
}

function toggleStep(i) {
  const card = document.getElementById('step-' + i);
  card.classList.toggle('open');
}

function estimateTotalCost(steps) {
  // Extract costs more intelligently
  // We'll collect min and max values from each obligatory step
  let totalMin = 0;
  let totalMax = 0;
  let hasVariable = false;

  steps.forEach(s => {
    if (!s.obligatoriu) return;
    const costStr = s.cost;

    // Skip purely variable costs (music rights etc) but flag them
    if (/variabil|lunar|lună|procent|%/i.test(costStr) && !/\d{3,}/.test(costStr)) {
      hasVariable = true;
      return;
    }

    // Extract all numbers from the cost string (handle dots as thousand separators)
    const nums = costStr.match(/\d[\d.]*\d|\d/g);
    if (!nums) { hasVariable = true; return; }

    const parsed = nums.map(n => parseInt(n.replace(/\./g, ''))).filter(n => n > 0 && n < 100000);
    if (parsed.length === 0) { hasVariable = true; return; }

    // Take min of extracted numbers as minimum cost, max as maximum
    const stepMin = Math.min(...parsed);
    const stepMax = Math.max(...parsed);
    totalMin += stepMin;
    totalMax += stepMax;
  });

  if (totalMin === 0 && !hasVariable) return 'Verificați instituțiile';

  const fmtMin = totalMin.toLocaleString('ro');
  const fmtMax = totalMax.toLocaleString('ro');

  let result = '';
  if (totalMin > 0 && totalMax > totalMin) {
    result = `${fmtMin}–${fmtMax} RON`;
  } else if (totalMin > 0) {
    result = `~${fmtMin} RON`;
  }

  if (hasVariable) result += result ? ' + redevențe lunare' : 'Parțial variabil';
  return result || 'Variabil';
}

function estimateTotalDays(steps) {
  let totalMin = 0;
  let totalMax = 0;
  steps.forEach(s => {
    const nums = s.durata.match(/\d+/g);
    if (nums) {
      totalMin += parseInt(nums[0]);
      totalMax += parseInt(nums[nums.length - 1]);
    }
  });
  if (totalMin === 0) return 'Variabil';
  const mMin = Math.round(totalMin / 30 * 10) / 10;
  const mMax = Math.round(totalMax / 30 * 10) / 10;
  if (totalMin === totalMax) return `~${totalMin} zile (≈${mMin} luni)`;
  return `${totalMin}–${totalMax} zile (≈${mMin}–${mMax} luni)`;
}

</script>
</body>
</html>
