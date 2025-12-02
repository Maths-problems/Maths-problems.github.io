<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Python → Discord Dev Roadmap</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://pyscript.net/latest/pyscript.css">
<script defer src="https://pyscript.net/latest/pyscript.js"></script>
<style>
:root {
  --bg:#030712; --panel:#0a0f1e; --card:#111827; --text:#e5e7eb; --accent:#3b82f6; --accent2:#22d3ee; --accent3:#a855f7;
}
body {margin:0; font-family:"Poppins",sans-serif; background:radial-gradient(circle at 20% 20%, #0f172a, #020617 70%); color:var(--text); padding:40px;}
#login-container, #main-container {max-width:1100px; margin:auto; backdrop-filter:blur(20px); background:rgba(255,255,255,0.03); border-radius:20px; padding:30px; border:1px solid rgba(255,255,255,0.05);}
h1 {font-size:36px; font-weight:700; background:linear-gradient(90deg,var(--accent),var(--accent2),var(--accent3)); -webkit-background-clip:text;color:transparent; margin-bottom:16px;}
.sub {color:#9ca3af;margin-bottom:30px;}
input {width:100%; padding:12px; margin-bottom:12px; border-radius:8px; border:1px solid #333; background:rgba(0,0,0,0.8); color:#e5e7eb; font-family:monospace;}
button {padding:12px; border:none; border-radius:8px; background:linear-gradient(90deg,var(--accent),var(--accent2)); color:#020617; cursor:pointer; font-weight:600;}
#error {color:#f87171; margin-bottom:12px;}
#main-container {display:none;}
.phase {background:rgba(255,255,255,0.03); padding:18px 20px; border-radius:14px; border:1px solid rgba(255,255,255,0.06); margin-bottom:20px; transition:0.3s;}
.phase:hover {transform:translateY(-6px) scale(1.02); box-shadow:0 12px 36px rgba(0,0,0,0.45);}
h2 {font-size:24px; background:linear-gradient(90deg,var(--accent),var(--accent3)); -webkit-background-clip:text;color:transparent;margin-bottom:12px;}
.resource-card {background: rgba(255,255,255,0.03); border:1px solid rgba(255,255,255,0.1); padding:18px 22px; border-radius:14px; margin-bottom:18px; transition: transform 0.3s, box-shadow 0.3s; display:flex; flex-direction:row; justify-content:space-between; gap:12px;}
.resource-card:hover {transform:translateY(-6px) scale(1.01); box-shadow:0 12px 28px rgba(0,0,0,0.45);}
.resource-content {flex:2;}
.resource-card h3 {color:#3b82f6; font-size:18px; margin-bottom:8px;}
.resource-card p, .resource-card ol, .resource-card li {font-size:14px; margin-bottom:8px;}
.resource-embed {margin-top:8px; border-radius:8px; overflow:hidden; border:1px solid rgba(255,255,255,0.1);}
.note-section {flex:1; display:flex; flex-direction:column;}
.note-section textarea {resize:none; background:rgba(0,0,0,0.8); border-radius:8px; border:1px solid #333; color:#e5e7eb; padding:8px; font-family:monospace; min-height:80px;}
.note-section label {margin-bottom:6px; font-size:13px; color:#22d3ee;}
.py-terminal {background:rgba(0,0,0,0.8); padding:12px; border-radius:12px; border:1px solid rgba(255,255,255,0.1); margin-top:30px;}
.py-terminal textarea {width:100%; height:120px; border-radius:8px; background:#020617; color:#e5e7eb; border:1px solid #333; padding:8px; font-family:monospace;}
.py-terminal button {margin-top:6px; padding:8px 12px; border:none; border-radius:8px; background:linear-gradient(90deg,var(--accent),var(--accent2)); color:#020617; cursor:pointer;}
.py-terminal pre {background:#020617; border-radius:8px; padding:10px; margin-top:8px; overflow-x:auto; max-height:250px;}
iframe {width:100%; height:200px; border:none; border-radius:8px;}
</style>
</head>
<body>

<!-- Login Page -->
<div id="login-container">
<h1>Login</h1>
<p class="sub">Enter your credentials to access the Python → Discord roadmap.</p>
<div id="error"></div>
<input type="text" id="username" placeholder="Username">
<input type="password" id="password" placeholder="Password">
<button onclick="checkLogin()">Login</button>
</div>

<!-- Main Roadmap -->
<div id="main-container">
<h1>Python → Discord Dev Roadmap</h1>
<p class="sub">Embedded resources, interactive terminal, and notes per card!</p>

<!-- ------------------ Phase 1 ------------------ -->
<div class="phase">
<h2>Phase 1 — Python Fundamentals</h2>

<div class="resource-card" data-id="phase1-1">
<div class="resource-content">
<h3>Learn Python Basics</h3>
<p>Variables, loops, functions, conditionals.</p>
<ol>
<li>Follow the tutorial to understand variables and loops.</li>
<li>Experiment in the Python terminal below.</li>
<li>Create a small calculator or text-based program.</li>
</ol>
<div class="resource-embed">
<iframe src="https://www.programiz.com/python-programming" title="Python Basics"></iframe>
</div>
</div>
<div class="note-section"><label>Notes:</label><textarea id="note-phase1-1"></textarea></div>
</div>

<div class="resource-card" data-id="phase1-2">
<div class="resource-content">
<h3>Practice Mini Projects</h3>
<p>Hands-on practice with simple programs.</p>
<ol>
<li>Guess the number game.</li>
<li>Text adventure simulation.</li>
<li>Function-based calculator.</li>
</ol>
<div class="resource-embed">
<iframe src="https://replit.com/languages/python3" title="Python Practice"></iframe>
</div>
</div>
<div class="note-section"><label>Notes:</label><textarea id="note-phase1-2"></textarea></div>
</div>
</div>

<!-- ------------------ Phase 2 ------------------ -->
<div class="phase">
<h2>Phase 2 — Developer Skills</h2>

<div class="resource-card" data-id="phase2-1">
<div class="resource-content">
<h3>Modules & Virtual Environments</h3>
<p>Organize code and simulate different environments.</p>
<ol>
<li>Create Python modules and import them.</li>
<li>Practice reusable functions.</li>
<li>Simulate virtual environments.</li>
</ol>
<div class="resource-embed">
<iframe src="https://docs.python.org/3/tutorial/modules.html" title="Python Modules"></iframe>
</div>
</div>
<div class="note-section"><label>Notes:</label><textarea id="note-phase2-1"></textarea></div>
</div>

<div class="resource-card" data-id="phase2-2">
<div class="resource-content">
<h3>Data Structures</h3>
<p>Lists, dictionaries, tuples, sets — organize and store data.</p>
<ol>
<li>Manipulate data with loops.</li>
<li>Create nested data structures.</li>
<li>Practice storing and retrieving data.</li>
</ol>
<div class="resource-embed">
<iframe src="https://www.w3schools.com/python/python_lists.asp" title="Python Data Structures"></iframe>
</div>
</div>
<div class="note-section"><label>Notes:</label><textarea id="note-phase2-2"></textarea></div>
</div>
</div>

<!-- ------------------ Phase 3 ------------------ -->
<div class="phase">
<h2>Phase 3 — Discord Bot Basics</h2>

<div class="resource-card" data-id="phase3-1">
<div class="resource-content">
<h3>Bot Event Simulation</h3>
<p>Simulate bot responses and events in Python.</p>
<ol>
<li>Create functions like `send_message()` and `on_message()`.</li>
<li>Test in terminal.</li>
<li>Experiment with different responses.</li>
</ol>
<div class="resource-embed">
<iframe src="https://discordpy.readthedocs.io/en/stable/intro.html" title="Discord.py Docs"></iframe>
</div>
</div>
<div class="note-section"><label>Notes:</label><textarea id="note-phase3-1"></textarea></div>
</div>

<div class="resource-card" data-id="phase3-2">
<div class="resource-content">
<h3>Events & Commands</h3>
<p>Simulate event handling in Python functions.</p>
<ol>
<li>Define `on_join()`, `on_reaction()` functions.</li>
<li>Test outputs in Python terminal.</li>
<li>Learn basic bot logic before deployment.</li>
</ol>
<div class="resource-embed">
<iframe src="https://www.youtube.com/embed/THxVj_VrKQA" title="Discord Bot Tutorial"></iframe>
</div>
</div>
<div class="note-section"><label>Notes:</label><textarea id="note-phase3-2"></textarea></div>
</div>
</div>

<!-- ------------------ Phases 4–6 follow same structure ------------------ -->
<!-- Phase 4 -->
<div class="phase">
<h2>Phase 4 — Advanced Bot Concepts</h2>
<div class="resource-card" data-id="phase4-1">
<div class="resource-content">
<h3>Commands & Interactions</h3>
<p>Design command structure and simulate slash commands.</p>
<ol>
<li>Define `/help`, `/ping` commands.</li>
<li>Test responses in terminal.</li>
<li>Practice arguments and options.</li>
</ol>
<div class="resource-embed">
<iframe src="https://realpython.com/how-to-make-a-discord-bot-python/" title="Real Python Discord Bot"></iframe>
</div>
</div>
<div class="note-section"><label>Notes:</label><textarea id="note-phase4-1"></textarea></div>
</div>

<div class="resource-card" data-id="phase4-2">
<div class="resource-content">
<h3>Data Handling & Persistence</h3>
<p>Simulate saving data with JSON or dicts.</p>
<ol>
<li>Create JSON files locally.</li>
<li>Store user points, settings.</li>
<li>Practice reading/writing structured data.</li>
</ol>
<div class="resource-embed">
<iframe src="https://www.w3schools.com/python/python_json.asp" title="JSON Python"></iframe>
</div>
</div>
<div class="note-section"><label>Notes:</label><textarea id="note-phase4-2"></textarea></div>
</div>
</div>

<!-- Phase 5 -->
<div class="phase">
<h2>Phase 5 — Testing & Deployment</h2>
<div class="resource-card" data-id="phase5-1">
<div class="resource-content">
<h3>Testing Your Code</h3>
<p>Simulate testing bot logic before deployment.</p>
<ol>
<li>Try edge cases.</li>
<li>Debug using print statements.</li>
<li>Refactor functions for clarity.</li>
</ol>
<div class="resource-embed">
<iframe src="https://realpython.com/python-testing/" title="Python Testing"></iframe>
</div>
</div>
<div class="note-section"><label>Notes:</label><textarea id="note-phase5-1"></textarea></div>
</div>

<div class="resource-card" data-id="phase5-2">
<div class="resource-content">
<h3>Deployment Planning</h3>
<p>Plan structure and deployment workflow.</p>
<ol>
<li>Prepare script structure and configs.</li>
<li>Simulate hosting locally.</li>
<li>Plan directories for future hosting.</li>
</ol>
<div class="resource-embed">
<iframe src="https://www.youtube.com/embed/BOtWkzgrk98" title="Deploy Python Bot"></iframe>
</div>
</div>
<div class="note-section"><label>Notes:</label><textarea id="note-phase5-2"></textarea></div>
</div>
</div>

<!-- Phase 6 -->
<div class="phase">
<h2>Phase 6 — Real Bot Hosting & Projects</h2>
<div class="resource-card" data-id="phase6-1">
<div class="resource-content">
<h3>Discord API & Libraries</h3>
<p>Learn Discord.py/Pycord async event loops (simulation).</p>
<ol>
<li>Plan bot structure, commands, events.</li>
<li>Simulate connections.</li>
<li>Experiment with logic in Python terminal.</li>
</ol>
<div class="resource-embed">
<iframe src="https://discordpy.readthedocs.io/en/stable/api.html" title="Discord API Docs"></iframe>
</div>
</div>
<div class="note-section"><label>Notes:</label><textarea id="note-phase6-1"></textarea></div>
</div>

<div class="resource-card" data-id="phase6-2">
<div class="resource-content">
<h3>Project Ideas</h3>
<p>Plan real bot projects.</p>
<ol>
<li>Moderation bot</li>
<li>Fun mini-games bot</li>
<li>Utility server bot</li>
</ol>
<div class="resource-embed">
<iframe src="https://replit.com/~" title="Code Practice"></iframe>
</div>
</div>
<div class="note-section"><label>Notes:</label><textarea id="note-phase6-2"></textarea></div>
</div>
</div>

<!-- ------------------ Python Terminal ------------------ -->
<div class="py-terminal">
<h3>Interactive Python Terminal</h3>
<textarea id="pycode">print("Hello, Python!")</textarea>
<button onclick="runPython()">Run Code</button>
<pre id="pyoutput"></pre>
<py-script id="pyscript" output="pyoutput"></py-script>
</div>

<script>
// Login
function checkLogin(){
    const u=document.getElementById('username').value;
    const p=document.getElementById('password').value;
    const error=document.getElementById('error');
    if(u==="ImSoOffline" && p==="6767"){
        document.getElementById('login-container').style.display="none";
        document.getElementById('main-container').style.display="block";
    }else error.innerText="Incorrect username or password!";
}

// PyScript run
function runPython(){
    const code=document.getElementById('pycode').value;
    const output=document.getElementById('pyoutput');
    const pyscript=document.getElementById('pyscript');
    pyscript.innerHTML=`<py-script>import sys
from io import StringIO
_code="""${code}"""
_output=StringIO()
sys.stdout=_output
sys.stderr=_output
try:
 exec(_code)
except Exception as e:
 print(e)
sys.stdout=sys.__stdout__
sys.stderr=sys.__stderr__
print(_output.getvalue())</py-script>`;
}

// Notes persistence
document.querySelectorAll('textarea[id^="note-"]').forEach(t=>{
    const id=t.id;
    const saved=localStorage.getItem(id);
    if(saved) t.value=saved;
    t.addEventListener('input',()=>{localStorage.setItem(id,t.value)});
});
</script>
</body>
</html>
