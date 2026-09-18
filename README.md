mkdir -p .github/workflows scripts

# ---------------- README.md ----------------
cat > README.md <<'EOF'
<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/pranav-sre/pranav-sre/main/dark.svg">
  <img alt="Pranav Tiwari" src="https://raw.githubusercontent.com/pranav-sre/pranav-sre/main/light.svg">
</picture>

### ☁️ Cloud & DevOps Engineer · SRE Enthusiast · Agentic AI Explorer

*B.Tech CSE '28 @ GLA University, Mathura · Building production-grade AWS infrastructure*

<img alt="Streak" src="https://streak-stats.demolab.com/?user=pranav-sre&hide_border=true&background=FFFFFF&stroke=0891B2&ring=7C3AED&fire=059669&currStreakLabel=0891B2&sideLabels=475569&currStreakNum=0F172A&sideNums=0F172A&dates=94A3B8&titleColor=0891B2&card_width=1180" />
<br/>
<img alt="Stats" src="https://github-readme-stats.vercel.app/api?username=pranav-sre&show_icons=true&include_all_commits=true&hide_rank=true&hide_border=true&title_color=0891B2&icon_color=7C3AED&text_color=0F172A&bg_color=FFFFFF&card_width=500" />
<img alt="Top languages" src="https://github-readme-stats.vercel.app/api/top-langs/?username=pranav-sre&layout=compact&langs_count=8&hide_border=true&title_color=0891B2&text_color=0F172A&bg_color=FFFFFF&card_width=500" />

</div>

## 👋 About me

I build cloud-native infrastructure and data pipelines on **AWS**, and I care about the boring-but-critical parts: automation, observability, security and cost. I'm working toward **Site Reliability Engineering** and experimenting with **Agentic AI** systems.

- 🔭 Building: production-grade AWS data platforms with Infrastructure as Code
- 🌱 Learning: Kubernetes (CKA), Terraform, Prometheus & Grafana
- 🎯 Preparing: AWS Solutions Architect Associate · Certified Kubernetes Administrator (CKA)
- 🏅 Certified: Microsoft Azure Fundamentals (AZ-900) · AWS Academy Cloud Foundations
- 📫 Reach me: pranavtiwari0813@gmail.com

## 🛠️ Tech stack

<div align="center">

<img src="https://skillicons.dev/icons?i=aws,azure,gcp,py,bash,java,linux,git,githubactions,docker,kubernetes,terraform,prometheus,grafana&perline=7&theme=light" />

</div>

| Area | Tools |
|---|---|
| **AWS** | S3 · Glue · Athena · CloudWatch · IAM · CloudFormation · SNS · EC2 · Lambda |
| **Languages** | Python (boto3, pandas, pyarrow) · SQL · Java · Bash |
| **DevOps** | Docker · GitHub Actions · Linux · Git · Kubernetes *(learning)* · Terraform *(learning)* |
| **Monitoring** | CloudWatch · Prometheus *(learning)* · Grafana *(learning)* |
| **AI / GenAI** | LangChain · LLM APIs · Agentic AI systems |
| **Concepts** | SRE · Medallion Architecture · ETL · IaC · CI/CD · Cloud Security |

## 🚀 Featured project: ZIPIT Data Lake

A production-style **AWS food-delivery data lake** with a Bronze → Silver → Gold medallion architecture.

- ⚙️ Python ETL (boto3, pandas, pyarrow): **87% storage reduction** via CSV → Parquet, schemas auto-registered in Glue
- 🔎 Serverless analytics on Athena: 8 BI queries on 10,000+ records at under ₹0.01 per query
- 📈 CloudWatch dashboard plus 4 SNS-triggered alarms for pipeline health
- 🔐 IAM least-privilege, AES-256 encryption, S3 versioning, Glacier lifecycle (**~80% long-term cost reduction**)
- 🧱 Entire stack deployed with **one CloudFormation CLI command**

👉 **[github.com/pranav-sre/zipit-data-lake](https://github.com/pranav-sre/zipit-data-lake)**

<div align="center">

<a href="https://github.com/pranav-sre?tab=repositories">
  <img alt="Projects" src="https://raw.githubusercontent.com/pranav-sre/pranav-sre/projects/projects.svg" />
</a>

</div>

## 🎓 Certifications

- Microsoft Certified: **Azure Fundamentals (AZ-900)**
- **AWS Academy Graduate**: Cloud Foundations
- Microsoft **AI Skills Fest 2026**
- **Deloitte** Technology Job Simulation (Forage): built a GitHub Actions CI/CD pipeline
- **Datacom** Intro to Cloud Job Simulation (Forage): deployed a cloud app via GitHub Actions
- **NPTEL (IIT)**: Software Engineering

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/pranav-sre/pranav-sre/output/snake-dark.svg">
  <img alt="Contribution snake" src="https://raw.githubusercontent.com/pranav-sre/pranav-sre/output/snake-light.svg">
</picture>

<br/><br/>

<a href="https://www.linkedin.com/in/pranav-tiwari-6209a1374"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0A101F?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0A101F"></a>
<a href="https://x.com/PranavTiwari013"><img alt="X" src="https://img.shields.io/badge/X-0A101F?style=for-the-badge&logo=x&logoColor=white&labelColor=0A101F"></a>
<a href="mailto:pranavtiwari0813@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-0A101F?style=for-the-badge&logo=gmail&logoColor=10B981&labelColor=0A101F"></a>

</div>
EOF

# ---------------- Banners ----------------
cat > light.svg <<'EOF'
<svg width="1180" height="240" viewBox="0 0 1180 240" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="g" x1="0" x2="1"><stop offset="0" stop-color="#0891B2"/><stop offset="1" stop-color="#7C3AED"/></linearGradient>
  </defs>
  <rect width="1180" height="240" fill="#FFFFFF"/>
  <rect x="0" y="0" width="1180" height="6" fill="url(#g)"/>
  <text x="590" y="110" text-anchor="middle" font-family="Segoe UI, Helvetica, Arial, sans-serif" font-size="68" font-weight="700" fill="url(#g)">Pranav Tiwari</text>
  <text x="590" y="158" text-anchor="middle" font-family="Segoe UI, Helvetica, Arial, sans-serif" font-size="24" fill="#475569">Cloud &amp; DevOps Engineer · SRE · Agentic AI</text>
  <text x="590" y="200" text-anchor="middle" font-family="Segoe UI, Helvetica, Arial, sans-serif" font-size="18" fill="#94A3B8">AWS · Terraform · Kubernetes · Python · CI/CD</text>
</svg>
EOF
sed -e 's/#FFFFFF/#0B1220/' -e 's/#475569/#CBD5E1/' -e 's/#94A3B8/#64748B/' light.svg > dark.svg

# ---------------- Projects data ----------------
cat > projects.json <<'EOF'
[
  {
    "name": "ZIPIT Data Lake",
    "desc": "Production AWS food-delivery data lake with a Bronze/Silver/Gold medallion architecture, 87% storage reduction via Parquet, and one-command CloudFormation deploys.",
    "tech": ["S3", "Glue", "Athena", "CloudWatch", "CloudFormation", "Python"],
    "url": "github.com/pranav-sre/zipit-data-lake"
  }
]
EOF

# ---------------- SVG generator ----------------
cat > scripts/generate_projects.py <<'EOF'
import json, os, textwrap
from xml.sax.saxutils import escape

projects = json.load(open("projects.json", encoding="utf-8"))
W, PAD, COLS, GAP, CH = 1180, 20, 3, 20, 210
cw = (W - 2 * PAD - (COLS - 1) * GAP) // COLS
rows = max(1, (len(projects) + COLS - 1) // COLS)
H = 70 + rows * CH + (rows - 1) * GAP + PAD

style = (
    ".card{fill:#F8FAFC;stroke:#E2E8F0}.t{fill:#0F172A}.m{fill:#475569}.a{fill:#0891B2}"
    "@media (prefers-color-scheme:dark){.card{fill:#0F172A;stroke:#1E293B}"
    ".t{fill:#F1F5F9}.m{fill:#94A3B8}.a{fill:#22D3EE}}"
    "text{font-family:'Segoe UI',Helvetica,Arial,sans-serif}"
)

out = [f'<svg width="{W}" height="{H}" viewBox="0 0 {W} {H}" xmlns="http://www.w3.org/2000/svg">',
       f"<style>{style}</style>",
       '<defs><linearGradient id="g" x1="0" x2="1"><stop offset="0" stop-color="#0891B2"/>'
       '<stop offset="1" stop-color="#7C3AED"/></linearGradient></defs>',
       f'<text x="{PAD}" y="42" font-size="24" font-weight="700" class="a">Featured Projects</text>']

for i, p in enumerate(projects):
    x = PAD + (i % COLS) * (cw + GAP)
    y = 64 + (i // COLS) * (CH + GAP)
    out.append(f'<rect x="{x}" y="{y}" width="{cw}" height="{CH}" rx="14" class="card"/>')
    out.append(f'<rect x="{x}" y="{y}" width="{cw}" height="5" rx="2" fill="url(#g)"/>')
    out.append(f'<text x="{x+20}" y="{y+40}" font-size="19" font-weight="700" class="t">{escape(p["name"])}</text>')
    for n, line in enumerate(textwrap.wrap(p.get("desc", ""), 46)[:4]):
        out.append(f'<text x="{x+20}" y="{y+68+n*20}" font-size="13.5" class="m">{escape(line)}</text>')
    tech = " · ".join(p.get("tech", []))
    for n, line in enumerate(textwrap.wrap(tech, 50)[:2]):
        out.append(f'<text x="{x+20}" y="{y+CH-56+n*18}" font-size="13" font-weight="600" class="a">{escape(line)}</text>')
    out.append(f'<text x="{x+20}" y="{y+CH-16}" font-size="12" class="m">{escape(p.get("url",""))}</text>')

out.append("</svg>")
os.makedirs("dist", exist_ok=True)
open("dist/projects.svg", "w", encoding="utf-8").write("\n".join(out))
print("Wrote dist/projects.svg")
EOF

# ---------------- Workflows ----------------
cat > .github/workflows/snake.yml <<'EOF'
name: Generate Snake
on:
  schedule:
    - cron: "0 */12 * * *"
  workflow_dispatch:
  push:
    branches: [main]
permissions:
  contents: write
jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/snake-light.svg?palette=github-light
            dist/snake-dark.svg?palette=github-dark
      - uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
EOF

cat > .github/workflows/projects.yml <<'EOF'
name: Projects Card
on:
  push:
    branches: [main]
    paths: [projects.json, scripts/generate_projects.py]
  workflow_dispatch:
permissions:
  contents: write
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: python scripts/generate_projects.py
      - uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: projects
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
EOF

echo "✅ All files created. Now: git add . && git commit -m 'profile' && git push"
