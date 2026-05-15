# apestein
<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>JEFFREY APESTEIN — THE APE FILES</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Special+Elite&family=Oswald:wght@500;700&family=IBM+Plex+Mono:wght@400;600&display=swap" rel="stylesheet">
<style>
  :root{
    --paper:#e9e1cf;
    --paper-2:#d8ccb0;
    --ink:#1a1411;
    --red:#c2241c;
    --red-dark:#8a1812;
    --black:#0c0a09;
  }

*{box-sizing:border-box;margin:0;padding:0}
html,body{background:var(–paper);color:var(–ink);font-family:‘IBM Plex Mono’,monospace;overflow-x:hidden}

body::before{
content:””;position:fixed;inset:0;pointer-events:none;z-index:1;
background-image:
radial-gradient(circle at 20% 30%, rgba(120,80,40,.08), transparent 40%),
radial-gradient(circle at 80% 70%, rgba(80,40,20,.10), transparent 50%);
}
body::after{
content:””;position:fixed;inset:0;pointer-events:none;z-index:2;opacity:.20;
background-image:url(“data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='200' height='200'><filter id='n'><feTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='2' seed='3'/><feColorMatrix values='0 0 0 0 0.2 0 0 0 0 0.15 0 0 0 0 0.1 0 0 0 0.4 0'/></filter><rect width='200' height='200' filter='url(%23n)'/></svg>”);
mix-blend-mode:multiply;
}

.topbar{
position:relative;z-index:5;background:var(–black);color:var(–paper);
padding:8px 20px;font-size:11px;letter-spacing:.2em;
display:flex;justify-content:space-between;align-items:center;
border-bottom:2px solid var(–red);text-transform:uppercase;
}
.topbar .blink{color:var(–red);animation:blink 1.2s steps(2) infinite}
@keyframes blink{50%{opacity:0}}

/* ===== HERO ===== */
.hero{
position:relative;z-index:5;max-width:1200px;margin:0 auto;
padding:80px 40px 60px;text-align:center;
border-bottom:3px double var(–ink);
}
.hero .stamp-classified{
position:absolute;top:30px;right:30px;
font-family:‘Oswald’,sans-serif;font-weight:700;color:var(–red);
border:5px solid var(–red);padding:6px 22px;font-size:32px;letter-spacing:.15em;
transform:rotate(8deg);opacity:.88;
}
.hero .stamp-sealed{
position:absolute;top:40px;left:30px;
font-family:‘Oswald’,sans-serif;font-weight:700;color:var(–red);
border:4px solid var(–red);padding:4px 18px;font-size:22px;letter-spacing:.2em;
transform:rotate(-6deg);opacity:.85;
}
.hero .eyebrow{
font-family:‘Special Elite’,monospace;font-size:14px;
letter-spacing:.4em;color:var(–red);margin-bottom:14px;
}
.hero h1{
font-family:‘Oswald’,sans-serif;font-weight:700;
font-size:clamp(56px,11vw,160px);line-height:.9;
letter-spacing:-.02em;text-transform:uppercase;
}
.hero h1 .red{color:var(–red)}
.hero .subtitle{
margin-top:20px;font-family:‘Special Elite’,monospace;
font-size:18px;letter-spacing:.05em;
}
.hero .redact{background:var(–ink);color:transparent;padding:0 10px;user-select:none;cursor:help}
.hero .quote{
margin:40px auto 0;max-width:700px;
border-left:4px solid var(–red);padding:14px 22px;text-align:left;
font-family:‘Special Elite’,monospace;font-style:italic;font-size:16px;
background:rgba(0,0,0,.04);
}
.hero .quote .red{color:var(–red);font-weight:700;font-style:normal}

.marquee{
overflow:hidden;white-space:nowrap;background:var(–red);color:var(–paper);
padding:12px 0;font-family:‘Oswald’,sans-serif;font-weight:700;letter-spacing:.3em;
font-size:14px;border-bottom:2px solid var(–ink);position:relative;z-index:5;
}
.marquee-track{display:inline-block;animation:scroll 30s linear infinite}
.marquee-track span{margin:0 30px}
@keyframes scroll{from{transform:translateX(0)}to{transform:translateX(-50%)}}

/* ===== DOSSIER ===== */
.dossier{
position:relative;z-index:5;max-width:1100px;margin:40px auto;
padding:40px 50px;background:var(–paper);border:2px solid var(–ink);
box-shadow:0 20px 60px rgba(0,0,0,.25);
}
.file-header{
display:flex;justify-content:space-between;align-items:flex-start;
border-bottom:3px double var(–ink);padding-bottom:14px;margin-bottom:24px;
font-family:‘Special Elite’,monospace;font-size:13px;flex-wrap:wrap;gap:14px;
}
.file-header strong{font-family:‘Oswald’,sans-serif;letter-spacing:.1em}
.file-header .right{text-align:right}

.dossier h3{
font-family:‘Oswald’,sans-serif;font-weight:700;letter-spacing:.2em;
font-size:18px;margin-bottom:14px;text-transform:uppercase;
border-bottom:2px solid var(–ink);padding-bottom:6px;
}
.dossier dl{display:grid;grid-template-columns:200px 1fr;gap:10px 20px;font-family:‘Special Elite’,monospace}
.dossier dt{font-weight:700;text-transform:uppercase;font-size:13px;letter-spacing:.1em;padding-top:3px}
.dossier dd{font-size:15px}
.redact-line{background:var(–ink);color:transparent;padding:0 6px;user-select:none;cursor:help}

/* ===== CONTRACT ===== */
.ca-block{
margin:40px auto;max-width:1100px;background:var(–ink);color:var(–paper);
border:2px solid var(–red);padding:28px 30px;position:relative;z-index:5;
box-shadow:8px 8px 0 var(–red);
}
.ca-label{
font-family:‘Oswald’,sans-serif;letter-spacing:.4em;font-size:13px;color:var(–red);
margin-bottom:12px;
}
.ca-row{display:flex;gap:14px;align-items:center;flex-wrap:wrap}
.ca-value{
flex:1;min-width:240px;font-family:‘IBM Plex Mono’,monospace;font-size:18px;
background:rgba(255,255,255,.06);padding:14px 18px;border:1px dashed var(–paper-2);
word-break:break-all;letter-spacing:.02em;color:var(–paper);
}
.ca-value.empty{color:#9d9485;font-style:italic}
.copy-btn{
background:var(–red);color:var(–paper);border:none;font-family:‘Oswald’,sans-serif;
font-weight:700;letter-spacing:.2em;padding:14px 22px;font-size:14px;cursor:pointer;
transition:transform .15s, background .15s;
}
.copy-btn:hover{background:var(–red-dark);transform:translate(-2px,-2px)}
.copy-btn:active{transform:translate(1px,1px)}
.ca-hint{
margin-top:14px;font-size:11px;letter-spacing:.2em;color:#9d9485;text-transform:uppercase;
}
.pump-link{color:var(–red);text-decoration:underline;text-underline-offset:3px}

/* ===== FILE CARDS ===== */
.files{max-width:1100px;margin:50px auto;position:relative;z-index:5}
.file-card{
background:var(–paper);border:2px solid var(–ink);padding:30px 36px;
margin-bottom:30px;position:relative;box-shadow:6px 6px 0 rgba(0,0,0,.2);
}
.file-card .file-tag{
position:absolute;top:-14px;left:24px;background:var(–paper);
border:2px solid var(–ink);padding:4px 14px;
font-family:‘Oswald’,sans-serif;font-weight:700;letter-spacing:.2em;font-size:12px;
}
.file-card h2{
font-family:‘Oswald’,sans-serif;font-weight:700;
font-size:clamp(28px,4vw,42px);letter-spacing:.03em;
text-transform:uppercase;margin-bottom:18px;line-height:1;
}
.file-card h2 .red{color:var(–red)}
.file-card p{
font-family:‘Special Elite’,monospace;font-size:16px;line-height:1.7;margin-bottom:14px;
}
.typed{
background:rgba(0,0,0,.04);border-left:4px solid var(–red);
padding:14px 18px;margin:18px 0;font-family:‘Special Elite’,monospace;font-style:italic;
}

.timeline{list-style:none;font-family:‘Special Elite’,monospace;font-size:15px;line-height:1.9}
.timeline li{padding-left:140px;position:relative;margin-bottom:10px}
.timeline li::before{
content:attr(data-date);position:absolute;left:0;top:0;
font-family:‘Oswald’,sans-serif;font-weight:700;letter-spacing:.1em;font-size:13px;color:var(–red);
}

.associates{display:grid;grid-template-columns:repeat(auto-fit,minmax(180px,1fr));gap:14px;margin-top:18px}
.associate{border:1px solid var(–ink);padding:12px;text-align:center;background:rgba(255,255,255,.3)}
.associate .name{font-family:‘Oswald’,sans-serif;font-weight:700;letter-spacing:.1em;font-size:14px}
.associate .role{font-family:‘Special Elite’,monospace;font-size:12px;margin-top:4px;color:#5a4030}

.tokenomics{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:18px;margin-top:14px}
.token-card{border:2px solid var(–ink);padding:18px;text-align:center;background:rgba(255,255,255,.2)}
.token-card .num{font-family:‘Oswald’,sans-serif;font-weight:700;font-size:36px;color:var(–red);line-height:1}
.token-card .lbl{font-family:‘Special Elite’,monospace;font-size:13px;margin-top:8px;letter-spacing:.05em}

.cta-block{
max-width:1100px;margin:60px auto;padding:50px 30px;text-align:center;
background:var(–ink);color:var(–paper);position:relative;z-index:5;
border:2px solid var(–red);
}
.cta-block h2{
font-family:‘Oswald’,sans-serif;font-weight:700;
font-size:clamp(36px,6vw,72px);letter-spacing:.02em;text-transform:uppercase;line-height:1;
}
.cta-block h2 .red{color:var(–red)}
.cta-block p{
font-family:‘Special Elite’,monospace;margin:18px 0 30px;font-size:16px;letter-spacing:.05em;
}
.cta-buttons{display:flex;gap:14px;justify-content:center;flex-wrap:wrap}
.btn-primary,.btn-secondary{
font-family:‘Oswald’,sans-serif;font-weight:700;letter-spacing:.2em;
padding:16px 28px;font-size:14px;cursor:pointer;text-decoration:none;display:inline-block;
transition:transform .15s;
}
.btn-primary{background:var(–red);color:var(–paper);border:2px solid var(–red)}
.btn-secondary{background:transparent;color:var(–paper);border:2px solid var(–paper)}
.btn-primary:hover,.btn-secondary:hover{transform:translate(-2px,-2px)}

footer{
max-width:1100px;margin:40px auto 20px;padding:20px;position:relative;z-index:5;
border-top:2px solid var(–ink);font-family:‘Special Elite’,monospace;font-size:12px;
display:flex;justify-content:space-between;flex-wrap:wrap;gap:14px;color:#5a4030;
}

.toast{
position:fixed;bottom:30px;left:50%;transform:translateX(-50%) translateY(120%);
background:var(–ink);color:var(–paper);padding:14px 24px;
font-family:‘Oswald’,sans-serif;letter-spacing:.2em;font-size:13px;
border:2px solid var(–red);z-index:100;transition:transform .3s;
}
.toast.show{transform:translateX(-50%) translateY(0)}
</style>

</head>
<body>

<div class="topbar">
  <span>FILE 001 / DEPT. CHIMERA / PROJECT PRIMATE</span>
  <span><span class="blink">●</span> LIVE FEED — DECLASSIFIED 05.16.2026</span>
</div>

<!-- HERO -->

<section class="hero">
  <div class="stamp-classified">CLASSIFIED</div>
  <div class="stamp-sealed">SEALED</div>
  <div class="eyebrow">— THE OFFICIAL DOSSIER —</div>
  <h1>JEFFREY <span class="red">APESTEIN</span></h1>
  <div class="subtitle">
    Banker. Primate. <span class="redact">[REDACTED]</span>. Friend of <span class="redact">[REDACTED]</span>.
  </div>
  <div class="quote">
    <span class="red">"</span>The ape files will remain sealed for national security reasons.<span class="red">"</span><br>
    — Director [REDACTED], Classified Division
  </div>
</section>

<div class="marquee">
  <div class="marquee-track">
    <span>★ THE APE FILES HAVE BEEN LEAKED ★</span>
    <span>★ $APESTEIN DID NOT KILL HIMSELF ★</span>
    <span>★ FOLLOW THE BANANAS ★</span>
    <span>★ CLIENT LIST WHEN ★</span>
    <span>★ THE APE FILES HAVE BEEN LEAKED ★</span>
    <span>★ $APESTEIN DID NOT KILL HIMSELF ★</span>
    <span>★ FOLLOW THE BANANAS ★</span>
    <span>★ CLIENT LIST WHEN ★</span>
  </div>
</div>

<!-- DOSSIER -->

<section class="dossier">
  <div class="file-header">
    <div>
      <strong>CASE FILE:</strong> JA-001-PRIMATE<br>
      <strong>SUBJECT:</strong> APESTEIN, JEFFREY<br>
      <strong>STATUS:</strong> <span style="color:var(--red)">AT LARGE — ON-CHAIN</span>
    </div>
    <div class="right">
      <strong>JURISDICTION:</strong> SOLANA<br>
      <strong>DIVISION:</strong> PUMP.FUN<br>
      <strong>CLEARANCE:</strong> DEGEN ONLY
    </div>
  </div>

  <h3>SUBJECT PROFILE</h3>
  <dl>
    <dt>Alias</dt><dd>"The Silverback of Wall Street"</dd>
    <dt>Species</dt><dd>Homo Sapiens-Primate Hybrid (unconfirmed)</dd>
    <dt>Occupation</dt><dd>Financier / Island Proprietor / <span class="redact-line">[REDACTED]</span></dd>
    <dt>Known For</dt><dd>Allegedly never killing himself</dd>
    <dt>Last Seen</dt><dd>Cell block B, <span class="redact-line">[REDACTED]</span></dd>
    <dt>Net Worth</dt><dd>$0.000000420 and climbing</dd>
    <dt>Favorite Fruit</dt><dd>Pumped bananas</dd>
    <dt>The Files</dt><dd>Will be released. Eventually. Allegedly.</dd>
  </dl>
</section>

<!-- CONTRACT -->

<section class="ca-block" id="contract">
  <div class="ca-label">▶ EVIDENCE TAG #001 — CONTRACT ADDRESS</div>
  <div class="ca-row">
    <div class="ca-value empty" id="ca-text">[PASTE CONTRACT ADDRESS HERE AFTER LAUNCH]</div>
    <button class="copy-btn" id="copy-btn">COPY CA</button>
  </div>
  <div class="ca-hint">
    LAUNCHING ON <a href="https://pump.fun" target="_blank" class="pump-link">PUMP.FUN</a> — TO UPDATE, OPEN INDEX.HTML AND REPLACE THE TEXT INSIDE <code style="color:var(--red)">id="ca-text"</code>
  </div>
</section>

<section class="files">

  <div class="file-card">
    <div class="file-tag">FILE 002 — THE LORE</div>
    <h2>Who is <span class="red">Jeffrey Apestein</span>?</h2>
    <p>Born in a private banana plantation off the coast of <span class="redact-line">[REDACTED]</span>, Jeffrey Apestein rose from humble origins to become the most powerful primate in modern finance. They say he had connections to <span class="redact-line">[REDACTED]</span>, <span class="redact-line">[REDACTED]</span>, and at least three sitting <span class="redact-line">[REDACTED]</span>.</p>
    <div class="typed">"He didn't just know the room. He owned the zoo." — Anonymous source, formerly of [REDACTED]</div>
    <p>But the chain remembers. The blockchain is the only ledger he could not bribe. And now, after years of cover-ups, hush money in bananas, and missing surveillance tapes — <strong>$APESTEIN</strong> is on Solana.</p>
  </div>

  <div class="file-card">
    <div class="file-tag">FILE 003 — TIMELINE</div>
    <h2>Known <span class="red">Movements</span></h2>
    <ul class="timeline">
      <li data-date="1953">Subject born. Hospital records destroyed.</li>
      <li data-date="1987">First spotted on the floor of the NYSE wearing a three-piece suit and a banana boutonnière.</li>
      <li data-date="2001">Founds Apestein Capital. Office: a single enormous tree in lower Manhattan.</li>
      <li data-date="2008">Survives financial crisis. Bonuses paid in 100% pure Madagascan banana.</li>
      <li data-date="2019">Arrested. <span class="redact-line">[REDACTED]</span>. Does not <span class="redact-line">[REDACTED]</span>.</li>
      <li data-date="2024">Sighted in Venice. Surveillance tapes go missing within 48 hours.</li>
      <li data-date="2026">Returns. On-chain. Holding a bag. The bag is full of bananas. The bananas are full of alpha.</li>
    </ul>
  </div>

  <div class="file-card">
    <div class="file-tag">FILE 004 — KNOWN ASSOCIATES</div>
    <h2>The <span class="red">Client List</span></h2>
    <p>Forensic accountants have recovered partial records. Many names are redacted. Some names are bananas.</p>
    <div class="associates">
      <div class="associate"><div class="name">[REDACTED]</div><div class="role">Hedge Fund</div></div>
      <div class="associate"><div class="name">[REDACTED]</div><div class="role">Royal Family</div></div>
      <div class="associate"><div class="name">DONKEY KONG</div><div class="role">Real Estate</div></div>
      <div class="associate"><div class="name">[REDACTED]</div><div class="role">Tech Founder</div></div>
      <div class="associate"><div class="name">CAESAR</div><div class="role">Political Consultant</div></div>
      <div class="associate"><div class="name">[REDACTED]</div><div class="role">"Foundation"</div></div>
      <div class="associate"><div class="name">KING KONG</div><div class="role">Construction</div></div>
      <div class="associate"><div class="name">[REDACTED]</div><div class="role">Media Mogul</div></div>
    </div>
  </div>

  <div class="file-card">
    <div class="file-tag">FILE 005 — TOKENOMICS (UNREDACTED)</div>
    <h2>The <span class="red">Numbers</span></h2>
    <p>Filed under: things they don't want you to know.</p>
    <div class="tokenomics">
      <div class="token-card"><div class="num">1B</div><div class="lbl">Total Supply</div></div>
      <div class="token-card"><div class="num">100%</div><div class="lbl">Liquidity Burned</div></div>
      <div class="token-card"><div class="num">0%</div><div class="lbl">Team Wallet</div></div>
      <div class="token-card"><div class="num">∞</div><div class="lbl">Bananas / Holder</div></div>
    </div>
    <p style="margin-top:18px"><em>This is a meme coin. It has no intrinsic value. It will not pay your rent. It might, however, get you on a list.</em></p>
  </div>

</section>

<section class="cta-block">
  <h2>FOLLOW THE <span class="red">BANANAS</span></h2>
  <p>$APESTEIN is now live on Pump.fun. The files have been leaked. The chain has been notified.</p>
  <div class="cta-buttons">
    <a href="https://pump.fun" target="_blank" class="btn-primary">BUY ON PUMP.FUN</a>
    <a href="#contract" class="btn-secondary">COPY CONTRACT</a>
    <a href="https://x.com/jeffrey8pstein" target="_blank" class="btn-secondary">X / TWITTER</a>
    <a href="https://t.me/+12aJtODGNVhmZDg0" target="_blank" class="btn-secondary">TELEGRAM</a>
  </div>
</section>

<footer>
  <div>© 2026 THE APESTEIN ESTATE • CASE FILE JA-001 • LEAKED FOR THE PUBLIC RECORD</div>
  <div>$APESTEIN IS A MEME. NOT FINANCIAL ADVICE. DEGEN AT OWN RISK.</div>
</footer>

<div class="toast" id="toast">CONTRACT COPIED TO CLIPBOARD</div>

<script>
  const copyBtn = document.getElementById('copy-btn');
  const caText = document.getElementById('ca-text');
  const toast = document.getElementById('toast');

  copyBtn.addEventListener('click', () => {
    const text = caText.textContent.trim();
    if (text.startsWith('[')) {
      toast.textContent = 'NO CONTRACT YET — PASTE IT IN THE HTML';
    } else {
      navigator.clipboard.writeText(text).then(() => {
        toast.textContent = 'CONTRACT COPIED TO CLIPBOARD';
      });
    }
    toast.classList.add('show');
    setTimeout(() => toast.classList.remove('show'), 2200);
  });

  document.querySelectorAll('.redact, .redact-line').forEach(el => {
    el.addEventListener('mouseenter', () => {
      el.style.color = 'var(--paper)';
      el.style.transition = 'color .2s';
    });
    el.addEventListener('mouseleave', () => {
      el.style.color = 'transparent';
    });
  });
</script>

</body>
</html>
