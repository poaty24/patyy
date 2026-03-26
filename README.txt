/* ==========================================
   PROYECTO FINAL — ESTILOS GLOBALES
   Tema: Vibrante · Moderno · Colorido
   ========================================== */

@import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=Syne:wght@700;800&display=swap');

/* ==========================================
   VARIABLES CSS
   ========================================== */
:root {
  --c-purple:       #7c3aed;
  --c-purple-dark:  #5b21b6;
  --c-purple-light: #ede9fe;
  --c-pink:         #ec4899;
  --c-pink-light:   #fce7f3;
  --c-indigo:       #4f46e5;
  --c-cyan:         #06b6d4;
  --c-cyan-light:   #cffafe;
  --c-emerald:      #10b981;
  --c-emerald-light:#d1fae5;
  --c-amber:        #f59e0b;
  --c-amber-light:  #fef3c7;
  --c-rose:         #f43f5e;
  --c-rose-light:   #ffe4e6;

  --color-bg:           #f0eef8;
  --color-surface:      #ffffff;
  --color-border:       #e0d9f5;
  --color-text:         #1e1b4b;
  --color-text-muted:   #6b7280;

  --color-sidebar:      #1e1b4b;
  --color-sidebar-text: #e0e7ff;

  --color-accent:       #7c3aed;
  --color-success:      #10b981;
  --color-warning:      #f59e0b;
  --color-danger:       #f43f5e;

  --grad-sidebar:  linear-gradient(175deg, #1e1b4b 0%, #2d1f6e 55%, #180f3d 100%);
  --grad-hero:     linear-gradient(135deg, #7c3aed 0%, #4f46e5 50%, #06b6d4 100%);
  --grad-card-1:   linear-gradient(135deg, #7c3aed, #ec4899);
  --grad-card-2:   linear-gradient(135deg, #4f46e5, #06b6d4);
  --grad-card-3:   linear-gradient(135deg, #10b981, #06b6d4);
  --grad-card-4:   linear-gradient(135deg, #f59e0b, #f43f5e);
  --grad-thead:    linear-gradient(90deg, #4f46e5 0%, #7c3aed 100%);

  --sidebar-width: 270px;
  --font-display:  'Syne', sans-serif;
  --font-body:     'Plus Jakarta Sans', sans-serif;

  --radius-sm: 8px;
  --radius:    12px;
  --radius-lg: 18px;

  --shadow-sm:    0 1px 3px rgba(124,58,237,0.08), 0 1px 2px rgba(0,0,0,0.04);
  --shadow-md:    0 8px 24px rgba(124,58,237,0.15), 0 2px 8px rgba(0,0,0,0.06);
  --shadow-lg:    0 20px 48px rgba(124,58,237,0.2), 0 8px 16px rgba(0,0,0,0.08);
  --shadow-color: 0 8px 24px rgba(124,58,237,0.35);

  --transition: 0.22s cubic-bezier(0.4,0,0.2,1);
}

/* ==========================================
   RESET & BASE
   ========================================== */
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-body);
  background: var(--color-bg);
  color: var(--color-text);
  font-size: 15px;
  line-height: 1.6;
  min-height: 100vh;
  display: flex;
  background-image:
    radial-gradient(circle at 15% 15%, rgba(124,58,237,0.07) 0%, transparent 45%),
    radial-gradient(circle at 85% 85%, rgba(6,182,212,0.06) 0%, transparent 45%);
  background-attachment: fixed;
}

a { color: inherit; text-decoration: none; }
img { display: block; max-width: 100%; height: auto; }

code {
  font-family: 'Courier New', monospace;
  font-size: 0.8em;
  background: var(--c-purple-light);
  color: var(--c-purple-dark);
  padding: 0.15em 0.45em;
  border-radius: 4px;
  font-weight: 600;
}

/* ==========================================
   SIDEBAR
   ========================================== */
.sidebar {
  width: var(--sidebar-width);
  min-height: 100vh;
  background: var(--grad-sidebar);
  color: var(--color-sidebar-text);
  position: fixed;
  top: 0; left: 0;
  z-index: 100;
  display: flex;
  flex-direction: column;
  transition: transform var(--transition);
  overflow-y: auto;
  overflow-x: hidden;
  border-right: 1px solid rgba(255,255,255,0.04);
}

.sidebar::before {
  content: '';
  position: absolute;
  top: -100px; right: -100px;
  width: 240px; height: 240px;
  background: radial-gradient(circle, rgba(124,58,237,0.25) 0%, transparent 70%);
  pointer-events: none;
}

.sidebar::after {
  content: '';
  position: absolute;
  bottom: 40px; left: -60px;
  width: 180px; height: 180px;
  background: radial-gradient(circle, rgba(6,182,212,0.12) 0%, transparent 70%);
  pointer-events: none;
}

.sidebar-brand {
  padding: 1.75rem 1.5rem 1.25rem;
  border-bottom: 1px solid rgba(255,255,255,0.07);
  position: relative;
  z-index: 1;
}

.brand-logo {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.brand-icon {
  width: 40px; height: 40px;
  border-radius: 11px;
  background: var(--grad-card-1);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.15rem;
  box-shadow: 0 4px 14px rgba(124,58,237,0.55);
  flex-shrink: 0;
}

.brand-name {
  font-family: var(--font-display);
  font-size: 1.3rem;
  font-weight: 800;
  color: #fff;
  letter-spacing: -0.01em;
  line-height: 1.1;
}

.brand-tagline {
  font-size: 0.62rem;
  font-weight: 600;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: rgba(196,181,253,0.65);
  margin-top: 0.2rem;
}

.sidebar-user {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  padding: 1.1rem 1.5rem;
  border-bottom: 1px solid rgba(255,255,255,0.06);
  position: relative;
  z-index: 1;
}

.user-avatar {
  width: 36px; height: 36px;
  border-radius: 50%;
  background: var(--grad-card-2);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.85rem;
  font-weight: 700;
  color: white;
  flex-shrink: 0;
  border: 2px solid rgba(255,255,255,0.2);
  box-shadow: 0 3px 8px rgba(0,0,0,0.2);
}

.user-name {
  font-size: 0.8rem;
  font-weight: 700;
  color: #fff;
}

.user-role {
  font-size: 0.62rem;
  color: rgba(196,181,253,0.55);
  text-transform: uppercase;
  letter-spacing: 0.1em;
}

.sidebar-nav {
  flex: 1;
  padding: 1rem 0.75rem;
  position: relative;
  z-index: 1;
}

.nav-section-label {
  font-size: 0.58rem;
  font-weight: 700;
  letter-spacing: 0.22em;
  text-transform: uppercase;
  color: rgba(196,181,253,0.38);
  padding: 0 0.75rem;
  margin-bottom: 0.3rem;
  margin-top: 1.25rem;
}
.nav-section-label:first-child { margin-top: 0; }

.nav-link {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  padding: 0.6rem 0.75rem;
  font-size: 0.84rem;
  font-weight: 500;
  color: rgba(224,231,255,0.6);
  transition: all var(--transition);
  border-radius: var(--radius-sm);
  margin-bottom: 2px;
  position: relative;
}

.nav-link:hover {
  color: #fff;
  background: rgba(255,255,255,0.07);
}

.nav-link.active {
  color: #fff;
  background: linear-gradient(90deg, rgba(124,58,237,0.4), rgba(79,70,229,0.2));
  box-shadow: inset 0 0 0 1px rgba(196,181,253,0.18);
}

.nav-link.active::before {
  content: '';
  position: absolute;
  left: -0.75rem;
  top: 50%;
  transform: translateY(-50%);
  width: 3px;
  height: 58%;
  background: var(--grad-card-1);
  border-radius: 0 3px 3px 0;
}

.nav-icon {
  font-size: 1rem;
  width: 22px;
  text-align: center;
  flex-shrink: 0;
}

.nav-badge {
  margin-left: auto;
  background: var(--grad-card-1);
  color: #fff;
  font-size: 0.6rem;
  font-weight: 700;
  padding: 0.15rem 0.5rem;
  border-radius: 20px;
  box-shadow: 0 2px 8px rgba(236,72,153,0.4);
}

.sidebar-footer {
  padding: 1rem 1.5rem;
  border-top: 1px solid rgba(255,255,255,0.06);
  font-size: 0.68rem;
  color: rgba(196,181,253,0.28);
  position: relative;
  z-index: 1;
}

/* ==========================================
   HAMBURGER MOBILE
   ========================================== */
.menu-toggle {
  display: none;
  position: fixed;
  top: 1rem; left: 1rem;
  z-index: 200;
  background: var(--c-purple);
  border: none;
  color: white;
  width: 44px; height: 44px;
  border-radius: var(--radius-sm);
  cursor: pointer;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 5px;
  box-shadow: var(--shadow-color);
  transition: background var(--transition);
}
.menu-toggle:hover { background: var(--c-purple-dark); }
.menu-toggle span {
  display: block;
  width: 20px; height: 2px;
  background: white;
  border-radius: 2px;
  transition: all var(--transition);
}

.sidebar-overlay {
  display: none;
  position: fixed;
  inset: 0;
  background: rgba(30,27,75,0.6);
  z-index: 90;
  backdrop-filter: blur(4px);
}

/* ==========================================
   CONTENIDO PRINCIPAL
   ========================================== */
.main-content {
  margin-left: var(--sidebar-width);
  flex: 1;
  min-width: 0;
  padding: 2rem 2.5rem;
}

/* ==========================================
   ENCABEZADO
   ========================================== */
.page-header {
  margin-bottom: 2rem;
  padding-bottom: 1.5rem;
  border-bottom: 2px solid var(--color-border);
  position: relative;
}
.page-header::after {
  content: '';
  position: absolute;
  bottom: -2px; left: 0;
  width: 70px; height: 2px;
  background: var(--grad-card-1);
  border-radius: 2px;
}

.page-breadcrumb {
  font-size: 0.7rem;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--color-text-muted);
  margin-bottom: 0.5rem;
}
.page-breadcrumb span { color: var(--c-purple); }

.page-title {
  font-family: var(--font-display);
  font-size: clamp(1.7rem, 4vw, 2.6rem);
  font-weight: 800;
  letter-spacing: -0.03em;
  line-height: 1.15;
  background: var(--grad-hero);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.page-subtitle {
  margin-top: 0.4rem;
  font-size: 0.9rem;
  color: var(--color-text-muted);
}

/* ==========================================
   TARJETAS ESTADÍSTICAS
   ========================================== */
.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(190px, 1fr));
  gap: 1rem;
  margin-bottom: 2rem;
}

.stat-card {
  background: var(--color-surface);
  border: 1px solid var(--color-border);
  border-radius: var(--radius-lg);
  padding: 1.5rem;
  transition: box-shadow var(--transition), transform var(--transition);
  position: relative;
  overflow: hidden;
  box-shadow: var(--shadow-sm);
}

.stat-card::before {
  content: '';
  position: absolute;
  top: 0; right: 0;
  width: 90px; height: 90px;
  border-radius: 0 var(--radius-lg) 0 90px;
  opacity: 0.12;
}
.stat-card:nth-child(1)::before { background: var(--grad-card-1); }
.stat-card:nth-child(2)::before { background: var(--grad-card-2); }
.stat-card:nth-child(3)::before { background: var(--grad-card-3); }
.stat-card:nth-child(4)::before { background: var(--grad-card-4); }

.stat-card:hover {
  box-shadow: var(--shadow-md);
  transform: translateY(-4px);
}

.stat-icon {
  font-size: 1.3rem;
  margin-bottom: 0.85rem;
  display: inline-flex;
  width: 46px; height: 46px;
  border-radius: 12px;
  align-items: center;
  justify-content: center;
}
.stat-card:nth-child(1) .stat-icon { background: var(--c-purple-light); }
.stat-card:nth-child(2) .stat-icon { background: var(--c-cyan-light); }
.stat-card:nth-child(3) .stat-icon { background: var(--c-emerald-light); }
.stat-card:nth-child(4) .stat-icon { background: var(--c-rose-light); }

.stat-label {
  font-size: 0.68rem;
  letter-spacing: 0.13em;
  text-transform: uppercase;
  color: var(--color-text-muted);
  font-weight: 600;
  margin-bottom: 0.35rem;
}

.stat-value {
  font-family: var(--font-display);
  font-size: 2.1rem;
  font-weight: 800;
  color: var(--color-text);
  letter-spacing: -0.04em;
  line-height: 1;
}

.stat-change {
  font-size: 0.7rem;
  margin-top: 0.45rem;
  font-weight: 700;
  display: inline-flex;
  align-items: center;
  gap: 0.25rem;
  padding: 0.18rem 0.55rem;
  border-radius: 20px;
}
.stat-change.up   { color: #065f46; background: var(--c-emerald-light); }
.stat-change.down { color: #9f1239; background: var(--c-rose-light); }

/* ==========================================
   SECCIÓN TITLE
   ========================================== */
.section-title {
  font-family: var(--font-display);
  font-size: 1.15rem;
  font-weight: 800;
  color: var(--color-text);
  letter-spacing: -0.02em;
  margin-bottom: 1rem;
  display: flex;
  align-items: center;
  gap: 0.6rem;
}
.section-title .title-dot {
  width: 8px; height: 8px;
  border-radius: 50%;
  background: var(--grad-card-1);
  flex-shrink: 0;
}
.section-title::after {
  content: '';
  flex: 1;
  height: 1px;
  background: linear-gradient(90deg, var(--color-border), transparent);
}

/* ==========================================
   GALERÍA
   ========================================== */
.images-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
  margin-bottom: 2.5rem;
}

.image-card {
  background: var(--color-surface);
  border: 1px solid var(--color-border);
  border-radius: var(--radius-lg);
  overflow: hidden;
  transition: box-shadow var(--transition), transform var(--transition);
  box-shadow: var(--shadow-sm);
}
.image-card:hover {
  box-shadow: var(--shadow-lg);
  transform: translateY(-5px);
}

.img-wrapper { position: relative; overflow: hidden; }

.image-card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  transition: transform 0.5s ease;
}
.image-card:hover img { transform: scale(1.07); }

.img-wrapper::after {
  content: '';
  position: absolute;
  inset: 0;
  opacity: 0;
  transition: opacity 0.3s ease;
}
.image-card:nth-child(1) .img-wrapper::after { background: var(--grad-card-1); }
.image-card:nth-child(2) .img-wrapper::after { background: var(--grad-card-2); }
.image-card:nth-child(3) .img-wrapper::after { background: var(--grad-card-3); }
.image-card:hover .img-wrapper::after { opacity: 0.2; }

.image-card-body {
  padding: 1rem 1.25rem 1.25rem;
  border-top: 3px solid transparent;
}
.image-card:nth-child(1) .image-card-body {
  background: linear-gradient(white,white) padding-box, var(--grad-card-1) border-box;
}
.image-card:nth-child(2) .image-card-body {
  background: linear-gradient(white,white) padding-box, var(--grad-card-2) border-box;
}
.image-card:nth-child(3) .image-card-body {
  background: linear-gradient(white,white) padding-box, var(--grad-card-3) border-box;
}

.image-card-title { font-weight: 700; font-size: 0.9rem; color: var(--color-text); margin-bottom: 0.2rem; }
.image-card-meta  { font-size: 0.75rem; color: var(--color-text-muted); }

/* ==========================================
   TABLA
   ========================================== */
.table-section {
  background: var(--color-surface);
  border: 1px solid var(--color-border);
  border-radius: var(--radius-lg);
  overflow: hidden;
  box-shadow: var(--shadow-sm);
}

.table-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1.25rem 1.5rem;
  border-bottom: 1px solid var(--color-border);
  background: linear-gradient(135deg, #fdfcff 0%, #f5f3ff 100%);
  flex-wrap: wrap;
  gap: 0.75rem;
}

.table-title {
  font-family: var(--font-display);
  font-size: 1rem;
  font-weight: 800;
  color: var(--color-text);
}

.table-actions { display: flex; gap: 0.5rem; }

.btn {
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
  padding: 0.5rem 1.1rem;
  border-radius: var(--radius-sm);
  font-size: 0.8rem;
  font-weight: 700;
  cursor: pointer;
  border: none;
  transition: all var(--transition);
  font-family: var(--font-body);
  letter-spacing: 0.01em;
}

.btn-primary {
  background: var(--grad-card-1);
  color: white;
  box-shadow: 0 4px 14px rgba(124,58,237,0.38);
}
.btn-primary:hover {
  box-shadow: 0 6px 20px rgba(124,58,237,0.55);
  transform: translateY(-1px);
}

.btn-outline {
  background: transparent;
  color: var(--c-purple);
  border: 1.5px solid var(--c-purple);
}
.btn-outline:hover { background: var(--c-purple-light); }

.table-wrapper { overflow-x: auto; }

table {
  width: 100%;
  border-collapse: collapse;
  font-size: 0.86rem;
}

thead th {
  background: var(--grad-thead);
  color: #fff;
  font-size: 0.67rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  padding: 0.9rem 1.25rem;
  text-align: left;
  white-space: nowrap;
}
thead th:first-child { padding-left: 1.5rem; }
thead th:last-child  { padding-right: 1.5rem; }

tbody tr {
  border-bottom: 1px solid #f0ebff;
  transition: background var(--transition);
}
tbody tr:nth-child(even) { background: #faf8ff; }
tbody tr:hover           { background: var(--c-purple-light); }
tbody tr:last-child      { border-bottom: none; }

tbody td {
  padding: 0.9rem 1.25rem;
  vertical-align: middle;
  color: var(--color-text);
}
tbody td:first-child { padding-left: 1.5rem; }
tbody td:last-child  { padding-right: 1.5rem; }

/* ==========================================
   BADGES
   ========================================== */
.badge {
  display: inline-flex;
  align-items: center;
  gap: 0.3rem;
  padding: 0.25rem 0.7rem;
  border-radius: 20px;
  font-size: 0.67rem;
  font-weight: 700;
  letter-spacing: 0.05em;
  text-transform: uppercase;
}
.badge::before {
  content: '';
  width: 5px; height: 5px;
  border-radius: 50%;
  background: currentColor;
  flex-shrink: 0;
}
.badge-success { background: var(--c-emerald-light); color: #065f46; }
.badge-warning { background: var(--c-amber-light);   color: #92400e; }
.badge-danger  { background: var(--c-rose-light);    color: #9f1239; }
.badge-info    { background: var(--c-cyan-light);    color: #164e63; }
.badge-neutral { background: #f1f5f9;                color: #475569; }

/* ==========================================
   TABLE FOOTER
   ========================================== */
.table-footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem 1.5rem;
  border-top: 1px solid #f0ebff;
  font-size: 0.8rem;
  color: var(--color-text-muted);
  background: linear-gradient(135deg, #fdfcff, #f8f5ff);
  flex-wrap: wrap;
  gap: 0.5rem;
}

.pagination { display: flex; gap: 0.3rem; }

.page-btn {
  width: 32px; height: 32px;
  border-radius: var(--radius-sm);
  border: 1.5px solid var(--color-border);
  background: white;
  font-size: 0.8rem;
  font-weight: 700;
  cursor: pointer;
  transition: all var(--transition);
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: var(--font-body);
  color: var(--color-text-muted);
}
.page-btn:hover, .page-btn.active {
  background: var(--grad-card-1);
  color: white;
  border-color: transparent;
  box-shadow: 0 4px 12px rgba(124,58,237,0.4);
}

/* ==========================================
   PRODUCTOS
   ========================================== */
.productos-table table { min-width: 720px; }

.precio {
  font-family: var(--font-display);
  font-weight: 800;
  font-size: 0.95rem;
  color: var(--c-purple);
}

.stock-bar { display: flex; align-items: center; gap: 0.5rem; }

.stock-bar-track {
  flex: 1;
  height: 6px;
  background: #ede9fe;
  border-radius: 3px;
  overflow: hidden;
  min-width: 60px;
}

.stock-bar-fill { height: 100%; border-radius: 3px; transition: width 0.4s ease; }
.stock-bar-fill.high { background: linear-gradient(90deg, #10b981, #06b6d4); }
.stock-bar-fill.mid  { background: linear-gradient(90deg, #f59e0b, #f97316); }
.stock-bar-fill.low  { background: linear-gradient(90deg, #f43f5e, #ec4899); }

.stock-num {
  font-size: 0.78rem;
  font-weight: 700;
  color: var(--color-text-muted);
  min-width: 26px;
  text-align: right;
}

.category-tag {
  font-size: 0.67rem;
  font-weight: 700;
  padding: 0.22rem 0.65rem;
  border-radius: 20px;
  white-space: nowrap;
  letter-spacing: 0.04em;
  text-transform: uppercase;
}
.category-tag[data-cat="Computación"] { background: var(--c-purple-light); color: var(--c-purple-dark); }
.category-tag[data-cat="Audio"]       { background: var(--c-cyan-light);   color: #164e63; }
.category-tag[data-cat="Periféricos"] { background: var(--c-pink-light);   color: #9d174d; }
.category-tag[data-cat="Mobiliario"]  { background: var(--c-emerald-light);color: #065f46; }

/* ==========================================
   PAGE FOOTER
   ========================================== */
.page-footer {
  margin-top: 3rem;
  padding: 1.5rem 0;
  border-top: 1px solid var(--color-border);
  font-size: 0.78rem;
  color: var(--color-text-muted);
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 0.5rem;
}
.page-footer a { color: var(--c-purple); font-weight: 700; }
.page-footer a:hover { color: var(--c-pink); }

/* ==========================================
   RESPONSIVE
   ========================================== */
@media (max-width: 1024px) {
  .images-grid { grid-template-columns: repeat(2,1fr); }
  .stats-grid  { grid-template-columns: repeat(2,1fr); }
}

@media (max-width: 768px) {
  .menu-toggle { display: flex; }
  .sidebar { transform: translateX(-100%); }
  .sidebar.open { transform: translateX(0); box-shadow: var(--shadow-lg); }
  .sidebar-overlay.open { display: block; }

  .main-content {
    margin-left: 0;
    padding: 1.5rem 1rem;
    padding-top: 4.5rem;
  }

  .images-grid { grid-template-columns: 1fr; }
  .stats-grid  { grid-template-columns: repeat(2,1fr); }
  .page-title  { font-size: 1.8rem; }

  .table-header { flex-direction: column; align-items: flex-start; }
  .page-footer  { flex-direction: column; text-align: center; }
}

@media (max-width: 480px) {
  .stats-grid { grid-template-columns: 1fr; }
  .main-content { padding: 1rem 0.75rem; padding-top: 4.5rem; }
  .table-actions { width: 100%; }
  .btn { flex: 1; justify-content: center; }
}
