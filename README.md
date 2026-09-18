pranav-sre-profile/.github/workflows/snake.yml (+30 -0)
     1 +name: Generate contribution snake
     2 +
     3 +on:
     4 +  schedule:
     5 +    - cron: "0 0 * * *"
     6 +  workflow_dispatch:
     7 +  push:
     8 +    branches: [main]
     9 +
    10 +permissions:
    11 +  contents: write
    12 +
    13 +jobs:
    14 +  generate:
    15 +    runs-on: ubuntu-latest
    16 +    steps:
    17 +      - name: Generate snake SVGs
    18 +        uses: Platane/snk/svg-only@v3
    19 +        with:
    20 +          github_user_name: pranav-sre
    21 +          outputs: |
    22 +            dist/snake-light.svg?palette=github-light
    23 +            dist/snake-dark.svg?palette=github-dark
    24 +      - name: Publish to output branch
    25 +        uses: crazy-max/ghaction-github-pages@v4
    26 +        with:
    27 +          target_branch: output
    28 +          build_dir: dist
    29 +        env:
    30 +          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

  └ pranav-sre-profile/README.md (+97 -0)
     1 +<!-- Copy this repository's contents into https://github.com/pranav-sre/pranav-sre -->
     2 +
     3 +<picture>
     4 +  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/pranav-sre/pranav-sre/main/dark.svg">
     5 +  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/pranav-sre/pranav-sre/main/light.svg">
     6 +  <img width="100%" alt="Pranav Tiwari — Site Reliability Engineer" src="https://raw.githubusercontent.com/pranav-sre/pranav-sre/main/light.svg">
     7 +</picture>
     8 +
     9 +<p align="center">
    10 +  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=2800&pause=850&color=38BDF8&center=true&vCenter=true&width=650
        &lines=Building+reliable+systems+from+the+ground+up;Automating+the+path+from+code+to+cloud;Learning+in+public+%7C+Shipping+with+intent" alt="Animated introducti
        on" />
    11 +</p>
    12 +
    13 +<p align="center">
    14 +  <a href="https://www.linkedin.com/in/pranav-tiwari-6209a1374"><img src="https://img.shields.io/badge/LinkedIn-0A101F?style=for-the-badge&logo=linkedin&logoCol
        or=38BDF8" alt="LinkedIn"></a>
    15 +  <a href="https://x.com/PranavTiwari013"><img src="https://img.shields.io/badge/X-0A101F?style=for-the-badge&logo=x&logoColor=E2E8F0" alt="X"></a>
    16 +  <a href="mailto:pranavtiwari0813@gmail.com"><img src="https://img.shields.io/badge/Email-0A101F?style=for-the-badge&logo=gmail&logoColor=F87171" alt="Email"><
        /a>
    17 +</p>
    18 +
    19 +<br>
    20 +
    21 +## `> about_me`
    22 +
    23 +```yaml
    24 +name: Pranav Tiwari
    25 +role: Aspiring Site Reliability Engineer
    26 +focus:
    27 +  - cloud infrastructure
    28 +  - CI/CD automation
    29 +  - observability and resilient systems
    30 +currently_learning: [AWS, Azure, Go, platform engineering]
    31 +```
    32 +
    33 +I enjoy making systems easier to operate: automating repetitive work, making
    34 +deployments predictable, and using monitoring to turn uncertainty into signals.
    35 +
    36 +## `> technology_stack`
    37 +
    38 +<p align="center">
    39 +  <img src="https://img.shields.io/badge/Python-0A101F?style=for-the-badge&logo=python&logoColor=FFD43B" alt="Python">
    40 +  <img src="https://img.shields.io/badge/Go-0A101F?style=for-the-badge&logo=go&logoColor=00ADD8" alt="Go">
    41 +  <img src="https://img.shields.io/badge/Java-0A101F?style=for-the-badge&logo=openjdk&logoColor=F89820" alt="Java">
    42 +  <img src="https://img.shields.io/badge/Linux-0A101F?style=for-the-badge&logo=linux&logoColor=FCC624" alt="Linux">
    43 +</p>
    44 +<p align="center">
    45 +  <img src="https://img.shields.io/badge/AWS-0A101F?style=for-the-badge&logo=amazonaws&logoColor=FF9900" alt="AWS">
    46 +  <img src="https://img.shields.io/badge/Azure-0A101F?style=for-the-badge&logo=microsoftazure&logoColor=38BDF8" alt="Azure">
    47 +  <img src="https://img.shields.io/badge/Docker-0A101F?style=for-the-badge&logo=docker&logoColor=2496ED" alt="Docker">
    48 +</p>
    49 +<p align="center">
    50 +  <img src="https://img.shields.io/badge/Jenkins-0A101F?style=for-the-badge&logo=jenkins&logoColor=D24939" alt="Jenkins">
    51 +  <img src="https://img.shields.io/badge/GitLab_CI-0A101F?style=for-the-badge&logo=gitlab&logoColor=FC6D26" alt="GitLab CI">
    52 +  <img src="https://img.shields.io/badge/GitHub_Actions-0A101F?style=for-the-badge&logo=githubactions&logoColor=2088FF" alt="GitHub Actions">
    53 +  <img src="https://img.shields.io/badge/CI%2FCD-0A101F?style=for-the-badge&logo=github&logoColor=22C55E" alt="CI/CD pipelines">
    54 +</p>
    55 +
    56 +## `> featured_build`
    57 +
    58 +<table>
    59 +  <tr>
    60 +    <td width="72%">
    61 +      <h3>🌊 ZIPIT — Food Delivery Data Lake</h3>
    62 +      <p>A production-grade AWS data lake that processes <b>5,000+ food-delivery orders</b> across seven Indian cities.</p>
    63 +      <p><code>Python</code> <code>boto3</code> <code>Amazon S3</code> <code>Glue</code> <code>Athena</code> <code>CloudWatch</code> <code>CloudFormation</code>
        </p>
    64 +      <ul>
    65 +        <li>Medallion data architecture: Bronze → Silver → Gold</li>
    66 +        <li>Converts raw CSV data to Parquet, reducing storage footprint by 87%</li>
    67 +        <li>Provides eight Athena business-insight queries and CloudWatch monitoring</li>
    68 +        <li>Deployable through CloudFormation on the AWS Free Tier</li>
    69 +      </ul>
    70 +      <a href="https://github.com/pranav-sre/zipit-data-lake"><img src="https://img.shields.io/badge/Explore_the_project-38BDF8?style=for-the-badge&logo=github&
        logoColor=0A101F" alt="Explore ZIPIT Data Lake"></a>
    71 +    </td>
    72 +    <td width="28%" align="center">
    73 +      <img src="https://github-readme-stats.vercel.app/api/pin/?username=pranav-sre&repo=zipit-data-lake&hide_border=true&bg_color=0A101F&title_color=38BDF8&tex
        t_color=CBD5E1&icon_color=A78BFA" alt="ZIPIT repository card">
    74 +    </td>
    75 +  </tr>
    76 +</table>
    77 +
    78 +## `> github_pulse`
    79 +
    80 +<p align="center">
    81 +  <img width="100%" src="https://streak-stats.demolab.com?user=pranav-sre&hide_border=true&background=0A101F&ring=38BDF8&fire=A78BFA&currStreakLabel=38BDF8&side
        Labels=94A3B8&currStreakNum=F8FAFC&sideNums=F8FAFC&dates=64748B&card_width=950" alt="GitHub contribution streak">
    82 +</p>
    83 +
    84 +<p align="center">
    85 +  <img width="49%" src="https://github-readme-stats.vercel.app/api?username=pranav-sre&show_icons=true&hide_rank=true&hide_border=true&title_color=38BDF8&icon_c
        olor=A78BFA&text_color=94A3B8&bg_color=0A101F" alt="GitHub statistics">
    86 +  <img width="49%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=pranav-sre&layout=compact&hide_border=true&title_color=38BDF8&text_color=
        94A3B8&bg_color=0A101F" alt="Top languages">
    87 +</p>
    88 +
    89 +## `> contribution_graph`
    90 +
    91 +<picture>
    92 +  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/pranav-sre/pranav-sre/output/snake-dark.svg">
    93 +  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/pranav-sre/pranav-sre/output/snake-light.svg">
    94 +  <img width="100%" alt="Animated contribution snake" src="https://raw.githubusercontent.com/pranav-sre/pranav-sre/output/snake-light.svg">
    95 +</picture>
    96 +
    97 +<p align="center"><i>Reliable systems are built one small, observable improvement at a time.</i></p>

  └ pranav-sre-profile/dark.svg (+17 -0)
     1 +<svg xmlns="http://www.w3.org/2000/svg" width="1200" height="310" viewBox="0 0 1200 310" role="img" aria-labelledby="title desc">
     2 +  <title id="title">Pranav Tiwari, aspiring Site Reliability Engineer</title>
     3 +  <desc id="desc">Dark themed profile banner</desc>
     4 +  <defs>
     5 +    <linearGradient id="g" x1="0" x2="1" y1="0" y2="1"><stop stop-color="#08111f"/><stop offset="1" stop-color="#11112a"/></linearGradient>
     6 +    <pattern id="grid" width="38" height="38" patternUnits="userSpaceOnUse"><path d="M38 0H0V38" fill="none" stroke="#334155" stroke-opacity=".55"/></pattern>
     7 +  </defs>
     8 +  <rect width="1200" height="310" rx="20" fill="url(#g)"/>
     9 +  <rect width="1200" height="310" rx="20" fill="url(#grid)"/>
    10 +  <circle cx="1045" cy="58" r="118" fill="#22d3ee" fill-opacity=".13"/><circle cx="1110" cy="250" r="145" fill="#a78bfa" fill-opacity=".13"/>
    11 +  <g fill="none" stroke="#22d3ee" stroke-width="2" stroke-opacity=".65"><path d="M875 95h110l34 34h105"/><path d="M900 203h85l32-32h114"/><path d="M1035 70v62"/
        ></g>
    12 +  <g fill="#22d3ee"><circle cx="875" cy="95" r="6"/><circle cx="1124" cy="129" r="6"/><circle cx="900" cy="203" r="6"/><circle cx="1131" cy="171" r="6"/></g>
    13 +  <text x="78" y="104" fill="#94a3b8" font-family="ui-monospace, SFMono-Regular, Menlo, monospace" font-size="18" letter-spacing="3">HELLO, WORLD_</text>
    14 +  <text x="78" y="165" fill="#f8fafc" font-family="Arial, sans-serif" font-size="53" font-weight="700">Pranav Tiwari</text>
    15 +  <text x="80" y="211" fill="#22d3ee" font-family="ui-monospace, SFMono-Regular, Menlo, monospace" font-size="21">ASPIRING SITE RELIABILITY ENGINEER</text>
    16 +  <g font-family="ui-monospace, SFMono-Regular, Menlo, monospace" font-size="15" fill="#94a3b8"><text x="80" y="260">cloud</text><text x="178" y="260">•</text><
        text x="203" y="260">automation</text><text x="335" y="260">•</text><text x="360" y="260">observability</text></g>
    17 +</svg>

  └ pranav-sre-profile/light.svg (+17 -0)
     1 +<svg xmlns="http://www.w3.org/2000/svg" width="1200" height="310" viewBox="0 0 1200 310" role="img" aria-labelledby="title desc">
     2 +  <title id="title">Pranav Tiwari, aspiring Site Reliability Engineer</title>
     3 +  <desc id="desc">Light themed profile banner</desc>
     4 +  <defs>
     5 +    <linearGradient id="g" x1="0" x2="1" y1="0" y2="1"><stop stop-color="#eff6ff"/><stop offset="1" stop-color="#f5f3ff"/></linearGradient>
     6 +    <pattern id="grid" width="38" height="38" patternUnits="userSpaceOnUse"><path d="M38 0H0V38" fill="none" stroke="#cbd5e1" stroke-opacity=".45"/></pattern>
     7 +  </defs>
     8 +  <rect width="1200" height="310" rx="20" fill="url(#g)"/>
     9 +  <rect width="1200" height="310" rx="20" fill="url(#grid)"/>
    10 +  <circle cx="1045" cy="58" r="118" fill="#38bdf8" fill-opacity=".14"/><circle cx="1110" cy="250" r="145" fill="#a78bfa" fill-opacity=".12"/>
    11 +  <g fill="none" stroke="#0284c7" stroke-width="2" stroke-opacity=".55"><path d="M875 95h110l34 34h105"/><path d="M900 203h85l32-32h114"/><path d="M1035 70v62"/
        ></g>
    12 +  <g fill="#0284c7"><circle cx="875" cy="95" r="6"/><circle cx="1124" cy="129" r="6"/><circle cx="900" cy="203" r="6"/><circle cx="1131" cy="171" r="6"/></g>
    13 +  <text x="78" y="104" fill="#0f172a" font-family="ui-monospace, SFMono-Regular, Menlo, monospace" font-size="18" letter-spacing="3">HELLO, WORLD_</text>
    14 +  <text x="78" y="165" fill="#0f172a" font-family="Arial, sans-serif" font-size="53" font-weight="700">Pranav Tiwari</text>
    15 +  <text x="80" y="211" fill="#0369a1" font-family="ui-monospace, SFMono-Regular, Menlo, monospace" font-size="21">ASPIRING SITE RELIABILITY ENGINEER</text>
    16 +  <g font-family="ui-monospace, SFMono-Regular, Menlo, monospace" font-size="15" fill="#475569"><text x="80" y="260">cloud</text><text x="178" y="260">•</text><
        text x="203" y="260">automation</text><text x="335" y="260">•</text><text x="360" y="260">observability</text></g>
    17 +</svg>

• Edited pranav-sre-profile/README.md (+12 -3)
    80  <p align="center">
    81 -  <img width="100%" src="https://streak-stats.demolab.com?user=pranav-sre&hide_border=true&background=0A101F&ring=38BDF8&fire=A78BFA&currStreakLabel=38BDF8&side
        Labels=94A3B8&currStreakNum=F8FAFC&sideNums=F8FAFC&dates=64748B&card_width=950" alt="GitHub contribution streak">
    81 +  <picture>
    82 +    <source media="(prefers-color-scheme: dark)" srcset="https://streak-stats.demolab.com?user=pranav-sre&hide_border=true&background=0A101F&ring=38BDF8&fire=A7
        8BFA&currStreakLabel=38BDF8&sideLabels=94A3B8&currStreakNum=F8FAFC&sideNums=F8FAFC&dates=64748B&card_width=950">
    83 +    <img width="100%" src="https://streak-stats.demolab.com?user=pranav-sre&hide_border=true&background=FFFFFF&ring=0284C7&fire=7C3AED&currStreakLabel=0284C7&si
        deLabels=475569&currStreakNum=0F172A&sideNums=0F172A&dates=64748B&card_width=950" alt="GitHub contribution streak">
    84 +  </picture>
    85  </p>
       ⋮
    87  <p align="center">
    85 -  <img width="49%" src="https://github-readme-stats.vercel.app/api?username=pranav-sre&show_icons=true&hide_rank=true&hide_border=true&title_color=38BDF8&icon_c
        olor=A78BFA&text_color=94A3B8&bg_color=0A101F" alt="GitHub statistics">
    86 -  <img width="49%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=pranav-sre&layout=compact&hide_border=true&title_color=38BDF8&text_color=
        94A3B8&bg_color=0A101F" alt="Top languages">
    88 +  <picture>
    89 +    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api?username=pranav-sre&show_icons=true&hide_rank=true&hide_bord
        er=true&title_color=38BDF8&icon_color=A78BFA&text_color=94A3B8&bg_color=0A101F">
    90 +    <img width="49%" src="https://github-readme-stats.vercel.app/api?username=pranav-sre&show_icons=true&hide_rank=true&hide_border=true&title_color=0284C7&icon
        _color=7C3AED&text_color=475569&bg_color=FFFFFF" alt="GitHub statistics">
    91 +  </picture>
    92 +  <picture>
    93 +    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=pranav-sre&layout=compact&hide_border=tr
        ue&title_color=38BDF8&text_color=94A3B8&bg_color=0A101F">
    94 +    <img width="49%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=pranav-sre&layout=compact&hide_border=true&title_color=0284C7&text_colo
        r=475569&bg_color=FFFFFF" alt="Top languages">
    95 +  </picture>
    96  </p>

