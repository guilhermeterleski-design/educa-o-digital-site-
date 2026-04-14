# educa-o-digital-site-
educação digital
:root {
  /* Fundo principal do site:
     bege claro inspirado em papel, palha e tons naturais do agro */
  --bg: #f8f3e7;

  /* Fundo suave auxiliar:
     usado como variação mais clara do fundo principal */
  --bg-soft: #fffaf0;

  /* Superfícies translúcidas:
     cards com aparência leve, quente e levemente acetinada */
  --surface: rgba(255, 251, 244, 0.82);

  /* Superfície sólida:
     usada em blocos que precisam parecer mais “limpos” e firmes */
  --surface-strong: #fffdf8;

  /* Cor principal do texto:
     marrom escuro quente, mais orgânico que preto puro */
  --text: #2d241c;

  /* Texto secundário:
     marrom acinzentado para descrições e textos de apoio */
  --muted: #685a4d;

  /* Linhas e bordas suaves:
     tom terroso transparente para divisões discretas */
  --line: rgba(120, 90, 40, 0.18);

  /* Cor principal da identidade visual:
     verde agrícola, remetendo ao campo, cultivo e sustentabilidade */
  --primary: #335f45;

  /* Versão mais forte do verde principal:
     usada para contrastes, títulos e destaques mais sérios */
  --primary-strong: #244533;

  /* Cor de destaque:
     dourado/ocre inspirado em cevada, malte e elementos naturais secos */
  --accent: #b27a2f;

  /* Versão suave do destaque:
     usada em detalhes delicados e fundos decorativos quentes */
  --accent-soft: #e8c78c;

  /* Sombra padrão:
     sombra quente e sutil, evitando o aspecto frio do cinza puro */
  --shadow: 0 10px 30px rgba(59, 39, 17, 0.10);

  /* Raios de borda:
     ajudam a manter o visual moderno, amigável e orgânico */
  --radius-lg: 24px;
  --radius-md: 18px;
  --radius-sm: 12px;

  /* Largura máxima do conteúdo:
     limita o layout para melhor leitura em telas grandes */
  --container: 1180px;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  font-size: 100%;
  scroll-behavior: smooth;
}

body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  font-size: 1rem;
  color: var(--text);
  background:
    radial-gradient(circle at top left, rgba(232, 199, 140, 0.22), transparent 28%),
    radial-gradient(circle at top right, rgba(85, 132, 92, 0.16), transparent 28%),
    linear-gradient(180deg, #fbf7ef 0%, #f7f0e1 100%);
  transition: background-color 0.3s, color 0.3s;
}

img {
  max-width: 100%;
  display: block;
}

a {
  color: inherit;
}

.header {
  position: sticky;
  top: 0;
  z-index: 1000;
  backdrop-filter: blur(14px);
  background: rgba(40, 63, 47, 0.88);
  border-bottom: 1px solid rgba(255, 255, 255, 0.08);
}

.header-inner,
.footer-inner,
.hero-section,
.content-section {
  width: min(calc(100% - 32px), var(--container));
  margin: 0 auto;
}

.header-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
  min-height: 84px;
}

.logo img {
  width: 132px;
  height: auto;
  object-fit: contain;
  transition: transform 0.25s ease;
}

.logo:hover img {
  transform: scale(1.04);
}

.site-title {
  flex: 1;
  text-align: center;
  color: #fff;
  font-size: 1.06rem;
  font-weight: 700;
  letter-spacing: 0.01em;
}

.navbar {
  position: relative;
}

.nav-desktop {
  display: flex;
  align-items: center;
  gap: 10px;
}

.hamburger {
  display: none;
  background: transparent;
  font-size: 1.7rem;
  color: #fff;
  border: none;
  cursor: pointer;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 8px;
}

.nav-links-primary {
  gap: 6px;
}

.nav-links-mobile {
  display: none;
}

.nav-links a {
  text-decoration: none;
  color: rgba(255, 255, 255, 0.92);
  font-weight: 700;
  font-size: 0.96rem;
  padding: 10px 14px;
  border-radius: 999px;
  transition: background 0.25s ease, color 0.25s ease, transform 0.25s ease;
}

.nav-links a:hover,
.nav-links a:focus-visible {
  background: rgba(255, 255, 255, 0.12);
  color: #fff4cf;
  transform: translateY(-1px);
}

.nav-more {
  position: relative;
}

.nav-more-only {
  margin-left: auto;
}

.nav-more-btn {
  min-height: 44px;
  padding: 10px 16px;
  border-radius: 999px;
  border: 1px solid rgba(255, 255, 255, 0.16);
  background: rgba(255, 255, 255, 0.08);
  color: rgba(255, 255, 255, 0.96);
  font-weight: 700;
  font-size: 0.96rem;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  gap: 10px;
  transition: background 0.25s ease, transform 0.25s ease, border-color 0.25s ease, box-shadow 0.25s ease, color 0.25s ease;
}

.nav-more-arrow {
  font-size: 0.95rem;
  line-height: 1;
  transform: translateY(1px);
  transition: transform 0.25s ease;
}

.nav-more.open .nav-more-arrow {
  transform: rotate(180deg) translateY(-1px);
}

.nav-more-btn:hover,
.nav-more-btn:focus-visible {
  background: rgba(243, 183, 74, 0.18);
  border-color: rgba(243, 183, 74, 0.42);
  color: #fff8ea;
  box-shadow: 0 10px 24px rgba(243, 183, 74, 0.14);
  transform: translateY(-1px);
}

.nav-more-panel {
  position: absolute;
  right: 0;
  top: calc(100% + 10px);
  width: 220px;
  padding: 10px;
  border-radius: 18px;
  background: rgba(255, 251, 243, 0.96);
  border: 1px solid rgba(140, 109, 63, 0.16);
  box-shadow: 0 16px 30px rgba(62, 48, 31, 0.14);
  backdrop-filter: blur(10px);
  display: none;
  flex-direction: column;
  gap: 4px;
}

.nav-more.open .nav-more-panel {
  display: flex;
}

.nav-more-panel a {
  text-decoration: none;
  color: var(--text);
  font-weight: 600;
  padding: 10px 12px;
  border-radius: 12px;
}

.nav-more-panel a:hover,
.nav-more-panel a:focus-visible {
  background: rgba(243, 183, 74, 0.16);
  color: var(--primary-strong);
}

main {
  padding: 34px 0 72px;
}

/* HERO */
.hero-section {
  display: grid;
  gap: 20px;
  padding-top: 10px;
}

.hero-shell {
  display: grid;
  grid-template-columns: minmax(0, 1.02fr) minmax(360px, 0.98fr);
  gap: 24px;
  align-items: stretch;
}

.hero-copy,
.surface-block,
.info-card,
.mini-card {
  border: 1px solid var(--line);
  background: var(--surface);
  box-shadow: var(--shadow);
  backdrop-filter: blur(8px);
}

.hero-copy {
  padding: 24px;
  border-radius: 28px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  min-height: 100%;
  height: 100%;
}

.eyebrow,
.section-tag,
.mini-label {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  width: fit-content;
  font-size: 0.82rem;
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--primary);
  background: rgba(51, 95, 69, 0.10);
  border: 1px solid rgba(51, 95, 69, 0.16);
  padding: 8px 12px;
  border-radius: 999px;
}

.hero-copy h1 {
  margin: 14px 0 14px;
  font-size: clamp(1.6rem, 2.2vw, 2.4rem);
  line-height: 1.05;
  letter-spacing: -0.035em;
  max-width: 36ch;
  text-align: center;
}

.hero-lead {
  font-size: 1.12rem;
  color: var(--muted);
  max-width: 100%;
  text-align: justify;
}

.hero-copy p + p {
  margin-top: 10px;
  text-align: justify;
}

.hero-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 14px;
  margin-top: 18px;
}

.action-btn,
.secondary-btn,
.card-toggle,
.accessibility-menu button,
.carousel-btn,
.dot {
  transition: transform 0.22s ease, background-color 0.22s ease, border-color 0.22s ease, opacity 0.22s ease;
}

.action-btn,
.secondary-btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  min-height: 48px;
  padding: 12px 20px;
  border-radius: 14px;
  font-weight: 700;
  text-decoration: none;
  border: 1px solid transparent;
  cursor: pointer;
}

.action-btn {
  background: linear-gradient(135deg, var(--accent) 0%, #c88e3d 100%);
  color: #fff;
}

.secondary-btn {
  background: rgba(255, 255, 255, 0.56);
  color: var(--primary-strong);
  border-color: rgba(51, 95, 69, 0.18);
}

.action-btn:hover,
.secondary-btn:hover,
.card-toggle:hover,
.accessibility-menu button:hover,
.carousel-btn:hover,
.dot:hover {
  transform: translateY(-2px);
}

.hero-points {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 10px;
  margin-top: 18px;
}

.hero-point {
  padding: 12px 12px 14px;
  border: 1px solid rgba(120, 90, 40, 0.14);
  border-radius: 18px;
  background: linear-gradient(180deg, rgba(255,255,255,0.78), rgba(248,242,231,0.96));
}

.hero-point strong {
  display: block;
  margin-bottom: 6px;
  color: var(--primary-strong);
  font-size: 1rem;
}

.hero-point span {
  color: var(--muted);
  font-size: 0.92rem;
  line-height: 1.5;
}

.hero-shell > .hero-copy,
.hero-shell > .hero-visual {
  height: 100%;
}

.hero-visual {
  min-height: 100%;
  padding: 0;
  display: flex;
  align-self: stretch;
}

.hero-image-card {
  position: relative;
  overflow: hidden;
  border-radius: 28px;
  width: 100%;
  height: 100%;
  min-height: 480px;
  box-shadow: var(--shadow);
}

.hero-image-card::after {
  content: "";
  position: absolute;
  inset: 0;
  background: linear-gradient(180deg, rgba(21, 17, 13, 0.02) 0%, rgba(21, 17, 13, 0.14) 52%, rgba(21, 17, 13, 0.78) 100%);
}

.hero-image-card img {
  width: 100%;
  height: 100%;
  min-height: 480px;
  object-fit: cover;
}

.hero-image-overlay {
  position: absolute;
  left: 18px;
  right: 18px;
  bottom: 18px;
  z-index: 1;
  padding: 18px 20px;
  border-radius: 20px;
  color: #fff;
  background: rgba(24, 20, 15, 0.30);
  border: 1px solid rgba(255, 255, 255, 0.14);
  backdrop-filter: blur(8px);
}

.hero-image-overlay span {
  display: inline-block;
  margin-bottom: 8px;
  font-size: 0.82rem;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  color: rgba(255, 255, 255, 0.84);
}

.hero-image-overlay strong {
  display: block;
  font-size: 1.08rem;
  line-height: 1.35;
  max-width: 28ch;
}

.content-section {
  padding-top: 84px;
}

.section-heading {
  max-width: 760px;
  margin-bottom: 18px;
}

.section-heading h2 {
  margin: 14px 0 8px;
  font-size: clamp(1.7rem, 3vw, 2.7rem);
  line-height: 1.1;
}

.section-heading p {
  color: var(--muted);
}

.surface-block {
  border-radius: var(--radius-lg);
  padding: 22px;
}

.gallery-block,
.video-shell,
.hq-shell,
.contact-card,
.info-box,
.quiz-form,
.quiz-result {
  background: var(--surface-strong);
}

.carousel-wrapper {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
}

.carousel-slide {
  width: 100%;
  overflow: hidden;
  border-radius: 22px;
  background: #efe4d0;
}

.carousel-slide img {
  width: 100%;
  aspect-ratio: 16 / 9;
  object-fit: cover;
}

.carousel-btn {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  width: 48px;
  height: 48px;
  border: none;
  border-radius: 50%;
  background: rgba(36, 69, 51, 0.9);
  color: #fff;
  font-size: 1.35rem;
  cursor: pointer;
  z-index: 1;
}

.carousel-btn.left {
  left: 14px;
}

.carousel-btn.right {
  right: 14px;
}

.carousel-caption {
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  gap: 20px;
  margin-top: 18px;
  padding: 20px;
  border: 1px solid var(--line);
  border-radius: 20px;
  background: linear-gradient(180deg, #fffdf9 0%, #faf4e8 100%);
}

.carousel-caption h3 {
  color: var(--primary);
  margin-bottom: 6px;
  font-size: 1.3rem;
}

.carousel-caption p {
  color: var(--muted);
  max-width: 740px;
}

.carousel-dots {
  display: flex;
  gap: 8px;
  flex-shrink: 0;
}

.dot {
  width: 12px;
  height: 12px;
  border-radius: 999px;
  border: none;
  background: #d9c7a5;
  cursor: pointer;
}

.dot.active {
  width: 28px;
  background: var(--accent);
}

.info-box p,
.contact-card p {
  font-size: 1.02rem;
}

.quiz-question + .quiz-question {
  margin-top: 22px;
}

.quiz-question p {
  margin-bottom: 10px;
  font-weight: 700;
}

.quiz-question label {
  display: flex;
  align-items: flex-start;
  gap: 10px;
  padding: 12px 14px;
  margin-top: 10px;
  border: 1px solid var(--line);
  border-radius: 14px;
  background: #fffaf3;
  cursor: pointer;
}

.quiz-question input {
  margin-top: 3px;
}

.quiz-question-last {
  margin-bottom: 10px;
}

.quiz-submit-btn {
  margin-top: 14px;
}

.quiz-result {
  display: none;
  margin-top: 16px;
  font-weight: 700;
  color: var(--primary-strong);
}

.quiz-result.show {
  display: block;
}

.process-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 18px;
}

.process-card {
  position: relative;
  min-height: 100%;
  display: flex;
  flex-direction: column;
  gap: 14px;
  background: linear-gradient(180deg, rgba(255,255,255,0.94), rgba(255,250,243,0.98));
}

.process-card::after {
  content: "";
  position: absolute;
  inset: 0;
  border-radius: inherit;
  pointer-events: none;
  background: linear-gradient(135deg, rgba(214,161,86,0.12), transparent 45%);
}

.process-number {
  width: 52px;
  height: 52px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border-radius: 16px;
  font-weight: 800;
  letter-spacing: 0.04em;
  color: #fff;
  background: linear-gradient(135deg, var(--accent), #b67b28);
  box-shadow: 0 12px 26px rgba(182, 123, 40, 0.22);
}

.process-card h3 {
  font-size: 1.18rem;
  color: var(--primary-strong);
}

.process-card p {
  color: var(--muted);
}

.cards-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 18px;
  align-items: stretch;
}

.info-card {
  align-self: stretch;
  height: 100%;
  background: transparent;
  border: none;
  box-shadow: none;
  backdrop-filter: none;
  display: flex;
  flex-direction: column;
  overflow: visible;
  border-radius: 22px;
}

.card-toggle {
  width: 100%;
  min-height: 88px;
  border: none;
  background: linear-gradient(135deg, var(--primary) 0%, #447257 100%);
  color: #fff;
  padding: 18px 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  text-align: left;
  font-size: 1rem;
  font-weight: 700;
  cursor: pointer;
  border-radius: 22px;
}

.expandable-card.open .card-toggle {
  border-radius: 22px 22px 0 0;
}

.card-icon {
  font-size: 1.45rem;
  line-height: 1;
}

.card-content {
  display: none;
  padding: 18px 20px 22px;
  background: var(--surface-strong);
  min-height: 148px;
  flex: 1;
  border: 1px solid var(--line);
  border-top: none;
  border-radius: 0 0 22px 22px;
  box-shadow: var(--shadow);
}

.expandable-card.open .card-content {
  display: block;
}

.video-container video {
  width: 100%;
  border-radius: 18px;
}

.hq-frame-container {
  border-radius: 18px;
  overflow: hidden;
  background: #f7ecd7;
  border: 1px solid var(--line);
}

.hq-frame-container iframe {
  width: 100%;
  height: 820px;
  border: none;
  display: block;
  background: #f7ecd7;
}

.contact-card-professional {
  display: grid;
  gap: 22px;
  padding: 28px;
  background: linear-gradient(180deg, #fffdf9 0%, #f8f1e4 100%);
}

.contact-card-header {
  display: grid;
  gap: 10px;
}

.contact-card-professional h3 {
  font-size: clamp(1.45rem, 2.5vw, 2rem);
  line-height: 1.1;
  color: var(--primary-strong);
}

.contact-role {
  margin: 0;
  max-width: 56ch;
  color: var(--muted);
  font-size: 1.02rem;
}

.contact-info-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 16px;
}

.contact-info-item {
  display: grid;
  gap: 6px;
  padding: 18px;
  border-radius: 18px;
  border: 1px solid var(--line);
  background: rgba(255, 255, 255, 0.78);
}

.contact-label {
  font-size: 0.8rem;
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--primary);
}

.contact-info-item strong,
.contact-info-item a {
  font-size: 1rem;
  color: var(--text);
  text-decoration: none;
  word-break: break-word;
}

.contact-info-item a:hover,
.contact-info-item a:focus-visible {
  color: var(--accent);
}

footer {
  background: #213628;
  color: #fff;
  border-top: 1px solid rgba(255, 255, 255, 0.08);
}

.footer-inner {
  min-height: 92px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 18px;
}

.footer-inner p {
  color: rgba(255, 255, 255, 0.88);
}

.footer-inner-enhanced {
  align-items: center;
}

.footer-copy {
  margin: 0;
}

.footer-right-cluster {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  gap: 18px;
  flex-wrap: wrap;
}

.footer-logos {
  display: flex;
  align-items: center;
  gap: 18px;
  flex-wrap: wrap;
}

.footer-logo {
  display: block;
  object-fit: contain;
  filter: brightness(0) invert(1);
  opacity: 0.92;
}

.footer-logo-nre {
  height: 54px;
  width: auto;
}

.footer-logo-programacao {
  height: 42px;
  width: auto;
}

.social-links {
  display: flex;
  gap: 12px;
}

.social-links a {
  width: 42px;
  height: 42px;
  border-radius: 50%;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  background: rgba(255, 255, 255, 0.10);
  border: 1px solid rgba(255, 255, 255, 0.10);
}

.social-icon {
  width: 20px;
  height: 20px;
}

.accessibility-fixed {
  position: fixed;
  right: 18px;
  bottom: 18px;
  width: 54px;
  height: 54px;
  border-radius: 50%;
  border: none;
  background: linear-gradient(135deg, var(--primary) 0%, #4d7a5f 100%);
  color: #fff;
  cursor: pointer;
  z-index: 1001;
  font-size: 1rem;
  font-weight: 700;
  box-shadow: 0 10px 24px rgba(0, 0, 0, 0.20);
}

.accessibility-menu {
  position: fixed;
  right: 18px;
  bottom: 82px;
  display: flex;
  flex-direction: column;
  gap: 10px;
  min-width: 190px;
  background: rgba(255, 253, 249, 0.96);
  border: 1px solid var(--line);
  border-radius: 18px;
  padding: 12px;
  box-shadow: var(--shadow);
  z-index: 1001;
}

.accessibility-menu.hidden {
  display: none;
}

.accessibility-menu button {
  padding: 10px 12px;
  border: 1px solid rgba(51, 95, 69, 0.12);
  background: #fff;
  color: var(--primary-strong);
  border-radius: 12px;
  cursor: pointer;
  font-weight: 700;
}

.high-contrast {
  background: #000 !important;
  color: #fff !important;
}

.high-contrast body,
.high-contrast main,
.high-contrast section,
.high-contrast p,
.high-contrast h1,
.high-contrast h2,
.high-contrast h3,
.high-contrast strong,
.high-contrast span,
.high-contrast li,
.high-contrast label,
.high-contrast button {
  color: #fff !important;
}

.high-contrast .header,
.high-contrast footer,
.high-contrast .nav-links,
.high-contrast .nav-more-panel,
.high-contrast .hero-copy,
.high-contrast .surface-block,
.high-contrast .info-card,
.high-contrast .hero-point,
.high-contrast .carousel-caption,
.high-contrast .card-content,
.high-contrast .quiz-question label,
.high-contrast .contact-info-item,
.high-contrast .accessibility-menu,
.high-contrast .hq-frame-container,
.high-contrast .hero-image-overlay {
  background: #111 !important;
  color: #fff !important;
  border-color: #fff !important;
  box-shadow: none !important;
}

.high-contrast .header,
.high-contrast footer {
  border-color: #fff !important;
}

.high-contrast .section-tag,
.high-contrast .eyebrow,
.high-contrast .contact-label {
  background: transparent !important;
  color: #ff0 !important;
  border-color: #ff0 !important;
}

.high-contrast .action-btn,
.high-contrast .secondary-btn,
.high-contrast .card-toggle,
.high-contrast .nav-more-btn,
.high-contrast .carousel-btn,
.high-contrast .accessibility-fixed,
.high-contrast .accessibility-menu button,
.high-contrast .social-links a {
  background: #111 !important;
  color: #fff !important;
  border: 1px solid #fff !important;
}

.high-contrast .nav-links a,
.high-contrast .nav-more-panel a,
.high-contrast .contact-info-item a,
.high-contrast a {
  color: #ff0 !important;
}

.high-contrast .nav-links a:hover,
.high-contrast .nav-links a:focus-visible,
.high-contrast .nav-more-panel a:hover,
.high-contrast .nav-more-panel a:focus-visible,
.high-contrast .contact-info-item a:hover,
.high-contrast .contact-info-item a:focus-visible,
.high-contrast .action-btn:hover,
.high-contrast .secondary-btn:hover,
.high-contrast .card-toggle:hover,
.high-contrast .nav-more-btn:hover,
.high-contrast .accessibility-menu button:hover,
.high-contrast .social-links a:hover {
  background: #222 !important;
  color: #ff0 !important;
  border-color: #ff0 !important;
}

.high-contrast .dot {
  background: #666 !important;
  border: 1px solid #fff !important;
}

.high-contrast .dot.active {
  background: #ff0 !important;
}

.high-contrast input {
  accent-color: #ff0;
}

.reveal {
  opacity: 0;
  transform: translateY(26px);
  transition: opacity 0.65s ease, transform 0.65s ease;
}

.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}

@media (max-width: 1080px) {
  .hero-shell {
    grid-template-columns: 1fr;
  }

  .hero-copy h1 {
    max-width: none;
  }

  .hero-visual {
    min-height: 420px;
  }

  .hero-image-card,
  .hero-image-card img {
    min-height: 420px;
  }
}

@media (max-width: 980px) {
  .hero-highlights {
    grid-template-columns: 1fr;
  }

  .highlight-card {
    min-height: auto;
  }
}

@media (max-width: 900px) {
  .process-grid {
    grid-template-columns: 1fr;
  }

  .cards-grid {
    grid-template-columns: 1fr;
  }

  .carousel-caption,
  .footer-inner {
    flex-direction: column;
    align-items: flex-start;
  }

  .footer-inner-enhanced {
    align-items: flex-start;
  }

  .footer-right-cluster {
    justify-content: flex-start;
    gap: 14px;
  }

  .footer-logos {
    gap: 14px;
  }

  .footer-logo-nre {
    height: 46px;
  }

  .footer-logo-programacao {
    height: 36px;
  }
}

@media (max-width: 768px) {
  .header-inner {
    min-height: 74px;
  }

  .site-title {
    text-align: left;
    font-size: 0.95rem;
  }

  .hamburger {
    display: block;
  }

  .nav-links {
    display: none;
    position: absolute;
    top: calc(100% + 10px);
    right: 0;
    flex-direction: column;
    min-width: 220px;
    padding: 10px;
    border-radius: 18px;
    background: rgba(33, 54, 40, 0.98);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.25);
  }

  .nav-links.show {
    display: flex;
  }

  main {
    padding-top: 18px;
  }

  .hero-copy,
  .surface-block {
    padding: 20px;
  }

  .hero-points {
    grid-template-columns: 1fr;
  }

  .hero-copy h1 {
    font-size: clamp(1.8rem, 7vw, 2.5rem);
    margin: 12px 0;
  }

  .hero-copy p + p {
    margin-top: 8px;
  }

  .hero-actions {
    margin-top: 16px;
  }

  .hero-points {
    margin-top: 16px;
  }

  .hero-visual {
    min-height: 320px;
  }

  .hero-image-card,
  .hero-image-card img {
    min-height: 320px;
  }

  .hero-image-overlay {
    left: 14px;
    right: 14px;
    bottom: 14px;
    padding: 16px;
  }

  .carousel-btn {
    width: 42px;
    height: 42px;
  }

  .hq-frame-container iframe {
    height: 620px;
  }

  .contact-card-professional {
    padding: 22px;
  }

  .contact-info-grid {
    grid-template-columns: 1fr;
  }

  .cards-grid {
    align-items: start;
  }

  .cards-grid .info-card {
    height: auto;
  }

  .cards-grid .card-content {
    min-height: auto;
    flex: initial;
  }

  .footer-inner-enhanced {
    align-items: flex-start;
  }

  .footer-copy {
    width: 100%;
  }

  .footer-right-cluster {
    width: 100%;
    justify-content: flex-start;
  }

  .footer-logos {
    justify-content: flex-start;
  }

  .accessibility-fixed {
    right: 14px;
    bottom: 14px;
  }

  .accessibility-menu {
    right: 14px;
    left: 14px;
    bottom: 78px;
    min-width: auto;
  }
}
const DEFAULT_FONT_SIZE = 16;
const MIN_FONT_SIZE = 14;
const MAX_FONT_SIZE = 20;
let currentFontSize = DEFAULT_FONT_SIZE;

const applyFontSize = () => {
  document.documentElement.style.fontSize = `${currentFontSize}px`;
};

const increaseFont = () => {
  currentFontSize = Math.min(MAX_FONT_SIZE, currentFontSize + 2);
  applyFontSize();
};

const decreaseFont = () => {
  currentFontSize = Math.max(MIN_FONT_SIZE, currentFontSize - 2);
  applyFontSize();
};

const toggleContrast = () => {
  document.body.classList.toggle('high-contrast');
};

const hamburger = document.querySelector('.hamburger');
const navLinks = document.querySelector('.nav-links');
const accessibilityBtn = document.getElementById('accessibility-btn');
const accessibilityMenu = document.getElementById('accessibility-menu');
const revealElements = document.querySelectorAll('.reveal');
const dots = document.querySelectorAll('.dot');
const navMore = document.querySelector('.nav-more');
const navMoreBtn = document.getElementById('nav-more-btn');

if (hamburger && navLinks) {
  hamburger.addEventListener('click', () => {
    const isOpen = navLinks.classList.toggle('show');
    hamburger.setAttribute('aria-expanded', String(isOpen));
  });

  navLinks.querySelectorAll('a').forEach((link) => {
    link.addEventListener('click', () => {
      navLinks.classList.remove('show');
      hamburger.setAttribute('aria-expanded', 'false');
    });
  });
}

if (navMore && navMoreBtn) {
  navMoreBtn.addEventListener('click', () => {
    const isOpen = navMore.classList.toggle('open');
    navMoreBtn.setAttribute('aria-expanded', String(isOpen));
  });

  navMore.querySelectorAll('a').forEach((link) => {
    link.addEventListener('click', () => {
      navMore.classList.remove('open');
      navMoreBtn.setAttribute('aria-expanded', 'false');
    });
  });

  document.addEventListener('click', (event) => {
    if (!navMore.contains(event.target)) {
      navMore.classList.remove('open');
      navMoreBtn.setAttribute('aria-expanded', 'false');
    }
  });
}

if (accessibilityBtn && accessibilityMenu) {
  accessibilityBtn.addEventListener('click', () => {
    const isHidden = accessibilityMenu.classList.toggle('hidden');
    accessibilityBtn.setAttribute('aria-expanded', String(!isHidden));
  });
}

function revealOnScroll() {
  const windowHeight = window.innerHeight;
  revealElements.forEach((el) => {
    const elementTop = el.getBoundingClientRect().top;
    if (elementTop < windowHeight - 60) {
      el.classList.add('visible');
    }
  });
}

window.addEventListener('scroll', revealOnScroll);
window.addEventListener('load', revealOnScroll);

const carouselItems = [
  {
    src: './img/campo.png',
    alt: 'Campo de cevada em Guarapuava',
    title: 'Campo de cevada',
    description: 'O início da jornada acontece no campo, onde o cultivo da cevada depende de planejamento, clima favorável e cuidado com os recursos naturais.'
  },
  {
    src: './img/malte.png',
    alt: 'Malte em processo de beneficiamento',
    title: 'Transformação em malte',
    description: 'Após a colheita, a cevada passa por etapas de beneficiamento e transformação, unindo produção agrícola, tecnologia e indústria.'
  },
  {
    src: './img/cidade.png',
    alt: 'Cidade conectada à cadeia produtiva do malte',
    title: 'Campo e cidade conectados',
    description: 'O produto final chega à cidade e mostra como o agro movimenta a economia, abastece o cotidiano e depende de um futuro sustentável.'
  }
];

let currentIndex = 0;
let autoSlide;

function updateDots() {
  dots.forEach((dot, index) => {
    dot.classList.toggle('active', index === currentIndex);
  });
}

function updateCarousel() {
  const item = carouselItems[currentIndex];
  const img = document.getElementById('carousel-image');
  const title = document.getElementById('carousel-title');
  const description = document.getElementById('carousel-description');

  if (!img || !title || !description) return;

  img.src = item.src;
  img.alt = item.alt;
  title.textContent = item.title;
  description.textContent = item.description;
  updateDots();
}

function changeSlide(direction) {
  currentIndex = (currentIndex + direction + carouselItems.length) % carouselItems.length;
  updateCarousel();
}

function goToSlide(index) {
  currentIndex = index;
  updateCarousel();
}

function startAutoSlide() {
  autoSlide = setInterval(() => {
    changeSlide(1);
  }, 5000);
}

function stopAutoSlide() {
  clearInterval(autoSlide);
}

dots.forEach((dot) => {
  dot.addEventListener('click', () => {
    goToSlide(Number(dot.dataset.index));
    stopAutoSlide();
    startAutoSlide();
  });
});

const facts = [
  'A cevada é um dos grãos cultivados há mais tempo pela humanidade e segue tendo grande importância econômica e alimentar.',
  'O malte não está presente apenas em bebidas: ele também pode ser utilizado em diferentes alimentos.',
  'A força do agro também depende do cuidado com o solo, a água e os demais recursos naturais.',
  'Produção e meio ambiente precisam caminhar juntos para garantir um futuro realmente sustentável.'
];

const factText = document.getElementById('fact-text');
const factBtn = document.getElementById('fact-btn');
let currentFactIndex = 0;

if (factBtn && factText) {
  factBtn.addEventListener('click', () => {
    let nextIndex;

    do {
      nextIndex = Math.floor(Math.random() * facts.length);
    } while (nextIndex === currentFactIndex && facts.length > 1);

    currentFactIndex = nextIndex;
    factText.textContent = facts[currentFactIndex];
  });
}

const quizForm = document.getElementById('quiz-form');
const quizResult = document.getElementById('quiz-result');

if (quizForm && quizResult) {
  quizForm.addEventListener('submit', (event) => {
    event.preventDefault();

    const answers = ['q1', 'q2', 'q3', 'q4', 'q5'];
    let score = 0;
    let allAnswered = true;

    answers.forEach((question) => {
      const selected = document.querySelector(`input[name="${question}"]:checked`);

      if (!selected) {
        allAnswered = false;
        return;
      }

      if (selected.value === 'certo') {
        score += 1;
      }
    });

    if (!allAnswered) {
      quizResult.textContent = 'Responda todas as perguntas para ver o resultado.';
      quizResult.classList.add('show');
      return;
    }

    const feedbacks = {
      5: 'Parabéns! Você acertou tudo e compreendeu muito bem a relação entre cevada, malte, campo, cidade e sustentabilidade.',
      4: 'Excelente! Você acertou 4 de 5 perguntas e demonstrou ótima compreensão do tema.',
      3: 'Muito bom! Você acertou 3 de 5 perguntas e já domina boa parte do conteúdo.',
      2: 'Você acertou 2 de 5 perguntas. Vale revisar o conteúdo e tentar novamente.',
      1: 'Você acertou 1 de 5 perguntas. Explore o site novamente e tente mais uma vez.',
      0: 'Você ainda não acertou nenhuma. Explore o site novamente e faça uma nova tentativa.'
    };

    quizResult.textContent = `Resultado: ${score}/5. ${feedbacks[score]}`;
    quizResult.classList.add('show');
  });
}

const cardToggles = document.querySelectorAll('.card-toggle');

cardToggles.forEach((toggle) => {
  toggle.addEventListener('click', () => {
    const card = toggle.closest('.expandable-card');
    const isOpen = card.classList.toggle('open');
    toggle.setAttribute('aria-expanded', String(isOpen));
    toggle.querySelector('.card-icon').textContent = isOpen ? '−' : '+';
  });
});

const carouselWrapper = document.querySelector('.carousel-wrapper');
if (carouselWrapper) {
  carouselWrapper.addEventListener('mouseenter', stopAutoSlide);
  carouselWrapper.addEventListener('mouseleave', startAutoSlide);
}

updateCarousel();
startAutoSlide();
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Do Campo ao Copo</title>
  <meta name="description" content="Projeto sobre a jornada da cevada ao malte, conectando agro, tecnologia, sustentabilidade e cidade." />
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header class="header" id="topo">
    <div class="header-inner">
      <a class="logo" href="#inicio" aria-label="Voltar ao início">
        <img src="./img/logo.png" alt="Logo Agrinho" />
      </a>

      <div class="site-title">Do Campo ao Copo: A Jornada do Malte em Guarapuava</div>

      <nav class="navbar" aria-label="Navegação principal">
        <div class="nav-desktop">
          <div class="nav-more nav-more-only">
            <button class="nav-more-btn" id="nav-more-btn" type="button" aria-expanded="false" aria-controls="nav-more-panel">
              <span>Explorar</span>
              <span class="nav-more-arrow" aria-hidden="true">▾</span>
            </button>
            <div class="nav-more-panel" id="nav-more-panel">
              <a href="#jornada">Jornada</a>
              <a href="#galeria">Galeria</a>
              <a href="#curiosidades">Curiosidades</a>
              <a href="#quiz">Quiz</a>
              <a href="#sustentabilidade">Sustentabilidade</a>
              <a href="#video">Vídeo</a>
              <a href="#hq">HQ</a>
              <a href="#contato">Contato</a>
            </div>
          </div>
        </div>

        <button class="hamburger" id="menu-toggle" aria-label="Abrir menu" aria-controls="nav-links" aria-expanded="false">
          ☰
        </button>

        <ul class="nav-links nav-links-mobile" id="nav-links">
          <li><a href="#jornada">Jornada</a></li>
          <li><a href="#galeria">Galeria</a></li>
          <li><a href="#curiosidades">Curiosidades</a></li>
          <li><a href="#quiz">Quiz</a></li>
          <li><a href="#sustentabilidade">Sustentabilidade</a></li>
          <li><a href="#video">Vídeo</a></li>
          <li><a href="#hq">HQ</a></li>
          <li><a href="#contato">Contato</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <button id="accessibility-btn" class="accessibility-fixed" aria-label="Menu de acessibilidade" aria-expanded="false">
    A+
  </button>

  <div id="accessibility-menu" class="accessibility-menu hidden" role="dialog" aria-label="Menu de acessibilidade">
    <button type="button" onclick="increaseFont()">Aumentar fonte</button>
    <button type="button" onclick="decreaseFont()">Diminuir fonte</button>
    <button type="button" onclick="toggleContrast()">Alto contraste</button>
  </div>

  <main>
    <section id="inicio" class="hero-section reveal">
      <div class="hero-shell">
        <div class="hero-copy">
          <span class="eyebrow">Do campo ao copo</span>
          <h1>Agro forte, futuro sustentável em cada etapa da jornada do malte</h1>
          <p class="hero-lead">
            Da <strong>cevada cultivada no campo</strong> ao <strong>malte que movimenta a indústria e chega à cidade</strong>,
            esta cadeia produtiva mostra como produção, tecnologia e cuidado ambiental podem caminhar juntos.
          </p>
          <p>
            Em Guarapuava, essa conexão revela que o desenvolvimento sustentável nasce do equilíbrio entre trabalho rural,
            inovação, transformação industrial e uso responsável dos recursos naturais.
          </p>

          <div class="hero-actions">
            <a class="action-btn" href="#jornada">Conhecer a jornada</a>
            <a class="secondary-btn" href="#sustentabilidade">Ver ações sustentáveis</a>
          </div>

          <div class="hero-points" aria-label="Pontos centrais do projeto">
            <div class="hero-point">
              <strong>Campo</strong>
              <span>Cultivo planejado e manejo responsável.</span>
            </div>
            <div class="hero-point">
              <strong>Tecnologia</strong>
              <span>Transformação do grão em valor e inovação.</span>
            </div>
            <div class="hero-point">
              <strong>Futuro</strong>
              <span>Produção com equilíbrio entre economia e meio ambiente.</span>
            </div>
          </div>
        </div>

        <div class="hero-visual">
          <div class="hero-image-card">
            <img src="./img/campo.png" alt="Campo de cevada em Guarapuava" />
            <div class="hero-image-overlay">
              <span>Uma mesma cadeia, muitos impactos</span>
              <strong>O campo produz, a indústria transforma e a cidade reconhece o valor dessa conexão.</strong>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="jornada" class="content-section reveal">
      <div class="section-heading">
        <span class="section-tag">Jornada produtiva</span>
        <h2>Da lavoura à transformação</h2>
        <p>A cadeia produtiva é apresentada em etapas visuais claras para mostrar como o campo, a indústria e a cidade se conectam ao longo do processo.</p>
      </div>

      <div class="process-grid">
        <article class="surface-block process-card">
          <div class="process-number">01</div>
          <h3>Cultivo no campo</h3>
          <p>A cevada começa sua jornada em lavouras planejadas, com atenção ao solo, ao clima e ao manejo responsável.</p>
        </article>

        <article class="surface-block process-card">
          <div class="process-number">02</div>
          <h3>Beneficiamento e malte</h3>
          <p>Após a colheita, o grão passa por processos técnicos que unem agro, indústria e tecnologia para gerar valor.</p>
        </article>

        <article class="surface-block process-card">
          <div class="process-number">03</div>
          <h3>Chegada à cidade</h3>
          <p>O malte conecta produção, economia e consumo, mostrando como o campo impacta diretamente a vida urbana.</p>
        </article>
      </div>
    </section>

    <section id="galeria" class="content-section reveal">
      <div class="section-heading">
        <span class="section-tag">Galeria</span>
        <h2>Do plantio ao produto final</h2>
        <p>Uma visão visual da cadeia produtiva que liga o campo, a indústria e o cotidiano urbano.</p>
      </div>

      <div class="surface-block gallery-block">
        <div class="carousel-wrapper">
          <button class="carousel-btn left" type="button" onclick="changeSlide(-1)" aria-label="Imagem anterior">&#10094;</button>

          <div class="carousel-slide">
            <img id="carousel-image" src="./img/campo.png" alt="Campo de cevada em Guarapuava" />
          </div>

          <button class="carousel-btn right" type="button" onclick="changeSlide(1)" aria-label="Próxima imagem">&#10095;</button>
        </div>

        <div class="carousel-caption">
          <div>
            <h3 id="carousel-title">Campo de cevada</h3>
            <p id="carousel-description">O início da jornada acontece no campo, onde o cultivo da cevada depende de planejamento, clima favorável e cuidado com os recursos naturais.</p>
          </div>
          <div class="carousel-dots" aria-label="Indicadores do carrossel">
            <button type="button" class="dot active" data-index="0" aria-label="Ir para imagem 1"></button>
            <button type="button" class="dot" data-index="1" aria-label="Ir para imagem 2"></button>
            <button type="button" class="dot" data-index="2" aria-label="Ir para imagem 3"></button>
          </div>
        </div>
      </div>
    </section>

    <section id="curiosidades" class="content-section reveal">
      <div class="section-heading">
        <span class="section-tag">Curiosidades</span>
        <h2>Você sabia?</h2>
        <p>Pequenos fatos que ajudam a entender a relevância da cevada, do malte e do agro sustentável.</p>
      </div>

      <div class="surface-block info-box">
        <p id="fact-text">A cevada é um dos grãos cultivados há mais tempo pela humanidade e segue tendo grande importância econômica e alimentar.</p>
        <button id="fact-btn" class="action-btn" type="button">Mostrar outra curiosidade</button>
      </div>
    </section>

    <section id="quiz" class="content-section reveal">
      <div class="section-heading">
        <span class="section-tag">Interatividade</span>
        <h2>Quiz: teste seus conhecimentos</h2>
        <p>Uma forma leve de revisar os principais conceitos apresentados no projeto.</p>
      </div>

      <form id="quiz-form" class="surface-block quiz-form">
        <div class="quiz-question">
          <p><strong>1.</strong> Qual grão é a base da cadeia produtiva apresentada no site?</p>
          <label><input type="radio" name="q1" value="errado" /> Milho</label>
          <label><input type="radio" name="q1" value="certo" /> Cevada</label>
          <label><input type="radio" name="q1" value="errado" /> Arroz</label>
        </div>

        <div class="quiz-question">
          <p><strong>2.</strong> Depois da colheita, a cevada passa por processos que resultam em:</p>
          <label><input type="radio" name="q2" value="errado" /> Algodão</label>
          <label><input type="radio" name="q2" value="certo" /> Malte</label>
          <label><input type="radio" name="q2" value="errado" /> Madeira</label>
        </div>

        <div class="quiz-question">
          <p><strong>3.</strong> A expressão “do campo ao copo” representa principalmente:</p>
          <label><input type="radio" name="q3" value="errado" /> Um passeio turístico pela cidade</label>
          <label><input type="radio" name="q3" value="certo" /> A ligação entre produção agrícola, indústria e consumo</label>
          <label><input type="radio" name="q3" value="errado" /> Apenas o transporte da colheita</label>
        </div>

        <div class="quiz-question">
          <p><strong>4.</strong> Qual prática ajuda a tornar essa cadeia produtiva mais sustentável?</p>
          <label><input type="radio" name="q4" value="certo" /> Uso consciente da água e cuidado com o solo</label>
          <label><input type="radio" name="q4" value="errado" /> Aumento do desperdício em todas as etapas</label>
          <label><input type="radio" name="q4" value="errado" /> Eliminação total da tecnologia no campo</label>
        </div>

        <div class="quiz-question quiz-question-last">
          <p><strong>5.</strong> O projeto mostra que campo e cidade estão conectados porque:</p>
          <label><input type="radio" name="q5" value="errado" /> São realidades sem relação entre si</label>
          <label><input type="radio" name="q5" value="certo" /> O que é produzido no campo movimenta a indústria e chega ao cotidiano urbano</label>
          <label><input type="radio" name="q5" value="errado" /> A cidade produz todo o malte sozinha</label>
        </div>

        <button type="submit" class="action-btn quiz-submit-btn">Ver resultado</button>
      </form>

      <div id="quiz-result" class="surface-block quiz-result" aria-live="polite"></div>
    </section>

    <section id="sustentabilidade" class="content-section reveal">
      <div class="section-heading">
        <span class="section-tag">Sustentabilidade</span>
        <h2>Agro forte, futuro sustentável</h2>
        <p>A produção da cevada e a transformação em malte mostram que desenvolvimento e responsabilidade ambiental precisam caminhar juntos.</p>
      </div>

      <div class="cards-grid">
        <article class="info-card expandable-card">
          <button class="card-toggle" type="button" aria-expanded="false">
            <span>Produção responsável</span>
            <span class="card-icon">+</span>
          </button>
          <div class="card-content">
            <p>Produzir com qualidade exige planejamento, tecnologia e boas práticas agrícolas desde o preparo do solo até a colheita.</p>
          </div>
        </article>

        <article class="info-card expandable-card">
          <button class="card-toggle" type="button" aria-expanded="false">
            <span>Equilíbrio ambiental</span>
            <span class="card-icon">+</span>
          </button>
          <div class="card-content">
            <p>O uso consciente da água, a preservação do solo e a redução de desperdícios ajudam a manter a produtividade sem comprometer o meio ambiente.</p>
          </div>
        </article>

        <article class="info-card expandable-card">
          <button class="card-toggle" type="button" aria-expanded="false">
            <span>Futuro sustentável</span>
            <span class="card-icon">+</span>
          </button>
          <div class="card-content">
            <p>Pensar no amanhã significa fortalecer o agro hoje com soluções que respeitem os recursos naturais e contribuam para as próximas gerações.</p>
          </div>
        </article>
      </div>
    </section>

    <section id="video" class="content-section reveal">
      <div class="section-heading">
        <span class="section-tag">Audiovisual</span>
        <h2>Vídeo: a cadeia produtiva do malte</h2>
        <p>Um complemento visual para aprofundar a compreensão do tema e enriquecer a apresentação do projeto.</p>
      </div>

      <div class="surface-block video-shell">
        <div class="video-container">
          <video controls>
            <source src="./img/cadeia produtiva.mp4" type="video/mp4" />
            Seu navegador não suporta vídeo.
          </video>
        </div>
      </div>
    </section>

    <section id="hq" class="content-section reveal">
      <div class="section-heading">
        <span class="section-tag">Narrativa</span>
        <h2>História em quadrinhos</h2>
        <p>Uma experiência complementar para apresentar o conteúdo de forma criativa e envolvente.</p>
      </div>

      <div class="surface-block hq-shell">
        <div class="hq-frame-container">
          <iframe src="./HQ/hq.html" title="História em Quadrinhos" loading="lazy" allowfullscreen></iframe>
        </div>
      </div>
    </section>

    <section id="contato" class="content-section reveal">
      <div class="section-heading">
        <span class="section-tag">Contato</span>
        <h2>Responsável pelo projeto</h2>
      </div>

      <div class="surface-block contact-card contact-card-professional">
        <div class="contact-card-header">
          <h3>Willian Schön Lopes</h3>
        </div>

        <div class="contact-info-grid">
          <div class="contact-info-item">
            <span class="contact-label">Função</span>
            <strong>Embaixador da Programação Paraná</strong>
          </div>
          <div class="contact-info-item">
            <span class="contact-label">E-mail</span>
            <a href="mailto:lopes.willian@escola.pr.gov.br">lopes.willian@escola.pr.gov.br</a>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="footer-inner footer-inner-enhanced">
      <p class="footer-copy">&copy; 2026 - NRE Guarapuava | Programação Paraná</p>

      <div class="footer-right-cluster">
        <div class="footer-logos" aria-label="Logos institucionais">
          <img src="./img/NRE Guarapuava_vert_branco.png" alt="Logo do NRE Guarapuava" class="footer-logo footer-logo-nre" />
          <img src="./img/ProgramacaoParana_logo-vertical-mono-branca.png" alt="Logo da Programação Paraná" class="footer-logo footer-logo-programacao" />
        </div>

        <div class="social-links">
          <a href="https://github.com/schonlopes" target="_blank" rel="noreferrer">
            <img src="./img/github.png" alt="GitHub" class="social-icon" />
          </a>
          <a href="https://www.instagram.com/schonlopes" target="_blank" rel="noreferrer">
            <img src="./img/instagram.png" alt="Instagram" class="social-icon" />
          </a>
        </div>
      </div>
    </div>
  </footer>

  <script src="script.js"></script>
</body>
</html>
