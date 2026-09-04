<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=170&color=gradient&customColorList=12,20,6&text=Abdul%20Malik&fontColor=ffffff&fontSize=52&fontAlignY=34&desc=I%20build%20systems%20that%20measure%20themselves&descAlignY=54&descSize=15&animation=fadeIn" width="100%" alt="Abdul Malik" />

<a href="https://github.com/AbdulMalik1287">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=21&pause=1400&color=7C3AED&center=true&vCenter=true&width=700&lines=CSE+(AI+%26+ML)+%40+IIIT+Nagpur+%E2%80%A2+CGPA+9.55;AI+Intern+%40+FuMind.ai+-+building+GenMES;RAG%2C+LLM+evaluation%2C+computer+vision;If+I+claim+a+number%2C+I+measured+it" alt="typing" />
</a>

<br/>

<a href="https://www.linkedin.com/in/abdul-malik-2a8962318/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
<a href="mailto:abdulmalik1234king@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
<a href="https://github.com/AbdulMalik1287?tab=followers"><img src="https://img.shields.io/github/followers/AbdulMalik1287?label=Follow&style=for-the-badge&color=7C3AED&labelColor=0B1120" alt="Followers" /></a>
<img src="https://komarev.com/ghpvc/?username=AbdulMalik1287&label=Profile+views&color=7C3AED&style=for-the-badge" alt="Profile views" />

</div>

---

## whoami

CS undergrad at **IIIT Nagpur** (AI & ML specialisation, class of 2028), currently **AI Intern at FuMind.ai** shipping production modules for GenMES, a manufacturing execution system with a genetic-algorithm scheduler.

I came up through full-stack work (FastAPI, PostgreSQL, React, Tauri) and I am pointing that at applied ML: retrieval, LLM tool use, evaluation, and computer vision.

The thing I care about most: **a system that reports its own accuracy is worth more than one that just claims it.** Most of what is below shipped with an eval set attached, and a few of them shipped with the benchmark I built to try to break them.

```text
focus      ->  RAG · LLM evaluation · CV deployment
shipping   ->  GenMES modules @ FuMind.ai
learning   ->  LoRA/PEFT fine-tuning, model serving
mentoring  ->  6 first-years, CRISPR Club (AIRA) @ IIITN
```

---

## Selected work

Every number here comes from a run I can point you at, not an estimate.

| Project | What it is | The measured part |
| :--- | :--- | :--- |
| **[LedgerStein](https://github.com/AbdulMalik1287/ledgerstein)** | Three-way payment reconciliation across ERP, Razorpay and bank: a 17-rule tiered matcher with an LLM adjudicator on the leftovers | **100% precision, 98.6% recall** on held-out data it was never tuned against, ~24k rows/sec, 56 tests |
| **[Dossier](https://github.com/AbdulMalik1287/dossier)** | Portfolio-as-agent: a citation-grounded RAG system that answers recruiter questions about my own work | Cross-encoder reranking lifted **recall@5 from 0.87 to 0.95** on a hand-labelled eval set |
| **[Hopper](https://github.com/AbdulMalik1287/hopper)** | Rust + Tauri 2 desktop app that safely auto-updates Minecraft Fabric mods | SHA-512-verified downloads, timestamped rollbacks, NSIS + MSI installers shipped |
| **[NLP capstone](https://github.com/AbdulMalik1287/NLP)** | Cross-domain complaint understanding with multilingual encoders (XLM-R) | LODO fold protocol: trained and scored per held-out domain, not one flattering split |
| **STMS v3** *(team repo)* | Traffic-intelligence rebuild for Manthan Yuva @ VNIT: detection, tracking, signal timing | Same clip, same 200 frames: **12.7 to 22.2 fps**, **13 to 32 vehicles** counted correctly |

<details>
<summary><b>Why "measured" keeps showing up</b></summary>

<br/>

Three habits that produced the numbers above:

- **Build the benchmark too, then make it harder.** LedgerStein scored 100/100 on its first benchmark, which told me the benchmark was easy, not that the matcher was good. I rebuilt it adversarially and re-scored.
- **Let the model decline.** The LLM tier in LedgerStein is bounded by a candidate whitelist enforced *after* the call, so a hallucinated id lands in the exception queue instead of the ledger. On a live run it correctly declined all six genuinely undecidable rows.
- **Benchmark the incumbent before replacing it.** On STMS the team's own checkpoint managed 11 detections/frame against 33.8 for a stock model, so it was demoted to the classes it was actually good at rather than thrown away.

</details>

---

## Featured: LedgerStein

> An AI finance controller that reconciles ERP invoices, Razorpay payments/settlements and bank statements, and is honest about what it could not match.

<a href="https://ledgerstein.onrender.com"><img src="https://img.shields.io/badge/Live%20demo-ledgerstein.onrender.com-7C3AED?style=for-the-badge&logo=render&logoColor=white" alt="Live" /></a>
<a href="https://youtu.be/EaOqJAiIKfo"><img src="https://img.shields.io/badge/Walkthrough-YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Video" /></a>
<a href="https://github.com/AbdulMalik1287/ledgerstein"><img src="https://img.shields.io/badge/Source-181717?style=for-the-badge&logo=github&logoColor=white" alt="Source" /></a>

Deterministic rules first (exact keys, derived arithmetic, bounded subset-sum, fuzzy inference), and only the rows the rules *declined* ever reach a model. Provider-pluggable across Anthropic, Gemini, Groq and Ollama. Ships as one self-seeding Docker container serving API and dashboard from a single origin. Built for the **Razorpay AI Buildathon, Track 04**.

---

## Toolbox

<div align="center">

**Languages**

<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="42" alt="Python" />&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" height="42" alt="TypeScript" />&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg" height="42" alt="C++" />&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/rust/rust-original.svg" height="42" alt="Rust" />&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" height="42" alt="SQL" />&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="42" alt="JavaScript" />

**ML / AI**

<img src="https://skillicons.dev/icons?i=pytorch,tensorflow,sklearn,opencv&theme=dark" alt="ML stack" />

<img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black" alt="Hugging Face" />
<img src="https://img.shields.io/badge/FAISS-0467DF?style=flat-square&logo=meta&logoColor=white" alt="FAISS" />
<img src="https://img.shields.io/badge/sentence--transformers-7C3AED?style=flat-square" alt="sentence-transformers" />
<img src="https://img.shields.io/badge/YOLOv8%20%2F%20v11-111F68?style=flat-square" alt="YOLO" />
<img src="https://img.shields.io/badge/Weights%20%26%20Biases-FFBE00?style=flat-square&logo=weightsandbiases&logoColor=black" alt="W&B" />
<img src="https://img.shields.io/badge/Roboflow-6706CE?style=flat-square&logo=roboflow&logoColor=white" alt="Roboflow" />

**Engineering**

<img src="https://skillicons.dev/icons?i=fastapi,react,tauri,docker,postgres,redis,git,linux,vite,tailwind&theme=dark" alt="Engineering stack" />

</div>

---

## The numbers GitHub keeps for me

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=AbdulMalik1287&show_icons=true&hide_border=true&bg_color=00000000&title_color=7C3AED&text_color=8B949E&icon_color=06B6D4&include_all_commits=true&count_private=true" alt="stats" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=AbdulMalik1287&layout=compact&hide_border=true&bg_color=00000000&title_color=7C3AED&text_color=8B949E&langs_count=8" alt="top languages" />

<br/>

<img height="165" src="https://streak-stats.demolab.com?user=AbdulMalik1287&hide_border=true&background=00000000&ring=7C3AED&fire=06B6D4&currStreakLabel=7C3AED&sideLabels=8B949E&dates=8B949E&currStreakNum=7C3AED&sideNums=7C3AED" alt="streak" />

<br/><br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=AbdulMalik1287&hide_border=true&bg_color=00000000&color=7C3AED&line=06B6D4&point=7C3AED&area=true&area_color=7C3AED" width="95%" alt="activity graph" />

</div>

---

## Beyond the code

- **CRISPR Club (AIRA, AI Research & Applications), IIIT Nagpur** - mentor six first-year students in ML fundamentals. Most of them wanted direction more than answers, so I wrote them structured learning paths with projects attached.
- **Marketing Coordinator**, college Techfest and Cultural Fest - outreach strategy across two festivals.
- Languages: Hindi, English, Urdu, and enough Arabic to follow along.

---

<div align="center">

### Let's talk

Open to **AI/ML internships** and applied-ML work. If you are building something where the accuracy has to be defensible, that is the part I enjoy.

<a href="mailto:abdulmalik1234king@gmail.com"><img src="https://img.shields.io/badge/abdulmalik1234king@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
<a href="https://www.linkedin.com/in/abdul-malik-2a8962318/"><img src="https://img.shields.io/badge/Connect%20on%20LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>

<img src="https://capsule-render.vercel.app/api?type=waving&height=110&color=gradient&customColorList=6,20,12&section=footer" width="100%" alt="" />

</div>
