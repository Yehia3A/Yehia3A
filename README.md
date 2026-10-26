<div align="center">

<!-- HEADER BANNER -->
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:0a3d62,100:00f7ff&height=200&section=header&text=Yehia%20Fadly&fontSize=60&fontColor=ffffff&fontAlignY=38&desc=AI%20Engineer%20%40%20Digified&descSize=20&descAlignY=58&descColor=00f7ff&animation=twinkling" />

<!-- ANIMATED TITLE -->
<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=24&pause=1000&color=00F7FF&center=true&vCenter=true&width=750&lines=🧠+NLP+Researcher+%7C+SOTA+86.4%25+F1-Score;🤖+AI+Agents+%7C+Tool-Calling+%26+MCP+Servers;⚡+LLM+Engineer+%7C+LoRA+Fine-Tuning+%26+Prompt+Engineering;👁️+Computer+Vision+%7C+YOLOv12+%2B+DeepSORT;🛡️+AI+Security+%7C+CipherCloud+IAM+Analyzer;🚀+Building+AI+for+Real-World+Impact" alt="Typing SVG" />

<br/>

<!-- PROFILE BADGES -->
<a href="https://linkedin.com/in/yehia-fadly">
  <img src="https://img.shields.io/badge/LinkedIn-Yehia_Fadly-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>
<a href="mailto:yehia.fadly@gmail.com">
  <img src="https://img.shields.io/badge/Email-yehia.fadly@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/>
</a>
<a href="https://github.com/Yehia3A">
  <img src="https://img.shields.io/badge/GitHub-Yehia3A-181717?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<br/><br/>

<!-- PROFILE VIEWS & FOLLOWERS -->
<img src="https://komarev.com/ghpvc/?username=Yehia3A&label=Profile+Views&color=00f7ff&style=flat-square" />
&nbsp;
<img src="https://img.shields.io/github/followers/Yehia3A?label=Followers&style=flat-square&color=00f7ff" />

</div>

---

## ⚡ About Me

```python
class YehiaFadly:
    role        = "AI Engineer"
    company     = "Digified"
    location    = "Cairo, Egypt 🇪🇬"
    education   = "B.Sc. Data Science, Minor: Software Engineering, GIU (2022–2026)"

    focus       = [
        "AI Agents, Tool-Calling & MCP",
        "LLM Fine-Tuning & Alignment",
        "NLP Research (Low-Resource & Code-Switched)",
        "Computer Vision & Object Tracking",
        "AI Security & Cloud Intelligence",
        "Full-Stack AI Systems"
    ]

    goal        = "Build AI that creates measurable, real-world impact"
```

---

## 💼 Experience

**AI Engineer · [Digified](https://digified.io)** *(2026 – Present)*

---

## 🏆 Research & Engineering Highlights

<div align="center">

| 🔬 Domain | 🚀 Achievement | 📊 Impact |
|-----------|---------------|-----------|
| **NLP Research** | SOTA Arabic-English Code-Switched NER | **86.4% F1**, beats CAMELBERT (79.2%) |
| **AI Agents** | **ExpenseAgent**: LLM tool-calling expense tracker + MCP server | Live multi-user app, **$0/month**, **270** automated tests |
| **LLM Engineering** | Fine-tuned `facebook/opt-1.3b` with **LoRA** | Deployed IAM policy auditor on Hugging Face Spaces |
| **Computer Vision** | **YOLOv12** + **DeepSORT** tracking pipeline | Real-time traffic sign detection on video streams |
| **AI Security** | 50,000-entry synthetic security dataset | Automated least-privilege IAM policy generation |
| **Full-Stack AI** | LMS with HuggingFace recommendation engine | End-to-end course personalization for students |

</div>

---

## 🔬 Featured Projects

<details>
<summary><b>🧠 Code-Switched Arabic-English NER — Bachelor Thesis (SOTA Research)</b></summary>
<br/>

> Achieved **State-of-the-Art 86.4% F1-score** on Arabic-English mixed-script Named Entity Recognition, surpassing CAMELBERT (79.2%) and Ensemble methods (81.7%).

**Key Engineering Contributions:**
- Designed a novel **3-phase training pipeline**: Targeted Data Augmentation → Intermediate Pre-training → Supervised Contrastive Loss
- Built a **Curriculum Learning** pipeline that orders training by sequence length & code-switching density
- Used `paraphrase-multilingual-MiniLM` for **embedding-based lexical augmentation** to resolve class imbalance for rare entities (ORG/MISC)
- Boosted Arabic-context accuracy by **+10.2%** by stabilizing low-resource embeddings

`PyTorch` `Transformers` `Contrastive Learning` `Curriculum Learning` `NLP` `HuggingFace`

</details>

<details>
<summary><b>💸 ExpenseAgent — AI Expense Tracker with Tool-Calling & MCP (Live)</b></summary>
<br/>

> Replaces the budgeting spreadsheet: type or say *"coffee 200, uber 85 yesterday"* and an LLM agent files each item, tracks budgets and builds monthly reports. Multi-user, live, and **free to run** on Cloudflare.
>
> 🌐 [**Live app**](https://expense-agent.let-apps.workers.dev) · 📦 [**Repository**](https://github.com/Yehia3A/expense-agent)

**Key Engineering Contributions:**
- Built an **LLM tool-calling agent** (Groq `gpt-oss-120b`) over 12 typed tools; the model only picks tools and fills arguments, while code computes every date and total, so numbers always match the database
- Designed **hybrid routing**: a regex fast path + learned merchant cache logs common entries with **no LLM call** (**0 false writes** on an 82-case eval), with automatic fallback to a smaller model on rate limits
- Exposed the same tools as an **MCP server**, so Claude Desktop / Claude Code can log and query expenses
- Added **voice input** (Whisper) with a hands-free **driving mode**, one-tap quick logging, custom categories, any currency and per-city time zones
- Secured a public multi-user app: per-account data isolation, hashed passwords, sessions, rate limits, CSRF guard and CSP, covered by **270 tests** and CI on GitHub Actions

`AI Agents` `Tool Calling` `MCP` `LLMs` `Groq` `Whisper` `TypeScript` `Cloudflare Workers` `D1 / SQLite` `Vitest`

</details>

<details>
<summary><b>🛡️ CipherCloud — AI-Powered AWS IAM Policy Analyzer</b></summary>
<br/>

> Automated cloud security auditing by fine-tuning an LLM to detect over-privileged IAM roles and generate **Least-Privilege** compliant alternatives.

**Key Engineering Contributions:**
- Fine-tuned `facebook/opt-1.3b` with **LoRA** (Hugging Face Optimum) to minimize memory footprint for low-latency inference
- Constructed a **50,000-entry JSON dataset** of paired Insecure/Secure IAM policies from scratch
- Deployed a production inference API on **Hugging Face Spaces** with strict JSON output enforcement via Prompt Engineering

`LLM Fine-Tuning` `LoRA` `AWS IAM` `Prompt Engineering` `FastAPI` `HuggingFace Spaces`

</details>

<details>
<summary><b>👁️ Real-Time Traffic Sign Detection — YOLOv12 + DeepSORT</b></summary>
<br/>

> End-to-end computer vision pipeline for traffic sign detection and tracking on live video streams.

- Trained **YOLOv12** on 3.5k images with data augmentation (mosaic, color-space adjustments)
- Integrated **DeepSORT** tracking to filter false positives and maintain object identity across frames
- Deployed inference on video data using **OpenCV**

`YOLOv12` `DeepSORT` `PyTorch` `Ultralytics` `OpenCV` `Computer Vision`

</details>

---

## 🧰 Tech Stack

<div align="center">

**🤖 AI / ML / DL**

<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white"/>
<img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white"/>
<img src="https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black"/>
<img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white"/>
<img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white"/>
<img src="https://img.shields.io/badge/YOLO-00FFFF?style=for-the-badge&logo=yolo&logoColor=black"/>
<img src="https://img.shields.io/badge/MCP-000000?style=for-the-badge&logo=anthropic&logoColor=white"/>

<br/><br/>

**💻 Languages**

<img src="https://skillicons.dev/icons?i=python,java,cpp,javascript,typescript,cs" />

<br/><br/>

**🌐 Frameworks & Backend**

<img src="https://skillicons.dev/icons?i=nextjs,nestjs,react,nodejs,express,fastapi,flutter,dotnet" />

<br/><br/>

**☁️ Cloud, Data & DevOps**

<img src="https://skillicons.dev/icons?i=aws,cloudflare,docker,kafka,git,github,githubactions,linux" />
<br/>
<img src="https://skillicons.dev/icons?i=mongodb,mysql,postgres,sqlite" />
&nbsp;
<img src="https://img.shields.io/badge/Cassandra-1287B1?style=for-the-badge&logo=apachecassandra&logoColor=white"/>
<img src="https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black"/>

</div>

---

## 🎓 Education

**German International University (GIU)**, Cairo, Egypt

🎓 B.Sc. Data Science | Minor: Software Engineering *(2022 – 2026, Graduated)*

Relevant Coursework: Machine learning · Deep Learning · Database Systems Design · Statistical Analysis · Cloud Computing (AWS) · Data Structures & Algorithms · Software Architecture · Calculus I & II · Project Management

---

## 🌍 Languages

🇬🇧 English — Fluent &nbsp;&nbsp;|&nbsp;&nbsp; 🇸🇦 Arabic — Native &nbsp;&nbsp;|&nbsp;&nbsp; 🇷🇺 Russian — Beginner   

---

<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:00f7ff,50:0a3d62,100:0d1117&height=120&section=footer"/>

</div>
