<div align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=26&duration=3000&pause=1000&color=4A9BC8&center=true&vCenter=true&width=700&lines=Hi,+I'm+Hun-Bot!;AI+×+Product+Engineer;Building+Interactive+AI+Experiences;Turning+Ideas+Into+Real+Products" alt="Typing SVG" />
</div>

<div align="center">
  <a href="https://hun-bot.dev/ko/">
    <img src="https://img.shields.io/badge/Tech%20Blog-hunbot.dev-orange?style=for-the-badge&logo=hashnode&logoColor=white" alt="Tech Blog" />
  </a>
  <a href="https://www.linkedin.com/in/hunbot-dev/">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
</div>

<br/>

<table>
  <tr>
    <td width="76%" valign="top">
      <h3>About Me</h3>
      <p>
        <b>"My best ideas come from my daily walks."</b>
      </p>
      <p>
        I am an engineer who finds inspiration in everyday life—whether it's language learning, stock markets, or finding better mobile plans—and turns them into working AI services. I don't limit myself to a single domain; if it's a problem I face, I build a solution.
      </p>
      <br/>
      <b>Origin of Ideas</b>
      My projects begin with a personal need.
      <ul>
        <li>Saw a language app ad but found features missing? <b>I built the extension.</b></li>
        <li>Wanted to grow assets without active management? <b>I engineered an AI trader.</b></li>
      </ul>
      <p>
      <b>I turn "I wish this existed" into deployed software.</b>
      </p>
    </td>
    <td width="24%" valign="top">
      <h3>Tech Stack</h3>
      <b>Languages</b><br/>
      <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white"/>
      <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
      <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
      <br/>
      <b>Frameworks</b><br/>
      <img src="https://img.shields.io/badge/Astro-BC52EE?style=flat-square&logo=astro&logoColor=white"/>
      <img src="https://img.shields.io/badge/gRPC-255F85?style=flat-square&logo=grpc&logoColor=white"/>
      <br/>
      <b>AI & Data</b><br/>
      <img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white"/>
      <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/>
      <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/>
      <br/>
      <b>Infra & Tools</b><br/>
      <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
      <img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white"/>
      <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white"/>
    </td>
  </tr>
</table>

<h3>Released & Operational</h3>

| Project | Description | Stack | Link |
| :--- | :--- | :--- | :--- |
| **[hunbot.dev](https://github.com/Hun-Bot2/hunbot.dev)** | **Engineering Blog with AI Pipeline**<br/>Static site with **Local AI** that auto-translates posts & commits via GitHub Actions. | `Astro` `Ollama` `Redis` | [Live ↗](https://hun-bot.dev) |
| **[Algo-Review Bot](https://github.com/Hun-Bot2/algo-review-bot)** | **Study Automation Agent**<br/>RAG-based problem recommender connecting Baekjoon & LeetCode. | `Go` `Python` `VectorDB` | [Code ↗](https://github.com/Hun-Bot2/algo-review-bot) |
| **[Local LLM Ops](https://github.com/Hun-Bot2/local-llm-observability)** | **MLOps Utility**<br/>Monitoring dashboard for the Local Ollama instance used in the blog pipeline. | `Grafana` `Python` | [Code ↗](https://github.com/Hun-Bot2/local-llm-observability) |
| **[BKGA Extension](https://github.com/Hun-Bot2/smart-korean-grammar-assistant)** | **VSCode Utility**<br/>Korean grammar checker for technical writing. | `TypeScript` | [Blog ↗](https://hun-bot.dev/ko/blog/devlog/vscode_extension/vscode_extension_01/) |

<br/>
<p align="center">
  👉 <b>For clear Architecture Images (PNG), please click the <a href="#released--operational">Blog</a> or <a href="#released--operational">Repo</a> links in the table above.</b>
</p>
<br/>

<details>
<summary><b>View System Architectures (Blog & Bots)</b></summary>

<br/>
<b>1. hunbot.dev (BlogOps Architecture)</b>

```mermaid
flowchart LR
    User -->|Access| CF[Cloudflare]
    CF --> Vercel[Vercel Edge]
    Vercel -->|Cache/View| Redis[Upstash Redis]
    
    subgraph Local Intelligence
    Runner[Self-Hosted Runner] -->|Inference| Ollama[Ollama LLM]
    Ollama -->|Translate & Commit| GH[GitHub]
    end
    
    GH -->|Trigger Deploy| Vercel
    Runner -.->|Metrics| Grafana[Grafana Dashboard]
```
</details>

<details>
<summary><b>View Algorithm Bot Architecture</b></summary>

<br/>

```mermaid
flowchart LR
    User(Solved Problem) -->|Trigger| Go[Go Backend]
    Go -->|gRPC| Py{Python AI Worker}
    Py -->|Embedding| DB[(Vector DB)]
    DB -->|Retrieve Similar| Py
    Py -->|RAG Response| Go
    Go -->|Notification| Slack[Slack Bot]
```

</details>

<h3> In Development</h3>

| Project | Description | Stack | Link |
| :--- | :--- | :--- | :--- |
| **JP Biz Coach** | **Japanese Communication AI**<br/>Business conversation & JLPT N1 speaking practice app. | `Go` `OpenAI` `TTS` | `🚧 Developing` |
| **Market Watcher** | **Multimodal Stock Trader**<br/>Analyzing Japanese market charts and news. | `Python` `Vision API` | `🚧 Developing` |
| **Add-on Dr.** | **Utility Service**<br/>Finding hidden carrier add-on services. | `Go` `Scraping` | `🚧 Developing` |
