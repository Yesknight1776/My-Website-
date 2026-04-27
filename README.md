# My-Website-
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Preston Yesquen | Cybersecurity Dashboard</title>

<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;600;800&family=Roboto:wght@300;400;500&display=swap" rel="stylesheet">

<style>
:root{
--bg:#03060f;
--panel:#0b1225;
--blue:#4B9CD3;
--neon:#00ffc3;
--danger:#ff3b3b;
--text:#cfe3ff;
}

*{margin:0;padding:0;box-sizing:border-box}

body{
font-family:Roboto, sans-serif;
background:linear-gradient(180deg,#02040a,#050b1a);
color:var(--text);
overflow-x:hidden;
}

h1,h2,h3{font-family:Orbitron}

nav{
position:fixed;top:0;width:100%;
background:#02040acc;
backdrop-filter:blur(6px);
border-bottom:1px solid var(--blue);
z-index:1000;
}

nav ul{display:flex;justify-content:center;padding:12px;list-style:none}
nav li{margin:0 15px}
nav a{color:var(--text);text-decoration:none;font-family:Orbitron}
nav a:hover{color:var(--neon);text-shadow:0 0 8px var(--neon)}

.dashboard{
padding-top:80px;
display:grid;
grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
gap:20px;
max-width:1200px;
margin:auto;
padding:100px 20px 40px;
}

.panel{
background:var(--panel);
border:1px solid var(--blue);
border-radius:10px;
padding:20px;
position:relative;
overflow:hidden;
}

.panel::after{
content:"";position:absolute;top:0;left:0;width:100%;height:2px;
background:linear-gradient(90deg,transparent,var(--neon),transparent);
animation:scan 3s infinite;
}

@keyframes scan{0%{transform:translateX(-100%)}100%{transform:translateX(100%)}}

.title{margin-bottom:15px;color:var(--blue)}
.stat{font-size:2rem;color:var(--neon)}

.bar{height:8px;background:#111;border-radius:5px;margin-top:10px;overflow:hidden}
.fill{height:100%;background:var(--neon)}

img.panel-img{
width:100%;
border-radius:8px;
margin-bottom:10px;
border:1px solid var(--blue);
}

.terminal{
background:black;padding:15px;border-radius:8px;
font-family:monospace;color:var(--neon);
height:200px;overflow:auto;
}

footer{text-align:center;padding:20px;border-top:1px solid var(--blue)}
</style>
</head>
<body>

<nav>
<ul>
<li><a href="#">Dashboard</a></li>
<li><a href="#">Profile</a></li>
<li><a href="#">Systems</a></li>
</ul>
</nav>

<div class="dashboard">

<div class="panel">
<img class="panel-img" src="https://images.unsplash.com/photo-1550751827-4bd374c3f58b?auto=format&fit=crop&w=800&q=80">
<h2 class="title">User Profile</h2>
<p><strong>Name:</strong> Preston Yesquen</p>
<p><strong>Status:</strong> Active</p>
<p><strong>Origin:</strong> Virginia</p>
<p><strong>Focus:</strong> Cybersecurity</p>
</div>

<div class="panel">
<img class="panel-img" src="https://images.unsplash.com/photo-1518779578993-ec3579fee39f?auto=format&fit=crop&w=800&q=80">
<h2 class="title">Threat Level</h2>
<div class="stat">LOW</div>
<div class="bar"><div class="fill" style="width:30%"></div></div>
</div>

<div class="panel">
<img class="panel-img" src="https://images.unsplash.com/photo-1555949963-aa79dcee981c?auto=format&fit=crop&w=800&q=80">
<h2 class="title">Skill Matrix</h2>
<p>Malware Analysis</p>
<div class="bar"><div class="fill" style="width:70%"></div></div>
<p>Cryptography</p>
<div class="bar"><div class="fill" style="width:60%"></div></div>
<p>Networking</p>
<div class="bar"><div class="fill" style="width:65%"></div></div>
</div>

<div class="panel">
<img class="panel-img" src="https://images.unsplash.com/photo-1605902711622-cfb43c44367f?auto=format&fit=crop&w=800&q=80">
<h2 class="title">Interests</h2>
<p>Warhammer 40K</p>
<p>Dungeons & Dragons (DM)</p>
<p>Washington Sports Teams</p>
</div>

<div class="panel">
<img class="panel-img" src="https://images.unsplash.com/photo-1526378722484-bd91ca387e72?auto=format&fit=crop&w=800&q=80">
<h2 class="title">Mission Objectives</h2>
<ul>
<li>Enter Cybersecurity Field</li>
<li>Work in Malware / Crypto</li>
<li>Government or AI Career</li>
</ul>
</div>

<div class="panel">
<img class="panel-img" src="https://images.unsplash.com/photo-1519389950473-47ba0277781c?auto=format&fit=crop&w=800&q=80">
<h2 class="title">System Logs</h2>
<div class="terminal" id="terminal"></div>
</div>

</div>

<footer>
<p>© 2026 Preston Yesquen | Cyber Dashboard Interface</p>
</footer>

<script>
const logs = [
"[INIT] System Booting...",
"[OK] Profile Loaded",
"[SCAN] Checking vulnerabilities...",
"[OK] No major threats detected",
"[LOAD] Interests modules initialized",
"[READY] Dashboard online"
];

let i=0;
function typeLog(){
if(i<logs.length){
document.getElementById("terminal").innerHTML += logs[i] + "<br>";
i++;
setTimeout(typeLog,800);
}
}
window.onload = typeLog;
</script>

</body>
</html>
