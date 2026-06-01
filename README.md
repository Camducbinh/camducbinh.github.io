<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nguyễn Văn A — Portfolio</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet" />
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --text-primary: #1a1a1a;
      --text-secondary: #6b6b6b;
      --text-muted: #a0a0a0;
      --bg: #fafaf8;
      --surface: #ffffff;
      --border: #e8e6e0;
      --accent: #2563eb;
      --accent-light: #eff4ff;
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'DM Sans', sans-serif;
      background: var(--bg);
      color: var(--text-primary);
      font-size: 16px;
      line-height: 1.7;
    }

    /* NAV */
    nav {
      position: fixed;
      top: 0; left: 0; right: 0;
      z-index: 100;
      background: rgba(250, 250, 248, 0.92);
      backdrop-filter: blur(8px);
      border-bottom: 1px solid var(--border);
      padding: 0 2rem;
      height: 60px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .nav-logo {
      font-family: 'DM Serif Display', serif;
      font-size: 1.2rem;
      color: var(--text-primary);
      text-decoration: none;
    }
    .nav-links { display: flex; gap: 2rem; list-style: none; }
    .nav-links a {
      font-size: 0.875rem;
      font-weight: 400;
      color: var(--text-secondary);
      text-decoration: none;
      letter-spacing: 0.02em;
      transition: color 0.2s;
    }
    .nav-links a:hover { color: var(--text-primary); }

    /* SECTIONS */
    section { padding: 6rem 2rem; max-width: 760px; margin: 0 auto; }
    section:first-of-type { padding-top: calc(60px + 5rem); }

    .section-label {
      font-size: 0.75rem;
      font-weight: 500;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--text-muted);
      margin-bottom: 2.5rem;
    }

    /* HERO */
    #hero { padding-top: calc(60px + 7rem); padding-bottom: 7rem; }
    .hero-tag {
      display: inline-block;
      background: var(--accent-light);
      color: var(--accent);
      font-size: 0.8rem;
      font-weight: 500;
      padding: 4px 12px;
      border-radius: 20px;
      margin-bottom: 1.5rem;
      letter-spacing: 0.03em;
    }
    .hero-name {
      font-family: 'DM Serif Display', serif;
      font-size: clamp(2.8rem, 6vw, 4.5rem);
      line-height: 1.1;
      letter-spacing: -0.02em;
      color: var(--text-primary);
      margin-bottom: 1.5rem;
    }
    .hero-name em {
      font-style: italic;
      color: var(--accent);
    }
    .hero-desc {
      font-size: 1.1rem;
      color: var(--text-secondary);
      max-width: 520px;
      line-height: 1.8;
      margin-bottom: 2.5rem;
      font-weight: 300;
    }
    .hero-cta {
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
      align-items: center;
    }
    .btn-primary {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: var(--text-primary);
      color: #fff;
      padding: 10px 22px;
      border-radius: 6px;
      font-size: 0.9rem;
      font-weight: 500;
      text-decoration: none;
      transition: opacity 0.2s;
    }
    .btn-primary:hover { opacity: 0.8; }
    .btn-secondary {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      color: var(--text-secondary);
      font-size: 0.9rem;
      text-decoration: none;
      border-bottom: 1px solid var(--border);
      padding-bottom: 1px;
      transition: color 0.2s, border-color 0.2s;
    }
    .btn-secondary:hover { color: var(--text-primary); border-color: var(--text-primary); }

    /* DIVIDER */
    .divider { border: none; border-top: 1px solid var(--border); max-width: 760px; margin: 0 auto; }

    /* ABOUT */
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 3rem;
      align-items: start;
    }
    .about-text p { color: var(--text-secondary); margin-bottom: 1rem; font-weight: 300; font-size: 1rem; }
    .about-text p:last-child { margin-bottom: 0; }
    .about-info { display: flex; flex-direction: column; gap: 1.2rem; }
    .info-row { display: flex; gap: 1rem; }
    .info-label {
      font-size: 0.8rem;
      font-weight: 500;
      color: var(--text-muted);
      letter-spacing: 0.05em;
      min-width: 80px;
      padding-top: 1px;
    }
    .info-value { font-size: 0.925rem; color: var(--text-secondary); }

    /* SKILLS */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      gap: 1rem;
    }
    .skill-card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 1.25rem 1.5rem;
    }
    .skill-card-title {
      font-size: 0.8rem;
      font-weight: 500;
      color: var(--text-muted);
      letter-spacing: 0.08em;
      text-transform: uppercase;
      margin-bottom: 0.75rem;
    }
    .skill-tags { display: flex; flex-wrap: wrap; gap: 6px; }
    .tag {
      font-size: 0.8rem;
      color: var(--text-secondary);
      background: var(--bg);
      border: 1px solid var(--border);
      padding: 3px 10px;
      border-radius: 20px;
    }

    /* PROJECTS */
    .projects-list { display: flex; flex-direction: column; gap: 1.5rem; }
    .project-card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 1.75rem 2rem;
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 2rem;
      transition: border-color 0.2s, box-shadow 0.2s;
    }
    .project-card:hover {
      border-color: #c0c0c0;
      box-shadow: 0 2px 12px rgba(0,0,0,0.06);
    }
    .project-body { flex: 1; }
    .project-header {
      display: flex;
      align-items: center;
      gap: 10px;
      margin-bottom: 0.5rem;
    }
    .project-title { font-weight: 500; font-size: 1rem; }
    .project-badge {
      font-size: 0.72rem;
      font-weight: 500;
      padding: 2px 8px;
      border-radius: 20px;
      background: var(--accent-light);
      color: var(--accent);
    }
    .project-desc { font-size: 0.925rem; color: var(--text-secondary); margin-bottom: 1rem; font-weight: 300; }
    .project-tags { display: flex; flex-wrap: wrap; gap: 6px; }
    .project-link {
      display: inline-flex;
      align-items: center;
      gap: 5px;
      color: var(--text-muted);
      text-decoration: none;
      font-size: 0.85rem;
      white-space: nowrap;
      transition: color 0.2s;
      flex-shrink: 0;
      padding-top: 2px;
    }
    .project-link:hover { color: var(--accent); }
    .project-link svg { width: 14px; height: 14px; }

    /* CONTACT */
    .contact-inner {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 3rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 2rem;
      flex-wrap: wrap;
    }
    .contact-heading {
      font-family: 'DM Serif Display', serif;
      font-size: 2rem;
      line-height: 1.2;
      margin-bottom: 0.5rem;
    }
    .contact-sub { color: var(--text-secondary); font-weight: 300; }
    .contact-links { display: flex; flex-direction: column; gap: 0.75rem; align-items: flex-end; }
    .contact-link {
      display: flex;
      align-items: center;
      gap: 8px;
      color: var(--text-secondary);
      text-decoration: none;
      font-size: 0.9rem;
      transition: color 0.2s;
    }
    .contact-link:hover { color: var(--text-primary); }
    .contact-link svg { width: 16px; height: 16px; flex-shrink: 0; }

    /* FOOTER */
    footer {
      text-align: center;
      padding: 2.5rem;
      font-size: 0.8rem;
      color: var(--text-muted);
      border-top: 1px solid var(--border);
    }

    /* ANIMATIONS */
    .fade-up {
      opacity: 0;
      transform: translateY(20px);
      transition: opacity 0.6s ease, transform 0.6s ease;
    }
    .fade-up.visible { opacity: 1; transform: translateY(0); }

    /* RESPONSIVE */
    @media (max-width: 640px) {
      nav { padding: 0 1.25rem; }
      .nav-links { gap: 1.25rem; }
      section { padding: 4rem 1.25rem; }
      #hero { padding-top: calc(60px + 4rem); }
      .about-grid { grid-template-columns: 1fr; }
      .contact-inner { padding: 2rem; flex-direction: column; }
      .contact-links { align-items: flex-start; }
      .project-card { flex-direction: column; gap: 1rem; }
      .divider { margin: 0 1.25rem; }
    }
  </style>
</head>
<body>

  <!-- NAV -->
  <nav>
    <a href="#hero" class="nav-logo">Văn A.</a>
    <ul class="nav-links">
      <li><a href="#about">Giới thiệu</a></li>
      <li><a href="#skills">Kỹ năng</a></li>
      <li><a href="#projects">Dự án</a></li>
      <li><a href="#contact">Liên hệ</a></li>
    </ul>
  </nav>

  <!-- HERO -->
  <section id="hero">
    <div class="hero-tag">Sẵn sàng hợp tác &amp; học hỏi</div>
    <h1 class="hero-name">Nguyễn<br /><em>Văn A.</em></h1>
    <p class="hero-desc">
      Sinh viên đam mê công nghệ và dữ liệu. Tôi thích xây dựng những thứ có ích, học hỏi không ngừng và giải quyết vấn đề bằng tư duy rõ ràng.
    </p>
    <div class="hero-cta">
      <a href="#projects" class="btn-primary">
        Xem dự án
        <svg viewBox="0 0 16 16" fill="none" width="14" height="14"><path d="M3 8h10M9 4l4 4-4 4" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
      </a>
      <a href="#contact" class="btn-secondary">Liên hệ với tôi</a>
    </div>
  </section>

  <hr class="divider" />

  <!-- ABOUT -->
  <section id="about" class="fade-up">
    <p class="section-label">Về tôi</p>
    <div class="about-grid">
      <div class="about-text">
        <p>
          Tôi là sinh viên năm [X] ngành [Tên ngành] tại [Tên trường]. Tôi quan tâm đến lĩnh vực khoa học dữ liệu, lập trình web, và các ứng dụng thực tế của Machine Learning.
        </p>
        <p>
          Ngoài việc học, tôi thích đọc sách, tham gia các cuộc thi lập trình và đóng góp vào các dự án cộng đồng. Tôi luôn tìm kiếm cơ hội để áp dụng kiến thức vào thực tiễn.
        </p>
      </div>
      <div class="about-info">
        <div class="info-row">
          <span class="info-label">Trường</span>
          <span class="info-value">[Tên trường của bạn]</span>
        </div>
        <div class="info-row">
          <span class="info-label">Ngành</span>
          <span class="info-value">[Tên ngành của bạn]</span>
        </div>
        <div class="info-row">
          <span class="info-label">Năm</span>
          <span class="info-value">Năm [X] (2021–2025)</span>
        </div>
        <div class="info-row">
          <span class="info-label">Vị trí</span>
          <span class="info-value">Hà Nội, Việt Nam</span>
        </div>
        <div class="info-row">
          <span class="info-label">Ngôn ngữ</span>
          <span class="info-value">Tiếng Việt, English</span>
        </div>
      </div>
    </div>
  </section>

  <hr class="divider" />

  <!-- SKILLS -->
  <section id="skills" class="fade-up">
    <p class="section-label">Kỹ năng</p>
    <div class="skills-grid">
      <div class="skill-card">
        <p class="skill-card-title">Lập trình</p>
        <div class="skill-tags">
          <span class="tag">Python</span>
          <span class="tag">JavaScript</span>
          <span class="tag">SQL</span>
          <span class="tag">Java</span>
        </div>
      </div>
      <div class="skill-card">
        <p class="skill-card-title">Data & ML</p>
        <div class="skill-tags">
          <span class="tag">Pandas</span>
          <span class="tag">NumPy</span>
          <span class="tag">Scikit-learn</span>
          <span class="tag">Matplotlib</span>
        </div>
      </div>
      <div class="skill-card">
        <p class="skill-card-title">Web</p>
        <div class="skill-tags">
          <span class="tag">HTML/CSS</span>
          <span class="tag">React</span>
          <span class="tag">ASP.NET</span>
          <span class="tag">Git</span>
        </div>
      </div>
      <div class="skill-card">
        <p class="skill-card-title">Công cụ</p>
        <div class="skill-tags">
          <span class="tag">VS Code</span>
          <span class="tag">Jupyter</span>
          <span class="tag">GitHub</span>
          <span class="tag">Figma</span>
        </div>
      </div>
    </div>
  </section>

  <hr class="divider" />

  <!-- PROJECTS -->
  <section id="projects" class="fade-up">
    <p class="section-label">Dự án nổi bật</p>
    <div class="projects-list">

      <div class="project-card">
        <div class="project-body">
          <div class="project-header">
            <span class="project-title">Dự án 1: Phân tích dữ liệu nhà ở</span>
            <span class="project-badge">ML</span>
          </div>
          <p class="project-desc">
            Dùng California Housing Dataset để xây dựng mô hình hồi quy tuyến tính dự đoán giá nhà. Bao gồm tiền xử lý dữ liệu, chuẩn hóa và đánh giá mô hình.
          </p>
          <div class="project-tags">
            <span class="tag">Python</span>
            <span class="tag">Scikit-learn</span>
            <span class="tag">Pandas</span>
            <span class="tag">Jupyter</span>
          </div>
        </div>
        <a href="https://github.com/username/repo" target="_blank" class="project-link" rel="noopener">
          GitHub
          <svg viewBox="0 0 16 16" fill="none"><path d="M3 8h10M9 4l4 4-4 4" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
        </a>
      </div>

      <div class="project-card">
        <div class="project-body">
          <div class="project-header">
            <span class="project-title">Dự án 2: Ứng dụng web quản lý</span>
            <span class="project-badge">Web</span>
          </div>
          <p class="project-desc">
            Ứng dụng quản lý sinh viên xây dựng bằng ASP.NET Core. Hỗ trợ thêm, sửa, xóa dữ liệu và xác thực người dùng.
          </p>
          <div class="project-tags">
            <span class="tag">ASP.NET</span>
            <span class="tag">C#</span>
            <span class="tag">SQL Server</span>
          </div>
        </div>
        <a href="https://github.com/username/repo" target="_blank" class="project-link" rel="noopener">
          GitHub
          <svg viewBox="0 0 16 16" fill="none"><path d="M3 8h10M9 4l4 4-4 4" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
        </a>
      </div>

      <div class="project-card">
        <div class="project-body">
          <div class="project-header">
            <span class="project-title">Dự án 3: Phân tích thống kê</span>
            <span class="project-badge">Thống kê</span>
          </div>
          <p class="project-desc">
            Phân tích phân phối chuẩn, tính toán z-score và xác định ngưỡng điểm cho hệ thống xếp loại 5 bậc. Trực quan hóa kết quả bằng Matplotlib.
          </p>
          <div class="project-tags">
            <span class="tag">Python</span>
            <span class="tag">SciPy</span>
            <span class="tag">Matplotlib</span>
          </div>
        </div>
        <a href="https://github.com/username/repo" target="_blank" class="project-link" rel="noopener">
          GitHub
          <svg viewBox="0 0 16 16" fill="none"><path d="M3 8h10M9 4l4 4-4 4" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
        </a>
      </div>

    </div>
  </section>

  <hr class="divider" />

  <!-- CONTACT -->
  <section id="contact" class="fade-up">
    <p class="section-label">Liên hệ</p>
    <div class="contact-inner">
      <div>
        <h2 class="contact-heading">Hãy kết nối<br />cùng tôi.</h2>
        <p class="contact-sub">Mở lòng với mọi cơ hội hợp tác và học hỏi.</p>
      </div>
      <div class="contact-links">
        <a href="mailto:your@email.com" class="contact-link">
          <svg viewBox="0 0 16 16" fill="none"><rect x="2" y="4" width="12" height="9" rx="1.5" stroke="currentColor" stroke-width="1.4"/><path d="M2 5.5l6 4 6-4" stroke="currentColor" stroke-width="1.4" stroke-linecap="round"/></svg>
          your@email.com
        </a>
        <a href="https://github.com/username" target="_blank" class="contact-link" rel="noopener">
          <svg viewBox="0 0 16 16" fill="none"><path d="M8 1.5a6.5 6.5 0 0 0-2.056 12.67c.325.06.444-.14.444-.313v-1.098c-1.806.393-2.187-.872-2.187-.872-.295-.75-.72-.95-.72-.95-.589-.402.044-.394.044-.394.65.046 1.002.668 1.002.668.576.987 1.515.7 1.884.536.059-.416.225-.7.41-.86-1.442-.164-2.957-.721-2.957-3.21 0-.71.254-1.29.668-1.745-.067-.163-.29-.824.064-1.718 0 0 .544-.174 1.781.664A6.2 6.2 0 0 1 8 5.42a6.2 6.2 0 0 1 1.624.219c1.237-.838 1.78-.664 1.78-.664.354.894.13 1.555.064 1.718.415.455.668 1.035.668 1.745 0 2.496-1.518 3.044-2.963 3.205.233.2.44.598.44 1.205v1.786c0 .174.118.376.447.312A6.502 6.502 0 0 0 8 1.5Z" fill="currentColor"/></svg>
          github.com/username
        </a>
        <a href="https://linkedin.com/in/username" target="_blank" class="contact-link" rel="noopener">
          <svg viewBox="0 0 16 16" fill="none"><rect x="1.5" y="1.5" width="13" height="13" rx="2" stroke="currentColor" stroke-width="1.4"/><path d="M5 6.5v4.5M5 4.5v.01M8 11V8.5c0-1 .5-2 2-2s2 1 2 2V11" stroke="currentColor" stroke-width="1.4" stroke-linecap="round" stroke-linejoin="round"/></svg>
          linkedin.com/in/username
        </a>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <p>© 2025 Nguyễn Văn A. Thiết kế bằng ❤️ và HTML thuần.</p>
  </footer>

  <script>
    const observer = new IntersectionObserver(
      (entries) => entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); }),
      { threshold: 0.12 }
    );
    document.querySelectorAll('.fade-up').forEach(el => observer.observe(el));
  </script>

</body>
</html>
