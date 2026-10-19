# CodeAlpha_ProjectName
A basic network sniffer built in Python with Scapy. It captures live
packets, analyzes their structure, and prints useful details.

## Features
- Captures live network traffic
- Shows timestamp, source IP, destination IP, protocol and ports
- Identifies TCP, UDP and ICMP packets
- Displays the first 50 bytes of each payload
- Prints a protocol summary at the end

## Requirements
- Python 3
- Scapy: `pip install scapy`
- Windows: install [Npcap](https://npcap.com) and run as Administrator
- Linux/Mac: run with `sudo`

## How to run
    python sniffer.py

## Sample output
(<img width="865" height="459" alt="snifffff3" src="https://github.com/user-attachments/assets/c81d5a4d-da8e-4035-be91-8cd2839a6ef4" />
)

<img width="923" height="482" alt="snifffff" src="https://github.com/user-attachments/assets/808e95d4-c401-493c-aa31-eaedd89e6f32" />

<img width="903" height="476" alt="snifffff 2" src="https://github.com/user-attachments/assets/df8d5883-4c5e-4365-8aff-3b2b9e7ecfdf" />


## What I learned
- Packets have layers: IP, then TCP/UDP/ICMP, then payload
- HTTPS and QUIC payloads are encrypted, so they look like random bytes
- ICMP (ping) payloads are unencrypted and readable

## Disclaimer
Use this only on networks you own or have permission to monitor.







<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Phishing Awareness Training</title>
<style>
:root{box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px);
--bg:#f6f8fb;--card:#fff;--text:#14213d;--muted:#5b6678;--accent:#0b6bcb;--bad:#c62828;--good:#1b7f3b;--line:#dde3ec;--warnbg:#fff4e5}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#0f1520;--card:#182131;--text:#e8edf5;--muted:#9aa7bb;--accent:#5aa9ff;--bad:#ff6b6b;--good:#4cd07d;--line:#2a364b;--warnbg:#2b2214}}
:root[data-theme="dark"]{--bg:#0f1520;--card:#182131;--text:#e8edf5;--muted:#9aa7bb;--accent:#5aa9ff;--bad:#ff6b6b;--good:#4cd07d;--line:#2a364b;--warnbg:#2b2214}
html{scroll-padding-top:60px;scroll-behavior:smooth}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--text);font:16px/1.6 system-ui,-apple-system,"Segoe UI",Roboto,sans-serif}
nav{position:sticky;top:env(safe-area-inset-top,0px);background:var(--card);border-bottom:1px solid var(--line);padding:10px 16px;display:flex;gap:14px;overflow-x:auto;white-space:nowrap;z-index:5}
nav a{color:var(--accent);text-decoration:none;font-size:14px;font-weight:600}
body::before{content:"";position:fixed;inset:0 0 auto;height:env(safe-area-inset-top,0px);background:var(--card);z-index:10}
header{padding:40px 20px 24px;max-width:820px;margin:auto}
h1{font-size:clamp(28px,6vw,42px);line-height:1.15;margin:0 0 10px}
h2{margin:0 0 12px;font-size:24px}
h3{margin:18px 0 6px;font-size:17px}
.sub{color:var(--muted);font-size:18px;margin:0}
main{max-width:820px;margin:auto;padding:0 16px 60px}
section{background:var(--card);border:1px solid var(--line);border-radius:14px;padding:22px;margin:18px 0}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:12px}
.item{border:1px solid var(--line);border-radius:10px;padding:12px 14px}
.item b{color:var(--accent)}
.mail{border:1px solid var(--line);border-radius:10px;overflow:hidden;font-size:14px;margin:12px 0}
.mail .h{background:var(--bg);padding:10px 14px;border-bottom:1px solid var(--line)}
.mail .b{padding:12px 14px}
.flag{color:var(--bad);font-weight:700;border-bottom:2px dotted var(--bad);cursor:help}
.btn{display:inline-block;background:var(--accent);color:#fff;border:0;border-radius:8px;padding:9px 16px;font:inherit;font-weight:600;cursor:pointer}
.btn.alt{background:transparent;color:var(--accent);border:1px solid var(--accent)}
.note{background:var(--warnbg);border-left:4px solid #f0a020;padding:10px 14px;border-radius:6px;margin:12px 0}
.url{font-family:ui-monospace,Menlo,Consolas,monospace;background:var(--bg);padding:2px 6px;border-radius:5px;word-break:break-all}
.bad{color:var(--bad)}.good{color:var(--good)}
.opt{display:block;width:100%;text-align:left;background:var(--bg);color:var(--text);border:1px solid var(--line);border-radius:8px;padding:10px 12px;margin:6px 0;font:inherit;cursor:pointer}
.opt:hover:not(:disabled){border-color:var(--accent)}
.opt.right{border-color:var(--good);background:color-mix(in srgb,var(--good) 18%,var(--card))}
.opt.wrong{border-color:var(--bad);background:color-mix(in srgb,var(--bad) 18%,var(--card))}
.fb{margin:8px 0 0;font-size:14px;color:var(--muted)}
.bar{height:8px;background:var(--line);border-radius:6px;overflow:hidden;margin-bottom:14px}
.bar i{display:block;height:100%;width:0;background:var(--accent);transition:width .3s}
ul{padding-left:20px;margin:6px 0}
footer{text-align:center;color:var(--muted);font-size:13px;padding:20px}
</style>
</head>
<body>
<nav>
<a href="#recognize">Spot Phishing</a><a href="#fake">Fake Websites</a><a href="#social">Social Engineering</a><a href="#tips">Best Practices</a><a href="#cases">Real Cases</a><a href="#quiz">Quiz</a>
</nav>
<header>
<h1>Phishing Awareness Training</h1>
<p class="sub">Learn to recognize, resist and report phishing attacks. About 15 minutes, with a quiz at the end.</p>
</header>
<main>

<section id="intro">
<h2>What is phishing?</h2>
<p>Phishing is a type of social engineering attack in which an attacker pretends to be a trusted person or organization to trick you into revealing credentials, sending money, or installing malware. It usually arrives by email, but also by SMS (<b>smishing</b>), phone call (<b>vishing</b>), and chat or social media messages.</p>
<div class="grid">
<div class="item"><b>Mass phishing</b><br>Generic emails sent to thousands of people.</div>
<div class="item"><b>Spear phishing</b><br>Targeted at one person, using details about them.</div>
<div class="item"><b>Whaling / BEC</b><br>Impersonating executives to trigger payments or data leaks.</div>
</div>
</section>

<section id="recognize">
<h2>1. Recognizing phishing emails</h2>
<p>Tap or hover over the red items in this sample email to see why each one is suspicious.</p>
<div class="mail">
<div class="h"><b>From:</b> <span class="flag" data-why="The display name says PayPal, but the real address belongs to an unrelated domain.">PayPal Support &lt;service@paypa1-secure.co&gt;</span><br>
<b>Subject:</b> <span class="flag" data-why="Urgency and threats are designed to make you act before you think.">URGENT: Your account will be suspended in 24 hours!</span></div>
<div class="b">
<span class="flag" data-why="Generic greeting. Real providers usually use your name.">Dear Customer,</span><br><br>
We noticed unusual activity. <span class="flag" data-why="Poor grammar and odd phrasing are common signs, although modern attacks can be polished.">Your account have been limited</span>. To restore access, <span class="flag" data-why="The link text looks safe, but the real destination differs. Always hover to check.">click here to verify</span> your password and card details immediately.<br><br>
<span class="flag" data-why="Unexpected attachments, especially .zip, .html or Office files with macros, can carry malware.">Attachment: Account_Form.zip</span>
</div>
</div>
<div id="why" class="note">Select a red item to see the explanation.</div>
<h3>Quick checklist</h3>
<ul>
<li>Check the <b>actual sender address</b>, not just the display name.</li>
<li>Look for <b>urgency, fear or too-good-to-be-true offers</b>.</li>
<li>Hover over links to preview the real URL before clicking.</li>
<li>Be wary of unexpected attachments and requests for passwords, OTPs or payments.</li>
</ul>
</section>

<section id="fake">
<h2>2. Spotting fake websites</h2>
<p>Attackers clone login pages and host them on look-alike domains. Compare these:</p>
<div class="grid">
<div class="item"><span class="good">Legitimate</span><br><span class="url">https://accounts.google.com</span></div>
<div class="item"><span class="bad">Typosquatting</span><br><span class="url">https://accounts.g00gle.com</span></div>
<div class="item"><span class="bad">Subdomain trick</span><br><span class="url">https://google.com.login-verify.net</span><br><small>The real domain is login-verify.net.</small></div>
<div class="item"><span class="bad">Misleading path</span><br><span class="url">https://evil-site.xyz/paypal.com/login</span></div>
</div>
<ul>
<li>Read the domain <b>right to left from the first single slash</b>: the part just before the TLD (.com, .net) is who owns the site.</li>
<li>A padlock (HTTPS) only means the connection is encrypted. <b>Phishing sites can have it too.</b></li>
<li>Type known addresses yourself or use bookmarks instead of clicking email links.</li>
<li>Watch for odd login prompts, missing pages, low-quality logos and unusual requests for extra data.</li>
</ul>
</section>

<section id="social">
<h2>3. Social engineering tactics</h2>
<p>Phishing works because it targets human psychology, not just technology.</p>
<div class="grid">
<div class="item"><b>Authority</b><br>“This is the CEO / IT department / tax office.”</div>
<div class="item"><b>Urgency</b><br>“Act now or your account will be closed.”</div>
<div class="item"><b>Fear</b><br>“Suspicious login detected from another country.”</div>
<div class="item"><b>Greed or curiosity</b><br>“You have won a prize”, “See who viewed your profile”.</div>
<div class="item"><b>Trust and familiarity</b><br>Messages that appear to come from a colleague or friend.</div>
<div class="item"><b>Pretexting</b><br>A made-up scenario, such as a fake support call, to extract information.</div>
<div class="item"><b>Baiting</b><br>Infected USB drives or free downloads left as bait.</div>
<div class="item"><b>Quid pro quo</b><br>A “free service” in exchange for credentials or access.</div>
</div>
<div class="note"><b>Rule of thumb:</b> when a message pressures you to skip normal procedure, stop and verify through a separate, trusted channel.</div>
</section>

<section id="tips">
<h2>4. Best practices to stay safe</h2>
<div class="grid">
<div class="item"><b>Pause and verify</b><br>Call the sender using a known number, not one in the message.</div>
<div class="item"><b>Enable MFA</b><br>Prefer authenticator apps or hardware keys over SMS codes.</div>
<div class="item"><b>Use a password manager</b><br>It won’t autofill on look-alike domains, which is a useful warning sign.</div>
<div class="item"><b>Keep software updated</b><br>Patch browsers, OS and email clients.</div>
<div class="item"><b>Never share OTPs</b><br>No legitimate support agent will ask for them.</div>
<div class="item"><b>Report it</b><br>Use your organization’s report button or tell the IT/security team. Then delete the message.</div>
</div>
<h3>If you already clicked</h3>
<ul>
<li>Disconnect from the network if you opened an attachment.</li>
<li>Change the affected password immediately and any others that reuse it.</li>
<li>Enable MFA, check account activity, and notify IT or your bank.</li>
</ul>
</section>

<section id="cases">
<h2>5. Real-world examples</h2>
<div class="item"><b>Google and Facebook invoice scam (2013 to 2015)</b><br>A fraudster posed as a legitimate hardware supplier and sent convincing fake invoices, tricking both companies into paying over $100 million in total. Much of it was later recovered. <i>Lesson: verify payment-detail changes through a separate channel.</i></div><br>
<div class="item"><b>RSA Security breach (2011)</b><br>Employees received a spear-phishing email with an Excel attachment titled “2011 Recruitment plan”. Opening it exploited a vulnerability and gave attackers a foothold in the network. <i>Lesson: even security companies are targeted, so be careful with unexpected attachments.</i></div><br>
<div class="item"><b>Twitter hack (2020)</b><br>Attackers used phone-based social engineering against employees to gain access to internal tools and took over high-profile accounts. <i>Lesson: vishing is real, so verify callers claiming to be IT.</i></div>
</section>

<section id="quiz">
<h2>6. Test your knowledge</h2>
<div class="bar"><i id="prog"></i></div>
<div id="qbox"></div>
</section>
</main>
<footer>Phishing Awareness Training · Educational use</footer>

<script>
document.querySelectorAll('.flag').forEach(function(el){
  var show=function(){document.getElementById('why').textContent=el.getAttribute('data-why');};
  el.addEventListener('click',show);el.addEventListener('mouseenter',show);
});

var Q=[
{q:'You receive an email from “IT Support” asking you to verify your password through a link within 1 hour. What should you do?',o:['Click the link quickly to avoid lockout','Reply with your password','Ignore the link and contact IT through a known channel','Forward it to colleagues as a warning'],a:2,e:'Urgency plus a credential request is a classic phishing pattern. Verify via a trusted channel and report it.'},
{q:'Which URL is most likely the real PayPal login page?',o:['https://paypal.com.secure-login.net','https://www.paypal.com/signin','https://paypa1.com/login','https://secure-paypal.xyz/signin'],a:1,e:'The domain paypal.com is the part immediately before the first single slash, with no look-alike characters.'},
{q:'A website shows a padlock icon. What does that guarantee?',o:['The site is legitimate','The connection is encrypted, but not that the site is trustworthy','The site is free of malware','The owner has been verified by your bank'],a:1,e:'HTTPS only encrypts traffic. Phishing sites commonly use it too.'},
{q:'Which of these is a social engineering tactic?',o:['Port scanning','Impersonating a senior executive to request an urgent transfer','Installing a firewall','Applying a software patch'],a:1,e:'Impersonating authority to create pressure is classic social engineering (whaling or BEC).'},
{q:'You clicked a suspicious link and entered your password. What is the best first step?',o:['Do nothing, it was probably fine','Change the password, enable MFA and report the incident','Delete your email account','Wait to see if anything happens'],a:1,e:'Act quickly: change the password (and any reused ones), turn on MFA, and notify IT or the service provider.'}
];
var i=0,score=0,box=document.getElementById('qbox'),prog=document.getElementById('prog');

function render(){
  prog.style.width=(i/Q.length*100)+'%';
  if(i>=Q.length){
    var msg=score>=4?'Excellent. You can spot phishing like a pro.':score>=3?'Good job. Review the sections above to sharpen up.':'Keep practicing. Re-read the sections above and try again.';
    box.innerHTML='<h3>You scored '+score+' / '+Q.length+'</h3><p>'+msg+'</p><button class="btn" id="again">Retake quiz</button>';
    document.getElementById('again').onclick=function(){i=0;score=0;render();};
    return;
  }
  var q=Q[i];
  box.innerHTML='<p><b>Question '+(i+1)+' of '+Q.length+'</b></p><p>'+q.q+'</p>';
  q.o.forEach(function(t,k){
    var b=document.createElement('button');b.className='opt';b.textContent=t;
    b.onclick=function(){answer(k);};box.appendChild(b);
  });
  var f=document.createElement('p');f.className='fb';f.id='fb';box.appendChild(f);
}
function answer(k){
  var q=Q[i],btns=box.querySelectorAll('.opt');
  btns.forEach(function(b,n){b.disabled=true;if(n===q.a)b.classList.add('right');else if(n===k)b.classList.add('wrong');});
  if(k===q.a)score++;
  document.getElementById('fb').textContent=(k===q.a?'Correct. ':'Not quite. ')+q.e;
  var nx=document.createElement('button');nx.className='btn';nx.textContent=i===Q.length-1?'See results':'Next question';
  nx.onclick=function(){i++;render();};box.appendChild(nx);
}
render();
</script>
</body>
</html>



