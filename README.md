from pathlib import Path
import base64

img_path = Path("/mnt/data/a_dramatic_richly_designed_orange_and_gold_theme.png")
img_b64 = base64.b64encode(img_path.read_bytes()).decode("utf-8")

html = f"""<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sumit Singhania | Personal Website</title>
<meta name="description" content="Sumit Singhania - Personal Website. YouTube, Instagram and more.">
<style>
*{{box-sizing:border-box;margin:0;padding:0}}
html{{scroll-behavior:smooth}}
body{{font-family:Arial,Helvetica,sans-serif;background:#120600;color:#fff;line-height:1.6}}
.hero{{min-height:100vh;position:relative;background:linear-gradient(rgba(20,5,0,.35),rgba(20,5,0,.75)),url("data:image/png;base64,{img_b64}") center/cover no-repeat;display:flex;flex-direction:column}}
nav{{position:sticky;top:0;z-index:10;background:rgba(18,6,0,.9);backdrop-filter:blur(10px);display:flex;justify-content:space-between;align-items:center;padding:14px 6%;border-bottom:1px solid rgba(255,160,30,.4)}}
.logo{{font-size:22px;font-weight:800;color:#ff9d22}}
.navlinks{{display:flex;gap:20px}}
.navlinks a{{color:#fff;text-decoration:none;font-size:15px}}
.main{{flex:1;display:flex;align-items:center;justify-content:center;text-align:center;padding:70px 20px}}
.card{{max-width:850px}}
.badge{{display:inline-block;padding:7px 15px;border:1px solid #ff9d22;border-radius:30px;color:#ffb14a;background:rgba(0,0,0,.35);margin-bottom:18px}}
h1{{font-size:clamp(42px,10vw,80px);line-height:1.05;margin-bottom:10px}}
.subtitle{{font-size:clamp(18px,4vw,27px);letter-spacing:4px;color:#ffd08a}}
.jai{{font-size:26px;color:#ffb13b;margin:20px 0;font-weight:bold}}
.buttons{{display:flex;gap:16px;justify-content:center;flex-wrap:wrap;margin-top:25px}}
.btn{{display:inline-block;text-decoration:none;color:#fff;padding:14px 28px;border-radius:40px;font-weight:700;min-width:190px;transition:.2s;box-shadow:0 8px 25px rgba(0,0,0,.3)}}
.btn:hover{{transform:translateY(-3px)}}
.youtube{{background:#e62117}}
.instagram{{background:linear-gradient(45deg,#f9ce34,#ee2a7b,#6228d7)}}
section{{padding:65px 7%;background:#160803}}
section:nth-of-type(even){{background:#0d0502}}
.section-title{{color:#ff9d22;font-size:35px;margin-bottom:20px}}
.about{{max-width:850px;font-size:18px;color:#eee}}
.links{{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:20px;margin-top:25px}}
.linkcard{{padding:28px;border:1px solid #9a4e0b;border-radius:20px;background:rgba(255,140,20,.06)}}
.linkcard h3{{font-size:24px;margin-bottom:8px}}
.smallbtn{{display:inline-block;margin-top:15px;padding:10px 18px;border-radius:25px;text-decoration:none;color:white;background:#ff7a00}}
footer{{padding:25px;text-align:center;border-top:1px solid #63330c;color:#bbb}}
@media(max-width:600px){{nav{{padding:13px 18px}}.navlinks{{gap:10px}}.navlinks a{{font-size:13px}}.logo{{font-size:18px}}}}
</style>
</head>
<body>
<div class="hero" id="home">
<nav>
<div class="logo">ॐ &nbsp; Sumit Singhania</div>
<div class="navlinks">
<a href="#home">Home</a><a href="#about">About</a><a href="#links">Links</a>
</div>
</nav>
<div class="main">
<div class="card">
<div class="badge">PERSONAL WEBSITE</div>
<h1>Sumit Singhania</h1>
<div class="subtitle">DREAM • WORK • ACHIEVE</div>
<div class="jai">🚩 जय श्री राम 🚩</div>
<p style="font-size:18px">Welcome to my personal website. Connect with me on YouTube & Instagram.</p>
<div class="buttons">
<a class="btn youtube" href="https://youtube.com/@sumit_singhania_9?si=9W5-TKoRC9qTYjFG" target="_blank">▶ YouTube</a>
<a class="btn instagram" href="https://www.instagram.com/sumit_singhania_9?stkn=b3AyeTBveDdoMjFm" target="_blank">◎ Instagram</a>
</div>
</div>
</div>
</div>

<section id="about">
<h2 class="section-title">👤 About Me</h2>
<p class="about">Hi, I'm <b>Sumit Singhania</b>. This is my personal website where you can find my YouTube and Instagram. I love creating content, exploring new things and sharing my journey with you all.</p>
<p class="jai">जय श्री राम 🚩</p>
</section>

<section id="links">
<h2 class="section-title">🔗 Quick Links</h2>
<div class="links">
<div class="linkcard">
<h3>▶ YouTube</h3><p>Subscribe and watch my latest videos.</p>
<a class="smallbtn" href="https://youtube.com/@sumit_singhania_9?si=9W5-TKoRC9qTYjFG" target="_blank">Visit Channel →</a>
</div>
<div class="linkcard">
<h3>📷 Instagram</h3><p>Follow me for reels, photos and updates.</p>
<a class="smallbtn" href="https://www.instagram.com/sumit_singhania_9?stkn=b3AyeTBveDdoMjFm" target="_blank">Follow Now →</a>
</div>
</div>
</section>

<footer>© 2026 Sumit Singhania &nbsp;|&nbsp; 🚩 जय श्री राम</footer>
</body>
</html>"""

out = Path("/mnt/data/Sumit_Singhania_Personal_Website.html")
out.write_text(html, encoding="utf-8")
print(f"Created: {out}")
