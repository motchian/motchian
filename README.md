<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>N. Dakon Richard Motchian — Software Engineer</title>
<meta name="description" content="N. Dakon Richard Motchian — software engineer focused on web and backend development. TypeScript, Node.js, React, REST APIs, SQL/NoSQL and modern engineering practices.">
<link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect width='100' height='100' rx='24' fill='%234F46E5'/><text x='50' y='72' text-anchor='middle' font-family='ui-sans-serif,system-ui,sans-serif' font-weight='700' font-size='62' fill='white'>M</text></svg>">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Sora:wght@500;600;700&family=IBM+Plex+Sans:wght@400;500&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/devicon.min.css">

<style>
  /* ============================== TOKENS ============================== */
  :root{
    --paper:#FAFBFD;
    --paper-2:#EEF2F8;
    --card:#FFFFFF;
    --ink:#0E1526;
    --ink-2:#334155;
    --ink-3:#64748B;
    --line:#E4EAF3;
    --accent:#4F46E5;
    --accent-2:#4338CA;
    --accent-soft:#EDEEFE;

    /* editor (dark panel — colors live only inside the panel) */
    --ed-bg:#0B1020;
    --ed-bar:#10172C;
    --ed-line:#1C2440;
    --ed-num:#3D4866;
    --ed-text:#E6EAF4;
    --c-comment:#5C6C8E;
    --c-kw:#C792EA;
    --c-var:#82AAFF;
    --c-key:#89DDFF;
    --c-str:#C3E88D;
    --c-bool:#F78C6C;
    --c-punc:#8593B3;

    --display:'Sora', ui-sans-serif, system-ui, sans-serif;
    --body:'IBM Plex Sans', ui-sans-serif, system-ui, sans-serif;
    --mono:'JetBrains Mono', ui-monospace, 'SFMono-Regular', Menlo, monospace;

    --maxw:1160px;
    --radius:14px;
  }

  /* ============================== BASE ============================== */
  *{ box-sizing:border-box; }
  html{ scroll-behavior:smooth; -webkit-text-size-adjust:100%; }
  body{
    margin:0;
    background:var(--paper);
    color:var(--ink);
    font-family:var(--body);
    font-size:17px;
    line-height:1.7;
    -webkit-font-smoothing:antialiased;
    text-rendering:optimizeLegibility;
  }
  a{ color:inherit; text-decoration:none; }
  h1,h2{ margin:0; font-family:var(--display); letter-spacing:-0.02em; line-height:1.05; }
  p{ margin:0; }
  ::selection{ background:var(--accent); color:#fff; }

  .container{ max-width:var(--maxw); margin-inline:auto; width:100%; }
  .section{ padding:clamp(72px, 10vw, 130px) 24px; }

  .eyebrow{
    font-family:var(--mono);
    font-size:0.78rem;
    letter-spacing:0.06em;
    color:var(--accent);
    text-transform:lowercase;
    margin-bottom:18px;
  }

  :focus-visible{
    outline:2px solid var(--accent);
    outline-offset:3px;
    border-radius:6px;
  }

  /* ============================== NAV ============================== */
  .nav{
    position:sticky; top:0; z-index:50;
    display:flex; align-items:center; justify-content:space-between;
    gap:16px;
    padding:14px clamp(16px,4vw,40px);
    background:color-mix(in srgb, var(--paper) 82%, transparent);
    backdrop-filter:blur(12px);
    -webkit-backdrop-filter:blur(12px);
    border-bottom:1px solid transparent;
    transition:border-color .25s ease, background .25s ease;
  }
  .nav.is-scrolled{ border-bottom-color:var(--line); }
  .nav__mono{
    display:inline-grid; place-items:center;
    width:38px; height:38px;
    font-family:var(--mono); font-weight:700; font-size:0.95rem;
    color:#fff; background:var(--ink);
    border-radius:10px;
    letter-spacing:0.02em;
  }
  .nav__links{ display:flex; align-items:center; gap:clamp(14px,2.4vw,28px); }
  .nav__link{
    font-size:0.95rem; color:var(--ink-2); font-weight:500;
    display:inline-flex; align-items:center; gap:6px;
    transition:color .2s ease;
  }
  .nav__link:hover{ color:var(--ink); }
  .nav__link svg{ width:13px; height:13px; }
  .nav__link--accent{ color:var(--accent); }
  .nav__link--accent:hover{ color:var(--accent-2); }
  .nav__link.is-hideable{ }
  @media (max-width:560px){ .nav__link.is-hideable{ display:none; } }

  /* ============================== HERO ============================== */
  .hero{
    position:relative;
    padding-top:clamp(56px, 9vh, 96px);
    padding-bottom:clamp(64px, 9vw, 110px);
    overflow:hidden;
  }
  /* faint engineering dot-grid behind the hero */
  .hero::before{
    content:"";
    position:absolute; inset:0;
    background-image:radial-gradient(circle, rgba(14,21,38,0.05) 1px, transparent 1.4px);
    background-size:26px 26px;
    -webkit-mask-image:radial-gradient(ellipse 90% 70% at 30% 20%, #000 0%, transparent 75%);
            mask-image:radial-gradient(ellipse 90% 70% at 30% 20%, #000 0%, transparent 75%);
    pointer-events:none;
  }
  .hero__grid{
    position:relative;
    display:grid;
    grid-template-columns:1.02fr 0.98fr;
    align-items:center;
    gap:clamp(36px, 5vw, 72px);
  }
  .hero__name{
    font-weight:700;
    font-size:clamp(2.7rem, 6.4vw, 4.6rem);
    margin:6px 0 22px;
  }
  .hero__tagline{
    font-size:clamp(1.08rem, 1.7vw, 1.3rem);
    color:var(--ink-2);
    max-width:30ch;
    margin-bottom:26px;
  }
  .hero__meta{
    display:flex; flex-wrap:wrap; align-items:center; gap:12px;
    font-family:var(--mono); font-size:0.82rem; color:var(--ink-3);
    margin-bottom:34px;
  }
  .hero__meta .dot{ width:4px; height:4px; border-radius:50%; background:var(--line); }
  .hero__actions{ display:flex; flex-wrap:wrap; align-items:center; gap:12px; }

  /* buttons */
  .btn{
    display:inline-flex; align-items:center; gap:9px;
    padding:13px 20px;
    font-family:var(--body); font-size:0.97rem; font-weight:500;
    border-radius:11px;
    border:1px solid transparent;
    transition:transform .16s ease, background .2s ease, border-color .2s ease, box-shadow .2s ease, color .2s ease;
  }
  .btn svg{ width:15px; height:15px; }
  .btn--primary{
    background:var(--ink); color:#fff;
    box-shadow:0 1px 2px rgba(14,21,38,.18);
  }
  .btn--primary:hover{ background:#000; transform:translateY(-2px); box-shadow:0 10px 24px -10px rgba(14,21,38,.55); }
  .btn--ghost{
    background:var(--card); color:var(--ink); border-color:var(--line);
  }
  .btn--ghost:hover{ border-color:var(--accent); color:var(--accent-2); transform:translateY(-2px); }
  .icon-btn{
    display:inline-grid; place-items:center;
    width:46px; height:46px;
    border:1px solid var(--line); border-radius:11px;
    background:var(--card); font-size:1.2rem; color:var(--ink);
    transition:border-color .2s ease, transform .16s ease;
  }
  .icon-btn:hover{ border-color:var(--accent); transform:translateY(-2px); }

  /* ---------- the signature: editor / HTTP response panel ---------- */
  .editor{
    background:var(--ed-bg);
    border-radius:16px;
    border:1px solid rgba(255,255,255,.06);
    box-shadow:0 28px 70px -30px rgba(11,16,32,.6), 0 4px 14px -6px rgba(11,16,32,.4);
    overflow:hidden;
    font-family:var(--mono);
  }
  .editor__bar{
    display:flex; align-items:center; gap:14px;
    padding:13px 16px;
    background:var(--ed-bar);
    border-bottom:1px solid rgba(255,255,255,.05);
  }
  .editor__dots{ display:inline-flex; gap:7px; }
  .editor__dots i{ width:11px; height:11px; border-radius:50%; display:block; }
  .editor__dots i:nth-child(1){ background:#FF5F57; }
  .editor__dots i:nth-child(2){ background:#FEBC2E; }
  .editor__dots i:nth-child(3){ background:#28C840; }
  .editor__file{ color:#9AA6C4; font-size:0.8rem; }
  .editor__pill{
    margin-left:auto;
    font-size:0.72rem; color:#AEB9D6;
    background:rgba(255,255,255,.05);
    border:1px solid rgba(255,255,255,.07);
    padding:4px 9px; border-radius:7px;
    white-space:nowrap;
  }
  .editor__pill .m{ color:var(--c-kw); font-weight:700; }
  .editor__body{
    margin:0; padding:18px 18px 22px;
    overflow-x:auto;
    counter-reset:ln;
    font-size:clamp(0.78rem, 1.05vw, 0.9rem);
    line-height:1.85;
    color:var(--ed-text);
  }
  .cl{
    display:block; position:relative;
    padding-left:3.1em;
    white-space:pre;
    counter-increment:ln;
    opacity:0;
    animation:lineIn .42s ease forwards;
  }
  .cl::before{
    content:counter(ln);
    position:absolute; left:0; width:2.2em; text-align:right;
    color:var(--ed-num);
    -webkit-user-select:none; user-select:none;
  }
  .cl:nth-child(1){ animation-delay:.20s } .cl:nth-child(2){ animation-delay:.27s }
  .cl:nth-child(3){ animation-delay:.34s } .cl:nth-child(4){ animation-delay:.41s }
  .cl:nth-child(5){ animation-delay:.48s } .cl:nth-child(6){ animation-delay:.55s }
  .cl:nth-child(7){ animation-delay:.62s } .cl:nth-child(8){ animation-delay:.69s }
  .cl:nth-child(9){ animation-delay:.76s } .cl:nth-child(10){ animation-delay:.83s }
  .c-comment{ color:var(--c-comment); font-style:italic; }
  .c-kw{ color:var(--c-kw); } .c-var{ color:var(--c-var); } .c-key{ color:var(--c-key); }
  .c-str{ color:var(--c-str); } .c-bool{ color:var(--c-bool); } .c-punc{ color:var(--c-punc); }

  /* ============================== ABOUT ============================== */
  #about, #skills{ scroll-margin-top:90px; }
  .about{ border-top:1px solid var(--line); }
  .about__grid{
    display:grid;
    grid-template-columns:0.95fr 1.05fr;
    gap:clamp(32px,5vw,80px);
    align-items:start;
  }
  .about__statement{
    font-weight:600;
    font-size:clamp(1.5rem, 2.6vw, 2.15rem);
    line-height:1.18;
    max-width:18ch;
  }
  .about__statement b{ color:var(--accent); font-weight:600; }
  .about__body p{ color:var(--ink-2); font-size:1.06rem; }
  .about__body p + p{ margin-top:1.1em; }

  /* ============================== SKILLS ============================== */
  .skills{ background:var(--paper-2); border-top:1px solid var(--line); }
  .skills__head{ margin-bottom:18px; }
  .skills__title{ font-weight:600; font-size:clamp(1.7rem, 3vw, 2.3rem); }
  .skills__list{ margin-top:8px; }

  .group{
    display:grid;
    grid-template-columns:170px 1fr;
    gap:clamp(14px,3vw,40px);
    padding:26px 0;
    border-top:1px solid var(--line);
    align-items:start;
  }
  .group__label{
    font-family:var(--mono);
    font-size:0.8rem;
    letter-spacing:0.04em;
    color:var(--ink-3);
    text-transform:lowercase;
    padding-top:8px;
    position:relative;
  }
  .group__label::before{
    content:""; display:inline-block;
    width:7px; height:7px; border-radius:2px;
    background:var(--accent); margin-right:9px; vertical-align:middle;
    transform:translateY(-1px);
  }
  .group__chips{ display:flex; flex-wrap:wrap; gap:11px; }

  .chip{
    display:inline-flex; align-items:center; gap:11px;
    padding:11px 15px 11px 13px;
    background:var(--card);
    border:1px solid var(--line);
    border-radius:12px;
    font-weight:500; font-size:0.97rem; color:var(--ink);
    transition:transform .16s ease, border-color .2s ease, box-shadow .2s ease;
  }
  .chip:hover{
    transform:translateY(-3px);
    border-color:color-mix(in srgb, var(--accent) 45%, var(--line));
    box-shadow:0 14px 28px -16px rgba(14,21,38,.4);
  }
  .chip i.devicon, .chip i[class*="devicon-"]{ font-size:1.35rem; line-height:1; }
  .chip .ic{ width:21px; height:21px; color:var(--accent); flex:none; }
  .chip .ic svg{ width:100%; height:100%; display:block; }

  /* ============================== FOOTER ============================== */
  .footer{ background:var(--ink); color:#fff; text-align:center; }
  .footer .eyebrow{ color:#A6AEFF; }
  .footer__title{
    font-family:var(--display); font-weight:700;
    font-size:clamp(2rem, 4.5vw, 3.2rem);
    letter-spacing:-0.02em;
  }
  .footer__sub{ color:#AEB6CC; margin:16px 0 30px; font-size:1.06rem; }
  .footer__actions{ display:flex; flex-wrap:wrap; justify-content:center; gap:12px; }
  .footer .btn--primary{ background:#fff; color:var(--ink); }
  .footer .btn--primary:hover{ background:#EDEFFE; }
  .footer .btn--ghost{ background:transparent; color:#fff; border-color:rgba(255,255,255,.22); }
  .footer .btn--ghost:hover{ border-color:#fff; color:#fff; }
  .footer__copy{
    margin-top:46px; font-family:var(--mono); font-size:0.75rem;
    color:#6B7693; letter-spacing:0.02em;
  }

  /* ============================== MOTION ============================== */
  @keyframes lineIn{ from{ opacity:0; transform:translateY(6px); } to{ opacity:1; transform:none; } }
  @keyframes up{ from{ opacity:0; transform:translateY(18px); } to{ opacity:1; transform:none; } }

  .hero__intro > *{ opacity:0; animation:up .65s cubic-bezier(.2,.7,.2,1) forwards; }
  .hero__intro > *:nth-child(1){ animation-delay:.05s }
  .hero__intro > *:nth-child(2){ animation-delay:.12s }
  .hero__intro > *:nth-child(3){ animation-delay:.19s }
  .hero__intro > *:nth-child(4){ animation-delay:.26s }
  .hero__intro > *:nth-child(5){ animation-delay:.33s }
  .hero__editor{ opacity:0; animation:up .7s cubic-bezier(.2,.7,.2,1) .22s forwards; }

  .reveal{ opacity:0; transform:translateY(22px); transition:opacity .7s ease, transform .7s ease; }
  .reveal.is-in{ opacity:1; transform:none; }

  @media (prefers-reduced-motion: reduce){
    html{ scroll-behavior:auto; }
    *{ animation:none !important; transition:none !important; }
    .hero__intro > *, .hero__editor, .cl, .reveal{ opacity:1 !important; transform:none !important; }
  }

  /* ============================== RESPONSIVE ============================== */
  @media (max-width:900px){
    .hero__grid{ grid-template-columns:1fr; gap:44px; }
    .hero__editor{ order:2; }
    .about__grid{ grid-template-columns:1fr; gap:24px; }
    .about__statement{ max-width:24ch; }
  }
  @media (max-width:620px){
    body{ font-size:16px; }
    .group{ grid-template-columns:1fr; gap:14px; padding:22px 0; }
    .group__label{ padding-top:0; }
    .hero__name br{ display:none; }
  }
</style>
</head>

<body id="top">

  <!-- ============================ NAV ============================ -->
  <header class="nav" id="nav">
    <a class="nav__brand" href="#top" aria-label="Back to top">
      <span class="nav__mono">RM</span>
    </a>
    <nav class="nav__links" aria-label="Primary">
      <a class="nav__link is-hideable" href="#about">About</a>
      <a class="nav__link is-hideable" href="#skills">Skills</a>
      <a class="nav__link nav__link--accent" href="https://www.linkedin.com/in/n-dakon-richard-motchian-033876199/" target="_blank" rel="noopener">
        LinkedIn
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M7 17 17 7M9 7h8v8"/></svg>
      </a>
    </nav>
  </header>

  <main>

    <!-- ============================ HERO ============================ -->
    <section class="hero section">
      <div class="container hero__grid">

        <div class="hero__intro">
          <p class="eyebrow">// software engineer</p>
          <h1 class="hero__name">N. Dakon Richard<br>Motchian</h1>
          <p class="hero__tagline">I build scalable web and backend systems — and keep them clean enough to grow.</p>
          <p class="hero__meta">
            <span>Web &amp; backend</span><span class="dot"></span>
            <span>TypeScript</span><span class="dot"></span>
            <span>Node.js</span><span class="dot"></span>
            <span>React</span>
          </p>
          <div class="hero__actions">
            <a class="btn btn--primary" href="https://www.linkedin.com/in/n-dakon-richard-motchian-033876199/" target="_blank" rel="noopener">
              Connect on LinkedIn
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M5 12h14M13 6l6 6-6 6"/></svg>
            </a>
            <!-- TODO: replace with your real email -->
            <a class="btn btn--ghost" href="mailto:hello@example.com">
              Email
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><rect x="3" y="5" width="18" height="14" rx="2"/><path d="m3 7 9 6 9-6"/></svg>
            </a>
            <!-- TODO: replace with your real GitHub URL -->
            <a class="icon-btn" href="https://github.com/" target="_blank" rel="noopener" aria-label="GitHub">
              <i class="devicon-github-original" aria-hidden="true"></i>
            </a>
          </div>
        </div>

        <!-- signature element: profile rendered as an HTTP/JSON response -->
        <div class="hero__editor">
          <div class="editor" role="img" aria-label="Profile summary shown as a TypeScript object: software engineer focused on web and backend, working with TypeScript, Node.js and React.">
            <div class="editor__bar">
              <span class="editor__dots" aria-hidden="true"><i></i><i></i><i></i></span>
              <span class="editor__file">profile.ts</span>
              <span class="editor__pill"><span class="m">GET</span> /engineers/motchian</span>
            </div>
            <pre class="editor__body" aria-hidden="true"><span class="cl"><span class="c-comment">// 200 OK · application/json</span></span><span class="cl"> </span><span class="cl"><span class="c-kw">const</span> <span class="c-var">motchian</span> <span class="c-punc">=</span> {</span><span class="cl">  <span class="c-key">name</span><span class="c-punc">:</span> <span class="c-str">"N. Dakon Richard Motchian"</span><span class="c-punc">,</span></span><span class="cl">  <span class="c-key">role</span><span class="c-punc">:</span> <span class="c-str">"Software Engineer"</span><span class="c-punc">,</span></span><span class="cl">  <span class="c-key">focus</span><span class="c-punc">:</span> [<span class="c-str">"web"</span><span class="c-punc">,</span> <span class="c-str">"backend"</span>]<span class="c-punc">,</span></span><span class="cl">  <span class="c-key">stack</span><span class="c-punc">:</span> [<span class="c-str">"TypeScript"</span><span class="c-punc">,</span> <span class="c-str">"Node.js"</span><span class="c-punc">,</span> <span class="c-str">"React"</span>]<span class="c-punc">,</span></span><span class="cl">  <span class="c-key">values</span><span class="c-punc">:</span> [<span class="c-str">"scalable"</span><span class="c-punc">,</span> <span class="c-str">"maintainable"</span>]<span class="c-punc">,</span></span><span class="cl">  <span class="c-key">learning</span><span class="c-punc">:</span> <span class="c-bool">true</span><span class="c-punc">,</span></span><span class="cl">}<span class="c-punc">;</span></span></pre>
          </div>
        </div>

      </div>
    </section>

    <!-- ============================ ABOUT ============================ -->
    <section class="about section reveal" id="about">
      <div class="container about__grid">
        <div class="about__head">
          <p class="eyebrow">// about</p>
          <h2 class="about__statement">Software that <b>lasts</b> — readable code, sensible systems, teams that ship together.</h2>
        </div>
        <div class="about__body">
          <p>I'm a software engineer focused on web and backend development, building scalable, maintainable applications. I like the part of the job where fuzzy requirements turn into systems people can actually rely on — and the part where the code still makes sense six months later.</p>
          <p>I work closely across product and engineering, and I'm always picking up new tools and practices to ship better. REST APIs, relational and NoSQL data, testing, and a disciplined Git workflow are where I spend most of my time.</p>
        </div>
      </div>
    </section>

    <!-- ============================ SKILLS ============================ -->
    <section class="skills section reveal" id="skills">
      <div class="container">
        <div class="skills__head">
          <p class="eyebrow">// skills</p>
          <h2 class="skills__title">What I work with</h2>
        </div>

        <div class="skills__list">

          <!-- Languages -->
          <div class="group">
            <p class="group__label">languages</p>
            <div class="group__chips">
              <span class="chip"><i class="devicon-javascript-plain colored" aria-hidden="true"></i>JavaScript</span>
              <span class="chip"><i class="devicon-typescript-plain colored" aria-hidden="true"></i>TypeScript</span>
            </div>
          </div>

          <!-- Frontend -->
          <div class="group">
            <p class="group__label">frontend</p>
            <div class="group__chips">
              <span class="chip"><i class="devicon-react-original colored" aria-hidden="true"></i>React</span>
              <span class="chip"><i class="devicon-html5-plain colored" aria-hidden="true"></i>HTML5</span>
              <span class="chip"><i class="devicon-css3-plain colored" aria-hidden="true"></i>CSS3</span>
            </div>
          </div>

          <!-- Backend & APIs -->
          <div class="group">
            <p class="group__label">backend &amp; apis</p>
            <div class="group__chips">
              <span class="chip"><i class="devicon-nodejs-plain colored" aria-hidden="true"></i>Node.js</span>
              <span class="chip">
                <span class="ic" aria-hidden="true"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M8 3H7a2 2 0 0 0-2 2v4a2 2 0 0 1-2 2 2 2 0 0 1 2 2v4a2 2 0 0 0 2 2h1M16 3h1a2 2 0 0 1 2 2v4a2 2 0 0 0 2 2 2 2 0 0 0-2 2v4a2 2 0 0 1-2 2h-1"/></svg></span>
                REST APIs
              </span>
            </div>
          </div>

          <!-- Data -->
          <div class="group">
            <p class="group__label">data</p>
            <div class="group__chips">
              <span class="chip">
                <span class="ic" aria-hidden="true"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><ellipse cx="12" cy="5" rx="8" ry="3"/><path d="M4 5v6c0 1.66 3.58 3 8 3s8-1.34 8-3V5"/><path d="M4 11v6c0 1.66 3.58 3 8 3s8-1.34 8-3v-6"/></svg></span>
                SQL / NoSQL databases
              </span>
            </div>
          </div>

          <!-- Workflow & quality -->
          <div class="group">
            <p class="group__label">workflow &amp; quality</p>
            <div class="group__chips">
              <span class="chip"><i class="devicon-git-plain colored" aria-hidden="true"></i>Git / GitHub</span>
              <span class="chip">
                <span class="ic" aria-hidden="true"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="m17 2 4 4-4 4"/><path d="M3 11v-1a4 4 0 0 1 4-4h14"/><path d="m7 22-4-4 4-4"/><path d="M21 13v1a4 4 0 0 1-4 4H3"/></svg></span>
                Agile practices
              </span>
              <span class="chip">
                <span class="ic" aria-hidden="true"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="9.5"/><path d="m8.5 12 2.5 2.5 4.5-5"/></svg></span>
                Unit testing &amp; automation
              </span>
            </div>
          </div>

        </div>
      </div>
    </section>

  </main>

  <!-- ============================ FOOTER ============================ -->
  <footer class="footer section">
    <div class="container">
      <p class="eyebrow">// get in touch</p>
      <h2 class="footer__title">Let's build something solid.</h2>
      <p class="footer__sub">Open to web &amp; backend roles and collaborations.</p>
      <div class="footer__actions">
        <a class="btn btn--primary" href="https://www.linkedin.com/in/n-dakon-richard-motchian-033876199/" target="_blank" rel="noopener">
          Connect on LinkedIn
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M5 12h14M13 6l6 6-6 6"/></svg>
        </a>
        <a class="btn btn--ghost" href="mailto:hello@example.com">Email</a>
      </div>
      <p class="footer__copy">© <span id="yr"></span> N. Dakon Richard Motchian · Built with care.</p>
    </div>
  </footer>

  <script>
    // year
    document.getElementById('yr').textContent = new Date().getFullYear();

    // nav border on scroll
    var nav = document.getElementById('nav');
    var onScroll = function(){ nav.classList.toggle('is-scrolled', window.scrollY > 8); };
    onScroll(); window.addEventListener('scroll', onScroll, { passive:true });

    // scroll reveal (progressive enhancement)
    var reveals = document.querySelectorAll('.reveal');
    if ('IntersectionObserver' in window) {
      var io = new IntersectionObserver(function(entries){
        entries.forEach(function(e){
          if (e.isIntersecting){ e.target.classList.add('is-in'); io.unobserve(e.target); }
        });
      }, { threshold:0.12, rootMargin:'0px 0px -8% 0px' });
      reveals.forEach(function(el){ io.observe(el); });
    } else {
      reveals.forEach(function(el){ el.classList.add('is-in'); });
    }
  </script>
</body>
</html>
