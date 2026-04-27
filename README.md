<title>Preston Yesquen | Cybersecurity Engineer</title>

<style>
:root{
  --bg:#05070f;
  --panel:#0f172a;
  --accent:#4B9CD3;
  --accent-soft:#6fb3e6;
  --highlight:#22d3ee;
  --text:#e6edf7;
  --muted:#94a3b8;
}

/* Reset */
*{margin:0;padding:0;box-sizing:border-box}

/* Base */
body{
  font-family: "Inter", system-ui, sans-serif;
  background: radial-gradient(circle at top, #0a0f1f, #02040a 70%);
  color:var(--text);
  line-height:1.6;
}

/* Headings = confident, not gamer */
h1,h2,h3{
  font-weight:600;
  letter-spacing:.5px;
}

/* NAV — cleaner + more “I know what I’m doing” */
nav{
  position:fixed;
  top:0;
  width:100%;
  background:rgba(5,7,15,0.75);
  backdrop-filter:blur(10px);
  border-bottom:1px solid rgba(255,255,255,0.06);
  z-index:1000;
}

nav ul{
  display:flex;
  justify-content:center;
  padding:14px;
  list-style:none;
}

nav li{margin:0 18px}

nav a{
  color:var(--muted);
  text-decoration:none;
  font-weight:500;
  transition:.25s;
}

nav a:hover{
  color:var(--text);
}

/* Layout */
.dashboard{
  padding-top:90px;
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(320px,1fr));
  gap:24px;
  max-width:1100px;
  margin:auto;
  padding:110px 20px 60px;
}

/* Panels — less glow, more authority */
.panel{
  background:linear-gradient(145deg,#0b1225,#0f172a);
  border:1px solid rgba(255,255,255,0.05);
  border-radius:12px;
  padding:22px;
  transition:.25s ease;
}

.panel:hover{
  transform:translateY(-4px);
  border-color:rgba(75,156,211,0.5);
}

/* Remove cheesy scan line */
.panel::after{display:none}

/* Titles */
.title{
  margin-bottom:12px;
  color:var(--accent-soft);
  font-size:.9rem;
  text-transform:uppercase;
  letter-spacing:1px;
}

/* Stats */
.stat{
  font-size:2.2rem;
  font-weight:600;
  color:var(--text);
}

/* Bars */
.bar{
  height:6px;
  background:#0a0f1f;
  border-radius:999px;
  margin-top:10px;
  overflow:hidden;
}

.fill{
  height:100%;
  background:linear-gradient(90deg,var(--accent),var(--highlight));
}

/* Images */
img.panel-img{
  width:100%;
  border-radius:10px;
  margin-bottom:12px;
  border:1px solid rgba(255,255,255,0.06);
}

/* Terminal — toned down */
.terminal{
  background:#02040a;
  padding:14px;
  border-radius:8px;
  font-family:monospace;
  color:#9ae6b4;
  height:180px;
  overflow:auto;
  font-size:.85rem;
}

/* Footer */
footer{
  text-align:center;
  padding:25px;
  border-top:1px solid rgba(255,255,255,0.05);
  color:var(--muted);
  font-size:.9rem;
}
</style>
