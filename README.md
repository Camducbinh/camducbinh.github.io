<html lang="vi">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Cam Đức Bình | Business Intelligence Analyst Intern</title>
  <meta name="description" content="Portfolio cá nhân của Cam Đức Bình - Business Intelligence Analyst Intern." />
  <style>
    :root {
      --bg: #f7f4ee;
      --surface: #fff;
      --ink: #18202a;
      --muted: #607080;
      --line: #ded8ce;
      --blue: #1e6bff;
      --green: #0c8f72;
      --coral: #e76f51;
      --shadow: 0 20px 60px rgba(24, 32, 42, .12);
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }

    body {
      margin: 0;
      background: var(--bg);
      color: var(--ink);
      font-family: "Segoe UI", system-ui, -apple-system, BlinkMacSystemFont, Arial, sans-serif;
      line-height: 1.6;
    }

    a { color: inherit; text-decoration: none; }

    .site-header {
      position: sticky;
      top: 0;
      z-index: 10;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 24px;
      padding: 18px clamp(20px, 5vw, 72px);
      border-bottom: 1px solid rgba(222, 216, 206, .76);
      background: rgba(247, 244, 238, .88);
      backdrop-filter: blur(16px);
    }

    .brand, .site-nav, .hero-actions, .quick-facts, .dashboard-top,
    .info-card, .info-meta, .contact-panel, .site-footer {
      display: flex;
      align-items: center;
    }

    .brand {
      gap: 12px;
      font-weight: 800;
    }

    .brand-mark {
      display: grid;
      width: 42px;
      height: 42px;
      place-items: center;
      border-radius: 8px;
      background: var(--ink);
      color: #fff;
      font-size: .88rem;
    }

    .site-nav {
      gap: 6px;
    }

    .site-nav a {
      border-radius: 8px;
      color: var(--muted);
      font-size: .94rem;
      font-weight: 700;
      padding: 10px 12px;
      white-space: nowrap;
    }

    .site-nav a:hover {
      background: var(--surface);
      color: var(--ink);
    }

    .section {
      width: min(1120px, calc(100% - 40px));
      margin: 0 auto;
      padding: 88px 0;
    }

    .hero {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(320px, .72fr);
      gap: clamp(32px, 6vw, 76px);
      align-items: center;
      min-height: calc(100vh - 80px);
      padding-top: 60px;
    }

    .eyebrow {
      margin: 0 0 14px;
      color: var(--green);
      font-size: .78rem;
      font-weight: 800;
      letter-spacing: .12em;
      text-transform: uppercase;
    }

    h1, h2, h3, p { margin-top: 0; }

    h1 {
      max-width: 840px;
      margin-bottom: 22px;
      font-size: clamp(2.55rem, 6vw, 5.8rem);
      line-height: .98;
    }

    h2 {
      margin-bottom: 0;
      font-size: clamp(2rem, 4vw, 3.4rem);
      line-height: 1.06;
    }

    h3 {
      margin-bottom: 8px;
      font-size: 1.16rem;
      line-height: 1.25;
    }

    .hero-text {
      max-width: 680px;
      color: var(--muted);
      font-size: clamp(1.05rem, 2vw, 1.25rem);
    }

    .hero-actions {
      flex-wrap: wrap;
      gap: 12px;
      margin: 34px 0;
    }

    .button {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      min-height: 48px;
      border: 1px solid var(--ink);
      border-radius: 8px;
      font-weight: 800;
      padding: 12px 18px;
    }

    .button.primary {
      background: var(--ink);
      color: #fff;
    }

    .button.secondary {
      background: transparent;
    }

    .quick-facts {
      flex-wrap: wrap;
      gap: 12px;
      margin: 0;
    }

    .quick-facts div {
      min-width: 150px;
      border: 1px solid var(--line);
      border-radius: 8px;
      background: rgba(255, 255, 255, .58);
      padding: 14px 16px;
    }

    .quick-facts dt, .panel-label, .award-card span {
      color: var(--muted);
      font-size: .78rem;
      font-weight: 800;
      letter-spacing: .08em;
      text-transform: uppercase;
    }

    .quick-facts dd {
      margin: 3px 0 0;
      font-weight: 800;
    }

    .dashboard-card {
      border: 1px solid rgba(24, 32, 42, .08);
      border-radius: 8px;
      background:
        linear-gradient(145deg, rgba(255,255,255,.94), rgba(255,255,255,.7)),
        repeating-linear-gradient(90deg, rgba(30,107,255,.09) 0 1px, transparent 1px 52px);
      box-shadow: var(--shadow);
      padding: clamp(22px, 4vw, 34px);
    }

    .dashboard-top {
      justify-content: space-between;
      gap: 16px;
    }

    .status-dot {
      border-radius: 999px;
      background: rgba(12, 143, 114, .1);
      color: var(--green);
      font-size: .8rem;
      font-weight: 800;
      padding: 7px 10px;
    }

    .score-ring {
      display: grid;
      width: min(220px, 70vw);
      aspect-ratio: 1;
      place-items: center;
      margin: 34px auto;
      border-radius: 50%;
      background:
        radial-gradient(circle closest-side, #fff 68%, transparent 70% 100%),
        conic-gradient(var(--blue) 0 54%, var(--green) 54% 86%, rgba(96,112,128,.16) 86% 100%);
    }

    .score-ring span {
      font-size: 2.75rem;
      font-weight: 800;
    }

    .bar-list { display: grid; gap: 16px; }

    .bar-row {
      display: grid;
      grid-template-columns: 82px 1fr;
      gap: 12px;
      align-items: center;
      color: var(--muted);
      font-size: .92rem;
      font-weight: 800;
    }

    .bar-row i {
      position: relative;
      display: block;
      height: 12px;
      overflow: hidden;
      border-radius: 999px;
      background: rgba(96,112,128,.16);
    }

    .bar-row i::before {
      position: absolute;
      inset: 0 auto 0 0;
      width: var(--value);
      border-radius: inherit;
      background: linear-gradient(90deg, var(--blue), var(--green));
      content: "";
    }

    .split, .contact {
      display: grid;
      grid-template-columns: minmax(0, .85fr) minmax(0, 1fr);
      gap: clamp(28px, 6vw, 72px);
      border-top: 1px solid var(--line);
    }

    .content-stack {
      display: grid;
      gap: 18px;
      color: var(--muted);
      font-size: 1.06rem;
    }

    .section-heading {
      max-width: 780px;
      margin-bottom: 32px;
    }

    .info-card, .timeline-item, .award-card, .contact-panel {
      border: 1px solid var(--line);
      border-radius: 8px;
      background: rgba(255, 255, 255, .72);
    }

    .info-card {
      justify-content: space-between;
      gap: 20px;
      padding: 24px;
    }

    .info-card p, .award-card p, .role {
      margin-bottom: 0;
      color: var(--muted);
    }

    .info-meta {
      flex-wrap: wrap;
      justify-content: flex-end;
      gap: 10px;
    }

    .info-meta span {
      border-radius: 8px;
      background: var(--ink);
      color: #fff;
      font-size: .88rem;
      font-weight: 800;
      padding: 9px 11px;
    }

    .timeline {
      display: grid;
      gap: 16px;
    }

    .timeline-item {
      display: grid;
      grid-template-columns: 190px 1fr;
      gap: 24px;
      padding: 24px;
    }

    .timeline-date {
      color: var(--coral);
      font-weight: 800;
    }

    .timeline-body ul {
      margin: 18px 0 0;
      padding-left: 20px;
      color: var(--muted);
    }

    .timeline-body li + li { margin-top: 10px; }

    .award-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 16px;
    }

    .award-card {
      padding: 22px;
    }

    .award-card span {
      display: inline-block;
      margin-bottom: 18px;
      color: var(--coral);
    }

    .contact-panel {
      flex-wrap: wrap;
      gap: 12px;
      padding: 22px;
    }

    .contact-panel a {
      border-radius: 8px;
      background: var(--ink);
      color: #fff;
      font-weight: 800;
      padding: 12px 14px;
    }

    .contact-panel a:nth-child(2) { background: var(--blue); }
    .contact-panel a:nth-child(3) { background: var(--green); }
    .contact-panel a:nth-child(4) { background: var(--coral); }

    .site-footer {
      justify-content: space-between;
      gap: 16px;
      padding: 28px clamp(20px, 5vw, 72px);
      border-top: 1px solid var(--line);
      color: var(--muted);
      font-size: .95rem;
    }

    .site-footer a { font-weight: 800; }

    @media (max-width: 900px) {
      .site-header, .hero, .split, .contact, .timeline-item {
        grid-template-columns: 1fr;
      }

      .site-header { display: grid; }

      .site-nav {
        overflow-x: auto;
        padding-bottom: 2px;
      }

      .section { padding: 68px 0; }

      .hero {
        min-height: auto;
        padding-top: 44px;
      }

      .award-grid { grid-template-columns: repeat(2, 1fr); }

      .info-card {
        align-items: flex-start;
        flex-direction: column;
      }

      .info-meta { justify-content: flex-start; }
    }

    @media (max-width: 560px) {
      .section {
        width: min(100% - 28px, 1120px);
        padding: 54px 0;
      }

      .site-header { padding: 14px; }

      h1 { font-size: 2.55rem; }

      .award-grid { grid-template-columns: 1fr; }

      .contact-panel a, .button { width: 100%; }

      .site-footer {
        align-items: flex-start;
        flex-direction: column;
        padding: 24px 14px;
      }
    }
  </style>
</head>

<body>
  <header class="site-header">
    <a class="brand" href="#top">
      <span class="brand-mark">CB</span>
      <span>Cam Đức Bình</span>
    </a>

    <nav class="site-nav">
      <a href="#about">Giới thiệu</a>
      <a href="#experience">Hoạt động</a>
      <a href="#awards">Chứng chỉ</a>
      <a href="#contact">Liên hệ</a>
    </nav>
  </header>

  <main id="top">
    <section class="hero section">
      <div>
        <p class="eyebrow">Business Intelligence Analyst Intern</p>
        <h1>Biến dữ liệu thành góc nhìn rõ ràng cho quyết định kinh doanh.</h1>
        <p class="hero-text">
          Tôi là Cam Đức Bình, sinh viên Quản trị kinh doanh quốc tế tại Đại học Ngoại thương,
          định hướng phát triển trong phân tích dữ liệu, BI và trực quan hóa dữ liệu.
        </p>

        <div class="hero-actions">
          <a class="button primary" href="mailto:camducbinh@gmail.com">Email</a>
          <a class="button secondary" href="https://mavenanalytics.io/profile/b89173b0-a011-70e9-9763-84b49ddce8d8" target="_blank" rel="noreferrer">
            Portfolio Maven
          </a>
        </div>

        <dl class="quick-facts">
          <div><dt>GPA</dt><dd>3.62/4.0</dd></div>
          <div><dt>Định hướng</dt><dd>BI & Data Analytics</dd></div>
          <div><dt>Địa điểm</dt><dd>Gia Lâm, Hà Nội</dd></div>
        </dl>
      </div>

      <aside class="dashboard-card">
        <div class="dashboard-top">
          <div>
            <p class="panel-label">Focus Area</p>
            <strong>BI Readiness</strong>
          </div>
          <span class="status-dot">Active</span>
        </div>

        <div class="score-ring">
          <span>86%</span>
        </div>

        <div class="bar-list">
          <div class="bar-row"><span>SQL</span><i style="--value: 78%"></i></div>
          <div class="bar-row"><span>Python</span><i style="--value: 72%"></i></div>
          <div class="bar-row"><span>Excel</span><i style="--value: 84%"></i></div>
          <div class="bar-row"><span>Power BI</span><i style="--value: 80%"></i></div>
        </div>
      </aside>
    </section>

    <section class="section split" id="about">
      <div>
        <p class="eyebrow">Mục tiêu nghề nghiệp</p>
        <h2>Học chắc công cụ, rèn tư duy phân tích, tạo giá trị từ dữ liệu.</h2>
      </div>
      <div class="content-stack">
        <p>
          Ngắn hạn, tôi tập trung thành thạo SQL, Python, Excel và các nền tảng trực quan hóa dữ liệu
          như Power BI hoặc Tableau, đồng thời rèn luyện khả năng giải quyết vấn đề dựa trên dữ liệu.
        </p>
        <p>
          Dài hạn, tôi hướng tới vai trò chuyên gia phân tích dữ liệu có tư duy chiến lược,
          có khả năng dẫn dắt các dự án phân tích quan trọng và đóng góp vào giải pháp ra quyết định cho doanh nghiệp.
        </p>
      </div>
    </section>

    <section class="section">
      <div class="section-heading">
        <p class="eyebrow">Học vấn</p>
        <h2>Nền tảng kinh doanh quốc tế kết hợp phân tích dữ liệu.</h2>
      </div>

      <article class="info-card">
        <div>
          <h3>Trường Đại học Ngoại thương</h3>
          <p>Quản trị kinh doanh quốc tế</p>
        </div>
        <div class="info-meta">
          <span>2023 - 2027</span>
          <span>GPA 3.62/4.0</span>
        </div>
      </article>
    </section>

    <section class="section" id="experience">
      <div class="section-heading">
        <p class="eyebrow">Hoạt động</p>
        <h2>Kinh nghiệm làm việc với dữ liệu khách hàng và nhân sự.</h2>
      </div>

      <div class="timeline">
        <article class="timeline-item">
          <div class="timeline-date">11/2023 - 07/2024</div>
          <div class="timeline-body">
            <h3>AIESEC tại Việt Nam</h3>
            <p class="role">Thành viên ban Quan hệ và chăm sóc khách hàng</p>
            <ul>
              <li>Quản lý cơ sở dữ liệu khách hàng và stakeholders, đảm bảo thông tin đầy đủ, chính xác và được cập nhật thường xuyên.</li>
              <li>Đo lường trải nghiệm khách hàng, thu thập phản hồi và phân tích dữ liệu để cải thiện quy trình dịch vụ.</li>
              <li>Đánh giá hiệu quả triển khai dự án và mức độ hài lòng của khách hàng, từ đó đề xuất cải tiến cho đội ngũ vận hành.</li>
            </ul>
          </div>
        </article>

        <article class="timeline-item">
          <div class="timeline-date">08/2024 - 01/2025</div>
          <div class="timeline-body">
            <h3>AIESEC tại Việt Nam</h3>
            <p class="role">Thành viên ban Tuyển dụng và Phát triển nhân tài</p>
            <ul>
              <li>Phân tích xu hướng phát triển nhân sự để hỗ trợ kế hoạch đào tạo và giữ chân nhân tài.</li>
              <li>Đánh giá hiệu suất làm việc, hỗ trợ quyết định khen thưởng, điều chỉnh mục tiêu và phân bổ nguồn lực.</li>
              <li>Phân tích năng lực nhân sự mới, hỗ trợ tuyển dụng, đánh giá thử việc và xây dựng lộ trình phát triển phù hợp.</li>
            </ul>
          </div>
        </article>
      </div>
    </section>

    <section class="section" id="awards">
      <div class="section-heading">
        <p class="eyebrow">Danh hiệu & chứng chỉ</p>
        <h2>Đầu tư nghiêm túc vào nền tảng phân tích dữ liệu.</h2>
      </div>

      <div class="award-grid">
        <article class="award-card">
          <span>05/2025</span>
          <h3>Giải Nhì Summer Data Bootcamp 2025</h3>
          <p>Câu lạc bộ CTE FTU</p>
        </article>
        <article class="award-card">
          <span>05/2025</span>
          <h3>Google Advanced Data Analytics Certificate</h3>
          <p>Coursera</p>
        </article>
        <article class="award-card">
          <span>05/2025</span>
          <h3>Google Business Intelligence Certificate</h3>
          <p>Coursera</p>
        </article>
        <article class="award-card">
          <span>05/2025</span>
          <h3>Google Data Analytics Professional Certificate</h3>
          <p>Coursera</p>
        </article>
      </div>
    </section>

    <section class="section contact" id="contact">
      <div>
        <p class="eyebrow">Liên hệ</p>
        <h2>Cùng trao đổi về dữ liệu, BI và cơ hội thực tập.</h2>
      </div>

      <div class="contact-panel">
        <a href="mailto:camducbinh@gmail.com">camducbinh@gmail.com</a>
        <a href="tel:+84353935642">0353935642</a>
        <a href="https://www.linkedin.com/in/đức-bình-cam-912a1034b" target="_blank" rel="noreferrer">LinkedIn</a>
        <a href="https://mavenanalytics.io/profile/b89173b0-a011-70e9-9763-84b49ddce8d8" target="_blank" rel="noreferrer">Maven Analytics Portfolio</a>
      </div>
    </section>
  </main>

  <footer class="site-footer">
    <span>© <span id="year"></span> Cam Đức Bình</span>
    <a href="#top">Lên đầu trang</a>
  </footer>

  <script>
    document.getElementById("year").textContent = new Date().getFullYear();

    document.querySelectorAll('a[href^="#"]').forEach((link) => {
      link.addEventListener("click", (event) => {
        const target = document.querySelector(link.getAttribute("href"));
        if (!target) return;

        event.preventDefault();
        target.scrollIntoView({ behavior: "smooth", block: "start" });
      });
    });
  </script>
</body>
</html>
