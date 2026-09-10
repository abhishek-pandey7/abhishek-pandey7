<!--
  Setup, once:
    1. Commit header.svg, otav.svg, stack.svg, linkedin.svg and mail.svg next to this file,
       at the repo root, in abhishek-pandey7/abhishek-pandey7
    2. If your default branch is "master", swap main -> master in the image URLs
    3. header-ascii.txt is a plain-text version of the header, if you ever
       want a code block instead of the animated SVG
-->

<p align="center">
  <img
    src="https://raw.githubusercontent.com/abhishek-pandey7/abhishek-pandey7/main/header.svg"
    width="900"
    alt="ASCII portrait of Abhishek Pandey beside a terminal readout: Software and AI Engineer, Mumbai, co-founder at Jireh Studios"
  />
</p>

<p align="center">
  <a href="https://github.com/abhishek-pandey7"><img src="https://cdn.simpleicons.org/github/f0b429" height="22" alt="github"/></a>
  &nbsp;&nbsp;<a href="https://www.linkedin.com/in/abhishek-pandey-409681332/"><img src="https://raw.githubusercontent.com/abhishek-pandey7/abhishek-pandey7/main/linkedin.svg" height="22" alt="linkedin"/></a>
  &nbsp;&nbsp;<a href="mailto:abhishekpandey.dev@yahoo.com"><img src="https://raw.githubusercontent.com/abhishek-pandey7/abhishek-pandey7/main/mail.svg" height="22" alt="mail"/></a>
  &nbsp;&nbsp;<a href="https://leetcode.com/u/abhishekp_7/"><img src="https://cdn.simpleicons.org/leetcode/f0b429" height="22" alt="leetcode"/></a>
</p>

A system that acts on your behalf should be able to say what it saw, what it decided, and why the next step followed from the last one. That is what the four things below have in common: an agent that narrates its own reasoning while it operates a desktop, a RAG pipeline that redacts before it retrieves, a benchmark harness that measures where long context actually fails, and a handful of production systems built for people who are not going to read the logs.

**01** [Experience](#experience) &nbsp;&nbsp;&middot;&nbsp;&nbsp; **02** [AURA](#aura), the featured build &nbsp;&nbsp;&middot;&nbsp;&nbsp; **03** [Other projects](#projects) &nbsp;&nbsp;&middot;&nbsp;&nbsp; **04** [Research](#research) &nbsp;&nbsp;&middot;&nbsp;&nbsp; **05** [Stack](#stack)

---

<a id="experience"></a>

## Experience

<table>
<tr>
<td width="190"><b>Jireh Studios</b><br/><sub>Co-Founder & Full Stack Engineer</sub></td>
<td>Architecting multi-tenant web platforms, serverless backend engines, and automated performance optimization pipelines. Two of the platforms below, MSAG and Sunzee Holidays, shipped out of this.</td>
</tr>
<tr>
<td><b>Global Pathway Solutions</b><br/><sub>SWE & AI Research Intern</sub></td>
<td>Prototyped hybrid OCR parsers, multi-model Socratic dialogue systems, and high-performance retrieval engines for EdTech platforms, under an Agile Scrum workflow.</td>
</tr>
<tr>
<td><b>DJ Init.AI</b><br/><sub>AI Research Mentee</sub></td>
<td>Built evaluation harnesses and studied long-context reasoning failure modes in frontier LLMs. Write-up under Research, below.</td>
</tr>
</table>

**B.Tech Information Technology**, DJ Sanghvi College of Engineering, Mumbai &nbsp;&middot;&nbsp; CGPA 9.155/10.0 &nbsp;&middot;&nbsp; expected May 2028

---

<a id="aura"></a>

## AURA
### Automated Realtime Assistant &nbsp;&middot;&nbsp; CLI-based autonomous desktop agent

Most agent demos work once, on the recorded run, at the recorded resolution. AURA is built around a loop instead of a script: it observes the screen, decides the next step, acts on the operating system, then checks whether that step actually worked before deciding the one after it. That loop is what lets it run unattended for hours and recover from its own mistakes mid-chain, rather than stalling the first time a button moves three pixels.

<p align="center">
  <img
    src="https://raw.githubusercontent.com/abhishek-pandey7/abhishek-pandey7/main/otav.svg"
    width="900"
    alt="Observe, Think, Act, Verify loop with a self-correct path back from Verify to Think"
  />
</p>

<table>
<tr><td width="190"><b>Desktop vision engine</b></td>
<td>Builds a live spatial coordinate map of UI elements and text with OpenCV and OCR, so the agent can navigate any application regardless of screen resolution.</td></tr>
<tr><td><b>Imitation learning</b></td>
<td>Listens to keyboard and mouse input through <code>pynput</code>, records organic user workflows, and synthesizes them into reusable PyAutoGUI macros with a vision-language model.</td></tr>
<tr><td><b>Browser automation</b></td>
<td>Drives headless and headed browser sessions with Playwright, carrying over Chrome profile cookies and session state to operate as an authenticated user.</td></tr>
<tr><td><b>Self-correction</b></td>
<td>Reads terminal stdout and stderr as it runs, debugs execution errors mid-chain, and keeps going without a human in the loop.</td></tr>
</table>

`Python` `Playwright` `PyAutoGUI` `OpenCV` `pynput` `VLM APIs` `OOD`

[repo &rarr;](https://github.com/abhishek-pandey7/AURA---Automated-Realtime-Assistant)

---

<a id="projects"></a>

## Other projects

<table>
<tr><td width="150"><b>Zero-Trust PII RAG</b></td>
<td>Redacts and masks PII locally with Microsoft Presidio and a thread-safe SQLite vault, before any text reaches an external LLM. Handles files past 1M characters.<br/>
<code>Python</code> <code>Flask</code> <code>LangChain</code> <code>ChromaDB</code> <code>SQLite</code> <code>Presidio</code><br/>
<a href="https://github.com/abhishek-pandey7/Zero-Trust-PII-RAG">repo</a> &middot; <a href="https://zero-trust-pii-rag.onrender.com/">live</a></td></tr>

<tr><td><b>Fluxion</b></td>
<td>Infrastructure-as-code generator that transpiles YAML specs into Snowflake SQL, dbt models, and Airflow DAGs, automating pipelines that would otherwise be written by hand.<br/>
<code>TypeScript</code> <code>React</code> <code>dbt</code> <code>Snowflake</code> <code>Airflow</code><br/>
<a href="https://github.com/abhishek-pandey7/Fluxion">repo</a> &middot; <a href="https://fluxion-lilac.vercel.app/">live</a></td></tr>

<tr><td><b>MSAG</b></td>
<td>Multi-tenant portal and public storefront for the Matti Sirviö Art Gallery, Muscat. Role-based JWT auth, a maker-checker audit workflow, and an on-the-fly WebP image proxy that cut load times 40%.<br/>
<code>Next.js 14</code> <code>React</code> <code>Express</code> <code>Prisma</code> <code>PostgreSQL</code> <code>Cloudflare R2</code><br/>
<a href="https://mattisirvioartgalleria.com/">live</a></td></tr>

<tr><td><b>OJAS</b></td>
<td>Objective judgement for academic sincerity: ranks exam-hall CCTV footage for human review instead of trying to auto-convict, with a signed custody ledger behind every verdict.<br/>
<code>Python</code> <code>Go</code> <code>Next.js</code> <code>OpenCV</code> <code>YOLOv8n</code> <code>Ed25519</code><br/>
<a href="https://github.com/abhishek-pandey7/Objective-Judgement-for-Academic-Security">repo</a></td></tr>

<tr><td><b>Sunzee Holidays</b></td>
<td>Travel platform for a B2B agency in Mauritius. Responsive exotic-luxury magazine design, custom marquees, parallax and scroll reveals, WhatsApp API booking.<br/>
<code>Next.js</code> <code>Tailwind CSS</code> <code>Framer Motion</code> <code>shadcn/ui</code></td></tr>

<tr><td><b>Football Advisor MAS</b></td>
<td>Multi-agent system on Google ADK coordinating specialist agents (input, scouting, tactics, finance) to answer natural-language football queries and suggest tactical counters.<br/>
<code>Google ADK</code> <code>React</code> <code>Python</code> <code>Gemini</code><br/>
<a href="https://github.com/abhishek-pandey7/Football-Advisor-MAS">repo</a></td></tr>

<tr><td><b>SpineIQ</b></td>
<td>Spinal rehab ecosystem tracking 33 skeletal landmarks in real time with MediaPipe Pose, streaming metrics over WebSocket at sub-30ms latency, with a clinical dashboard and a recovery chatbot.<br/>
<code>React</code> <code>FastAPI</code> <code>MediaPipe</code> <code>LangGraph</code> <code>Supabase</code> <code>Gemini</code><br/>
<a href="https://github.com/abhishek-pandey7/Spine-Guard">repo</a></td></tr>

<tr><td><b>PhishNet</b></td>
<td>Multi-modal security platform catching phishing emails via NLP and synthetic-voice deepfakes via audio feature analysis: MFCC variance, spectral flatness, zero-crossing rate.<br/>
<code>React</code> <code>FastAPI</code> <code>PyTorch</code> <code>HuggingFace</code> <code>Librosa</code></td></tr>

<tr><td><b>Reply Truman</b></td>
<td>Adaptive sender-profiling system built for the Reply Code Challenge. Fraud detection plus LLM reranking of suspicious activity, wired to Langfuse for observability.<br/>
<code>Python</code> <code>scikit-learn</code> <code>LangChain</code> <code>pandas</code> <code>Langfuse</code></td></tr>

<tr><td><b>CampusNav</b></td>
<td>Browser-based AR campus navigation overlaying directional cues on the live camera feed, using DeviceOrientation compass tracking, OSRM road routing, and spoken prompts.<br/>
<code>JavaScript</code> <code>HTML5/CSS3</code> <code>OSRM API</code> <code>Geolocation API</code><br/>
<a href="https://github.com/abhishek-pandey7/CampusNav">repo</a></td></tr>
</table>

---

<a id="research"></a>

## Research

### Position-aware benchmarking for long-context LLMs
*DJ Init.AI &middot; Nov 2025 to Jun 2026*

Standard benchmarks mostly score whether a long-context model gets the right answer, not where in the context the information it needed was sitting. I built a Python evaluation harness that benchmarked five frontier models across context windows from 32K to 1M tokens, varying only the position of the answer inside the window.

The result reproduced and quantified "lost in the middle": up to 30% accuracy degradation when the critical fact sits in the middle of a long context rather than at either end. The findings shaped inference-time mitigations and a Socratic prompting framework that the team carried forward.

---

<a id="stack"></a>

## Stack

<p align="center">
  <img
    src="https://raw.githubusercontent.com/abhishek-pandey7/abhishek-pandey7/main/stack.svg"
    width="900"
    alt="Stack: languages; web, data and cloud; ai, ml and vision; agentic, llm and tooling"
  />
</p>

No logo exists for the half that mattered most: the Observe/Think/Act/Verify loop itself, Presidio-based PII redaction ahead of retrieval, position-aware long-context evaluation, and Maker-Checker audit workflows.

---

## Reach me

|  |  |  |
| :-: | --- | --- |
| <img src="https://raw.githubusercontent.com/abhishek-pandey7/abhishek-pandey7/main/mail.svg" height="20" alt=""/> | **mail** | [abhishekpandey.dev@yahoo.com](mailto:abhishekpandey.dev@yahoo.com) |
| <img src="https://raw.githubusercontent.com/abhishek-pandey7/abhishek-pandey7/main/linkedin.svg" height="20" alt=""/> | **linkedin** | [/in/abhishek-pandey-409681332](https://www.linkedin.com/in/abhishek-pandey-409681332/) |
| <img src="https://cdn.simpleicons.org/github/f0b429" height="20" alt=""/> | **github** | [/abhishek-pandey7](https://github.com/abhishek-pandey7) |
| <img src="https://cdn.simpleicons.org/leetcode/f0b429" height="20" alt=""/> | **leetcode** | [/u/abhishekp_7](https://leetcode.com/u/abhishekp_7/) |

*Mumbai, India. Open to internships and collaborations, if you're building something ambitious.*
