<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Mikaela Larsell Ayesa — CV</title>
<style>
  *, *::before, *::after { box-sizing: border-box; }
  html { font-size: 16px; }
  body {
    margin: 0;
    padding: 2rem 1.5rem 3rem;
    background: #f5f4f0;
    font-family: 'Georgia', serif;
    color: #1a1a1a;
    min-height: 100vh;
  }
 
  .page-wrap {
    max-width: 780px;
    margin: 0 auto;
  }
 
  /* Edit bar */
  .edit-bar {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 1.2rem;
    padding: 10px 16px;
    background: #fff;
    border: 0.5px solid #d8d6ce;
    border-radius: 8px;
    font-family: 'Helvetica Neue', sans-serif;
  }
  .edit-dot { width: 8px; height: 8px; border-radius: 50%; background: #639922; flex-shrink: 0; }
  .edit-bar-label { font-size: 12px; color: #666; flex: 1; }
  .edit-bar button {
    font-size: 12px;
    padding: 5px 14px;
    border-radius: 6px;
    border: 0.5px solid #bbb;
    background: #fafaf8;
    color: #1a1a1a;
    cursor: pointer;
    font-family: 'Helvetica Neue', sans-serif;
  }
  .edit-bar button:hover { background: #f0efeb; }
 
  /* CV card */
  .cv {
    background: #fff;
    border: 0.5px solid #d8d6ce;
    border-radius: 12px;
    overflow: hidden;
  }
 
  /* Header */
  .cv-header {
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 2rem;
    padding: 2.2rem 2.8rem 1.6rem;
    border-bottom: 2px solid #1a1a1a;
  }
  .cv-name {
    font-family: 'Georgia', serif;
    font-size: 28px;
    font-weight: normal;
    color: #1a1a1a;
    margin: 0 0 5px;
    letter-spacing: -0.3px;
  }
  .cv-role {
    font-family: 'Helvetica Neue', sans-serif;
    font-size: 10px;
    letter-spacing: 1.8px;
    text-transform: uppercase;
    color: #888;
    margin: 0 0 10px;
  }
  .cv-tagline {
    font-family: 'Helvetica Neue', sans-serif;
    font-size: 13px;
    color: #555;
    line-height: 1.75;
    max-width: 420px;
    margin: 0;
  }
  .cv-badges {
    display: flex;
    gap: 5px;
    flex-wrap: wrap;
    margin-top: 12px;
  }
  .badge {
    font-family: 'Helvetica Neue', sans-serif;
    font-size: 11px;
    padding: 3px 10px;
    border-radius: 20px;
    font-weight: 500;
  }
  .b-gtm   { background: #E1F5EE; color: #085041; }
  .b-founder { background: #EEEDFE; color: #3C3489; }
  .b-board { background: #FAECE7; color: #712B13; }
  .b-ops   { background: #E6F1FB; color: #0C447C; }
  .b-lang  { background: #FBEAF0; color: #72243E; }
 
  .cv-contact {
    text-align: right;
    font-family: 'Helvetica Neue', sans-serif;
    font-size: 12px;
    color: #666;
    line-height: 2.1;
  }
  .cv-contact .note {
    margin-top: 5px;
    font-size: 10px;
    color: #aaa;
  }
 
  /* Body grid */
  .cv-body {
    display: grid;
    grid-template-columns: 1.65fr 1fr;
  }
  .cv-main {
    padding: 1.8rem 2rem 2rem 2.8rem;
    border-right: 0.5px solid #e8e6de;
  }
  .cv-side {
    padding: 1.8rem 2rem 2rem 1.8rem;
  }
 
  /* Sections */
  .sec { margin-bottom: 1.6rem; }
  .sec-title {
    font-family: 'Helvetica Neue', sans-serif;
    font-size: 9px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: #888;
    margin: 0 0 12px;
    padding-bottom: 6px;
    border-bottom: 0.5px solid #e8e6de;
  }
 
  /* Roles */
  .role { margin-bottom: 1.1rem; }
  .role-hd {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    gap: 6px;
  }
  .role-title {
    font-family: 'Helvetica Neue', sans-serif;
    font-size: 13px;
    font-weight: 500;
    color: #1a1a1a;
  }
  .role-date {
    font-family: 'Helvetica Neue', sans-serif;
    font-size: 10px;
    color: #aaa;
    white-space: nowrap;
  }
  .role-org {
    font-family: 'Helvetica Neue', sans-serif;
    font-size: 11px;
    color: #888;
    margin: 2px 0 3px;
    font-style: italic;
  }
  .role-desc {
    font-family: 'Helvetica Neue', sans-serif;
    font-size: 11.5px;
    color: #555;
    line-height: 1.7;
  }
 
  /* Board */
  .board-item {
    padding: 9px 0;
    border-bottom: 0.5px solid #e8e6de;
  }
  .board-item:last-child { border-bottom: none; }
  .board-role {
    font-family: 'Helvetica Neue', sans-serif;
    font-size: 13px;
    font-weight: 500;
    color: #1a1a1a;
  }
  .board-org {
    font-family: 'Helvetica Neue', sans-serif;
    font-size: 11px;
    color: #888;
    margin-top: 2px;
  }
 
  /* Stats grid */
  .stats {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 7px;
  }
  .stat {
    background: #f7f6f2;
    border-radius: 8px;
    padding: 9px 10px;
  }
  .stat-n {
    font-family: 'Helvetica Neue', sans-serif;
    font-size: 18px;
    font-weight: 500;
    color: #1a1a1a;
  }
  .stat-l {
    font-family: 'Helvetica Neue', sans-serif;
    font-size: 10px;
    color: #888;
    line-height: 1.4;
    margin-top: 2px;
  }
 
  /* Language bars */
  .lang-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-family: 'Helvetica Neue', sans-serif;
    font-size: 11px;
    padding: 5px 0;
    border-bottom: 0.5px solid #e8e6de;
    color: #666;
  }
  .lang-row:last-child { border-bottom: none; }
  .lang-bar { width: 72px; height: 2px; background: #e8e6de; border-radius: 1px; overflow: hidden; }
  .lang-fill { height: 100%; background: #888; border-radius: 1px; }
 
  /* Anthropic note */
  .anthropic-note {
    padding: 10px 12px;
    background: #E1F5EE;
    border-left: 3px solid #1D9E75;
    margin-top: 0.6rem;
  }
  .anthropic-note-title {
    font-family: 'Helvetica Neue', sans-serif;
    font-size: 10px;
    font-weight: 500;
    color: #085041;
    letter-spacing: 0.5px;
    margin: 0 0 4px;
  }
  .anthropic-note-text {
    font-family: 'Helvetica Neue', sans-serif;
    font-size: 11px;
    color: #085041;
    line-height: 1.65;
  }
 
  /* Editable */
  [contenteditable] {
    outline: none;
    border-radius: 3px;
    transition: background 0.15s;
    cursor: text;
  }
  [contenteditable]:hover { background: #f5f4f0; }
  [contenteditable]:focus {
    background: #f5f4f0;
    box-shadow: 0 0 0 2px #bbb;
  }
 
  /* Copy button */
  .copy-btn {
    display: block;
    width: 100%;
    margin-top: 1.2rem;
    padding: 11px;
    font-family: 'Helvetica Neue', sans-serif;
    font-size: 12px;
    border: 0.5px solid #bbb;
    border-radius: 8px;
    background: #fff;
    color: #1a1a1a;
    cursor: pointer;
    text-align: center;
    letter-spacing: 0.3px;
  }
  .copy-btn:hover { background: #f0efeb; }
 
  @media print {
    body { background: #fff; padding: 0; }
    .edit-bar, .copy-btn { display: none; }
    .cv { border: none; border-radius: 0; }
  }
</style>
</head>
<body>
<div class="page-wrap">
 
  <div class="edit-bar">
    <div class="edit-dot"></div>
    <span class="edit-bar-label">Click any text to edit — all content is yours to change before sending</span>
    <button onclick="copyCV()">Copy HTML</button>
    <button onclick="window.print()">Print / Save PDF</button>
  </div>
 
  <div class="cv" id="cv-content">
 
    <div class="cv-header">
      <div>
        <h1 class="cv-name" contenteditable="true">Mikaela Larsell Ayesa</h1>
        <p class="cv-role" contenteditable="true">Head of Investor Relations · Forbes 30u30 Europe · Founder · Board Director</p>
        <p class="cv-tagline" contenteditable="true">Startup &amp; investor ecosystem networker, connecting investors, entrepreneurs, decision-makers and leaders. Generalist with a passion for operations — previously co-founder, COO, and inventor of the Lean Circular Framework.</p>
        <div class="cv-badges">
          <span class="badge b-founder">Founder</span>
          <span class="badge b-board">Board Director</span>
          <span class="badge b-ops">C-level exec</span>
          <span class="badge b-gtm">Creative</span>
          <span class="badge b-lang">Systems thinker</span>
        </div>
      </div>
      <div class="cv-contact">
        <div contenteditable="true">mikaela.larsell@gmail.com</div>
        <div contenteditable="true">Stockholm, Sweden</div>
        <div contenteditable="true">linkedin.com/in/mikaelalarsell-ayesa</div>
        <div class="note" contenteditable="true">Forbes 30u30 · YEOS · LP Project Europe</div>
      </div>
    </div>
 
    <div class="cv-body">
      <div class="cv-main">
 
        <div class="sec">
          <p class="sec-title">Experience</p>
 
          <div class="role">
            <div class="role-hd">
              <span class="role-title" contenteditable="true">Head of IR &amp; Business Area</span>
              <span class="role-date" contenteditable="true">2024–present</span>
            </div>
            <div class="role-org" contenteditable="true">TechArena · Scandinavia's biggest tech &amp; innovation platform</div>
            <div class="role-desc" contenteditable="true">Responsible for all investor activities, accelerator programs, startup competitions, and corporate initiatives. Built investor ecosystem from scratch — Investor Day (2500 investors, 2 editions), LP/GP lunches (192 matched), Time to Raise accelerator (cohorts 4–7, 34 VCs, 66 startups, 335 mentorship sessions). Created Circle Series, Family Office Days, and BuildArena Hackathon 2026.</div>
          </div>
 
          <div class="role">
            <div class="role-hd">
              <span class="role-title" contenteditable="true">Executive Program Director</span>
              <span class="role-date" contenteditable="true">2023–present</span>
            </div>
            <div class="role-org" contenteditable="true">Time to Raise (acquired by TechArena)</div>
            <div class="role-desc" contenteditable="true">Cohort-based accelerator for female founders and mixed teams. Responsible for everything from finding financial partners, workshop leaders, and mentors, to selecting startups and supporting them through fundraising. Engaged 34 leading VC funds — NEA, Sequoia scout fund, Atomico, Northzone, Felix Capital, Creandum and more — with 101 mentors and 335 mentorship sessions supporting 66 startups.</div>
          </div>
 
          <div class="role">
            <div class="role-hd">
              <span class="role-title" contenteditable="true">Chief Operating Officer</span>
              <span class="role-date" contenteditable="true">2022–2024</span>
            </div>
            <div class="role-org" contenteditable="true">uBIT Venture Studio</div>
            <div class="role-desc" contenteditable="true">Venture studio building tech startup MVPs through equity investment in software development hours. Responsible for processes between customers and developers, full budget ownership of e-commerce branch and equity projects, and primary contact for all clients and 11 in-house developers. Investment committee member — deal selection and deal flow development. Supported 7 e-com brands and 10 startups.</div>
          </div>
 
          <div class="role">
            <div class="role-hd">
              <span class="role-title" contenteditable="true">Co-founder &amp; COO</span>
              <span class="role-date" contenteditable="true">2019–2022</span>
            </div>
            <div class="role-org" contenteditable="true">Hack Your Closet · fashion tech, Stockholm</div>
            <div class="role-desc" contenteditable="true">Grew the company to 45 employees in 2 European markets with 3200 active subscribers and 45 250 boxes shipped over 3 years. Raised a total of $3M with an ARR of $1.5M. Responsible for operations &amp; logistics, HR management, B2B partnerships and sustainability strategy. Inventor of the Lean Circular Framework.</div>
          </div>
        </div>
 
        <div class="sec">
          <p class="sec-title">Education</p>
          <div class="role">
            <div class="role-hd">
              <span class="role-title" contenteditable="true">MSc Innovation Management &amp; Product Realisation</span>
              <span class="role-date" contenteditable="true">2017–2019</span>
            </div>
            <div class="role-org" contenteditable="true">KTH Royal Institute of Technology</div>
          </div>
          <div class="role">
            <div class="role-hd">
              <span class="role-title" contenteditable="true">BSc Design &amp; Product Development</span>
              <span class="role-date" contenteditable="true">2014–2017</span>
            </div>
            <div class="role-org" contenteditable="true">KTH Royal Institute of Technology</div>
          </div>
        </div>
 
      </div>
 
      <div class="cv-side">
 
        <div class="sec">
          <p class="sec-title">Board positions</p>
          <div class="board-item">
            <div class="board-role" contenteditable="true">Chairwoman of the Board</div>
            <div class="board-org" contenteditable="true">YEoS · Young Entrepreneurs of Sweden · Since 2025</div>
          </div>
          <div class="board-item">
            <div class="board-role" contenteditable="true">Board Director</div>
            <div class="board-org" contenteditable="true">YEoS Ventures · early-stage investment firm · Since 2024</div>
          </div>
          <div class="board-item">
            <div class="board-role" contenteditable="true">Chairwoman of the Board</div>
            <div class="board-org" contenteditable="true">Herbox AB · SEK 20.3M revenue, 9000+ dispensers in 15 countries · Since 2023</div>
          </div>
        </div>
 
        <div class="sec">
          <p class="sec-title">Impact by numbers</p>
          <div class="stats">
            <div class="stat"><div class="stat-n">2500+</div><div class="stat-l">investors engaged across two Investor Day editions</div></div>
            <div class="stat"><div class="stat-n">66</div><div class="stat-l">startups supported in fundraising</div></div>
            <div class="stat"><div class="stat-n">$3M</div><div class="stat-l">raised as co-founder</div></div>
            <div class="stat"><div class="stat-n">45K+</div><div class="stat-l">boxes shipped at Hack Your Closet</div></div>
          </div>
        </div>
 
        <div class="sec">
          <p class="sec-title">Languages</p>
          <div class="lang-row"><span>Swedish</span><div class="lang-bar"><div class="lang-fill" style="width:100%"></div></div></div>
          <div class="lang-row"><span>Spanish</span><div class="lang-bar"><div class="lang-fill" style="width:100%"></div></div></div>
          <div class="lang-row"><span>English</span><div class="lang-bar"><div class="lang-fill" style="width:85%"></div></div></div>
          <div class="lang-row"><span>French</span><div class="lang-bar"><div class="lang-fill" style="width:55%"></div></div></div>
        </div>
 
        <div class="sec">
          <p class="sec-title">Consulting</p>
          <div class="role">
            <div class="role-hd">
              <span class="role-title" contenteditable="true">Founder as a Service</span>
              <span class="role-date" contenteditable="true">2022–present</span>
            </div>
            <div class="role-org" contenteditable="true">Larsell Ayesa Consulting</div>
            <div class="role-desc" contenteditable="true">Hands-on work with startups, corporates and research projects within venture building, business modelling, logistics &amp; operations development and sustainability. Clients include Melle Sweden AB, Parently AB, STING, Herbox, and Minimist.</div>
          </div>
        </div>
 
      </div>
    </div>
  </div>
 
  <button class="copy-btn" onclick="copyCV()">Copy full CV HTML to clipboard</button>
 
</div>
 
<script>
function copyCV() {
  const content = document.documentElement.outerHTML;
  navigator.clipboard.writeText(content).then(() => {
    const btn = document.querySelector('.copy-btn');
    const orig = btn.textContent;
    btn.textContent = 'Copied!';
    setTimeout(() => btn.textContent = orig, 2000);
  });
}
</script>
</body>
</html>
