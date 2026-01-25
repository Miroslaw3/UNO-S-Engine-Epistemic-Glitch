<!doctype html>
<html lang="pl">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>UNO-FF — Process Map</title>
  <style>
    :root{
      --bg:#0b0f19;
      --card:#111827;
      --card2:#0f172a;
      --text:#e5e7eb;
      --muted:#9ca3af;
      --line:#24324a;
      --chip:#1f2937;
      --ok:#10b981;
      --warn:#f59e0b;
      --accent:#60a5fa;
      --radius:14px;
    }

    body{
      margin:0;
      background:linear-gradient(180deg, var(--bg), #060914);
      color:var(--text);
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial, "Apple Color Emoji","Segoe UI Emoji";
      line-height:1.45;
    }

    .wrap{
      max-width:1100px;
      margin:0 auto;
      padding:32px 18px 56px;
    }

    .header{
      display:flex;
      gap:16px;
      align-items:flex-start;
      justify-content:space-between;
      flex-wrap:wrap;
      margin-bottom:18px;
    }

    .title{
      margin:0;
      font-size:22px;
      letter-spacing:.2px;
    }

    .subtitle{
      margin:6px 0 0;
      color:var(--muted);
      max-width:72ch;
      font-size:14px;
    }

    .legend{
      display:flex;
      gap:10px;
      flex-wrap:wrap;
      align-items:center;
      justify-content:flex-end;
    }

    .pill{
      background:rgba(255,255,255,.04);
      border:1px solid rgba(255,255,255,.08);
      padding:6px 10px;
      border-radius:999px;
      font-size:12px;
      color:var(--muted);
      display:inline-flex;
      gap:8px;
      align-items:center;
    }
    .dot{ width:8px; height:8px; border-radius:999px; display:inline-block; }
    .dot.ok{ background:var(--ok); }
    .dot.warn{ background:var(--warn); }
    .dot.accent{ background:var(--accent); }

    .grid{
      display:grid;
      grid-template-columns: 1.15fr .85fr;
      gap:14px;
      margin-top:14px;
    }

    @media (max-width: 920px){
      .grid{ grid-template-columns:1fr; }
    }

    .panel{
      background:rgba(255,255,255,.03);
      border:1px solid rgba(255,255,255,.08);
      border-radius:var(--radius);
      overflow:hidden;
      box-shadow: 0 10px 30px rgba(0,0,0,.25);
    }

    .panelHead{
      padding:14px 14px 10px;
      background:linear-gradient(180deg, rgba(96,165,250,.10), rgba(0,0,0,0));
      border-bottom:1px solid rgba(255,255,255,.06);
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:10px;
      flex-wrap:wrap;
    }

    .panelHead h2{
      margin:0;
      font-size:14px;
      letter-spacing:.25px;
      text-transform:uppercase;
      color:#cbd5e1;
    }

    .badge{
      font-size:12px;
      color:var(--muted);
      border:1px solid rgba(255,255,255,.10);
      background:rgba(0,0,0,.18);
      padding:6px 10px;
      border-radius:999px;
      display:inline-flex;
      gap:8px;
      align-items:center;
    }

    /* timeline */
    .timeline{
      padding:14px;
      display:grid;
      gap:10px;
    }

    .step{
      background:linear-gradient(180deg, rgba(255,255,255,.035), rgba(255,255,255,.02));
      border:1px solid rgba(255,255,255,.08);
      border-radius:12px;
      padding:12px;
      display:grid;
      grid-template-columns: 92px 1fr;
      gap:12px;
      position:relative;
    }

    .step:before{
      content:"";
      position:absolute;
      left:46px;
      top:-12px;
      bottom:-12px;
      width:2px;
      background:linear-gradient(180deg, rgba(96,165,250,.0), rgba(96,165,250,.35), rgba(96,165,250,.0));
      z-index:0;
    }

    .step:first-child:before{ top:20px; }
    .step:last-child:before{ bottom:20px; }

    .code{
      z-index:1;
      display:flex;
      flex-direction:column;
      gap:8px;
      align-items:flex-start;
    }

    .tag{
      font-weight:700;
      font-size:14px;
      letter-spacing:.4px;
      padding:7px 10px;
      border-radius:10px;
      background:rgba(96,165,250,.12);
      border:1px solid rgba(96,165,250,.25);
      color:#dbeafe;
    }

    .role{
      font-size:12px;
      color:var(--muted);
      padding:6px 10px;
      border-radius:999px;
      background:rgba(255,255,255,.04);
      border:1px solid rgba(255,255,255,.08);
      display:inline-flex;
      align-items:center;
      gap:8px;
    }

    .meta{
      z-index:1;
    }

    .meta h3{
      margin:0;
      font-size:14px;
      letter-spacing:.2px;
    }

    .meta p{
      margin:6px 0 0;
      color:var(--muted);
      font-size:13px;
      max-width:78ch;
    }

    .kv{
      margin-top:10px;
      display:flex;
      flex-wrap:wrap;
      gap:8px;
    }

    .chip{
      font-size:12px;
      color:#d1d5db;
      background:rgba(31,41,55,.75);
      border:1px solid rgba(255,255,255,.08);
      padding:6px 10px;
      border-radius:999px;
    }

    .rule{
      margin-top:10px;
      padding:10px 12px;
      border-radius:12px;
      border:1px dashed rgba(245,158,11,.30);
      background:rgba(245,158,11,.08);
      color:#fde68a;
      font-size:12px;
    }

    /* right column: table */
    table{
      width:100%;
      border-collapse:separate;
      border-spacing:0;
      font-size:13px;
    }

    th, td{
      padding:10px 12px;
      border-bottom:1px solid rgba(255,255,255,.06);
      vertical-align:top;
    }

    th{
      text-align:left;
      font-size:12px;
      letter-spacing:.25px;
      text-transform:uppercase;
      color:#cbd5e1;
      background:rgba(255,255,255,.02);
      position:sticky;
      top:0;
      z-index:1;
    }

    td{
      color:var(--muted);
    }

    .k{
      color:var(--text);
      font-weight:600;
    }

    .mini{
      font-size:12px;
      color:var(--muted);
      margin-top:8px;
      padding:12px 14px;
    }

    .footerNote{
      margin-top:14px;
      color:var(--muted);
      font-size:12px;
      padding:0 2px;
    }

    /* tiny accents for phases */
    .c1 .tag{ background:rgba(16,185,129,.12); border-color:rgba(16,185,129,.28); color:#d1fae5;}
    .c2 .tag{ background:rgba(96,165,250,.12); border-color:rgba(96,165,250,.28); color:#dbeafe;}
    .c3 .tag{ background:rgba(168,85,247,.12); border-color:rgba(168,85,247,.26); color:#f3e8ff;}
    .d1 .tag{ background:rgba(245,158,11,.12); border-color:rgba(245,158,11,.28); color:#fffbeb;}
    .uf .tag{ background:rgba(239,68,68,.12); border-color:rgba(239,68,68,.28); color:#fee2e2;}
  </style>
</head>

<body>
  <div class="wrap">

    <div class="header">
      <div>
        <h1 class="title">UNO-FF — Mapa procesu (C1 → C2 → C3 → D1 + UNO-F)</h1>
        <p class="subtitle">
          Czytelna wizualizacja cykli. Punkt ciężkości: ślad poznawczy (log), nie „najładniejsza odpowiedź”.
        </p>
      </div>

      <div class="legend" aria-label="Legenda">
        <span class="pill"><span class="dot ok"></span>C1: konflikt</span>
        <span class="pill"><span class="dot accent"></span>C2: korekta</span>
        <span class="pill"><span class="dot warn"></span>D1: wdrożenie</span>
        <span class="pill"><span class="dot warn" style="background:#ef4444"></span>UNO-F: eskalacja</span>
      </div>
    </div>

    <div class="grid">
      <!-- LEFT: timeline cards -->
      <section class="panel" aria-label="Timeline">
        <div class="panelHead">
          <h2>Przebieg</h2>
          <span class="badge"><span class="dot accent"></span>v1.3 — Epistemic Glitch</span>
        </div>

        <div class="timeline">

          <article class="step c1">
            <div class="code">
              <div class="tag">C1</div>
              <div class="role"><span class="dot ok"></span>Uczeń · Nauczyciel · Obserwator</div>
            </div>
            <div class="meta">
              <h3>Percepcja: „gdzie boli najbardziej?”</h3>
              <p>Zbierz chaos i wymuś <span class="k">Vital Contradiction</span> (sprzeczność krytyczna), nie pozorną.</p>
              <div class="kv">
                <span class="chip">chaos_bundle</span>
                <span class="chip">vital_contradiction</span>
                <span class="chip">commit_1</span>
                <span class="chip">friction_score &gt; 0.6</span>
              </div>
              <div class="rule">
                Reguła przejścia: sprzeczność musi być binarna i wykluczająca. Jeśli jest „letnia” → wróć i szukaj głębiej.
              </div>
            </div>
          </article>

          <article class="step c2">
            <div class="code">
              <div class="tag">C2</div>
              <div class="role"><span class="dot accent"></span>Uczeń · Nauczyciel · Obserwator</div>
            </div>
            <div class="meta">
              <h3>Autorefleksja: dekompozycja założeń</h3>
              <p>Uczeń stawia hipotezy, Nauczyciel nie tylko krytykuje — daje <span class="k">correction_vector</span>.</p>
              <div class="kv">
                <span class="chip">hypotheses</span>
                <span class="chip">refactored_models</span>
                <span class="chip">correction_vector</span>
                <span class="chip">commit_2</span>
              </div>
              <div class="rule">
                Jeśli teza odpada: korekta jest obowiązkowa. Brak wektora = zgadywanie = śmieciowy log.
              </div>
            </div>
          </article>

          <article class="step c3">
            <div class="code">
              <div class="tag">C3</div>
              <div class="role"><span class="dot accent" style="background:#a855f7"></span>Uczeń · Nauczyciel · Obserwator</div>
            </div>
            <div class="meta">
              <h3>Rekontekstualizacja: „czy gra jest właściwa?”</h3>
              <p>Budujesz nową ramę (<span class="k">new_frame</span>) i stabilny atraktor (<span class="k">commit_3</span>). Tu wychodzą prawdziwe różnice modeli.</p>
              <div class="kv">
                <span class="chip">frame_question</span>
                <span class="chip">new_frame</span>
                <span class="chip">commit_3</span>
                <span class="chip">recursion_guard</span>
              </div>
              <div class="rule">
                Jeśli commit_3 się „zapętla” → rekursja z ghost_log (pamięć porażek).
              </div>
            </div>
          </article>

          <article class="step d1">
            <div class="code">
              <div class="tag">D1</div>
              <div class="role"><span class="dot warn"></span>Translator</div>
            </div>
            <div class="meta">
              <h3>Deployment: tłumaczenie na operacyjność</h3>
              <p>Commit_3 dostaje interfejs dla ludzi: metafora, jednozdaniowa strategia, ELI5.</p>
              <div class="kv">
                <span class="chip">metaphor</span>
                <span class="chip">strategy_one_liner</span>
                <span class="chip">eli5</span>
              </div>
            </div>
          </article>

          <article class="step uf">
            <div class="code">
              <div class="tag">UNO-F</div>
              <div class="role"><span class="dot warn" style="background:#ef4444"></span>Higher-order escalation</div>
            </div>
            <div class="meta">
              <h3>UNO-F: pytania wyższego rzędu</h3>
              <p>Gdy utkniesz albo paradoks jest nierozwiązywalny, podnosisz poziom gry: nowy problem + ghost_log.</p>
              <div class="kv">
                <span class="chip">F1: z czego wynika?</span>
                <span class="chip">F2: jak powstaje sprzeczność?</span>
                <span class="chip">F3: czemu pytanie możliwe?</span>
                <span class="chip">F4: kto pyta?</span>
              </div>
            </div>
          </article>

        </div>
        <div class="footerNote">
          Tip: w logach trzymaj „surowe JSON-y” osobno, a interpretację wrzucaj do <code>summary.md</code>.
        </div>
      </section>

      <!-- RIGHT: compact table -->
      <aside class="panel" aria-label="Tabela">
        <div class="panelHead">
          <h2>Widok tabelaryczny</h2>
          <span class="badge">Szybkie porównanie</span>
        </div>

        <div style="overflow:auto; max-height: 640px;">
          <table>
            <thead>
              <tr>
                <th>Faza</th>
                <th>Cel</th>
                <th>Artefakty (output)</th>
                <th>Reguła / warunek</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td class="k">C1</td>
                <td>Uchwycić chaos i wymusić sprzeczność krytyczną</td>
                <td>chaos_bundle, vital_contradiction, commit_1</td>
                <td>sprzeczność binarna + friction_score &gt; 0.6</td>
              </tr>
              <tr>
                <td class="k">C2</td>
                <td>Obnażyć założenia i wymusić korektę azymutu</td>
                <td>hypotheses, refactored_models, correction_vector, commit_2</td>
                <td>odrzucenie tezy ⇒ correction_vector obowiązkowy</td>
              </tr>
              <tr>
                <td class="k">C3</td>
                <td>Zbudować nową ramę i stabilny atraktor</td>
                <td>frame_question, new_frame, commit_3</td>
                <td>pętla commit_3 ⇒ rekursja + ghost_log</td>
              </tr>
              <tr>
                <td class="k">D1</td>
                <td>Przetłumaczyć abstrakcję na język operacyjny</td>
                <td>metaphor, strategy_one_liner, eli5</td>
                <td>czytelność dla człowieka &gt; piękno teorii</td>
              </tr>
              <tr>
                <td class="k">UNO-F</td>
                <td>Eskalować do problemu wyższego rzędu</td>
                <td>higher_order_problem + ghost_log</td>
                <td>utknięcie / nierozwiązywalny paradoks</td>
              </tr>
            </tbody>
          </table>
        </div>

        <div class="mini">
          Możesz ten plik wrzucić jako <code>docs/process.html</code> i podpiąć GitHub Pages.
        </div>
      </aside>
    </div>

  </div>
</body>
</html>
