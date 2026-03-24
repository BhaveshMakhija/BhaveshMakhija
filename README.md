<div align="center">

<!-- ═══════════════════════════════════════════════════════════ -->
<!--           HEADER SVG — native SVG animate only             -->
<!-- ═══════════════════════════════════════════════════════════ -->

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 280" width="100%">
  <defs>
    <linearGradient id="bg" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#0D1117"/>
      <stop offset="100%" stop-color="#0f0a20"/>
    </linearGradient>
    <linearGradient id="gline" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%"   stop-color="#7c3aed" stop-opacity="0"/>
      <stop offset="50%"  stop-color="#a78bfa" stop-opacity="1"/>
      <stop offset="100%" stop-color="#7c3aed" stop-opacity="0"/>
    </linearGradient>
    <filter id="glow">
      <feGaussianBlur stdDeviation="3.5" result="b"/>
      <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <filter id="sglow">
      <feGaussianBlur stdDeviation="7" result="b"/>
      <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <pattern id="dots" x="0" y="0" width="28" height="28" patternUnits="userSpaceOnUse">
      <circle cx="14" cy="14" r="0.9" fill="#a78bfa"/>
    </pattern>
  </defs>

  <!-- Background -->
  <rect width="900" height="280" fill="url(#bg)"/>
  <rect width="900" height="280" fill="url(#dots)" opacity=".06"/>

  <!-- Scanline sweep -->
  <rect x="0" y="0" width="900" height="8" fill="#a78bfa" opacity=".04">
    <animateTransform attributeName="transform" type="translate" from="0,0" to="0,290" dur="5s" repeatCount="indefinite"/>
  </rect>

  <!-- LEFT neural net — lines -->
  <g filter="url(#glow)" opacity=".65">
    <line x1="58" y1="82"  x2="108" y2="128" stroke="#7c3aed" stroke-width=".8" stroke-dasharray="4 3"/>
    <line x1="58" y1="158" x2="108" y2="128" stroke="#7c3aed" stroke-width=".8" stroke-dasharray="4 3"/>
    <line x1="58" y1="122" x2="108" y2="162" stroke="#7c3aed" stroke-width=".8" stroke-dasharray="4 3"/>
    <line x1="58" y1="198" x2="108" y2="162" stroke="#7c3aed" stroke-width=".8" stroke-dasharray="4 3"/>
    <line x1="108" y1="128" x2="152" y2="145" stroke="#a78bfa" stroke-width="1"/>
    <line x1="108" y1="162" x2="152" y2="145" stroke="#a78bfa" stroke-width="1"/>

    <!-- Pulsing nodes — layer 1 -->
    <circle cx="58" cy="82" fill="#7c3aed">
      <animate attributeName="r" values="3;5;3" dur="2.4s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.35;1;0.35" dur="2.4s" repeatCount="indefinite"/>
    </circle>
    <circle cx="58" cy="122" fill="#7c3aed">
      <animate attributeName="r" values="3;5;3" dur="2.4s" begin="0.8s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.35;1;0.35" dur="2.4s" begin="0.8s" repeatCount="indefinite"/>
    </circle>
    <circle cx="58" cy="158" fill="#7c3aed">
      <animate attributeName="r" values="3;5;3" dur="2.4s" begin="1.6s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.35;1;0.35" dur="2.4s" begin="1.6s" repeatCount="indefinite"/>
    </circle>
    <circle cx="58" cy="198" fill="#7c3aed">
      <animate attributeName="r" values="3;5;3" dur="2.4s" begin="0.4s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.35;1;0.35" dur="2.4s" begin="0.4s" repeatCount="indefinite"/>
    </circle>

    <!-- Layer 2 -->
    <circle cx="108" cy="128" fill="#a78bfa">
      <animate attributeName="r" values="3;5;3" dur="2.4s" begin="1.2s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.35;1;0.35" dur="2.4s" begin="1.2s" repeatCount="indefinite"/>
    </circle>
    <circle cx="108" cy="162" fill="#a78bfa">
      <animate attributeName="r" values="3;5;3" dur="2.4s" begin="0.3s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.35;1;0.35" dur="2.4s" begin="0.3s" repeatCount="indefinite"/>
    </circle>

    <!-- Output node -->
    <circle cx="152" cy="145" r="4" fill="#c4b5fd">
      <animate attributeName="opacity" values="0.5;1;0.5" dur="1.8s" repeatCount="indefinite"/>
    </circle>
  </g>

  <!-- RIGHT neural net — lines -->
  <g filter="url(#glow)" opacity=".65">
    <line x1="842" y1="82"  x2="792" y2="128" stroke="#7c3aed" stroke-width=".8" stroke-dasharray="4 3"/>
    <line x1="842" y1="158" x2="792" y2="128" stroke="#7c3aed" stroke-width=".8" stroke-dasharray="4 3"/>
    <line x1="842" y1="122" x2="792" y2="162" stroke="#7c3aed" stroke-width=".8" stroke-dasharray="4 3"/>
    <line x1="842" y1="198" x2="792" y2="162" stroke="#7c3aed" stroke-width=".8" stroke-dasharray="4 3"/>
    <line x1="792" y1="128" x2="748" y2="145" stroke="#a78bfa" stroke-width="1"/>
    <line x1="792" y1="162" x2="748" y2="145" stroke="#a78bfa" stroke-width="1"/>

    <circle cx="842" cy="82" fill="#7c3aed">
      <animate attributeName="r" values="3;5;3" dur="2.4s" begin="1.6s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.35;1;0.35" dur="2.4s" begin="1.6s" repeatCount="indefinite"/>
    </circle>
    <circle cx="842" cy="122" fill="#7c3aed">
      <animate attributeName="r" values="3;5;3" dur="2.4s" begin="0.4s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.35;1;0.35" dur="2.4s" begin="0.4s" repeatCount="indefinite"/>
    </circle>
    <circle cx="842" cy="158" fill="#7c3aed">
      <animate attributeName="r" values="3;5;3" dur="2.4s" begin="1.0s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.35;1;0.35" dur="2.4s" begin="1.0s" repeatCount="indefinite"/>
    </circle>
    <circle cx="842" cy="198" fill="#7c3aed">
      <animate attributeName="r" values="3;5;3" dur="2.4s" begin="2.0s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.35;1;0.35" dur="2.4s" begin="2.0s" repeatCount="indefinite"/>
    </circle>
    <circle cx="792" cy="128" fill="#a78bfa">
      <animate attributeName="r" values="3;5;3" dur="2.4s" begin="0.6s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.35;1;0.35" dur="2.4s" begin="0.6s" repeatCount="indefinite"/>
    </circle>
    <circle cx="792" cy="162" fill="#a78bfa">
      <animate attributeName="r" values="3;5;3" dur="2.4s" begin="1.4s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.35;1;0.35" dur="2.4s" begin="1.4s" repeatCount="indefinite"/>
    </circle>
    <circle cx="748" cy="145" r="4" fill="#c4b5fd">
      <animate attributeName="opacity" values="0.5;1;0.5" dur="1.8s" begin="0.9s" repeatCount="indefinite"/>
    </circle>
  </g>

  <!-- Glow divider line -->
  <rect x="0" y="139" width="900" height="1" fill="url(#gline)" opacity=".45"/>

  <!-- Terminal prompt -->
  <text x="450" y="72" font-family="'JetBrains Mono',monospace" font-size="12" fill="#4a3a6e" text-anchor="middle">
    ▸  initializing  profile.py ...
    <animate attributeName="opacity" values="0;1" dur="0.5s" begin="0.1s" fill="freeze"/>
  </text>

  <!-- Name -->
  <text x="450" y="128" font-family="'JetBrains Mono',monospace" font-size="44" font-weight="700" fill="#ffffff" text-anchor="middle" letter-spacing="2" filter="url(#sglow)">
    Bhavesh Makhija
    <animate attributeName="opacity" values="0;1" dur="0.6s" begin="0.4s" fill="freeze"/>
  </text>

  <!-- Underline accent -->
  <rect x="285" y="136" width="330" height="2" rx="1" fill="url(#gline)">
    <animate attributeName="opacity" values="0;1" dur="0.5s" begin="0.6s" fill="freeze"/>
  </rect>

  <!-- Role -->
  <text x="450" y="166" font-family="'JetBrains Mono',monospace" font-size="14.5" fill="#a78bfa" text-anchor="middle" letter-spacing="1">
    AI/ML Engineer  ·  RAG Systems  ·  Full-Stack GenAI
    <animate attributeName="opacity" values="0;1" dur="0.5s" begin="0.8s" fill="freeze"/>
  </text>

  <!-- Pill tags -->
  <g>
    <animate attributeName="opacity" values="0;1" dur="0.5s" begin="1.0s" fill="freeze"/>
    <rect x="220" y="184" width="88"  height="21" rx="10.5" fill="#130a2e" stroke="#5b21b6" stroke-width=".8"/>
    <text x="264" y="199" font-family="monospace" font-size="10.5" fill="#c4b5fd" text-anchor="middle">LangChain</text>
    <rect x="316" y="184" width="62"  height="21" rx="10.5" fill="#130a2e" stroke="#5b21b6" stroke-width=".8"/>
    <text x="347" y="199" font-family="monospace" font-size="10.5" fill="#c4b5fd" text-anchor="middle">FastAPI</text>
    <rect x="386" y="184" width="50"  height="21" rx="10.5" fill="#130a2e" stroke="#5b21b6" stroke-width=".8"/>
    <text x="411" y="199" font-family="monospace" font-size="10.5" fill="#c4b5fd" text-anchor="middle">FAISS</text>
    <rect x="444" y="184" width="56"  height="21" rx="10.5" fill="#130a2e" stroke="#5b21b6" stroke-width=".8"/>
    <text x="472" y="199" font-family="monospace" font-size="10.5" fill="#c4b5fd" text-anchor="middle">RAGAS</text>
    <rect x="508" y="184" width="60"  height="21" rx="10.5" fill="#130a2e" stroke="#5b21b6" stroke-width=".8"/>
    <text x="538" y="199" font-family="monospace" font-size="10.5" fill="#c4b5fd" text-anchor="middle">Ollama</text>
    <rect x="576" y="184" width="90"  height="21" rx="10.5" fill="#130a2e" stroke="#5b21b6" stroke-width=".8"/>
    <text x="621" y="199" font-family="monospace" font-size="10.5" fill="#c4b5fd" text-anchor="middle">HuggingFace</text>
  </g>

  <!-- Status + blinking cursor -->
  <text x="438" y="248" font-family="'JetBrains Mono',monospace" font-size="11.5" fill="#3d3160" text-anchor="middle">
    Pune, Maharashtra  ·  Open to AI/ML Engineering roles
    <animate attributeName="opacity" values="0;1" dur="0.5s" begin="1.3s" fill="freeze"/>
  </text>
  <text x="672" y="248" font-family="monospace" font-size="13" fill="#7c3aed">
    ▋
    <animate attributeName="opacity" values="1;0;1" dur="1s" repeatCount="indefinite"/>
  </text>
</svg>

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/bhavesh-makhija)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:bhavesh60000@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/BhaveshMakhija)
[![Profile Views](https://komarev.com/ghpvc/?username=BhaveshMakhija&style=for-the-badge&color=7c3aed&label=PROFILE+VIEWS)](https://github.com/BhaveshMakhija)

</div>

---

## 🧠 About Me

<div align="center">

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 860 212" width="96%">
  <defs>
    <linearGradient id="tbg" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#0d1117"/>
      <stop offset="100%" stop-color="#090d14"/>
    </linearGradient>
  </defs>

  <!-- Window -->
  <rect width="860" height="212" fill="url(#tbg)" rx="10"/>
  <rect width="860" height="212" fill="none" stroke="#1e1535" stroke-width="1" rx="10"/>

  <!-- Title bar -->
  <rect x="0" y="0" width="860" height="30" fill="#100a22" rx="10"/>
  <rect x="0" y="20" width="860" height="10" fill="#100a22"/>
  <circle cx="20" cy="15" r="4.5" fill="#ff5f57" opacity=".9"/>
  <circle cx="38" cy="15" r="4.5" fill="#febc2e" opacity=".9"/>
  <circle cx="56" cy="15" r="4.5" fill="#28c840" opacity=".9"/>
  <text x="430" y="20" font-family="monospace" font-size="10.5" fill="#4a3a6e" text-anchor="middle">bhavesh.py — ~/profile</text>

  <!-- Line numbers -->
  <g font-family="'JetBrains Mono','Courier New',monospace" font-size="12.5" fill="#2e2450">
    <text x="24" y="58">1</text>
    <text x="24" y="75">2</text>
    <text x="24" y="92">3</text>
    <text x="24" y="109">4</text>
    <text x="24" y="126">5</text>
    <text x="24" y="143">6</text>
    <text x="24" y="160">7</text>
    <text x="24" y="177">8</text>
    <text x="24" y="194">9</text>
  </g>

  <!-- Active line highlight -->
  <rect x="44" y="181" width="772" height="16" fill="#a78bfa" opacity=".05" rx="2"/>

  <!-- Code lines — fade in sequentially -->
  <g font-family="'JetBrains Mono','Courier New',monospace" font-size="12.5">

    <g opacity="0">
      <animate attributeName="opacity" values="0;1" dur="0.3s" begin="0.1s" fill="freeze"/>
      <text x="48" y="58" fill="#c4b5fd">bhavesh</text>
      <text x="132" y="58" fill="#94a3b8"> = {</text>
    </g>

    <g opacity="0">
      <animate attributeName="opacity" values="0;1" dur="0.3s" begin="0.5s" fill="freeze"/>
      <text x="48" y="75" fill="#64748b">    "role"      :</text>
      <text x="206" y="75" fill="#86efac"> "AI/ML Engineer · Full-Stack GenAI Developer"</text>
      <text x="622" y="75" fill="#64748b">,</text>
    </g>

    <g opacity="0">
      <animate attributeName="opacity" values="0;1" dur="0.3s" begin="0.9s" fill="freeze"/>
      <text x="48" y="92" fill="#64748b">    "location"  :</text>
      <text x="206" y="92" fill="#86efac"> "Pune, Maharashtra"</text>
      <text x="364" y="92" fill="#64748b">,</text>
    </g>

    <g opacity="0">
      <animate attributeName="opacity" values="0;1" dur="0.3s" begin="1.3s" fill="freeze"/>
      <text x="48" y="109" fill="#64748b">    "education" :</text>
      <text x="206" y="109" fill="#86efac"> "B.E. AI &amp; Data Science — CGPA 7.92/10"</text>
      <text x="582" y="109" fill="#64748b">,</text>
    </g>

    <g opacity="0">
      <animate attributeName="opacity" values="0;1" dur="0.3s" begin="1.7s" fill="freeze"/>
      <text x="48" y="126" fill="#64748b">    "focus"     :</text>
      <text x="206" y="126" fill="#fbbf24"> ["RAG", "LLM Eval", "Vector Search", "Doc Intelligence"]</text>
      <text x="697" y="126" fill="#64748b">,</text>
    </g>

    <g opacity="0">
      <animate attributeName="opacity" values="0;1" dur="0.3s" begin="2.1s" fill="freeze"/>
      <text x="48" y="143" fill="#64748b">    "stack"     :</text>
      <text x="206" y="143" fill="#fbbf24"> ["Python", "FastAPI", "LangChain", "FAISS", "React"]</text>
      <text x="672" y="143" fill="#64748b">,</text>
    </g>

    <g opacity="0">
      <animate attributeName="opacity" values="0;1" dur="0.3s" begin="2.5s" fill="freeze"/>
      <text x="48" y="160" fill="#64748b">    "currently" :</text>
      <text x="206" y="160" fill="#86efac"> "Production AI pipelines &amp; LLM applications"</text>
      <text x="617" y="160" fill="#64748b">,</text>
    </g>

    <g opacity="0">
      <animate attributeName="opacity" values="0;1" dur="0.3s" begin="2.9s" fill="freeze"/>
      <text x="48" y="177" fill="#64748b">    "open_to"   :</text>
      <text x="206" y="177" fill="#86efac"> "AI/ML · GenAI · NLP · RAG Systems roles"</text>
      <text x="588" y="177" fill="#64748b">,</text>
    </g>

    <g opacity="0">
      <animate attributeName="opacity" values="0;1" dur="0.3s" begin="3.2s" fill="freeze"/>
      <text x="48" y="194" fill="#94a3b8">}</text>
    </g>

    <!-- Blinking cursor -->
    <text x="66" y="194" font-size="14" fill="#7c3aed">
      ▋
      <animate attributeName="opacity" values="1;0;1" dur="1s" begin="3.3s" repeatCount="indefinite"/>
    </text>

  </g>
</svg>

</div>

---

## 🛠️ Tech Stack

<div align="center">

### 🤖 AI · ML · GenAI
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-F55036?style=for-the-badge&logo=groq&logoColor=white)

### 🔍 RAG · Vector Search · Evaluation
![FAISS](https://img.shields.io/badge/FAISS-0467DF?style=for-the-badge&logo=meta&logoColor=white)
![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?style=for-the-badge&logo=elasticsearch&logoColor=white)
![BM25](https://img.shields.io/badge/BM25_Retrieval-6D28D9?style=for-the-badge&logoColor=white)
![RAGAS](https://img.shields.io/badge/RAGAS_Evaluation-10B981?style=for-the-badge&logoColor=white)

### 🏗️ Backend · APIs · Auth
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)

### 🎨 Frontend
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Framer](https://img.shields.io/badge/Framer_Motion-0055FF?style=for-the-badge&logo=framer&logoColor=white)

### 🗄️ Databases
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)

### ☁️ Cloud · DevOps · Tools
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=for-the-badge&logo=railway&logoColor=white)
![Camunda](https://img.shields.io/badge/Camunda_8-FC5D0D?style=for-the-badge&logo=camunda&logoColor=white)

</div>

---

## 📊 GitHub Stats

<div align="center">
  <img height="175em" src="https://github-readme-stats.vercel.app/api?username=BhaveshMakhija&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true&hide_border=true&bg_color=0D1117&title_color=A78BFA&icon_color=A78BFA&text_color=ffffff" />
  <img height="175em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=BhaveshMakhija&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=A78BFA&text_color=ffffff&langs_count=8" />
</div>

<div align="center">
  <img width="68%" src="https://github-readme-streak-stats.herokuapp.com/?user=BhaveshMakhija&theme=tokyonight&hide_border=true&background=0D1117&ring=A78BFA&fire=A78BFA&currStreakLabel=A78BFA" />
</div>

---

## 📈 Contribution Activity

<div align="center">
  <img width="100%" src="https://github-readme-activity-graph.vercel.app/graph?username=BhaveshMakhija&theme=tokyo-night&bg_color=0D1117&color=A78BFA&line=A78BFA&point=ffffff&area=true&hide_border=true" />
</div>

---

<!-- ═══════════════════════════════════════════════════════════ -->
<!--                     FOOTER SVG                             -->
<!-- ═══════════════════════════════════════════════════════════ -->

<div align="center">

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 64" width="100%">
  <defs>
    <linearGradient id="fg" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%"   stop-color="#7c3aed" stop-opacity="0"/>
      <stop offset="30%"  stop-color="#a78bfa" stop-opacity="1"/>
      <stop offset="70%"  stop-color="#a78bfa" stop-opacity="1"/>
      <stop offset="100%" stop-color="#7c3aed" stop-opacity="0"/>
    </linearGradient>
  </defs>
  <rect x="0" y="30" width="900" height="1" fill="url(#fg)" opacity=".4"/>
  <text x="450" y="22" font-family="'JetBrains Mono',monospace" font-size="12" fill="#4a3a6e" text-anchor="middle">Open to full-time opportunities · AI/ML · GenAI · RAG Systems</text>
  <text x="450" y="52" font-family="'JetBrains Mono',monospace" font-size="11" fill="#2e2450" text-anchor="middle">bhavesh60000@gmail.com  ·  linkedin.com/in/bhavesh-makhija</text>
  <text x="756" y="52" font-family="monospace" font-size="12" fill="#7c3aed">
    ▋
    <animate attributeName="opacity" values="1;0;1" dur="1.2s" repeatCount="indefinite"/>
  </text>
</svg>

</div>
