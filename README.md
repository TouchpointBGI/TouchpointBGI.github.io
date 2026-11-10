<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Touchpoint BGI | SOPs, onboarding and admin for hospitality teams</title>
<meta name="description" content="Remote SOP writing, onboarding and offboarding kits, and payroll hours support for hotels and restaurants.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Manrope:wght@400;500;700&family=Unbounded:wght@600;700&display=swap" rel="stylesheet">
<style>
  /* EDIT ME: change colours here and the whole page updates */
  :root{
    --cream:#FFF5E6; --ink:#2D2D2D; --mint:#BDECB0;
    --sage:#9AA88A; --blush:#DCCBBD; --clay:#CF7F5C;
    --display:"Unbounded","Arial Black",system-ui,sans-serif;
    --body:"Manrope",system-ui,-apple-system,"Segoe UI",sans-serif;
  }
  *{box-sizing:border-box;margin:0}
  html{scroll-behavior:smooth}
  body{background:var(--cream);color:var(--ink);font-family:var(--body);font-size:1.0625rem;line-height:1.65}
  a{color:inherit}
  :focus-visible{outline:3px solid var(--ink);outline-offset:3px;border-radius:4px}
  .wrap{max-width:1040px;margin:0 auto;padding:0 1.5rem}
  h1,h2,h3{font-family:var(--display);font-weight:700;line-height:1.15;letter-spacing:-.01em}

  /* Hero */
  .hero{padding:clamp(3rem,9vw,6.5rem) 0 clamp(2.5rem,6vw,4rem)}
  .mark{font-size:clamp(2.4rem,11.5vw,7.6rem);line-height:1;isolation:isolate;display:inline-block;position:relative}
  .mark .o{position:relative;display:inline-block}
  .mark .o::before{content:"";position:absolute;z-index:-1;width:.82em;height:.82em;border-radius:50%;background:var(--mint);left:52%;top:63%;transform:translate(-50%,-50%) scale(1);animation:pop .9s cubic-bezier(.2,.8,.2,1) both}
  .mark .o:nth-of-type(2)::before{animation-delay:.15s}
  .mark .o:nth-of-type(3)::before{animation-delay:.3s}
  @keyframes pop{from{transform:translate(-50%,-50%) scale(0)}to{transform:translate(-50%,-50%) scale(1)}}
  .bgi{display:block;font-family:var(--body);font-weight:500;font-size:clamp(1.6rem,5vw,3rem);letter-spacing:.14em;line-height:1;margin:1.5rem 0 0 .4rem}
  .swatches{display:flex;gap:.5rem;margin:1.75rem 0 2.25rem;flex-wrap:wrap}
  .sw{height:46px;width:clamp(96px,17vw,170px);border-radius:60% 40% 55% 45% / 70% 55% 45% 30%}
  .sw:nth-child(1){background:var(--sage)}
  .sw:nth-child(2){background:var(--blush);border-radius:45% 55% 40% 60% / 60% 70% 30% 40%}
  .sw:nth-child(3){background:var(--clay);border-radius:55% 45% 60% 40% / 55% 45% 70% 30%}
  .lead{font-family:var(--display);font-weight:600;font-size:clamp(1.35rem,3.6vw,2.2rem);line-height:1.3;max-width:20em}
  .sub{max-width:34em;margin-top:1.25rem}
  .btn{display:inline-block;margin-top:2rem;background:var(--ink);color:var(--cream);text-decoration:none;font-weight:700;padding:.95rem 1.6rem;border-radius:999px;transition:background .2s,color .2s}
  .btn:hover{background:var(--clay);color:var(--ink)}

  section{padding:clamp(2.5rem,6vw,4.5rem) 0}
  h2{font-size:clamp(1.5rem,3.6vw,2.3rem);margin-bottom:1.5rem;max-width:18em}

  /* About */
  .about{display:grid;gap:2rem;grid-template-columns:1fr}
  .about p{max-width:36em}
  .about p + p{margin-top:1rem}
  .facts{list-style:none;padding:0;display:grid;gap:.75rem;align-content:start}
  .facts li{background:var(--mint);padding:.9rem 1.2rem;border-radius:999px;font-weight:700;width:fit-content}
  @media(min-width:800px){.about{grid-template-columns:1.4fr 1fr;gap:4rem}}

  /* Services: paint-swatch blocks, each shaped differently */
  .services{display:grid;gap:1.25rem;grid-template-columns:1fr}
  .svc{padding:2rem 1.75rem 2.25rem}
  .svc h3{font-size:1.15rem;margin-bottom:.6rem}
  .svc:nth-child(1){background:var(--sage);border-radius:2.6rem 1rem 3rem 1rem}
  .svc:nth-child(2){background:var(--blush);border-radius:1rem 3rem 1rem 2.6rem}
  .svc:nth-child(3){background:var(--clay);border-radius:1rem 2.6rem 1rem 3rem}
  .svc:nth-child(4){background:var(--mint);border-radius:3rem 1rem 2.6rem 1rem}
  @media(min-width:700px){.services{grid-template-columns:1fr 1fr}}

  /* Process: a real sequence, so numbered */
  .steps{list-style:none;padding:0;display:grid;gap:1.5rem;counter-reset:s}
  .steps li{counter-increment:s;display:grid;grid-template-columns:3.2rem 1fr;gap:1rem;align-items:start;max-width:40em}
  .steps li::before{content:counter(s);font-family:var(--display);font-weight:700;width:3.2rem;height:3.2rem;border-radius:50%;background:var(--mint);display:grid;place-items:center}
  .steps strong{display:block;font-family:var(--display);font-size:1.05rem;font-weight:600;margin-bottom:.15rem}

  /* Contact */
  .contact{background:var(--ink);color:var(--cream);border-radius:2.5rem 2.5rem 0 0}
  .contact h2{max-width:14em}
  .contact p{max-width:32em}
  .contact .btn{background:var(--mint);color:var(--ink)}
  .contact .btn:hover{background:var(--clay)}
  .links{margin-top:1.75rem;display:flex;gap:1.5rem;flex-wrap:wrap}
  .links a{text-underline-offset:4px}
  footer{background:var(--ink);color:var(--blush);padding:1.5rem 0 2.5rem;font-size:.9rem}

  @media(prefers-reduced-motion:reduce){
    html{scroll-behavior:auto}
    .mark .o::before{animation:none}
    .btn{transition:none}
  }
</style>
</head>
<body>

<header class="hero">
  <div class="wrap">
    <h1 class="mark" aria-label="Touchpoint">T<span class="o">o</span>uch<span class="o">p</span><span class="o">o</span>int</h1>
    <span class="bgi">BGI</span>
    <div class="swatches" aria-hidden="true"><div class="sw"></div><div class="sw"></div><div class="sw"></div></div>
    <p class="lead">Systems that make your team's day easier.</p>
    <p class="sub">I write the procedures, onboarding kits and handover documents that hotels and restaurants need, and I help keep payroll hours in order. Remote, clear and ready for your team to use.</p>
    <a class="btn" href="#contact">Request a quote</a>
  </div>
</header>

<main>
  <section id="about">
    <div class="wrap about">
      <div>
        <h2>Admin experience from inside the hotel and restaurant.</h2>
        <p>I'm Danielle Sanson. For nearly two years my main role has been the admin behind hotel and restaurant operations: payroll hours, staff onboarding and offboarding, and writing, revising and refining standard operating procedures.</p>
        <p>I know what a busy team needs written down, and how to say it so line staff will actually follow it.</p>
      </div>
      <ul class="facts">
        <li>Hospitality-specific</li>
        <li>Plain, clear writing</li>
        <li>Editable files you keep</li>
      </ul>
    </div>
  </section>

  <section id="services">
    <div class="wrap">
      <h2>What I can do for you</h2>
      <div class="services">
        <article class="svc">
          <h3>SOP writing and clean-up</h3>
          <p>Step-by-step procedures for the jobs your team repeats every day: opening and closing, cash handling, guest service, tip policies. I write new ones and tidy the ones you already have.</p>
        </article>
        <article class="svc">
          <h3>Onboarding kits</h3>
          <p>Checklists, first-week schedules and welcome packs, so every new hire knows what to do from day one.</p>
        </article>
        <article class="svc">
          <h3>Offboarding and handover</h3>
          <p>Exit checklists and handover templates, so knowledge, keys and system access don't leave with the person.</p>
        </article>
        <article class="svc">
          <h3>Payroll hours support</h3>
          <p>Timesheet preparation and checking before payroll goes out. This is admin and prep support, not payroll filing.</p>
        </article>
      </div>
    </div>
  </section>

  <section id="process">
    <div class="wrap">
      <h2>How it works</h2>
      <ol class="steps">
        <li><div><strong>Tell me what's slowing your team down</strong>A short message or call is enough to start.</div></li>
        <li><div><strong>I draft it in your venue's voice</strong>Your procedures, your terms, written so they're easy to follow.</div></li>
        <li><div><strong>We refine it, then you keep it</strong>You get editable files in Google Docs or Word, ready to update as you grow.</div></li>
      </ol>
    </div>
  </section>

  <section id="contact" class="contact">
    <div class="wrap">
      <h2>Tell me what you need.</h2>
      <p>Send a short note about your team and the process you'd like help with, and I'll reply with next steps and a quote.</p>
      <!-- EDIT ME: replace the email address below -->
      <a class="btn" href="mailto:touchpointbgi@gmail.com?subject=Quote%20request">Email Touchpoint BGI</a>
      <div class="links">
        <!-- EDIT ME: replace these with your real profile links, or delete a line -->
        <a href="https://instagram.com/yourhandle">Instagram</a>
      </div>
    </div>
  </section>
</main>

<footer>
  <div class="wrap">&copy; 2026 Touchpoint BGI</div>
</footer>

</body>
</html>
