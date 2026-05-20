<div align="center">

<svg viewBox="0 0 960 300" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <pattern id="dots" x="0" y="0" width="36" height="36" patternUnits="userSpaceOnUse">
      <circle cx="18" cy="18" r="0.9" fill="#CC0000" opacity="0.10"/>
    </pattern>
    <pattern id="scanlines" x="0" y="0" width="960" height="3" patternUnits="userSpaceOnUse">
      <rect x="0" y="0" width="960" height="1" fill="#000000" opacity="0.18"/>
    </pattern>
    <filter id="redglow" x="-8%" y="-40%" width="116%" height="180%">
      <feGaussianBlur in="SourceGraphic" stdDeviation="7" result="blur_outer"/>
      <feColorMatrix in="blur_outer" type="matrix"
        values="1 0 0 0 0.8  0 0 0 0 0  0 0 0 0 0  0 0 0 0.85 0" result="glow_outer"/>
      <feGaussianBlur in="SourceGraphic" stdDeviation="2.5" result="blur_inner"/>
      <feColorMatrix in="blur_inner" type="matrix"
        values="1 0 0 0 0.95  0 0 0 0 0  0 0 0 0 0  0 0 0 1 0" result="glow_inner"/>
      <feMerge>
        <feMergeNode in="glow_outer"/>
        <feMergeNode in="glow_inner"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
    <filter id="subtleglow" x="-5%" y="-60%" width="110%" height="220%">
      <feGaussianBlur in="SourceGraphic" stdDeviation="3" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
    <!-- Red → White → Red gradient: hot white core bleeding into brand red -->
    <linearGradient id="asciiGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#7a0000"/>
      <stop offset="18%"  stop-color="#CC0000"/>
      <stop offset="36%"  stop-color="#FF5555"/>
      <stop offset="50%"  stop-color="#FFFFFF"/>
      <stop offset="64%"  stop-color="#FF5555"/>
      <stop offset="82%"  stop-color="#CC0000"/>
      <stop offset="100%" stop-color="#7a0000"/>
    </linearGradient>
    <linearGradient id="borderGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#CC0000" stop-opacity="0.0"/>
      <stop offset="20%"  stop-color="#CC0000" stop-opacity="0.6"/>
      <stop offset="50%"  stop-color="#FF1C1C" stop-opacity="0.9"/>
      <stop offset="80%"  stop-color="#CC0000" stop-opacity="0.6"/>
      <stop offset="100%" stop-color="#CC0000" stop-opacity="0.0"/>
    </linearGradient>
    <linearGradient id="whiteGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#ffffff" stop-opacity="0.0"/>
      <stop offset="30%"  stop-color="#ffffff" stop-opacity="0.7"/>
      <stop offset="50%"  stop-color="#ffffff" stop-opacity="0.9"/>
      <stop offset="70%"  stop-color="#ffffff" stop-opacity="0.7"/>
      <stop offset="100%" stop-color="#ffffff" stop-opacity="0.0"/>
    </linearGradient>
  </defs>

  <!-- Base layers -->
  <rect width="960" height="300" fill="#0a0a0a"/>
  <rect width="960" height="300" fill="url(#dots)"/>
  <rect width="960" height="300" fill="url(#scanlines)"/>

  <!-- Outer border -->
  <rect x="2" y="2" width="956" height="296" fill="none" stroke="url(#borderGrad)" stroke-width="1.2"/>

  <!-- Corner brackets -->
  <polyline points="2,30 2,2 30,2"       fill="none" stroke="#CC0000" stroke-width="2.5" opacity="0.9"/>
  <polyline points="930,2 958,2 958,30"   fill="none" stroke="#CC0000" stroke-width="2.5" opacity="0.9"/>
  <polyline points="2,270 2,298 30,298"   fill="none" stroke="#CC0000" stroke-width="2.5" opacity="0.9"/>
  <polyline points="930,298 958,298 958,270" fill="none" stroke="#CC0000" stroke-width="2.5" opacity="0.9"/>
  <circle cx="2"   cy="2"   r="2.5" fill="#CC0000" opacity="0.95"/>
  <circle cx="958" cy="2"   r="2.5" fill="#CC0000" opacity="0.95"/>
  <circle cx="2"   cy="298" r="2.5" fill="#CC0000" opacity="0.95"/>
  <circle cx="958" cy="298" r="2.5" fill="#CC0000" opacity="0.95"/>

  <!-- Top label -->
  <text x="480" y="22" text-anchor="middle"
        font-family="'Courier New', Courier, monospace" font-size="9"
        fill="#CC0000" letter-spacing="5" opacity="0.65">
    ◈  RAPTOR LABS HQ  ◈  IRELAND BASED · WORLDWIDE OPERATIONAL  ◈
  </text>

  <!-- ASCII art — red glow layer -->
  <text font-family="'Courier New', Courier, monospace" font-size="11.6"
        fill="#CC0000" filter="url(#redglow)"
        text-anchor="middle" xml:space="preserve" opacity="0.6">
    <tspan x="480" y="82">██████╗  █████╗ ██████╗ ████████╗ ██████╗ ██████╗     ██╗      █████╗ ██████╗ ███████╗</tspan>
    <tspan x="480" dy="17">██╔══██╗██╔══██╗██╔══██╗╚══██╔══╝██╔═══██╗██╔══██╗    ██║     ██╔══██╗██╔══██╗██╔════╝</tspan>
    <tspan x="480" dy="17">██████╔╝███████║██████╔╝   ██║   ██║   ██║██████╔╝    ██║     ███████║██████╔╝███████╗</tspan>
    <tspan x="480" dy="17">██╔══██╗██╔══██║██╔═══╝    ██║   ██║   ██║██╔══██╗    ██║     ██╔══██║██╔══██╗╚════██║</tspan>
    <tspan x="480" dy="17">██║  ██║██║  ██║██║        ██║   ╚██████╔╝██║  ██║    ███████╗██║  ██║██████╔╝███████║</tspan>
    <tspan x="480" dy="17">╚═╝  ╚═╝╚═╝  ╚═╝╚═╝        ╚═╝    ╚═════╝ ╚═╝  ╚═╝    ╚══════╝╚═╝  ╚═╝╚═════╝ ╚══════╝</tspan>
  </text>

  <!-- ASCII art — sharp white-to-red gradient layer on top -->
  <text font-family="'Courier New', Courier, monospace" font-size="11.6"
        fill="url(#asciiGrad)"
        text-anchor="middle" xml:space="preserve">
    <tspan x="480" y="82">██████╗  █████╗ ██████╗ ████████╗ ██████╗ ██████╗     ██╗      █████╗ ██████╗ ███████╗</tspan>
    <tspan x="480" dy="17">██╔══██╗██╔══██╗██╔══██╗╚══██╔══╝██╔═══██╗██╔══██╗    ██║     ██╔══██╗██╔══██╗██╔════╝</tspan>
    <tspan x="480" dy="17">██████╔╝███████║██████╔╝   ██║   ██║   ██║██████╔╝    ██║     ███████║██████╔╝███████╗</tspan>
    <tspan x="480" dy="17">██╔══██╗██╔══██║██╔═══╝    ██║   ██║   ██║██╔══██╗    ██║     ██╔══██║██╔══██╗╚════██║</tspan>
    <tspan x="480" dy="17">██║  ██║██║  ██║██║        ██║   ╚██████╔╝██║  ██║    ███████╗██║  ██║██████╔╝███████║</tspan>
    <tspan x="480" dy="17">╚═╝  ╚═╝╚═╝  ╚═╝╚═╝        ╚═╝    ╚═════╝ ╚═╝  ╚═╝    ╚══════╝╚═╝  ╚═╝╚═════╝ ╚══════╝</tspan>
  </text>

  <!-- Divider -->
  <line x1="80" y1="213" x2="880" y2="213" stroke="url(#borderGrad)" stroke-width="0.8"/>

  <!-- Tagline -->
  <text x="480" y="236" text-anchor="middle"
        font-family="'Courier New', Courier, monospace" font-size="12.5"
        fill="url(#whiteGrad)" letter-spacing="6" opacity="0.92"
        filter="url(#subtleglow)">
    AGENTIC AI ENGINEERING AT PREDATOR SPEED
  </text>

  <!-- Bottom divider -->
  <line x1="80" y1="252" x2="880" y2="252" stroke="url(#borderGrad)" stroke-width="0.6"/>

  <!-- Footer meta -->
  <text x="300" y="272" text-anchor="middle"
        font-family="'Courier New', Courier, monospace" font-size="9.5"
        fill="#CC0000" letter-spacing="3" opacity="0.8">raptorlabs.dev</text>
  <text x="480" y="272" text-anchor="middle"
        font-family="'Courier New', Courier, monospace" font-size="9.5"
        fill="#444444" letter-spacing="1">◆</text>
  <text x="660" y="272" text-anchor="middle"
        font-family="'Courier New', Courier, monospace" font-size="9.5"
        fill="#888888" letter-spacing="3" opacity="0.75">IRELAND · WORLDWIDE</text>
</svg>

<br/>

<img src="https://img.shields.io/badge/AGENTIC_AI-ENGINEERING-CC0000?style=for-the-badge&labelColor=0a0a0a" />
<img src="https://img.shields.io/badge/PREDATOR-SPEED-CC0000?style=for-the-badge&labelColor=0a0a0a" />
<img src="https://img.shields.io/badge/FULLY-AGENTIC-CC0000?style=for-the-badge&labelColor=0a0a0a" />

<br/><br/>

<img src="https://img.shields.io/badge/Status-ACTIVE-CC0000?style=flat-square&labelColor=0a0a0a" />
<img src="https://img.shields.io/badge/Agents-DEPLOYED-CC0000?style=flat-square&labelColor=0a0a0a" />
<img src="https://img.shields.io/badge/MVPs-SHIPPING_IN_DAYS-CC0000?style=flat-square&labelColor=0a0a0a" />
<img src="https://img.shields.io/badge/Base-Ireland_🇮🇪-CC0000?style=flat-square&labelColor=0a0a0a" />
<img src="https://img.shields.io/badge/Reach-Worldwide_🌍-CC0000?style=flat-square&labelColor=0a0a0a" />

</div>

---

<div align="center">

```
╔══════════════════════════════════════════════════════════════════════════╗
║   🦖  Autonomous agents that build, deploy & scale at predator speed    ║
║        Ireland based  ·  Worldwide operational  ·  Always building      ║
╚══════════════════════════════════════════════════════════════════════════╝
```

</div>

## 🎯 Mission Statement

> **"Agentic AI engineering at predator speed. Autonomous agents ship enterprise-grade software and launch MVPs in days, scale to millions."**

At **Raptor Labs**, we are a fully agentic business — autonomous AI agents handle the heavy engineering while our team runs hackathons and drives open-source innovation. We don't just write code; we deploy agents that write it for us — faster, smarter, and without compromise. Ireland based. Worldwide operational.

---

## 🔴 What We Do

### 🤖 Agentic AI Engineering

- ⚡ **Autonomous AI Agents** — Agents that design, code, test, and deploy end-to-end
- 🚀 **Rapid MVP Delivery** — From validated idea to live product in days, not months
- 🏗️ **Enterprise-Grade Architecture** — Scalable from day one. Built to handle millions
- 🔁 **Agentic Workflows** — Fully automated engineering pipelines, no hand-holding required
- 🌐 **Web Application Development** — High-performance platforms engineered at predator speed

### 🛠️ Our Products

<div align="center">

| Product | Description | Status |
|---------|-------------|--------|
| 🦖 **[raptor-code](https://github.com/RaptorLabsHQ/raptor-code)** | Agentic Coding CLI — terminal-native AI engineering co-pilot | 🔴 Active |
| ⚡ **More incoming** | We build fast. Star this repo and watch this space. | 🔜 Soon |

</div>

### 💼 Engineering Services

```yaml
Agentic AI Development:
  - Autonomous agent design & deployment
  - Agentic workflow architecture & orchestration
  - AI inference, fine-tuning & MLOps pipelines
  - LLM integration across OpenAI, Anthropic, Google AI

Rapid Product Engineering:
  - MVP development — days, not months
  - Full-stack web application builds
  - API design, REST & GraphQL implementation
  - SaaS product architecture & launch

Enterprise Solutions:
  - Scalable cloud-native architecture
  - CI/CD automation & DevSecOps
  - Blockchain & Web3 integrations
  - Performance optimization & infrastructure review

Open Source & Community:
  - Developer tooling, CLIs & SDKs
  - Hackathon-bred innovations
  - Community-first open source contributions
```

---

## 🦖 raptor-code — Flagship Product

<div align="center">

```
╔══════════════════════════════════════════════════════════════════════╗
║  🔴  raptor-code  ·  Agentic Coding CLI App                         ║
║      Your terminal. Supercharged by autonomous AI agents.           ║
╚══════════════════════════════════════════════════════════════════════╝
```

</div>

**raptor-code** is an agentic coding CLI that brings the full power of autonomous AI engineering directly into your terminal. It doesn't autocomplete — it plans, architects, executes, and ships.

```bash
# Clone and set up raptor-code
git clone https://github.com/RaptorLabsHQ/raptor-code.git
cd raptor-code
npm install
npm run build

# Unleash the raptor
raptor-code run
```

> 📌 Full documentation, usage guide, and examples inside [`raptor-code`](https://github.com/RaptorLabsHQ/raptor-code).

---

## ⚡ Technical DNA

<div align="center">

**— AI & Intelligence —**

![OpenAI](https://img.shields.io/badge/OpenAI-0a0a0a?style=for-the-badge&logo=openai&logoColor=CC0000)
![Anthropic](https://img.shields.io/badge/Anthropic-CC0000?style=for-the-badge&labelColor=0a0a0a&logoColor=white)
![Google AI](https://img.shields.io/badge/Google_AI-0a0a0a?style=for-the-badge&logo=google&logoColor=CC0000)
![HuggingFace](https://img.shields.io/badge/HuggingFace-0a0a0a?style=for-the-badge&logo=huggingface&logoColor=CC0000)

**— Developer Environment & Tooling —**

![Warp](https://img.shields.io/badge/Warp.dev-CC0000?style=for-the-badge&labelColor=0a0a0a&logoColor=white)
![Linux](https://img.shields.io/badge/Linux_Native_Ops-0a0a0a?style=for-the-badge&logo=linux&logoColor=CC0000)
![Docker](https://img.shields.io/badge/Docker-0a0a0a?style=for-the-badge&logo=docker&logoColor=CC0000)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-0a0a0a?style=for-the-badge&logo=githubactions&logoColor=CC0000)

**— Languages —**

![Rust](https://img.shields.io/badge/Rust-0a0a0a?style=for-the-badge&logo=rust&logoColor=CC0000)
![Python](https://img.shields.io/badge/Python-0a0a0a?style=for-the-badge&logo=python&logoColor=CC0000)
![TypeScript](https://img.shields.io/badge/TypeScript-0a0a0a?style=for-the-badge&logo=typescript&logoColor=CC0000)
![PHP](https://img.shields.io/badge/PHP-0a0a0a?style=for-the-badge&logo=php&logoColor=CC0000)
![Solidity](https://img.shields.io/badge/Solidity-0a0a0a?style=for-the-badge&logo=solidity&logoColor=CC0000)

**— Infrastructure & Cloud —**

![DigitalOcean](https://img.shields.io/badge/DigitalOcean-0a0a0a?style=for-the-badge&logo=digitalocean&logoColor=CC0000)
![Render](https://img.shields.io/badge/Render.com-0a0a0a?style=for-the-badge&logo=render&logoColor=CC0000)
![Cloudflare](https://img.shields.io/badge/Cloudflare-0a0a0a?style=for-the-badge&logo=cloudflare&logoColor=CC0000)
![Kubernetes](https://img.shields.io/badge/Kubernetes-0a0a0a?style=for-the-badge&logo=kubernetes&logoColor=CC0000)

**— Web3 & Blockchain —**

![Web3](https://img.shields.io/badge/Web3-0a0a0a?style=for-the-badge&logo=web3.js&logoColor=CC0000)
![Blockchain](https://img.shields.io/badge/Blockchain-CC0000?style=for-the-badge&labelColor=0a0a0a)
![Ethereum](https://img.shields.io/badge/Ethereum-0a0a0a?style=for-the-badge&logo=ethereum&logoColor=CC0000)
![QuickNode](https://img.shields.io/badge/QuickNode-CC0000?style=for-the-badge&labelColor=0a0a0a)

**— Data & APIs —**

![GraphQL](https://img.shields.io/badge/GraphQL-0a0a0a?style=for-the-badge&logo=graphql&logoColor=CC0000)
![Redis](https://img.shields.io/badge/Redis-0a0a0a?style=for-the-badge&logo=redis&logoColor=CC0000)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-0a0a0a?style=for-the-badge&logo=postgresql&logoColor=CC0000)
![Supabase](https://img.shields.io/badge/Supabase-0a0a0a?style=for-the-badge&logo=supabase&logoColor=CC0000)

</div>

---

## 🤝 Contributing

Raptor Labs thrives on hackers, builders, and open-source contributors. If you move fast and care about craft — you belong here.

```bash
# 1. Fork the repository
# 2. Create your feature branch
git checkout -b feature/your-feature-name

# 3. Commit with clarity and intent
git commit -m "feat: describe what you built and why"

# 4. Push to your fork
git push origin feature/your-feature-name

# 5. Open a Pull Request — we review fast ⚡
```

We host hackathons, ship open source, and welcome contributors who treat speed as a core feature. See individual repository `CONTRIBUTING.md` files for project-specific guidelines.

---

## 🌐 Find Us Everywhere

<div align="center">

| Platform | Link |
|----------|------|
| 🌐 **Website** | [raptorlabs.dev](https://raptorlabs.dev) |
| 🐙 **GitHub** | [github.com/RaptorLabsHQ](https://github.com/RaptorLabsHQ) |
| 💼 **LinkedIn** | [linkedin.com/company/raptorlabs](https://www.linkedin.com/company/raptorlabs) |
| 🐦 **X / Twitter** | [@RaptorLabsX](https://x.com/RaptorLabsX) |
| 🚀 **F6S** | [f6s.com/raptorlabs](https://www.f6s.com/raptorlabs) |
| 📧 **Email** | [info@raptorlabs.dev](mailto:info@raptorlabs.dev) |

</div>

---

<div align="center">

<img src="https://img.shields.io/badge/BUILT_BY-AGENTS-CC0000?style=for-the-badge&labelColor=0a0a0a" />
<img src="https://img.shields.io/badge/SHIPPED_AT-PREDATOR_SPEED-CC0000?style=for-the-badge&labelColor=0a0a0a" />
<img src="https://img.shields.io/badge/IRELAND_BASED-WORLDWIDE_OPERATIONAL-CC0000?style=for-the-badge&labelColor=0a0a0a" />

<br/><br/>

**© 2025 Raptor Labs. All rights reserved.**

*Engineered by agents. Shipped at predator speed. Built to scale.*

</div>
