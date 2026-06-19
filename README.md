@@ -0,0 +1,216 @@
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nebula Venture Builder</title>
  <style>
    :root {
      --bg: #09051e;
      --purple: #9b5cff;
      --orange: #ff9a42;
      --text: #f3f2ff;
      --muted: #b9b0ff;
      --surface: rgba(255, 255, 255, 0.08);
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      min-height: 100vh;
      font-family: Inter, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      color: var(--text);
      background: radial-gradient(circle at top, rgba(155, 92, 255, 0.22), transparent 30%),
                  radial-gradient(circle at right, rgba(255, 154, 66, 0.18), transparent 22%),
                  linear-gradient(180deg, #0b0823 0%, #06020f 100%);
    }

    .page {
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 48px 24px;
      min-height: 100vh;
    }

    .card {
      max-width: 920px;
      width: 100%;
      padding: 48px;
      border-radius: 28px;
      background: linear-gradient(180deg, rgba(255,255,255,0.06), rgba(255,255,255,0.03));
      border: 1px solid rgba(255, 255, 255, 0.1);
      box-shadow: 0 28px 90px rgba(0, 0, 0, 0.35);
      position: relative;
      overflow: hidden;
    }

    .glow {
      position: absolute;
      border-radius: 999px;
      filter: blur(72px);
      opacity: 0.55;
    }

    .glow.purple {
      width: 260px;
      height: 260px;
      background: rgba(155, 92, 255, 0.4);
      top: -70px;
      left: -70px;
    }

    .glow.orange {
      width: 260px;
      height: 260px;
      background: rgba(255, 154, 66, 0.35);
      bottom: -80px;
      right: -70px;
    }

    h1 {
      margin: 0 0 20px;
      font-size: clamp(2.7rem, 5vw, 4.8rem);
      letter-spacing: -0.05em;
      line-height: 1.02;
    }

    .brand {
      display: inline-flex;
      align-items: center;
      gap: 0.9rem;
    }

    .brand-mark {
      width: 54px;
      height: 54px;
      border-radius: 18px;
      background: radial-gradient(circle at 30% 30%, #ff9a42, #9b5cff 58%);
      box-shadow: 0 0 36px rgba(255, 154, 66, 0.22);
      position: relative;
    }

    .brand-mark::before,
    .brand-mark::after {
      content: "";
      position: absolute;
      border-radius: 999px;
    }

    .brand-mark::before {
      width: 26px;
      height: 26px;
      top: 12px;
      left: 14px;
      background: rgba(255, 255, 255, 0.85);
      box-shadow: 0 0 28px rgba(255, 255, 255, 0.35);
    }

    .brand-mark::after {
      width: 86px;
      height: 86px;
      border: 2px solid rgba(255, 255, 255, 0.16);
      top: -16px;
      left: -16px;
      opacity: 0.7;
    }

    p {
      margin: 0 0 28px;
      max-width: 760px;
      color: var(--muted);
      font-size: 1.08rem;
      line-height: 1.9;
    }

    .stats {
      display: grid;
      gap: 18px;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      margin-top: 12px;
    }

    .stat {
      padding: 24px;
      border-radius: 22px;
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(255, 255, 255, 0.08);
    }

    .stat strong {
      display: block;
      font-size: 2rem;
      color: #fff;
      margin-bottom: 10px;
    }

    .stat span {
      color: var(--muted);
      font-size: 0.97rem;
    }

    .tagline {
      display: inline-flex;
      align-items: center;
      padding: 10px 16px;
      border-radius: 999px;
      background: rgba(155, 92, 255, 0.12);
      color: #d9d1ff;
      font-size: 0.95rem;
      letter-spacing: 0.03em;
      margin-bottom: 30px;
    }

    .tagline::before {
      content: "★";
      margin-right: 10px;
    }

    @media (max-width: 620px) {
      .card {
        padding: 32px 22px;
      }
      .brand-mark {
        width: 46px;
        height: 46px;
      }
    }
  </style>
</head>
<body>
  <main class="page">
    <section class="card">
      <div class="glow purple"></div>
      <div class="glow orange"></div>
      <div class="tagline">Venture Builder Ecosystem Platform</div>
      <div class="brand">
        <div class="brand-mark" aria-hidden="true"></div>
        <div>
          <h1>Nebula</h1>
          <p>Forging the next generation of startups with a venture builder ecosystem for founders, investors, and builders.</p>
        </div>
      </div>
      <p>
        Nebula is a venture builder ecosystem platform designed to accelerate bold ideas into scalable companies. We combine strategic launch support, capital access, and operational infrastructure with a collaborative platform that fuels growth across founders, partners, and builders.
      </p>
      <div class="stats">
        <div class="stat">
          <strong>Launch-ready</strong>
          <span>From concept to product-market fit in streamlined sprints.</span>
        </div>
        <div class="stat">
          <strong>Network-led</strong>
          <span>Built for founders, investors, and builders to connect across sectors.</span>
        </div>
        <div class="stat">
          <strong>Venture builder</strong>
          <span>A platform dedicated to building and scaling new companies with clarity.</span>
        </div>
      </div>
    </section>
  </main>
</body>
</html>
