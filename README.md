<!doctype html>
<html lang="vi"><head><script>window["__codeletBootstrap__"]=JSON.parse('{"A":"A","B":"20260723-05-e9a76f4"}');</script><script src="/_sdk/e358eac22bd01364.telemetry_sdk.js" integrity="sha512-KPxp3rw4K8Nu9ceWJc3gyM7srgaZxiFWOVbyu260EYzzAqdz10mfo5xyXrCx+wEKtGo77JbtmwXvFLbwrGzwvw=="></script>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dòng thời gian Marx – Lenin – Hồ Chí Minh</title>
  <script src="https://cdn.tailwindcss.com/3.4.17"></script>
  <script src="https://cdn.jsdelivr.net/npm/lucide@0.263.0/dist/umd/lucide.min.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Libre+Franklin:wght@500;600;700&amp;family=Source+Serif+Pro:ital,wght@0,400;0,600;0,700;1,400&amp;display=swap" rel="stylesheet">
  <style>
    :root {
      --paper: #eee4d0;
      --ink: #211c17;
      --muted: #6e6255;
      --red: #9f241e;
      --gold: #b58a3b;
      --line: rgba(238, 218, 181, .34);
    }
    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      width: 100%;
      margin: 0;
      font-family: "Source Serif Pro", Georgia, serif;
      color: var(--ink);
      overflow-x: hidden;
    }
    .sans { font-family: "Libre Franklin", sans-serif; }

    .page-background {
      position: fixed;
      inset: 0;
      z-index: -5;
      overflow: hidden;
      background: #241713;
    }
    .background-image {
      position: absolute;
      inset: -3%;
      width: 106%;
      height: 106%;
      object-fit: cover;
      opacity: 0;
      transform: scale(1.06);
      filter: sepia(.64) saturate(.68) contrast(1.08) brightness(.56);
      transition: opacity 1.15s ease, transform 7s ease;
    }
    .background-image.is-active {
      opacity: 1;
      transform: scale(1);
    }
    .background-shade {
      position: absolute;
      inset: 0;
      background:
        linear-gradient(90deg, rgba(24,15,11,.82), rgba(35,22,16,.54) 48%, rgba(24,15,11,.76)),
        linear-gradient(0deg, rgba(20,13,10,.82), rgba(28,18,13,.36) 45%, rgba(20,13,10,.72));
    }
    .paper-texture {
      position: fixed;
      inset: 0;
      pointer-events: none;
      opacity: .18;
      background-image:
        repeating-linear-gradient(0deg, transparent 0 3px, rgba(245,223,183,.05) 3px 4px),
        radial-gradient(circle at 12% 18%, rgba(181,138,59,.28), transparent 23%),
        radial-gradient(circle at 88% 82%, rgba(159,36,30,.2), transparent 25%);
      mix-blend-mode: screen;
      z-index: 45;
    }

    .masthead {
      border-bottom: 1px solid rgba(239,220,183,.22);
      backdrop-filter: blur(16px);
    }
    .hero-section { min-height: 620px; }
    .hero-vignette {
      background:
        linear-gradient(90deg, rgba(25,17,12,.86), rgba(25,17,12,.22) 60%, rgba(25,17,12,.55)),
        linear-gradient(0deg, rgba(25,17,12,.74), transparent 58%);
    }
    .filter-button, .audio-button {
      border: 1px solid rgba(255,255,255,.24);
      transition: background .2s ease, color .2s ease, transform .2s ease, border-color .2s ease;
    }
    .filter-button:hover, .audio-button:hover { transform: translateY(-1px); }
    .filter-button.is-active {
      background: #f0d9aa !important;
      color: #4e1814 !important;
      border-color: #f0d9aa;
      box-shadow: 0 0 0 2px rgba(240,217,170,.18);
    }
    .audio-button .state-on { display: none; }
    .audio-button.is-on .state-off { display: none; }
    .audio-button.is-on .state-on { display: inline; }
    .audio-button svg { width: 16px; height: 16px; }

    .timeline-section {
      position: relative;
      isolation: isolate;
      background: linear-gradient(180deg, rgba(31,20,15,.69), rgba(49,30,20,.55));
      border-top: 1px solid rgba(238,218,181,.18);
      border-bottom: 1px solid rgba(238,218,181,.18);
    }
    .timeline-section::before {
      content: "";
      position: absolute;
      inset: 0;
      z-index: -1;
      pointer-events: none;
      background:
        radial-gradient(circle at 12% 12%, rgba(181,138,59,.13), transparent 30%),
        linear-gradient(90deg, rgba(255,255,255,.025), transparent 35%, rgba(159,36,30,.08));
    }
    .era-banner {
      position: sticky;
      top: 92px;
      z-index: 10;
      width: fit-content;
      margin: 0 auto 3rem;
      border: 1px solid rgba(244,221,180,.33);
      box-shadow: 0 8px 26px rgba(10,5,2,.28);
      backdrop-filter: blur(14px);
    }
    .timeline-shell { position: relative; --progress: 0%; }
    .timeline-track {
      position: absolute;
      inset: 0 auto 0 50%;
      width: 2px;
      background: var(--line);
      transform: translateX(-50%);
    }
    .timeline-progress {
      position: absolute;
      top: 0;
      left: 50%;
      width: 3px;
      height: var(--progress);
      max-height: 100%;
      transform: translateX(-50%);
      background: linear-gradient(to bottom, #edc06c, #bd3028);
      transition: height .12s linear;
    }
    .event-row {
      position: relative;
      display: grid;
      grid-template-columns: minmax(0,1fr) 76px minmax(0,1fr);
      align-items: start;
      margin-bottom: 7rem;
      scroll-margin-top: 12rem;
    }
    .event-row:nth-child(odd) .event-card { grid-column: 1; }
    .event-row:nth-child(even) .event-card { grid-column: 3; }
    .timeline-node {
      grid-column: 2;
      grid-row: 1;
      justify-self: center;
      width: 20px;
      height: 20px;
      margin-top: 2.1rem;
      border: 4px solid #ead7b7;
      border-radius: 999px;
      background: var(--red);
      box-shadow: 0 0 0 2px #bf453b, 0 3px 12px rgba(0,0,0,.38);
      z-index: 2;
    }
    .event-card {
      position: relative;
      border: 1px solid rgba(238,218,181,.28);
      border-top: 4px solid var(--red);
      box-shadow: 0 18px 45px rgba(0,0,0,.28);
      opacity: 0;
      transform: translateY(32px);
      transition: opacity .65s ease, transform .65s cubic-bezier(.2,.75,.25,1), box-shadow .25s ease;
      backdrop-filter: blur(5px);
    }
    .event-row.is-visible .event-card { opacity: 1; transform: translateY(0); }
    .event-card:hover { box-shadow: 0 24px 58px rgba(0,0,0,.38); }
    .event-row.is-filtered { display: none; }
    .event-year { letter-spacing: -.04em; font-variant-numeric: oldstyle-nums; }
    .category-chip {
      font-family: "Libre Franklin", sans-serif;
      text-transform: uppercase;
      letter-spacing: .12em;
      font-size: .68rem;
      font-weight: 700;
    }
    .world-note { border-left: 3px solid var(--gold); background: rgba(181,138,59,.09); }
    .detail-panel { display: grid; grid-template-rows: 0fr; transition: grid-template-rows .38s ease; }
    .detail-panel > div { overflow: hidden; }
    .event-row.is-open .detail-panel { grid-template-rows: 1fr; }
    .learn-button .less-label { display: none; }
    .event-row.is-open .learn-button .more-label { display: none; }
    .event-row.is-open .learn-button .less-label { display: inline; }
    .event-row.is-open .learn-button svg { transform: rotate(180deg); }
    .learn-button svg { transition: transform .25s ease; }
    .document-quote { position: relative; border-left: 3px solid var(--red); }
    .document-quote::before {
      content: "“";
      position: absolute;
      left: .55rem;
      top: -.55rem;
      color: rgba(159,36,30,.16);
      font-size: 4rem;
      line-height: 1;
    }
    .paper-card { background: rgba(247,239,223,.95); }
    button:focus-visible, a:focus-visible { outline: 3px solid #f2bf58; outline-offset: 3px; }

    @media (max-width: 1023px) {
      .era-banner { top: 136px; }
      .hero-section { min-height: 570px; }
    }
    @media (max-width: 767px) {
      .era-banner { top: 158px; max-width: calc(100% - 2rem); }
      .timeline-track, .timeline-progress { left: 14px; transform: none; }
      .event-row { grid-template-columns: 29px minmax(0,1fr); gap: .75rem; margin-bottom: 4.5rem; }
      .event-row:nth-child(odd) .event-card, .event-row:nth-child(even) .event-card { grid-column: 2; }
      .timeline-node { grid-column: 1; width: 16px; height: 16px; margin-top: 2rem; }
      .hero-section { min-height: 520px; }
    }
    @media (prefers-reduced-motion: reduce) {
      html { scroll-behavior: auto; }
      .event-card { opacity: 1; transform: none; transition: none; }
      .detail-panel, .filter-button, .background-image { transition: none; }
    }
  </style>
  <script src="/_sdk/935a53bc2e11fb8d.data_sdk.js" type="text/javascript" integrity="sha512-qr2oyPnEys1WebcOABaRh6hG77r5PWpqeWW6JTKbRJqly/INsfBi31CVNlTmHqjgeLpkVmmHZJUdxSx/32tOFQ=="></script>
  <script src="/_sdk/6030e540d4419216.resizing_sdk.js" type="text/javascript" integrity="sha512-b5KWzyoXsbWP4smq4sftIi6Kts4YVBpBsz0BwCViwbBJkK64a3/Z6ZMdWA+qnplNcXw4mhZeqvQi3mOosiRJdA=="></script>
 </head>
 <body data-template-id="__page-root" style="background: rgb(36, 23, 19);">
  <div class="page-background" aria-hidden="true"><img data-template-id="background-industrial" loading="lazy" class="canva-image background-image is-active" data-era-background="industrial" src="https://images.pexels.com/photos/36676007/pexels-photo-36676007.jpeg" alt="Ảnh đen trắng về một đầu máy hơi nước cổ với các chi tiết cơ khí."> <img data-template-id="background-revolutions" loading="lazy" class="canva-image background-image" data-era-background="revolutions" src="https://images.pexels.com/photos/5937872/pexels-photo-5937872.jpeg" alt="Đường phố lịch sử ở Lviv với các tòa nhà cổ và người đi bộ trong mùa đông."> <img data-template-id="background-imperial" loading="lazy" class="canva-image background-image" data-era-background="imperial" src="https://images.pexels.com/photos/34532118/pexels-photo-34532118.jpeg" alt="Nhóm binh sĩ mặc quân phục đứng trong một chiến hào lịch sử."> <img data-template-id="background-revolution" loading="lazy" class="canva-image background-image" data-era-background="revolution" src="https://images.pexels.com/photos/34632882/pexels-photo-34632882.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1920" alt="Ảnh lịch sử đen trắng về một cuộc diễu hành tại Quảng trường Đỏ."> <img data-template-id="background-liberation" loading="lazy" class="canva-image background-image" data-era-background="liberation" src="https://images.pexels.com/photos/31647022/pexels-photo-31647022.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1920" alt="Lăng Chủ tịch Hồ Chí Minh và quốc kỳ Việt Nam lúc hoàng hôn ở Hà Nội.">
   <div class="background-shade"></div>
  </div>
  <div class="paper-texture" aria-hidden="true"></div>
  <header class="masthead sticky top-0 z-30 text-white" style="background:rgba(75,18,15,.94)">
   <div class="w-full max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-3">
    <div class="flex flex-col xl:flex-row xl:items-center gap-3 xl:gap-5">
     <div class="min-w-0 xl:flex-1">
      <p data-template-id="header-kicker" class="canva-text sans uppercase tracking-[.2em] mb-1" style="color: rgb(230, 201, 142); font-weight: 700; font-style: normal; font-size: 11px; letter-spacing: 0.18rem;">Sản phẩm sáng tạo nhóm 6 - Website lịch sử CNXH</p>
      <h1 data-template-id="page-title" class="canva-text font-bold leading-tight" style="color: rgb(255, 248, 233); font-weight: 700; font-style: normal; font-size: 24px;">Dòng thời gian Marx – Lenin – Hồ Chí Minh</h1>
     </div>
     <nav aria-label="Bộ lọc dòng thời gian" class="flex flex-wrap items-center gap-2"><button data-filter="politics" data-template-id="filter-politics" class="canva-button filter-button sans rounded-full px-3 py-2" type="button" aria-pressed="false" style="background: rgb(125, 29, 24); color: rgb(255, 255, 255); font-weight: 600; font-style: normal; font-size: 13px;">Chính trị</button> <button data-filter="economics" data-template-id="filter-economics" class="canva-button filter-button sans rounded-full px-3 py-2" type="button" aria-pressed="false" style="background: rgb(125, 29, 24); color: rgb(255, 255, 255); font-weight: 600; font-style: normal; font-size: 13px;">Kinh tế</button> <button data-filter="wars" data-template-id="filter-wars" class="canva-button filter-button sans rounded-full px-3 py-2" type="button" aria-pressed="false" style="background: rgb(125, 29, 24); color: rgb(255, 255, 255); font-weight: 600; font-style: normal; font-size: 13px;">Chiến tranh</button> <button data-filter="vietnam" data-template-id="filter-vietnam" class="canva-button filter-button sans rounded-full px-3 py-2" type="button" aria-pressed="false" style="background: rgb(125, 29, 24); color: rgb(255, 255, 255); font-weight: 600; font-style: normal; font-size: 13px;">Việt Nam</button> <button id="show-all" data-template-id="filter-all" class="canva-button sans rounded-full px-3 py-2 border border-white/30 hover:bg-white/10" type="button" style="background: rgb(77, 21, 19); color: rgb(248, 231, 197); font-weight: 600; font-style: normal; font-size: 13px;">Hiển thị tất cả</button>
     </nav>
      <div class="hidden 2xl:flex items-center gap-2 border-l border-white/20 pl-4"><i data-lucide="clock-3" class="w-4 h-4 text-amber-200" aria-hidden="true"></i>
       <div><span data-template-id="period-label" class="canva-text sans block uppercase tracking-[.16em]" style="color: rgb(230, 201, 142); font-weight: 700; font-style: normal; font-size: 10px;">Giai đoạn hiện tại</span> <span id="period-value" class="sans text-sm font-semibold" aria-live="polite">1818–1847</span>
       </div>
      </div>
     </div>
      </div>
  </header>
  <main>
   <section data-template-id="hero-section" class="canva-section hero-section relative w-full overflow-hidden" style="background: rgba(36, 23, 19, 0.12);">
    <div class="hero-vignette absolute inset-0"></div>
    <div class="relative w-full max-w-7xl mx-auto px-6 lg:px-8 py-20 lg:py-28">
     <div class="max-w-3xl text-white">
      <p data-template-id="hero-eyebrow" class="canva-text sans uppercase tracking-[.28em] mb-5" style="color: rgb(235, 197, 115); font-weight: 700; font-style: normal; font-size: 13px; letter-spacing: 0.22rem;">1818—1976 • Dòng lịch sử tương tác mở rộng</p>
      <h2 data-template-id="hero-title" class="canva-text font-bold leading-[1.02] mb-6" style="color: rgb(255, 248, 233); font-weight: 700; font-style: normal; font-size: 58px; line-height: 1.03;">Hành trình của chủ nghĩa xã hội, Marx - Lenin - Hồ Chí Minh</h2>
      <p data-template-id="hero-description" class="canva-text max-w-2xl leading-relaxed mb-8" style="color: rgb(239, 227, 206); font-weight: 400; font-style: normal; font-size: 20px; line-height: 1.55;">Theo dõi một hành trình dài từ châu Âu công nghiệp, qua chủ nghĩa quốc tế xã hội chủ nghĩa và đấu tranh chống thực dân, đến độc lập và thống nhất Việt Nam.</p><a href="#timeline" data-template-id="hero-button" class="canva-button inline-flex items-center gap-2 rounded-sm px-5 py-3 sans font-bold shadow-lg hover:-translate-y-0.5 transition-transform" style="background: rgb(177, 42, 35); color: rgb(255, 255, 255); font-weight: 700; font-style: normal; font-size: 15px;">Bắt đầu dòng thời gian</a>
     </div>
     <aside data-template-id="hero-note" class="canva-panel mt-12 max-w-xl border-l-4 p-5 backdrop-blur-sm" style="background: rgba(46, 27, 21, 0.78);">
      <h3 data-template-id="hero-note-title" class="canva-text sans font-bold mb-2" style="color: rgb(241, 203, 126); font-weight: 700; font-style: normal; font-size: 15px;">Made by</h3>
      <p data-template-id="hero-note-text" class="canva-text leading-relaxed" style="color: rgb(247, 236, 218); font-weight: 400; font-style: normal; font-size: 16px;">Group 6 - MLN131</p>
     </aside>
    </div>
   </section>
   <section id="timeline" class="timeline-section w-full py-16 lg:py-24 scroll-mt-28">
    <div class="max-w-6xl mx-auto px-5 sm:px-8">
     <div class="text-center max-w-3xl mx-auto mb-12">
      <p data-template-id="timeline-kicker" class="canva-text sans uppercase tracking-[.22em] mb-3" style="color: rgb(241, 197, 110); font-weight: 700; font-style: normal; font-size: 12px; letter-spacing: 0.2rem;">Những dòng lịch sử song hành</p>
      <h2 data-template-id="timeline-title" class="canva-text font-bold mb-4" style="color: rgb(255, 244, 221); font-weight: 700; font-style: normal; font-size: 42px;">Con người, tư tưởng, xung đột và giải phóng</h2>
      <p data-template-id="timeline-intro" class="canva-text leading-relaxed" style="color: rgb(234, 219, 195); font-weight: 400; font-style: normal; font-size: 18px;">Mười tám cột mốc nối tư tưởng chính trị với công nghiệp hóa, đế quốc, chiến tranh thế giới, cách mạng, phi thực dân hóa và nhà nước Việt Nam hiện đại. Ảnh nền toàn trang thay đổi theo từng thời đại.</p>
     </div>
     <div data-template-id="era-banner" class="canva-banner era-banner rounded-full px-5 py-2.5 flex items-center gap-3" style="background: rgba(72, 31, 24, 0.9);"><i data-lucide="scroll-text" class="w-4 h-4 text-amber-200" aria-hidden="true"></i> <span data-template-id="era-label" class="canva-text sans uppercase tracking-[.15em]" style="color: rgb(240, 198, 111); font-weight: 700; font-style: normal; font-size: 11px;">Đang xem</span> <span id="era-value" class="sans font-bold text-white" aria-live="polite">Châu Âu công nghiệp</span>
     </div>
     <div id="timeline-shell" class="timeline-shell">
      <div class="timeline-track" aria-hidden="true"></div>
      <div class="timeline-progress" aria-hidden="true"></div>
      <div id="events">
       <article class="event-row" data-year="1818" data-period="1818–1847" data-era="industrial" data-categories="politics economics"><span class="timeline-node" aria-hidden="true"></span>
        <div data-template-id="event-1818-card" class="canva-card event-card paper-card rounded-sm overflow-hidden" style="background: rgba(247, 239, 223, 0.96);">
         <div class="p-6 sm:p-7">
          <div class="flex items-start justify-between gap-4 mb-4"><span data-template-id="event-1818-year" class="canva-text event-year font-bold" style="color: rgb(159, 36, 30); font-weight: 700; font-style: normal; font-size: 37px;">1818</span>
           <div class="flex flex-wrap justify-end gap-2"><span data-template-id="event-1818-tag-politics" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 212, 205); color: rgb(123, 33, 28); font-weight: 400; font-style: normal; font-size: 16px;">Chính trị</span> <span data-template-id="event-1818-tag-economics" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(232, 222, 193); color: rgb(102, 82, 28); font-weight: 400; font-style: normal; font-size: 16px;">Kinh tế</span>
           </div>
          </div>
          <h3 data-template-id="event-1818-title" class="canva-text font-bold leading-tight mb-3" style="color: rgb(36, 28, 23); font-weight: 700; font-style: normal; font-size: 27px;">Karl Marx chào đời tại Trier</h3>
          <p data-template-id="event-1818-summary" class="canva-text leading-relaxed" style="color: rgb(76, 64, 54); font-weight: 400; font-style: normal; font-size: 16px;">Sinh ngày 5 tháng 5 tại Phổ, Marx về sau trở thành nhà triết học, kinh tế chính trị học, nhà báo và một trong những nhà phê phán chủ nghĩa tư bản có ảnh hưởng nhất thế kỷ XIX.</p>
          <div class="world-note mt-5 p-4">
           <p data-template-id="event-1818-world-label" class="canva-text sans font-bold uppercase tracking-[.12em] mb-1" style="color: rgb(118, 85, 31); font-weight: 400; font-style: normal; font-size: 11px;">Cùng thời điểm</p>
           <p data-template-id="event-1818-world" class="canva-text leading-relaxed" style="color: rgb(87, 73, 59); font-weight: 400; font-style: normal; font-size: 16px;">Châu Âu đang được sắp xếp lại sau các cuộc Chiến tranh Napoleon, trong khi công nghiệp hóa tăng tốc ở Anh và lan rộng khắp lục địa.</p>
          </div><button class="learn-button mt-5 inline-flex items-center gap-2 sans font-bold text-left" type="button" aria-expanded="false"> <span data-template-id="event-1818-more" class="canva-text more-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Tìm hiểu thêm</span> <span data-template-id="event-1818-less" class="canva-text less-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Đóng chi tiết</span> <i data-lucide="chevron-down" class="w-4 h-4" aria-hidden="true"></i> </button>
         </div>
         <div class="detail-panel">
          <div>
           <div class="border-t border-stone-300/70 p-6 sm:p-7 grid sm:grid-cols-[150px_1fr] gap-5"><img data-template-id="marx-image" loading="lazy" class="canva-image w-full h-44 sm:h-full object-cover grayscale sepia rounded-sm" src="https://images.pexels.com/photos/5972010/pexels-photo-5972010.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=800" alt="Góc nhìn nghiêng của tượng Karl Marx trong một công viên xanh ở Berlin.">
            <p data-template-id="event-1818-detail" class="canva-text leading-relaxed" style="color: rgb(68, 56, 47); font-weight: 400; font-style: normal; font-size: 16px;">Marx học luật và triết học trước khi chuyển sang báo chí và kinh tế chính trị. Cuộc sống lưu vong đưa ông qua Paris và Brussels đến London, nơi ông nghiên cứu chủ nghĩa tư bản và tham gia tổ chức các phong trào xã hội chủ nghĩa.</p>
           </div>
          </div>
         </div>
        </div>
       </article>
       <article class="event-row" data-year="1844" data-period="1844–1847" data-era="industrial" data-categories="politics economics"><span class="timeline-node" aria-hidden="true"></span>
        <div data-template-id="event-1844-card" class="canva-card event-card paper-card rounded-sm overflow-hidden" style="background: rgba(247, 239, 223, 0.96);">
         <div class="p-6 sm:p-7">
          <div class="flex items-start justify-between gap-4 mb-4"><span data-template-id="event-1844-year" class="canva-text event-year font-bold" style="color: rgb(159, 36, 30); font-weight: 700; font-style: normal; font-size: 37px;">1844</span>
           <div class="flex flex-wrap justify-end gap-2"><span data-template-id="event-1844-tag-politics" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 212, 205); color: rgb(123, 33, 28); font-weight: 400; font-style: normal; font-size: 16px;">Chính trị</span> <span data-template-id="event-1844-tag-economics" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(232, 222, 193); color: rgb(102, 82, 28); font-weight: 400; font-style: normal; font-size: 16px;">Kinh tế</span>
           </div>
          </div>
          <h3 data-template-id="event-1844-title" class="canva-text font-bold leading-tight mb-3" style="color: rgb(36, 28, 23); font-weight: 700; font-style: normal; font-size: 27px;">Marx và Engels bắt đầu sự cộng tác suốt đời</h3>
          <p data-template-id="event-1844-summary" class="canva-text leading-relaxed" style="color: rgb(76, 64, 54); font-weight: 400; font-style: normal; font-size: 16px;">Gặp nhau tại Paris, Marx và Friedrich Engels nhận thấy sự đồng thuận sâu rộng về triết học, kinh tế chính trị và vai trò lịch sử của đấu tranh giai cấp.</p>
          <div class="world-note mt-5 p-4">
           <p data-template-id="event-1844-world-label" class="canva-text sans font-bold uppercase tracking-[.12em] mb-1" style="color: rgb(118, 85, 31); font-weight: 400; font-style: normal; font-size: 11px;">Cùng thời điểm</p>
           <p data-template-id="event-1844-world" class="canva-text leading-relaxed" style="color: rgb(87, 73, 59); font-weight: 400; font-style: normal; font-size: 16px;">Nhà máy và đường sắt làm biến đổi các thành phố châu Âu, còn điều kiện lao động khắc nghiệt thúc đẩy sự hình thành các hiệp hội công nhân và những trước tác chính trị cấp tiến.</p>
          </div><button class="learn-button mt-5 inline-flex items-center gap-2 sans font-bold" type="button" aria-expanded="false"> <span data-template-id="event-1844-more" class="canva-text more-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Tìm hiểu thêm</span> <span data-template-id="event-1844-less" class="canva-text less-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Đóng chi tiết</span> <i data-lucide="chevron-down" class="w-4 h-4" aria-hidden="true"></i> </button>
         </div>
         <div class="detail-panel">
          <div>
           <div class="border-t border-stone-300/70 p-6 sm:p-7 grid sm:grid-cols-[170px_1fr] gap-5"><img data-template-id="engels-image" loading="lazy" class="canva-image w-full h-44 sm:h-full object-cover grayscale sepia rounded-sm" src="https://images.pexels.com/photos/15814717/pexels-photo-15814717.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=800" alt="Tượng Karl Marx và Friedrich Engels trong một công viên ở Berlin.">
            <p data-template-id="event-1844-detail" class="canva-text leading-relaxed" style="color: rgb(68, 56, 47); font-weight: 400; font-style: normal; font-size: 16px;">Engels đóng góp những quan sát về Manchester công nghiệp, hỗ trợ tài chính và kỹ năng biên tập. Sự hợp tác của họ tạo nên Hệ tư tưởng Đức và Tuyên ngôn của Đảng Cộng sản; sau khi Marx qua đời, Engels chuẩn bị các tập sau của bộ Tư bản.</p>
           </div>
          </div>
         </div>
        </div>
       </article>
       <article class="event-row" data-year="1848" data-period="1848–1863" data-era="revolutions" data-categories="politics economics wars"><span class="timeline-node" aria-hidden="true"></span>
        <div data-template-id="event-1848-card" class="canva-card event-card paper-card rounded-sm overflow-hidden" style="background: rgba(247, 239, 223, 0.96);"><img data-template-id="manifesto-image" loading="lazy" class="canva-image w-full h-52 object-cover sepia" src="https://images.pexels.com/photos/1757852/pexels-photo-1757852.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=800" alt="Cận cảnh một cuốn sách mở với những trang giấy cũ và phần chữ rõ nét.">
         <div class="p-6 sm:p-7">
          <div class="flex items-start justify-between gap-4 mb-4"><span data-template-id="event-1848-year" class="canva-text event-year font-bold" style="color: rgb(159, 36, 30); font-weight: 700; font-style: normal; font-size: 37px;">1848</span>
           <div class="flex flex-wrap justify-end gap-2"><span data-template-id="event-1848-tag-politics" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 212, 205); color: rgb(123, 33, 28); font-weight: 400; font-style: normal; font-size: 16px;">Chính trị</span> <span data-template-id="event-1848-tag-wars" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(223, 197, 189); color: rgb(113, 28, 24); font-weight: 400; font-style: normal; font-size: 16px;">Cách mạng</span>
           </div>
          </div>
          <h3 data-template-id="event-1848-title" class="canva-text font-bold leading-tight mb-3" style="color: rgb(36, 28, 23); font-weight: 700; font-style: normal; font-size: 27px;">Tuyên ngôn của Đảng Cộng sản ra đời</h3>
          <p data-template-id="event-1848-summary" class="canva-text leading-relaxed" style="color: rgb(76, 64, 54); font-weight: 400; font-style: normal; font-size: 16px;">Được Liên đoàn những người Cộng sản ủy nhiệm, văn kiện ngắn do Marx và Engels viết diễn giải lịch sử qua đấu tranh giai cấp và kêu gọi tổ chức quốc tế của giai cấp công nhân.</p>
          <div class="world-note mt-5 p-4">
           <p data-template-id="event-1848-world-label" class="canva-text sans font-bold uppercase tracking-[.12em] mb-1" style="color: rgb(118, 85, 31); font-weight: 400; font-style: normal; font-size: 11px;">Sự kiện thế giới</p>
           <p data-template-id="event-1848-world" class="canva-text leading-relaxed" style="color: rgb(87, 73, 59); font-weight: 400; font-style: normal; font-size: 16px;">Các cuộc cách mạng lan khắp Pháp, các quốc gia Đức, Đế quốc Áo và Italy, được thúc đẩy bởi yêu cầu về hiến pháp, quyền tự quyết dân tộc và cải cách xã hội.</p>
          </div><button class="learn-button mt-5 inline-flex items-center gap-2 sans font-bold" type="button" aria-expanded="false"> <span data-template-id="event-1848-more" class="canva-text more-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Mở ghi chú văn kiện</span> <span data-template-id="event-1848-less" class="canva-text less-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Đóng ghi chú văn kiện</span> <i data-lucide="chevron-down" class="w-4 h-4" aria-hidden="true"></i> </button>
         </div>
         <div class="detail-panel">
          <div>
           <div class="border-t border-stone-300/70 p-6 sm:p-7">
            <blockquote data-template-id="manifesto-quote" class="canva-text document-quote italic py-3 pl-10 pr-4 leading-relaxed" style="color: rgb(85, 37, 31); font-weight: 400; font-style: italic; font-size: 18px;">Lịch sử tất cả các xã hội từ trước đến nay là lịch sử đấu tranh giai cấp.</blockquote>
            <p data-template-id="event-1848-detail" class="canva-text mt-4 leading-relaxed" style="color: rgb(68, 56, 47); font-weight: 400; font-style: normal; font-size: 16px;">Ban đầu chỉ là một trong nhiều văn bản chính trị của năm cách mạng, Tuyên ngôn dần có ảnh hưởng toàn cầu khi các phong trào công nhân và xã hội chủ nghĩa dịch thuật, tranh luận và vận dụng nó.</p>
           </div>
          </div>
         </div>
        </div>
       </article>
       <article class="event-row" data-year="1864" data-period="1864–1866" data-era="revolutions" data-categories="politics economics"><span class="timeline-node" aria-hidden="true"></span>
        <div data-template-id="event-1864-card" class="canva-card event-card paper-card rounded-sm overflow-hidden" style="background: rgba(247, 239, 223, 0.96);"><img data-template-id="international-image" loading="lazy" class="canva-image w-full h-48 object-cover sepia" src="https://images.pexels.com/photos/18729210/pexels-photo-18729210.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=800" alt="Kiến trúc Victoria chi tiết của khách sạn St Pancras Renaissance tại London.">
         <div class="p-6 sm:p-7">
          <div class="flex items-start justify-between gap-4 mb-4"><span data-template-id="event-1864-year" class="canva-text event-year font-bold" style="color: rgb(159, 36, 30); font-weight: 700; font-style: normal; font-size: 37px;">1864</span>
           <div class="flex flex-wrap justify-end gap-2"><span data-template-id="event-1864-tag-politics" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 212, 205); color: rgb(123, 33, 28); font-weight: 400; font-style: normal; font-size: 16px;">Chính trị</span> <span data-template-id="event-1864-tag-economics" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(232, 222, 193); color: rgb(102, 82, 28); font-weight: 400; font-style: normal; font-size: 16px;">Lao động</span>
           </div>
          </div>
          <h3 data-template-id="event-1864-title" class="canva-text font-bold leading-tight mb-3" style="color: rgb(36, 28, 23); font-weight: 700; font-style: normal; font-size: 27px;">Quốc tế thứ nhất được thành lập</h3>
          <p data-template-id="event-1864-summary" class="canva-text leading-relaxed" style="color: rgb(76, 64, 54); font-weight: 400; font-style: normal; font-size: 16px;">Công nhân và các nhà hoạt động chính trị họp tại London đã thành lập Hiệp hội Công nhân Quốc tế, liên kết các tổ chức lao động vượt qua biên giới quốc gia.</p>
          <div class="world-note mt-5 p-4">
           <p data-template-id="event-1864-world-label" class="canva-text sans font-bold uppercase tracking-[.12em] mb-1" style="color: rgb(118, 85, 31); font-weight: 400; font-style: normal; font-size: 11px;">Bối cảnh lịch sử</p>
           <p data-template-id="event-1864-world" class="canva-text leading-relaxed" style="color: rgb(87, 73, 59); font-weight: 400; font-style: normal; font-size: 16px;">Đường sắt, di cư, thương mại và các nơi làm việc công nghiệp mở rộng khiến việc phối hợp quốc tế vừa trở nên khả thi hơn vừa cấp thiết hơn.</p>
          </div><button class="learn-button mt-5 inline-flex items-center gap-2 sans font-bold" type="button" aria-expanded="false"> <span data-template-id="event-1864-more" class="canva-text more-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Mở ghi chú tổ chức</span> <span data-template-id="event-1864-less" class="canva-text less-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Đóng ghi chú tổ chức</span> <i data-lucide="chevron-down" class="w-4 h-4" aria-hidden="true"></i> </button>
         </div>
         <div class="detail-panel">
          <div>
           <div class="border-t border-stone-300/70 p-6 sm:p-7">
            <p data-template-id="event-1864-detail" class="canva-text leading-relaxed" style="color: rgb(68, 56, 47); font-weight: 400; font-style: normal; font-size: 16px;">Marx soạn diễn văn khai mạc và điều lệ lâm thời. Hiệp hội gồm các nhà công đoàn, xã hội chủ nghĩa, vô chính phủ, cộng hòa và nhiều khuynh hướng khác; những bất đồng sau đó đã làm tổ chức phân rẽ.</p>
           </div>
          </div>
         </div>
        </div>
       </article>
       <article class="event-row" data-year="1867" data-period="1867–1870" data-era="revolutions" data-categories="economics politics"><span class="timeline-node" aria-hidden="true"></span>
        <div data-template-id="event-1867-card" class="canva-card event-card paper-card rounded-sm overflow-hidden" style="background: rgba(247, 239, 223, 0.96);">
         <div class="p-6 sm:p-7">
          <div class="flex items-start justify-between gap-4 mb-4"><span data-template-id="event-1867-year" class="canva-text event-year font-bold" style="color: rgb(159, 36, 30); font-weight: 700; font-style: normal; font-size: 37px;">1867</span> <span data-template-id="event-1867-tag-economics" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(232, 222, 193); color: rgb(102, 82, 28); font-weight: 400; font-style: normal; font-size: 16px;">Kinh tế</span>
          </div>
          <h3 data-template-id="event-1867-title" class="canva-text font-bold leading-tight mb-3" style="color: rgb(36, 28, 23); font-weight: 700; font-style: normal; font-size: 27px;">Tập I của bộ Tư bản được xuất bản</h3>
          <p data-template-id="event-1867-summary" class="canva-text leading-relaxed" style="color: rgb(76, 64, 54); font-weight: 400; font-style: normal; font-size: 16px;">Công trình lớn của Marx khảo sát hàng hóa, giá trị, lao động làm thuê, tích lũy và động lực của nền sản xuất tư bản chủ nghĩa.</p>
          <div class="world-note mt-5 p-4">
           <p data-template-id="event-1867-world-label" class="canva-text sans font-bold uppercase tracking-[.12em] mb-1" style="color: rgb(118, 85, 31); font-weight: 400; font-style: normal; font-size: 11px;">Cùng thời điểm</p>
           <p data-template-id="event-1867-world" class="canva-text leading-relaxed" style="color: rgb(87, 73, 59); font-weight: 400; font-style: normal; font-size: 16px;">Cuộc Cách mạng công nghiệp lần thứ hai tăng tốc với thép, hóa chất, điện khí hóa, thị trường mở rộng và cạnh tranh đế quốc ngày càng quyết liệt.</p>
          </div><button class="learn-button mt-5 inline-flex items-center gap-2 sans font-bold" type="button" aria-expanded="false"> <span data-template-id="event-1867-more" class="canva-text more-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Đọc ghi chú văn kiện</span> <span data-template-id="event-1867-less" class="canva-text less-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Đóng ghi chú văn kiện</span> <i data-lucide="chevron-down" class="w-4 h-4" aria-hidden="true"></i> </button>
         </div>
         <div class="detail-panel">
          <div>
           <div class="border-t border-stone-300/70 p-6 sm:p-7">
            <blockquote data-template-id="capital-quote" class="canva-text document-quote italic py-3 pl-10 pr-4 leading-relaxed" style="color: rgb(85, 37, 31); font-weight: 400; font-style: italic; font-size: 18px;">Của cải của những xã hội trong đó phương thức sản xuất tư bản chủ nghĩa chiếm địa vị thống trị biểu hiện ra như một “đống hàng hóa khổng lồ”.</blockquote>
            <p data-template-id="event-1867-detail" class="canva-text mt-4 leading-relaxed" style="color: rgb(68, 56, 47); font-weight: 400; font-style: normal; font-size: 16px;">Chỉ tập đầu tiên được xuất bản khi Marx còn sống. Sau khi ông qua đời, Engels biên tập và xuất bản Tập II và Tập III từ khối lượng bản thảo và ghi chép đồ sộ.</p>
           </div>
          </div>
         </div>
        </div>
       </article>
       <article class="event-row" data-year="1871" data-period="1871–1910" data-era="revolutions" data-categories="politics wars"><span class="timeline-node" aria-hidden="true"></span>
        <div data-template-id="event-1871-card" class="canva-card event-card paper-card rounded-sm overflow-hidden" style="background: rgba(247, 239, 223, 0.96);"><img data-template-id="paris-image" loading="lazy" class="canva-image w-full h-48 object-cover sepia" src="https://images.pexels.com/photos/31543003/pexels-photo-31543003.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=800" alt="Mặt tiền một tòa nhà Paris cổ điển mang kiến trúc thế kỷ XIX.">
         <div class="p-6 sm:p-7">
          <div class="flex items-start justify-between gap-4 mb-4"><span data-template-id="event-1871-year" class="canva-text event-year font-bold" style="color: rgb(159, 36, 30); font-weight: 700; font-style: normal; font-size: 37px;">1871</span>
           <div class="flex flex-wrap justify-end gap-2"><span data-template-id="event-1871-tag-politics" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 212, 205); color: rgb(123, 33, 28); font-weight: 400; font-style: normal; font-size: 16px;">Chính trị</span> <span data-template-id="event-1871-tag-wars" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(223, 197, 189); color: rgb(113, 28, 24); font-weight: 400; font-style: normal; font-size: 16px;">Xung đột</span>
           </div>
          </div>
          <h3 data-template-id="event-1871-title" class="canva-text font-bold leading-tight mb-3" style="color: rgb(36, 28, 23); font-weight: 700; font-style: normal; font-size: 27px;">Công xã Paris</h3>
          <p data-template-id="event-1871-summary" class="canva-text leading-relaxed" style="color: rgb(76, 64, 54); font-weight: 400; font-style: normal; font-size: 16px;">Sau thất bại của Pháp trong chiến tranh, một chính quyền đô thị cách mạng kiểm soát Paris trong khoảng hai tháng trước khi bị đàn áp dữ dội.</p>
          <div class="world-note mt-5 p-4">
           <p data-template-id="event-1871-world-label" class="canva-text sans font-bold uppercase tracking-[.12em] mb-1" style="color: rgb(118, 85, 31); font-weight: 400; font-style: normal; font-size: 11px;">Ý nghĩa diễn giải</p>
           <p data-template-id="event-1871-world" class="canva-text leading-relaxed" style="color: rgb(87, 73, 59); font-weight: 400; font-style: normal; font-size: 16px;">Công xã trở thành một điểm tham chiếu lâu dài cho các tranh luận về chính quyền nhân dân, quyền lực nhà nước, cách mạng và tổ chức chính trị.</p>
          </div><button class="learn-button mt-5 inline-flex items-center gap-2 sans font-bold" type="button" aria-expanded="false"> <span data-template-id="event-1871-more" class="canva-text more-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Tìm hiểu thêm</span> <span data-template-id="event-1871-less" class="canva-text less-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Đóng chi tiết</span> <i data-lucide="chevron-down" class="w-4 h-4" aria-hidden="true"></i> </button>
         </div>
         <div class="detail-panel">
          <div>
           <div class="border-t border-stone-300/70 p-6 sm:p-7">
            <p data-template-id="event-1871-detail" class="canva-text leading-relaxed" style="color: rgb(68, 56, 47); font-weight: 400; font-style: normal; font-size: 16px;">Marx xem Công xã là bằng chứng rằng giai cấp công nhân không thể chỉ tiếp quản nguyên trạng bộ máy nhà nước sẵn có. Các truyền thống xã hội chủ nghĩa sau này rút ra những bài học chiến lược rất khác nhau từ thành tựu và thất bại của Công xã.</p>
           </div>
          </div>
         </div>
        </div>
       </article>
       <article class="event-row" data-year="1911" data-period="1911–1913" data-era="imperial" data-categories="vietnam politics"><span class="timeline-node" aria-hidden="true"></span>
        <div data-template-id="event-1911-card" class="canva-card event-card paper-card rounded-sm overflow-hidden" style="background: rgba(247, 239, 223, 0.96);">
         <div class="p-6 sm:p-7">
          <div class="flex items-start justify-between gap-4 mb-4"><span data-template-id="event-1911-year" class="canva-text event-year font-bold" style="color: rgb(159, 36, 30); font-weight: 700; font-style: normal; font-size: 37px;">1911</span>
           <div class="flex flex-wrap justify-end gap-2"><span data-template-id="event-1911-tag-vietnam" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 210, 174); color: rgb(111, 65, 18); font-weight: 400; font-style: normal; font-size: 16px;">Việt Nam</span> <span data-template-id="event-1911-tag-politics" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 212, 205); color: rgb(123, 33, 28); font-weight: 400; font-style: normal; font-size: 16px;">Chính trị</span>
           </div>
          </div>
          <h3 data-template-id="event-1911-title" class="canva-text font-bold leading-tight mb-3" style="color: rgb(36, 28, 23); font-weight: 700; font-style: normal; font-size: 27px;">Nguyễn Tất Thành rời Việt Nam</h3>
          <p data-template-id="event-1911-summary" class="canva-text leading-relaxed" style="color: rgb(76, 64, 54); font-weight: 400; font-style: normal; font-size: 16px;">Người thanh niên sau này trở thành Hồ Chí Minh rời Bến Nhà Rồng ở Sài Gòn, bắt đầu nhiều thập niên đi qua các nước, học hỏi chính trị, tổ chức và hoạt động chống thực dân.</p>
          <div class="world-note mt-5 p-4">
           <p data-template-id="event-1911-world-label" class="canva-text sans font-bold uppercase tracking-[.12em] mb-1" style="color: rgb(118, 85, 31); font-weight: 400; font-style: normal; font-size: 11px;">Cùng thời điểm</p>
           <p data-template-id="event-1911-world" class="canva-text leading-relaxed" style="color: rgb(87, 73, 59); font-weight: 400; font-style: normal; font-size: 16px;">Các đế quốc châu Âu kiểm soát những vùng lãnh thổ rộng lớn tại châu Á và châu Phi, trong khi các phong trào dân tộc và cải cách thách thức chế độ thuộc địa.</p>
          </div><button class="learn-button mt-5 inline-flex items-center gap-2 sans font-bold" type="button" aria-expanded="false"> <span data-template-id="event-1911-more" class="canva-text more-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Tìm hiểu thêm</span> <span data-template-id="event-1911-less" class="canva-text less-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Đóng chi tiết</span> <i data-lucide="chevron-down" class="w-4 h-4" aria-hidden="true"></i> </button>
         </div>
         <div class="detail-panel">
          <div>
           <div class="border-t border-stone-300/70 p-6 sm:p-7">
            <p data-template-id="event-1911-detail" class="canva-text leading-relaxed" style="color: rgb(68, 56, 47); font-weight: 400; font-style: normal; font-size: 16px;">Làm việc trên tàu và sinh sống tại nhiều quốc gia giúp Nguyễn Tất Thành quan sát các hệ thống thuộc địa, cộng đồng di cư, chính trị lao động và tranh luận xã hội chủ nghĩa. Về sau, Người sử dụng nhiều tên gọi, trong đó có Nguyễn Ái Quốc.</p>
           </div>
          </div>
         </div>
        </div>
       </article>
       <article class="event-row" data-year="1914" data-period="1914–1915" data-era="imperial" data-categories="wars politics economics"><span class="timeline-node" aria-hidden="true"></span>
        <div data-template-id="event-1914-card" class="canva-card event-card paper-card rounded-sm overflow-hidden" style="background: rgba(247, 239, 223, 0.96);"><img data-template-id="ww1-image" loading="lazy" class="canva-image w-full h-48 object-cover grayscale sepia" src="https://images.pexels.com/photos/20769502/pexels-photo-20769502.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=800" alt="Ảnh đơn sắc về một đài tưởng niệm lịch sử tại Gallipoli giữa những hàng cây.">
         <div class="p-6 sm:p-7">
          <div class="flex items-start justify-between gap-4 mb-4"><span data-template-id="event-1914-year" class="canva-text event-year font-bold" style="color: rgb(159, 36, 30); font-weight: 700; font-style: normal; font-size: 37px;">1914</span>
           <div class="flex flex-wrap justify-end gap-2"><span data-template-id="event-1914-tag-wars" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(223, 197, 189); color: rgb(113, 28, 24); font-weight: 400; font-style: normal; font-size: 16px;">Chiến tranh</span> <span data-template-id="event-1914-tag-politics" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 212, 205); color: rgb(123, 33, 28); font-weight: 400; font-style: normal; font-size: 16px;">Chính trị</span>
           </div>
          </div>
          <h3 data-template-id="event-1914-title" class="canva-text font-bold leading-tight mb-3" style="color: rgb(36, 28, 23); font-weight: 700; font-style: normal; font-size: 27px;">Chiến tranh thế giới thứ nhất bùng nổ</h3>
          <p data-template-id="event-1914-summary" class="canva-text leading-relaxed" style="color: rgb(76, 64, 54); font-weight: 400; font-style: normal; font-size: 16px;">Một cuộc khủng hoảng khu vực leo thang thành chiến tranh công nghiệp toàn cầu, huy động người dân và tài nguyên từ châu Âu, châu Phi, châu Á và Thái Bình Dương.</p>
          <div class="world-note mt-5 p-4">
           <p data-template-id="event-1914-world-label" class="canva-text sans font-bold uppercase tracking-[.12em] mb-1" style="color: rgb(118, 85, 31); font-weight: 400; font-style: normal; font-size: 11px;">Hệ quả chính trị</p>
           <p data-template-id="event-1914-world" class="canva-text leading-relaxed" style="color: rgb(87, 73, 59); font-weight: 400; font-style: normal; font-size: 16px;">Chiến tranh chia rẽ các phong trào xã hội chủ nghĩa quanh vấn đề ủng hộ chính phủ quốc gia, đồng thời làm gay gắt tranh luận về chủ nghĩa đế quốc, hòa bình và cách mạng.</p>
          </div><button class="learn-button mt-5 inline-flex items-center gap-2 sans font-bold" type="button" aria-expanded="false"> <span data-template-id="event-1914-more" class="canva-text more-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Mở bối cảnh chiến tranh</span> <span data-template-id="event-1914-less" class="canva-text less-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Đóng bối cảnh chiến tranh</span> <i data-lucide="chevron-down" class="w-4 h-4" aria-hidden="true"></i> </button>
         </div>
         <div class="detail-panel">
          <div>
           <div class="border-t border-stone-300/70 p-6 sm:p-7">
            <p data-template-id="event-1914-detail" class="canva-text leading-relaxed" style="color: rgb(68, 56, 47); font-weight: 400; font-style: normal; font-size: 16px;">Binh lính và lao động thuộc địa được huy động trên quy mô lớn. Tử vong hàng loạt, khan hiếm, di dời và khủng hoảng chính trị làm suy yếu nhiều đế quốc và mở ra những khả năng cách mạng mới.</p>
           </div>
          </div>
         </div>
        </div>
       </article>
       <article class="event-row" data-year="1916" data-period="1916" data-era="imperial" data-categories="politics economics wars"><span class="timeline-node" aria-hidden="true"></span>
        <div data-template-id="event-1916-card" class="canva-card event-card paper-card rounded-sm overflow-hidden" style="background: rgba(247, 239, 223, 0.96);"><img data-template-id="imperialism-image" loading="lazy" class="canva-image w-full h-48 object-cover sepia" src="https://images.pexels.com/photos/19328669/pexels-photo-19328669.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=800" alt="Những cuốn sách bìa da cổ được xếp trên kệ gỗ trong một thư viện ở Vienna.">
         <div class="p-6 sm:p-7">
          <div class="flex items-start justify-between gap-4 mb-4"><span data-template-id="event-1916-year" class="canva-text event-year font-bold" style="color: rgb(159, 36, 30); font-weight: 700; font-style: normal; font-size: 37px;">1916</span>
           <div class="flex flex-wrap justify-end gap-2"><span data-template-id="event-1916-tag-politics" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 212, 205); color: rgb(123, 33, 28); font-weight: 400; font-style: normal; font-size: 16px;">Chính trị</span> <span data-template-id="event-1916-tag-economics" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(232, 222, 193); color: rgb(102, 82, 28); font-weight: 400; font-style: normal; font-size: 16px;">Kinh tế</span>
           </div>
          </div>
          <h3 data-template-id="event-1916-title" class="canva-text font-bold leading-tight mb-3" style="color: rgb(36, 28, 23); font-weight: 700; font-style: normal; font-size: 27px;">Lenin viết Chủ nghĩa đế quốc</h3>
          <p data-template-id="event-1916-summary" class="canva-text leading-relaxed" style="color: rgb(76, 64, 54); font-weight: 400; font-style: normal; font-size: 16px;">Lenin liên hệ tư bản độc quyền, tư bản tài chính, mở rộng thuộc địa và cạnh tranh giữa các cường quốc trong một phân tích về kinh tế thế giới và chiến tranh.</p>
          <div class="world-note mt-5 p-4">
           <p data-template-id="event-1916-world-label" class="canva-text sans font-bold uppercase tracking-[.12em] mb-1" style="color: rgb(118, 85, 31); font-weight: 400; font-style: normal; font-size: 11px;">Bối cảnh lịch sử</p>
           <p data-template-id="event-1916-world" class="canva-text leading-relaxed" style="color: rgb(87, 73, 59); font-weight: 400; font-style: normal; font-size: 16px;">Chiến tranh châu Âu tiếp diễn, trong khi các thuộc địa cung cấp binh lính, nguyên liệu, lao động và nguồn thu cho các cường quốc đế quốc.</p>
          </div><button class="learn-button mt-5 inline-flex items-center gap-2 sans font-bold" type="button" aria-expanded="false"> <span data-template-id="event-1916-more" class="canva-text more-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Mở ghi chú tác phẩm</span> <span data-template-id="event-1916-less" class="canva-text less-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Đóng ghi chú tác phẩm</span> <i data-lucide="chevron-down" class="w-4 h-4" aria-hidden="true"></i> </button>
         </div>
         <div class="detail-panel">
          <div>
           <div class="border-t border-stone-300/70 p-6 sm:p-7">
            <p data-template-id="event-1916-detail" class="canva-text leading-relaxed" style="color: rgb(68, 56, 47); font-weight: 400; font-style: normal; font-size: 16px;">Tác phẩm có ảnh hưởng lớn trong các cách diễn giải Marxist–Leninist về chủ nghĩa thực dân và giải phóng dân tộc. Giới nghiên cứu vẫn tiếp tục tranh luận về cách phân kỳ kinh tế và phạm vi giải thích của tác phẩm.</p>
           </div>
          </div>
         </div>
        </div>
       </article>
       <article class="event-row" data-year="1917" data-period="1917–1919" data-era="revolution" data-categories="politics wars economics"><span class="timeline-node" aria-hidden="true"></span>
        <div data-template-id="event-1917-card" class="canva-card event-card paper-card rounded-sm overflow-hidden" style="background: rgba(247, 239, 223, 0.96);"><img data-template-id="october-image" loading="lazy" class="canva-image w-full h-52 object-cover grayscale contrast-125" src="https://images.pexels.com/photos/34632882/pexels-photo-34632882.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=800" alt="Ảnh lịch sử đen trắng về một cuộc diễu hành tại Quảng trường Đỏ.">
         <div class="p-6 sm:p-7">
          <div class="flex items-start justify-between gap-4 mb-4"><span data-template-id="event-1917-year" class="canva-text event-year font-bold" style="color: rgb(159, 36, 30); font-weight: 700; font-style: normal; font-size: 37px;">1917</span>
           <div class="flex flex-wrap justify-end gap-2"><span data-template-id="event-1917-tag-politics" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 212, 205); color: rgb(123, 33, 28); font-weight: 400; font-style: normal; font-size: 16px;">Chính trị</span> <span data-template-id="event-1917-tag-wars" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(223, 197, 189); color: rgb(113, 28, 24); font-weight: 400; font-style: normal; font-size: 16px;">Cách mạng</span>
           </div>
          </div>
          <h3 data-template-id="event-1917-title" class="canva-text font-bold leading-tight mb-3" style="color: rgb(36, 28, 23); font-weight: 700; font-style: normal; font-size: 27px;">Lenin và Cách mạng Tháng Mười</h3>
          <p data-template-id="event-1917-summary" class="canva-text leading-relaxed" style="color: rgb(76, 64, 54); font-weight: 400; font-style: normal; font-size: 16px;">Sau khi trở về từ lưu vong, Lenin chủ trương chuyển quyền lực cho các Xô viết công nhân và binh sĩ. Lực lượng Bolshevik lật đổ Chính phủ Lâm thời tại Petrograd vào tháng 11 theo lịch hiện đại.</p>
          <div class="world-note mt-5 p-4">
           <p data-template-id="event-1917-world-label" class="canva-text sans font-bold uppercase tracking-[.12em] mb-1" style="color: rgb(118, 85, 31); font-weight: 400; font-style: normal; font-size: 11px;">Sự kiện thế giới</p>
           <p data-template-id="event-1917-world" class="canva-text leading-relaxed" style="color: rgb(87, 73, 59); font-weight: 400; font-style: normal; font-size: 16px;">Chiến tranh thế giới thứ nhất gây thương vong lớn, khan hiếm, khủng hoảng chính trị và binh biến. Nước Nga sau đó bước vào một cuộc nội chiến tàn khốc.</p>
          </div><button class="learn-button mt-5 inline-flex items-center gap-2 sans font-bold" type="button" aria-expanded="false"> <span data-template-id="event-1917-more" class="canva-text more-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Mở trích đoạn diễn văn</span> <span data-template-id="event-1917-less" class="canva-text less-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Đóng trích đoạn diễn văn</span> <i data-lucide="chevron-down" class="w-4 h-4" aria-hidden="true"></i> </button>
         </div>
         <div class="detail-panel">
          <div>
           <div class="border-t border-stone-300/70 p-6 sm:p-7 grid sm:grid-cols-[145px_1fr] gap-5"><img data-template-id="lenin-image" loading="lazy" class="canva-image w-full h-44 sm:h-full object-cover grayscale sepia rounded-sm" src="https://images.pexels.com/photos/15209924/pexels-photo-15209924.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=800" alt="Tượng Lenin nổi bật trước mặt tiền một tòa nhà tại Minsk, Belarus.">
            <div>
             <blockquote data-template-id="lenin-quote" class="canva-text document-quote italic py-3 pl-10 pr-4 leading-relaxed" style="color: rgb(85, 37, 31); font-weight: 400; font-style: italic; font-size: 18px;">Giờ đây chúng ta sẽ bắt tay xây dựng trật tự xã hội chủ nghĩa.</blockquote>
             <p data-template-id="event-1917-detail" class="canva-text mt-4 leading-relaxed" style="color: rgb(68, 56, 47); font-weight: 400; font-style: normal; font-size: 16px;">Các lý luận của Lenin về tổ chức đảng, chủ nghĩa đế quốc và chiến lược cách mạng trở thành điểm tham chiếu cho nhiều phong trào cộng sản thế kỷ XX, dù cách diễn giải chúng luôn được tranh luận mạnh mẽ.</p>
            </div>
           </div>
          </div>
         </div>
        </div>
       </article>
       <article class="event-row" data-year="1920" data-period="1920" data-era="revolution" data-categories="vietnam politics"><span class="timeline-node" aria-hidden="true"></span>
        <div data-template-id="event-1920-card" class="canva-card event-card paper-card rounded-sm overflow-hidden" style="background: rgba(247, 239, 223, 0.96);">
         <div class="p-6 sm:p-7">
          <div class="flex items-start justify-between gap-4 mb-4"><span data-template-id="event-1920-year" class="canva-text event-year font-bold" style="color: rgb(159, 36, 30); font-weight: 700; font-style: normal; font-size: 37px;">1920</span>
           <div class="flex flex-wrap justify-end gap-2"><span data-template-id="event-1920-tag-vietnam" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 210, 174); color: rgb(111, 65, 18); font-weight: 400; font-style: normal; font-size: 16px;">Việt Nam</span> <span data-template-id="event-1920-tag-politics" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 212, 205); color: rgb(123, 33, 28); font-weight: 400; font-style: normal; font-size: 16px;">Chính trị</span>
           </div>
          </div>
          <h3 data-template-id="event-1920-title" class="canva-text font-bold leading-tight mb-3" style="color: rgb(36, 28, 23); font-weight: 700; font-style: normal; font-size: 27px;">Hồ Chí Minh tiếp cận luận cương của Lenin về vấn đề thuộc địa</h3>
          <p data-template-id="event-1920-summary" class="canva-text leading-relaxed" style="color: rgb(76, 64, 54); font-weight: 400; font-style: normal; font-size: 16px;">Tại Pháp, Nguyễn Ái Quốc đọc các luận cương của Lenin về vấn đề dân tộc và thuộc địa, từ đó nhìn thấy con đường giải phóng dân tộc Việt Nam gắn với cách mạng xã hội chủ nghĩa.</p>
          <div class="world-note mt-5 p-4">
           <p data-template-id="event-1920-world-label" class="canva-text sans font-bold uppercase tracking-[.12em] mb-1" style="color: rgb(118, 85, 31); font-weight: 400; font-style: normal; font-size: 11px;">Cùng thời điểm</p>
           <p data-template-id="event-1920-world" class="canva-text leading-relaxed" style="color: rgb(87, 73, 59); font-weight: 400; font-style: normal; font-size: 16px;">Trật tự hậu chiến đề cao quyền dân tộc tự quyết một cách không đồng đều, vẫn duy trì các đế quốc thuộc địa châu Âu trong khi phong trào chống thực dân phát triển.</p>
          </div><button class="learn-button mt-5 inline-flex items-center gap-2 sans font-bold" type="button" aria-expanded="false"> <span data-template-id="event-1920-more" class="canva-text more-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Tìm hiểu thêm</span> <span data-template-id="event-1920-less" class="canva-text less-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Đóng chi tiết</span> <i data-lucide="chevron-down" class="w-4 h-4" aria-hidden="true"></i> </button>
         </div>
         <div class="detail-panel">
          <div>
           <div class="border-t border-stone-300/70 p-6 sm:p-7">
            <p data-template-id="event-1920-detail" class="canva-text leading-relaxed" style="color: rgb(68, 56, 47); font-weight: 400; font-style: normal; font-size: 16px;">Tại Đại hội Tours, Nguyễn Ái Quốc ủng hộ bộ phận thành lập Đảng Cộng sản Pháp. Trong các hồi ức sau này, Hồ Chí Minh mô tả lập trường của Lenin về các dân tộc thuộc địa là một bước ngoặt quyết định.</p>
           </div>
          </div>
         </div>
        </div>
       </article>
       <article class="event-row" data-year="1921" data-period="1921–1929" data-era="revolution" data-categories="politics economics"><span class="timeline-node" aria-hidden="true"></span>
        <div data-template-id="event-1921-card" class="canva-card event-card paper-card rounded-sm overflow-hidden" style="background: rgba(247, 239, 223, 0.96);">
         <div class="p-6 sm:p-7">
          <div class="flex items-start justify-between gap-4 mb-4"><span data-template-id="event-1921-year" class="canva-text event-year font-bold" style="color: rgb(159, 36, 30); font-weight: 700; font-style: normal; font-size: 37px;">1921</span>
           <div class="flex flex-wrap justify-end gap-2"><span data-template-id="event-1921-tag-politics" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 212, 205); color: rgb(123, 33, 28); font-weight: 400; font-style: normal; font-size: 16px;">Chính trị</span> <span data-template-id="event-1921-tag-economics" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(232, 222, 193); color: rgb(102, 82, 28); font-weight: 400; font-style: normal; font-size: 16px;">Kinh tế</span>
           </div>
          </div>
          <h3 data-template-id="event-1921-title" class="canva-text font-bold leading-tight mb-3" style="color: rgb(36, 28, 23); font-weight: 700; font-style: normal; font-size: 27px;">Chính sách Kinh tế mới bắt đầu</h3>
          <p data-template-id="event-1921-summary" class="canva-text leading-relaxed" style="color: rgb(76, 64, 54); font-weight: 400; font-style: normal; font-size: 16px;">Sau nội chiến và sụp đổ kinh tế, lãnh đạo Xô viết cho phép thị trường và thương mại tư nhân có giới hạn, đồng thời giữ quyền kiểm soát nhà nước đối với các ngành công nghiệp lớn.</p>
          <div class="world-note mt-5 p-4">
           <p data-template-id="event-1921-world-label" class="canva-text sans font-bold uppercase tracking-[.12em] mb-1" style="color: rgb(118, 85, 31); font-weight: 400; font-style: normal; font-size: 11px;">Bối cảnh lịch sử</p>
           <p data-template-id="event-1921-world" class="canva-text leading-relaxed" style="color: rgb(87, 73, 59); font-weight: 400; font-style: normal; font-size: 16px;">Các chính quyền cách mạng đối diện thách thức thực tế: khôi phục sản xuất, duy trì quyền lực chính trị và xác định con đường đi lên chủ nghĩa xã hội.</p>
          </div><button class="learn-button mt-5 inline-flex items-center gap-2 sans font-bold" type="button" aria-expanded="false"> <span data-template-id="event-1921-more" class="canva-text more-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Mở ghi chú chính sách</span> <span data-template-id="event-1921-less" class="canva-text less-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Đóng ghi chú chính sách</span> <i data-lucide="chevron-down" class="w-4 h-4" aria-hidden="true"></i> </button>
         </div>
         <div class="detail-panel">
          <div>
           <div class="border-t border-stone-300/70 p-6 sm:p-7">
            <p data-template-id="event-1921-detail" class="canva-text leading-relaxed" style="color: rgb(68, 56, 47); font-weight: 400; font-style: normal; font-size: 16px;">Chính sách thể hiện sự linh hoạt chiến thuật nhưng cũng gây tranh luận về thị trường, quan hệ giai cấp, quyền lực của đảng và tốc độ chuyển đổi. Chính sách kết thúc khi công nghiệp hóa và tập thể hóa tăng tốc vào cuối thập niên.</p>
           </div>
          </div>
         </div>
        </div>
       </article>
       <article class="event-row" data-year="1930" data-period="1930–1944" data-era="revolution" data-categories="vietnam politics"><span class="timeline-node" aria-hidden="true"></span>
        <div data-template-id="event-1930-card" class="canva-card event-card paper-card rounded-sm overflow-hidden" style="background: rgba(247, 239, 223, 0.96);">
         <div class="p-6 sm:p-7">
          <div class="flex items-start justify-between gap-4 mb-4"><span data-template-id="event-1930-year" class="canva-text event-year font-bold" style="color: rgb(159, 36, 30); font-weight: 700; font-style: normal; font-size: 37px;">1930</span>
           <div class="flex flex-wrap justify-end gap-2"><span data-template-id="event-1930-tag-vietnam" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 210, 174); color: rgb(111, 65, 18); font-weight: 400; font-style: normal; font-size: 16px;">Việt Nam</span> <span data-template-id="event-1930-tag-politics" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 212, 205); color: rgb(123, 33, 28); font-weight: 400; font-style: normal; font-size: 16px;">Chính trị</span>
           </div>
          </div>
          <h3 data-template-id="event-1930-title" class="canva-text font-bold leading-tight mb-3" style="color: rgb(36, 28, 23); font-weight: 700; font-style: normal; font-size: 27px;">Các tổ chức cộng sản ở Việt Nam được thống nhất</h3>
          <p data-template-id="event-1930-summary" class="canva-text leading-relaxed" style="color: rgb(76, 64, 54); font-weight: 400; font-style: normal; font-size: 16px;">Nguyễn Ái Quốc góp phần hợp nhất các nhóm cách mạng cạnh tranh thành một tổ chức cộng sản thống nhất, tạo dựng cơ cấu bền vững cho cuộc đấu tranh chống thực dân.</p>
          <div class="world-note mt-5 p-4">
           <p data-template-id="event-1930-world-label" class="canva-text sans font-bold uppercase tracking-[.12em] mb-1" style="color: rgb(118, 85, 31); font-weight: 400; font-style: normal; font-size: 11px;">Cùng thời điểm</p>
           <p data-template-id="event-1930-world" class="canva-text leading-relaxed" style="color: rgb(87, 73, 59); font-weight: 400; font-style: normal; font-size: 16px;">Đại Khủng hoảng làm gián đoạn thương mại, việc làm và kinh tế thuộc địa, khiến căng thẳng xã hội và vận động chính trị gia tăng trên toàn thế giới.</p>
          </div><button class="learn-button mt-5 inline-flex items-center gap-2 sans font-bold" type="button" aria-expanded="false"> <span data-template-id="event-1930-more" class="canva-text more-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Mở ghi chú tổ chức</span> <span data-template-id="event-1930-less" class="canva-text less-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Đóng ghi chú tổ chức</span> <i data-lucide="chevron-down" class="w-4 h-4" aria-hidden="true"></i> </button>
         </div>
         <div class="detail-panel">
          <div>
           <div class="border-t border-stone-300/70 p-6 sm:p-7">
            <p data-template-id="event-1930-detail" class="canva-text leading-relaxed" style="color: rgb(68, 56, 47); font-weight: 400; font-style: normal; font-size: 16px;">Tên gọi và cơ cấu tổ chức thay đổi qua các thời kỳ đàn áp, hoạt động bí mật, chuyển đổi mặt trận và chiến tranh. Tổ chức gắn độc lập dân tộc với biến đổi xã hội và kinh tế.</p>
           </div>
          </div>
         </div>
        </div>
       </article>
       <article class="event-row" data-year="1945" data-period="1945–1953" data-era="liberation" data-categories="vietnam politics wars"><span class="timeline-node" aria-hidden="true"></span>
        <div data-template-id="event-1945-card" class="canva-card event-card paper-card rounded-sm overflow-hidden" style="background: rgba(247, 239, 223, 0.96);"><img data-template-id="vietnam-independence-image" loading="lazy" class="canva-image w-full h-52 object-cover sepia" src="https://images.pexels.com/photos/31647022/pexels-photo-31647022.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=800" alt="Lăng Chủ tịch Hồ Chí Minh và quốc kỳ Việt Nam lúc hoàng hôn ở Hà Nội.">
         <div class="p-6 sm:p-7">
          <div class="flex items-start justify-between gap-4 mb-4"><span data-template-id="event-1945-year" class="canva-text event-year font-bold" style="color: rgb(159, 36, 30); font-weight: 700; font-style: normal; font-size: 37px;">1945</span>
           <div class="flex flex-wrap justify-end gap-2"><span data-template-id="event-1945-tag-vietnam" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 210, 174); color: rgb(111, 65, 18); font-weight: 400; font-style: normal; font-size: 16px;">Việt Nam</span> <span data-template-id="event-1945-tag-wars" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(223, 197, 189); color: rgb(113, 28, 24); font-weight: 400; font-style: normal; font-size: 16px;">Chiến tranh</span>
           </div>
          </div>
          <h3 data-template-id="event-1945-title" class="canva-text font-bold leading-tight mb-3" style="color: rgb(36, 28, 23); font-weight: 700; font-style: normal; font-size: 27px;">Việt Nam tuyên bố độc lập</h3>
          <p data-template-id="event-1945-summary" class="canva-text leading-relaxed" style="color: rgb(76, 64, 54); font-weight: 400; font-style: normal; font-size: 16px;">Sau Cách mạng Tháng Tám, Hồ Chí Minh tuyên bố thành lập nước Việt Nam Dân chủ Cộng hòa trước đông đảo nhân dân tại Quảng trường Ba Đình, Hà Nội, ngày 2 tháng 9.</p>
          <div class="world-note mt-5 p-4">
           <p data-template-id="event-1945-world-label" class="canva-text sans font-bold uppercase tracking-[.12em] mb-1" style="color: rgb(118, 85, 31); font-weight: 400; font-style: normal; font-size: 11px;">Sự kiện thế giới</p>
           <p data-template-id="event-1945-world" class="canva-text leading-relaxed" style="color: rgb(87, 73, 59); font-weight: 400; font-style: normal; font-size: 16px;">Chiến tranh thế giới thứ hai kết thúc tại châu Á. Trên khắp thế giới thuộc địa, phong trào độc lập tăng tốc khi các cường quốc châu Âu tìm cách tái lập quyền kiểm soát.</p>
          </div><button class="learn-button mt-5 inline-flex items-center gap-2 sans font-bold" type="button" aria-expanded="false"> <span data-template-id="event-1945-more" class="canva-text more-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Mở trích đoạn tuyên ngôn</span> <span data-template-id="event-1945-less" class="canva-text less-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Đóng trích đoạn tuyên ngôn</span> <i data-lucide="chevron-down" class="w-4 h-4" aria-hidden="true"></i> </button>
         </div>
         <div class="detail-panel">
          <div>
           <div class="border-t border-stone-300/70 p-6 sm:p-7">
            <blockquote data-template-id="independence-quote" class="canva-text document-quote italic py-3 pl-10 pr-4 leading-relaxed" style="color: rgb(85, 37, 31); font-weight: 400; font-style: italic; font-size: 18px;">Tất cả mọi người đều sinh ra có quyền bình đẳng. Tạo hóa cho họ những quyền không ai có thể xâm phạm được; trong những quyền ấy, có quyền được sống, quyền tự do và quyền mưu cầu hạnh phúc.</blockquote>
            <p data-template-id="event-1945-detail" class="canva-text mt-4 leading-relaxed" style="color: rgb(68, 56, 47); font-weight: 400; font-style: normal; font-size: 16px;">Bản tuyên ngôn viện dẫn các văn kiện cách mạng của Hoa Kỳ và Pháp trước khi trình bày những tội ác của chế độ thực dân Pháp. Độc lập sau đó được tiếp nối bởi cuộc kháng chiến kéo dài chống Pháp.</p>
           </div>
          </div>
         </div>
        </div>
       </article>
       <article class="event-row" data-year="1954" data-period="1954–1968" data-era="liberation" data-categories="vietnam politics wars"><span class="timeline-node" aria-hidden="true"></span>
        <div data-template-id="event-1954-card" class="canva-card event-card paper-card rounded-sm overflow-hidden" style="background: rgba(247, 239, 223, 0.96);"><img data-template-id="dien-bien-image" loading="lazy" class="canva-image w-full h-52 object-cover sepia" src="https://images.pexels.com/photos/7300735/pexels-photo-7300735.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=800" alt="Đài tưởng niệm chiến thắng lịch sử tại Việt Nam dưới bầu trời trong xanh.">
         <div class="p-6 sm:p-7">
          <div class="flex items-start justify-between gap-4 mb-4"><span data-template-id="event-1954-year" class="canva-text event-year font-bold" style="color: rgb(159, 36, 30); font-weight: 700; font-style: normal; font-size: 37px;">1954</span>
           <div class="flex flex-wrap justify-end gap-2"><span data-template-id="event-1954-tag-vietnam" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 210, 174); color: rgb(111, 65, 18); font-weight: 400; font-style: normal; font-size: 16px;">Việt Nam</span> <span data-template-id="event-1954-tag-wars" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(223, 197, 189); color: rgb(113, 28, 24); font-weight: 400; font-style: normal; font-size: 16px;">Chiến tranh</span>
           </div>
          </div>
          <h3 data-template-id="event-1954-title" class="canva-text font-bold leading-tight mb-3" style="color: rgb(36, 28, 23); font-weight: 700; font-style: normal; font-size: 27px;">Chiến thắng Điện Biên Phủ</h3>
          <p data-template-id="event-1954-summary" class="canva-text leading-relaxed" style="color: rgb(76, 64, 54); font-weight: 400; font-style: normal; font-size: 16px;">Quân đội Việt Nam đánh bại tập đoàn cứ điểm của Pháp tại Điện Biên Phủ, làm thay đổi quyết định các cuộc đàm phán về tương lai của Đông Dương thuộc Pháp.</p>
          <div class="world-note mt-5 p-4">
           <p data-template-id="event-1954-world-label" class="canva-text sans font-bold uppercase tracking-[.12em] mb-1" style="color: rgb(118, 85, 31); font-weight: 400; font-style: normal; font-size: 11px;">Hệ quả toàn cầu</p>
           <p data-template-id="event-1954-world" class="canva-text leading-relaxed" style="color: rgb(87, 73, 59); font-weight: 400; font-style: normal; font-size: 16px;">Chiến thắng tạo tiếng vang trong các xã hội thuộc địa, còn Hiệp định Genève tạm thời chia cắt Việt Nam để chờ tổng tuyển cử trên toàn quốc.</p>
          </div><button class="learn-button mt-5 inline-flex items-center gap-2 sans font-bold" type="button" aria-expanded="false"> <span data-template-id="event-1954-more" class="canva-text more-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Mở bối cảnh chiến dịch</span> <span data-template-id="event-1954-less" class="canva-text less-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Đóng bối cảnh chiến dịch</span> <i data-lucide="chevron-down" class="w-4 h-4" aria-hidden="true"></i> </button>
         </div>
         <div class="detail-panel">
          <div>
           <div class="border-t border-stone-300/70 p-6 sm:p-7">
            <p data-template-id="event-1954-detail" class="canva-text leading-relaxed" style="color: rgb(68, 56, 47); font-weight: 400; font-style: normal; font-size: 16px;">Chiến dịch kết hợp hậu cần, pháo binh, hệ thống chiến hào và huy động bền bỉ trên địa hình khó khăn. Kết quả chấm dứt Chiến tranh Đông Dương lần thứ nhất nhưng chưa đem lại hòa bình lâu dài cho Việt Nam.</p>
           </div>
          </div>
         </div>
        </div>
       </article>
       <article class="event-row" data-year="1969" data-period="1969–1974" data-era="liberation" data-categories="vietnam politics wars"><span class="timeline-node" aria-hidden="true"></span>
        <div data-template-id="event-1969-card" class="canva-card event-card paper-card rounded-sm overflow-hidden" style="background: rgba(247, 239, 223, 0.96);">
         <div class="p-6 sm:p-7">
          <div class="flex items-start justify-between gap-4 mb-4"><span data-template-id="event-1969-year" class="canva-text event-year font-bold" style="color: rgb(159, 36, 30); font-weight: 700; font-style: normal; font-size: 37px;">1969</span>
           <div class="flex flex-wrap justify-end gap-2"><span data-template-id="event-1969-tag-vietnam" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 210, 174); color: rgb(111, 65, 18); font-weight: 400; font-style: normal; font-size: 16px;">Việt Nam</span> <span data-template-id="event-1969-tag-wars" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(223, 197, 189); color: rgb(113, 28, 24); font-weight: 400; font-style: normal; font-size: 16px;">Chiến tranh</span>
           </div>
          </div>
          <h3 data-template-id="event-1969-title" class="canva-text font-bold leading-tight mb-3" style="color: rgb(36, 28, 23); font-weight: 700; font-style: normal; font-size: 27px;">Di chúc và di sản lâu dài của Hồ Chí Minh</h3>
          <p data-template-id="event-1969-summary" class="canva-text leading-relaxed" style="color: rgb(76, 64, 54); font-weight: 400; font-style: normal; font-size: 16px;">Hồ Chí Minh qua đời tại Hà Nội ngày 2 tháng 9. Di chúc chính trị của Người nhấn mạnh đoàn kết, tình hữu nghị quốc tế và công cuộc tái thiết Việt Nam sau chiến tranh.</p>
          <div class="world-note mt-5 p-4">
           <p data-template-id="event-1969-world-label" class="canva-text sans font-bold uppercase tracking-[.12em] mb-1" style="color: rgb(118, 85, 31); font-weight: 400; font-style: normal; font-size: 11px;">Cùng thời điểm</p>
           <p data-template-id="event-1969-world" class="canva-text leading-relaxed" style="color: rgb(87, 73, 59); font-weight: 400; font-style: normal; font-size: 16px;">Chiến tranh Việt Nam vẫn diễn ra ác liệt, trong khi các phong trào phản chiến, dân quyền, sinh viên và phi thực dân hóa làm thay đổi chính trị toàn cầu.</p>
          </div><button class="learn-button mt-5 inline-flex items-center gap-2 sans font-bold" type="button" aria-expanded="false"> <span data-template-id="event-1969-more" class="canva-text more-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Mở trích đoạn di chúc</span> <span data-template-id="event-1969-less" class="canva-text less-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Đóng trích đoạn di chúc</span> <i data-lucide="chevron-down" class="w-4 h-4" aria-hidden="true"></i> </button>
         </div>
         <div class="detail-panel">
          <div>
           <div class="border-t border-stone-300/70 p-6 sm:p-7 grid sm:grid-cols-[170px_1fr] gap-5"><img data-template-id="ho-chi-minh-image" loading="lazy" class="canva-image w-full h-44 sm:h-full object-cover grayscale sepia rounded-sm" src="https://images.pexels.com/photos/34361934/pexels-photo-34361934.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=800" alt="Kiến trúc trang nghiêm của Lăng Chủ tịch Hồ Chí Minh tại Hà Nội.">
            <div>
             <blockquote data-template-id="testament-quote" class="canva-text document-quote italic py-3 pl-10 pr-4 leading-relaxed" style="color: rgb(85, 37, 31); font-weight: 400; font-style: italic; font-size: 18px;">Điều mong muốn cuối cùng của tôi là: Toàn Đảng, toàn dân ta đoàn kết phấn đấu, xây dựng một nước Việt Nam hòa bình, thống nhất, độc lập, dân chủ và giàu mạnh.</blockquote>
             <p data-template-id="event-1969-detail" class="canva-text mt-4 leading-relaxed" style="color: rgb(68, 56, 47); font-weight: 400; font-style: normal; font-size: 16px;">Di sản Hồ Chí Minh kết hợp chủ nghĩa yêu nước chống thực dân, chủ nghĩa Marx–Lenin, vai trò lãnh đạo nhà nước, năng lực tổ chức chính trị và hình ảnh đạo đức công vụ giản dị.</p>
            </div>
           </div>
          </div>
         </div>
        </div>
       </article>
       <article class="event-row" data-year="1975" data-period="1975" data-era="liberation" data-categories="vietnam politics wars"><span class="timeline-node" aria-hidden="true"></span>
        <div data-template-id="event-1975-card" class="canva-card event-card paper-card rounded-sm overflow-hidden" style="background: rgba(247, 239, 223, 0.96);"><img data-template-id="reunification-image" loading="lazy" class="canva-image w-full h-52 object-cover sepia" src="https://images.pexels.com/photos/34230016/pexels-photo-34230016.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=800" alt="Mặt trước Dinh Độc Lập và đài phun nước tại Thành phố Hồ Chí Minh.">
         <div class="p-6 sm:p-7">
          <div class="flex items-start justify-between gap-4 mb-4"><span data-template-id="event-1975-year" class="canva-text event-year font-bold" style="color: rgb(159, 36, 30); font-weight: 700; font-style: normal; font-size: 37px;">1975</span>
           <div class="flex flex-wrap justify-end gap-2"><span data-template-id="event-1975-tag-vietnam" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 210, 174); color: rgb(111, 65, 18); font-weight: 400; font-style: normal; font-size: 16px;">Việt Nam</span> <span data-template-id="event-1975-tag-wars" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(223, 197, 189); color: rgb(113, 28, 24); font-weight: 400; font-style: normal; font-size: 16px;">Chiến tranh</span>
           </div>
          </div>
          <h3 data-template-id="event-1975-title" class="canva-text font-bold leading-tight mb-3" style="color: rgb(36, 28, 23); font-weight: 700; font-style: normal; font-size: 27px;">Chiến tranh kết thúc, đất nước tiến tới thống nhất</h3>
          <p data-template-id="event-1975-summary" class="canva-text leading-relaxed" style="color: rgb(76, 64, 54); font-weight: 400; font-style: normal; font-size: 16px;">Sài Gòn được giải phóng ngày 30 tháng 4, chấm dứt nhiều thập niên chiến tranh và đưa cả nước về dưới một chính quyền quốc gia.</p>
          <div class="world-note mt-5 p-4">
           <p data-template-id="event-1975-world-label" class="canva-text sans font-bold uppercase tracking-[.12em] mb-1" style="color: rgb(118, 85, 31); font-weight: 400; font-style: normal; font-size: 11px;">Hệ quả lịch sử</p>
           <p data-template-id="event-1975-world" class="canva-text leading-relaxed" style="color: rgb(87, 73, 59); font-weight: 400; font-style: normal; font-size: 16px;">Việc kết thúc xung đột làm thay đổi chính trị Đông Nam Á và mở đầu giai đoạn khó khăn của tái thiết, di cư và điều chỉnh hậu chiến.</p>
          </div><button class="learn-button mt-5 inline-flex items-center gap-2 sans font-bold" type="button" aria-expanded="false"> <span data-template-id="event-1975-more" class="canva-text more-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Mở ghi chú thống nhất</span> <span data-template-id="event-1975-less" class="canva-text less-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Đóng ghi chú thống nhất</span> <i data-lucide="chevron-down" class="w-4 h-4" aria-hidden="true"></i> </button>
         </div>
         <div class="detail-panel">
          <div>
           <div class="border-t border-stone-300/70 p-6 sm:p-7">
            <p data-template-id="event-1975-detail" class="canva-text leading-relaxed" style="color: rgb(68, 56, 47); font-weight: 400; font-style: normal; font-size: 16px;">Thắng lợi quân sự không thể lập tức giải quyết những tổn thất to lớn về con người và vật chất. Khôi phục hạ tầng, hòa nhập các vùng miền và xử lý tình trạng di dời trở thành những nhiệm vụ quốc gia cấp bách.</p>
           </div>
          </div>
         </div>
        </div>
       </article>
       <article class="event-row" data-year="1976" data-period="1976" data-era="liberation" data-categories="vietnam politics economics"><span class="timeline-node" aria-hidden="true"></span>
        <div data-template-id="event-1976-card" class="canva-card event-card paper-card rounded-sm overflow-hidden" style="background: rgba(247, 239, 223, 0.96);">
         <div class="p-6 sm:p-7">
          <div class="flex items-start justify-between gap-4 mb-4"><span data-template-id="event-1976-year" class="canva-text event-year font-bold" style="color: rgb(159, 36, 30); font-weight: 700; font-style: normal; font-size: 37px;">1976</span>
           <div class="flex flex-wrap justify-end gap-2"><span data-template-id="event-1976-tag-vietnam" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 210, 174); color: rgb(111, 65, 18); font-weight: 400; font-style: normal; font-size: 16px;">Việt Nam</span> <span data-template-id="event-1976-tag-politics" class="canva-tag category-chip rounded-full px-2.5 py-1" style="background: rgb(234, 212, 205); color: rgb(123, 33, 28); font-weight: 400; font-style: normal; font-size: 16px;">Chính trị</span>
           </div>
          </div>
          <h3 data-template-id="event-1976-title" class="canva-text font-bold leading-tight mb-3" style="color: rgb(36, 28, 23); font-weight: 700; font-style: normal; font-size: 27px;">Nước Cộng hòa Xã hội Chủ nghĩa Việt Nam được thành lập</h3>
          <p data-template-id="event-1976-summary" class="canva-text leading-relaxed" style="color: rgb(76, 64, 54); font-weight: 400; font-style: normal; font-size: 16px;">Quốc hội chính thức thống nhất nhà nước với tên gọi Cộng hòa Xã hội Chủ nghĩa Việt Nam và thủ đô là Hà Nội.</p>
          <div class="world-note mt-5 p-4">
           <p data-template-id="event-1976-world-label" class="canva-text sans font-bold uppercase tracking-[.12em] mb-1" style="color: rgb(118, 85, 31); font-weight: 400; font-style: normal; font-size: 11px;">Một chương mới</p>
           <p data-template-id="event-1976-world" class="canva-text leading-relaxed" style="color: rgb(87, 73, 59); font-weight: 400; font-style: normal; font-size: 16px;">Việt Nam hậu chiến bước vào công cuộc tái thiết giữa khó khăn kinh tế, cô lập quốc tế, căng thẳng khu vực và những hệ quả xã hội lâu dài của xung đột.</p>
          </div><button class="learn-button mt-5 inline-flex items-center gap-2 sans font-bold" type="button" aria-expanded="false"> <span data-template-id="event-1976-more" class="canva-text more-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Mở ghi chú xây dựng nhà nước</span> <span data-template-id="event-1976-less" class="canva-text less-label" style="color: rgb(142, 32, 27); font-weight: 700; font-style: normal; font-size: 16px;">Đóng ghi chú xây dựng nhà nước</span> <i data-lucide="chevron-down" class="w-4 h-4" aria-hidden="true"></i> </button>
         </div>
         <div class="detail-panel">
          <div>
           <div class="border-t border-stone-300/70 p-6 sm:p-7">
            <p data-template-id="event-1976-detail" class="canva-text leading-relaxed" style="color: rgb(68, 56, 47); font-weight: 400; font-style: normal; font-size: 16px;">Nhà nước mới tiếp nhận những thể chế thời chiến và các nền kinh tế bị tổn hại khác nhau ở hai miền. Lịch sử tiếp theo gồm tái thiết, tập thể hóa, xung đột khu vực và công cuộc Đổi Mới bắt đầu từ năm 1986.</p>
           </div>
          </div>
         </div>
        </div>
       </article>
      </div>
      <div id="empty-state" data-template-id="empty-state" class="canva-banner hidden relative z-10 max-w-xl mx-auto rounded-sm p-8 text-center shadow-md" style="background: rgb(247, 239, 223); color: rgb(90, 69, 56); font-weight: 600; font-style: normal; font-size: 18px;">Không có sự kiện nào phù hợp với tổ hợp bộ lọc này. Hãy chọn chủ đề khác hoặc chọn “Hiển thị tất cả”.</div>
     </div>
    </div>
   </section>
   <section data-template-id="closing-section" class="canva-section w-full border-y border-amber-100/20 py-12 backdrop-blur-md" style="background: rgba(48, 25, 18, 0.72);">
    <div class="max-w-4xl mx-auto px-6 text-center"><i data-lucide="library" class="w-8 h-8 mx-auto mb-4 text-amber-300" aria-hidden="true"></i>
     <h2 data-template-id="closing-title" class="canva-text font-bold mb-3" style="color: rgb(255, 241, 216); font-weight: 700; font-style: normal; font-size: 30px;">Đọc lịch sử qua tư liệu — và qua tranh luận</h2>
     <p data-template-id="closing-text" class="canva-text leading-relaxed" style="color: rgb(234, 219, 195); font-weight: 400; font-style: normal; font-size: 17px;">Cách diễn giải lịch sử thay đổi theo chứng cứ, bản dịch và góc nhìn. Hãy xem dòng thời gian này là điểm khởi đầu, rồi đối chiếu văn bản gốc, hồ sơ lưu trữ, tiểu sử và nghiên cứu từ nhiều truyền thống khác nhau.</p>
    </div>
   </section>
  </main>
  <footer data-template-id="footer-section" class="canva-footer w-full py-8" style="background: rgba(56, 23, 20, 0.95);">
   <div class="max-w-6xl mx-auto px-6 flex flex-col sm:flex-row items-center justify-between gap-4">
    <p data-template-id="footer-text" class="canva-text text-center sm:text-left" style="color: rgb(230, 213, 185); font-weight: 400; font-style: normal; font-size: 14px;">Ưebsite host trên Github nên bố cục hơi có vấn đề, mong mọi người thông cảm</p><button id="back-to-top" data-template-id="back-to-top" class="canva-button inline-flex items-center gap-2 rounded-sm px-4 py-2 sans font-bold" type="button" style="background: rgb(169, 42, 35); color: rgb(255, 255, 255); font-weight: 700; font-style: normal; font-size: 14px;">Về đầu trang</button>
   </div>
  </footer>
  <script src="/_sdk/c939c145c3c74230.editing_sdk.js" integrity="sha512-jh2pv/gl9Gzzn5dxfzwQO4wkqtnAQIim+LIUDYfVu2cdqPkQV2MqbjsDUW5IYbrSZFjRlOBrIWzlvWDXQYxOjg=="></script>
  <script>
    document.addEventListener("DOMContentLoaded", () => {
      lucide.createIcons();

      const rows = Array.from(document.querySelectorAll(".event-row"));
      const filterButtons = Array.from(document.querySelectorAll("[data-filter]"));
      const showAllButton = document.getElementById("show-all");
      const emptyState = document.getElementById("empty-state");
      const timelineShell = document.getElementById("timeline-shell");
      const timelineSection = document.getElementById("timeline");
      const periodValue = document.getElementById("period-value");
      const eraValue = document.getElementById("era-value");
      const backgrounds = Array.from(document.querySelectorAll("[data-era-background]"));
      const activeFilters = new Set();

      const eraNames = {
        industrial: "Châu Âu công nghiệp",
        revolutions: "Cách mạng và tổ chức",
        imperial: "Đế quốc và chiến tranh thế giới",
        revolution: "Cách mạng và chủ nghĩa quốc tế",
        liberation: "Giải phóng và thống nhất Việt Nam"
      };

      const revealObserver = new IntersectionObserver((entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            entry.target.classList.add("is-visible");
            revealObserver.unobserve(entry.target);
          }
        });
      }, { threshold: 0.12 });

      rows.forEach((row, index) => {
        row.querySelector(".event-card").style.transitionDelay = `${Math.min(index * 35, 175)}ms`;
        revealObserver.observe(row);
        const button = row.querySelector(".learn-button");
        button.addEventListener("click", () => {
          const isOpen = row.classList.toggle("is-open");
          button.setAttribute("aria-expanded", String(isOpen));
          requestAnimationFrame(updateScrollState);
        });
      });

      function applyFilters() {
        let visibleCount = 0;
        rows.forEach((row) => {
          const categories = row.dataset.categories.split(" ");
          const matches = activeFilters.size === 0 || categories.some((category) => activeFilters.has(category));
          row.classList.toggle("is-filtered", !matches);
          if (matches) {
            visibleCount += 1;
            row.classList.add("is-visible");
          }
        });
        filterButtons.forEach((button) => {
          const selected = activeFilters.has(button.dataset.filter);
          button.classList.toggle("is-active", selected);
          button.setAttribute("aria-pressed", String(selected));
        });
        emptyState.classList.toggle("hidden", visibleCount !== 0);
        requestAnimationFrame(updateScrollState);
      }

      filterButtons.forEach((button) => {
        button.addEventListener("click", () => {
          const filter = button.dataset.filter;
          if (activeFilters.has(filter)) activeFilters.delete(filter);
          else activeFilters.add(filter);
          applyFilters();
        });
      });

      showAllButton.addEventListener("click", () => {
        activeFilters.clear();
        applyFilters();
      });

      let activeEra = "industrial";

      function setEra(nextEra) {
        if (!nextEra || nextEra === activeEra) return;
        activeEra = nextEra;
        eraValue.textContent = eraNames[nextEra];
        backgrounds.forEach((image) => {
          image.classList.toggle("is-active", image.dataset.eraBackground === nextEra);
        });
      }

      function updateScrollState() {
        const rect = timelineShell.getBoundingClientRect();
        const viewportReference = window.innerHeight * 0.48;
        const progress = Math.max(0, Math.min(1, (viewportReference - rect.top) / Math.max(rect.height, 1)));
        timelineShell.style.setProperty("--progress", `${progress * 100}%`);

        if (timelineSection.getBoundingClientRect().top > viewportReference) {
          periodValue.textContent = "1818–1847";
          setEra("industrial");
          return;
        }

        const visibleRows = rows.filter((row) => !row.classList.contains("is-filtered"));
        let closest = null;
        let closestDistance = Infinity;

        visibleRows.forEach((row) => {
          const distance = Math.abs(row.getBoundingClientRect().top - viewportReference);
          if (distance < closestDistance) {
            closest = row;
            closestDistance = distance;
          }
        });

        if (closest) {
          periodValue.textContent = closest.dataset.period;
          if (closest.dataset.era === activeEra) {
            eraValue.textContent = eraNames[activeEra];
          } else {
            setEra(closest.dataset.era);
          }
        }
      }

      let ticking = false;
      window.addEventListener("scroll", () => {
        if (!ticking) {
          requestAnimationFrame(() => {
            updateScrollState();
            ticking = false;
          });
          ticking = true;
        }
      }, { passive: true });
      window.addEventListener("resize", updateScrollState);

      document.getElementById("back-to-top").addEventListener("click", () => {
        window.scrollTo({ top: 0, behavior: "smooth" });
      });

      const musicButton = document.getElementById("music-toggle");
      const muteButton = document.getElementById("mute-toggle");
      let audioContext = null;
      let masterGain = null;
      let musicTimer = null;
      let musicPlaying = false;
      let muted = false;
      let step = 0;
      const progression = [
        [146.83, 220.00, 293.66],
        [130.81, 196.00, 261.63],
        [110.00, 164.81, 220.00],
        [123.47, 185.00, 246.94]
      ];

      function createTone(frequency, start, duration, volume, type) {
        const oscillator = audioContext.createOscillator();
        const gain = audioContext.createGain();
        oscillator.type = type;
        oscillator.frequency.setValueAtTime(frequency, start);
        gain.gain.setValueAtTime(0.0001, start);
        gain.gain.exponentialRampToValueAtTime(volume, start + 0.35);
        gain.gain.exponentialRampToValueAtTime(0.0001, start + duration);
        oscillator.connect(gain);
        gain.connect(masterGain);
        oscillator.start(start);
        oscillator.stop(start + duration + 0.05);
      }

      function playMeasure() {
        if (!musicPlaying || !audioContext) return;
        const now = audioContext.currentTime;
        const chord = progression[step % progression.length];
        chord.forEach((note, index) => createTone(note / 2, now + index * 0.12, 6.5, 0.024, "triangle"));
        createTone(chord[1] * 2, now + 1.6, 2.4, 0.012, "sine");
        createTone(chord[2] * 2, now + 4.3, 2.1, 0.009, "sine");
        step += 1;
      }

      async function startMusic() {
        if (!audioContext) {
          audioContext = new (window.AudioContext || window.webkitAudioContext)();
          masterGain = audioContext.createGain();
          masterGain.gain.value = 0.72;
          masterGain.connect(audioContext.destination);
        }
        if (audioContext.state === "suspended") await audioContext.resume();
        musicPlaying = true;
        musicButton.classList.add("is-on");
        musicButton.setAttribute("aria-pressed", "true");
        muteButton.disabled = false;
        playMeasure();
        musicTimer = window.setInterval(playMeasure, 6400);
      }

      function stopMusic() {
        musicPlaying = false;
        musicButton.classList.remove("is-on");
        musicButton.setAttribute("aria-pressed", "false");
        if (musicTimer) window.clearInterval(musicTimer);
        musicTimer = null;
        if (audioContext && audioContext.state === "running") audioContext.suspend();
      }

      musicButton.addEventListener("click", async () => {
        if (musicPlaying) stopMusic();
        else await startMusic();
      });

      muteButton.addEventListener("click", () => {
        if (!masterGain) return;
        muted = !muted;
        masterGain.gain.setTargetAtTime(muted ? 0.0001 : 0.72, audioContext.currentTime, 0.08);
        muteButton.classList.toggle("is-on", muted);
        muteButton.setAttribute("aria-pressed", String(muted));
      });

      eraValue.textContent = eraNames.industrial;
      updateScrollState();
    });
  </script>
 
</body></html>
