<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>PlayBNB — Project Roadmap</title>

<style>
:root{
  --bg:#000;
  --gold-1:#ffd84d;
  --gold-2:#ffb300;
  --muted:rgba(255,255,255,0.75);
}
*{box-sizing:border-box;margin:0;padding:0}
html,body{height:100%}

body{
  background:var(--bg);
  color:#fff;
  font-family:Inter,system-ui,-apple-system,"Segoe UI",Roboto,Arial;
  display:flex;
  align-items:center;
  justify-content:center;
  padding:28px;
  overflow:hidden;
}

/* Background */
.bg{
  position:fixed;
  inset:0;
  z-index:0;
  pointer-events:none;
}
.dot{
  position:absolute;
  border-radius:50%;
  background:radial-gradient(circle at 30% 25%,var(--gold-1),var(--gold-2));
  box-shadow:0 0 8px rgba(255,215,0,.45);
  mix-blend-mode:screen;
  opacity:.9;
}
@keyframes floatY{
  0%{transform:translateY(0)}
  50%{transform:translateY(-12px)}
  100%{transform:translateY(0)}
}
@keyframes driftX{
  0%{transform:translateX(0)}
  50%{transform:translateX(8px)}
  100%{transform:translateX(0)}
}

/* Layout */
.wrap{
  position:relative;
  z-index:2;
  width:min(1200px,96vw);
}
.card{
  background:linear-gradient(180deg,rgba(255,255,255,.02),rgba(255,255,255,.01));
  border-radius:14px;
  padding:42px;
  border:1px solid rgba(255,255,255,.04);
  box-shadow:0 28px 80px rgba(0,0,0,.75);
}

.title{
  text-align:center;
  font-size:clamp(28px,5vw,54px);
  font-weight:900;
  color:var(--gold-1);
}
.subtitle{
  text-align:center;
  margin-top:10px;
  color:var(--muted);
  font-size:15px;
}

/* Roadmap */
.roadmap{
  margin-top:40px;
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
  gap:26px;
}
.phase{
  background:rgba(255,255,255,0.02);
  border-radius:14px;
  padding:28px;
  border:1px solid rgba(255,255,255,0.04);
}
.phase h3{
  font-size:22px;
  font-weight:800;
  color:var(--gold-1);
  margin-bottom:14px;
}
.phase p{
  font-size:14px;
  line-height:1.75;
  color:var(--muted);
  margin-bottom:18px;
}
.progress{
  height:8px;
  background:rgba(255,255,255,0.08);
  border-radius:8px;
  overflow:hidden;
}
.progress span{
  display:block;
  height:100%;
  background:linear-gradient(90deg,var(--gold-1),var(--gold-2));
  border-radius:8px;
}
</style>
</head>

<body>

<div class="bg" id="bg"></div>

<div class="wrap">
  <div class="card">

    <div class="title">Project Roadmap</div>
    <div class="subtitle">Long-term vision and structured development path of the PlayBNB ecosystem</div>

    <div class="roadmap">

      <!-- Phase 1 -->
      <div class="phase">
        <h3>Phase 1 — Foundation & Launch</h3>
        <p>
          This phase focuses on establishing the core foundation of the PlayBNB project.
          It includes the complete design and deployment of smart contracts, token creation,
          security reviews, and initial blockchain integration. During this stage, the team
          concentrates on building trust through transparency, documentation, and open
          communication with early supporters.
        </p>
        <p>
          Community channels are launched and moderated, brand identity is finalized, and
          early contributors are onboarded. The objective of Phase 1 is to ensure that the
          PlayBNB ecosystem starts with a solid technical and strategic base, minimizing risks
          and ensuring long-term sustainability.
        </p>
        <div class="progress"><span style="width:100%"></span></div>
      </div>

      <!-- Phase 2 -->
      <div class="phase">
        <h3>Phase 2 — Expansion & Adoption</h3>
        <p>
          Phase 2 marks the expansion of PlayBNB into active market participation. This phase
          includes token listing on decentralized platforms, liquidity provisioning, and
          structured airdrop campaigns designed to reward early adopters and active community
          members.
        </p>
        <p>
          Platform upgrades are introduced to improve user experience, enhance performance,
          and prepare the ecosystem for Play-to-Earn mechanics. Strategic partnerships and
          marketing initiatives are executed to increase visibility and attract new users,
          while maintaining a fair and organic growth model.
        </p>
        <div class="progress"><span style="width:60%"></span></div>
      </div>

      <!-- Phase 3 -->
      <div class="phase">
        <h3>Phase 3 — Growth & Ecosystem Scaling</h3>
        <p>
          The final phase focuses on scaling the PlayBNB ecosystem into a fully operational
          and sustainable platform. Advanced game mechanics, mining systems, and reward
          distribution models are activated, enabling long-term user engagement.
        </p>
        <p>
          This phase also emphasizes ecosystem expansion through global partnerships,
          continuous feature development, and long-term governance planning. The goal is to
          transform PlayBNB into a robust Web3 gaming ecosystem with real utility, economic
          balance, and a strong community-driven future.
        </p>
        <div class="progress"><span style="width:30%"></span></div>
      </div>

    </div>

  </div>
</div>

<script>
(function(){
  const bg=document.getElementById('bg');
  const COUNT=48;
  for(let i=0;i<COUNT;i++){
    const d=document.createElement('div');
    d.className='dot';
    const s=4+Math.random()*8;
    d.style.width=s+'px';
    d.style.height=s+'px';
    d.style.left=Math.random()*100+'vw';
    d.style.top=Math.random()*100+'vh';
    d.style.animation=
      `floatY ${1.5+Math.random()*3}s ease-in-out infinite,
       driftX ${2+Math.random()*3}s ease-in-out infinite`;
    bg.appendChild(d);
  }
})();
</script>

</body>
</html>
