<!-- styled:v2 -->
<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1d1726,50:167dfe,100:9533fa&height=180&section=header&text=Filevine%20Case%20Status%20%26%20Deadline%20Automation&fontSize=25&fontColor=ffffff&fontAlignY=36&desc=Case%20study%20%E2%80%A2%20Legal%20%E2%80%A2%20Node.js%20and%20n8n%20integration&descAlignY=58&descSize=16&animation=fadeIn" width="100%" alt="Filevine Case Status & Deadline Automation" />

**A Node.js webhook service and n8n workflow that turn every Filevine phase change into a plain-English client update by SMS and email.**

<p>
  <img src="https://img.shields.io/badge/Legal-167dfe?style=flat-square" alt="Legal" />
  <img src="https://img.shields.io/badge/Node.js%20and%20n8n%20integration-9533fa?style=flat-square" alt="Node.js and n8n integration" />
  <img src="https://img.shields.io/badge/Node.js-231f20?style=flat-square" alt="Node.js" />
  <img src="https://img.shields.io/badge/TypeScript-231f20?style=flat-square" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Filevine%20API-231f20?style=flat-square" alt="Filevine API" />
  <img src="https://img.shields.io/badge/n8n-231f20?style=flat-square" alt="n8n" />
  <img src="https://img.shields.io/badge/OpenAI-231f20?style=flat-square" alt="OpenAI" />
  <img src="https://img.shields.io/badge/Twilio%20SMS-231f20?style=flat-square" alt="Twilio SMS" />
</p>

<p>
  <a href="#overview">Overview</a> ·
  <a href="#how-it-works">How it works</a> ·
  <a href="#key-features">Key features</a> ·
  <a href="#results">Results</a> ·
  <a href="#screens">Screens</a> ·
  <a href="#tech-stack">Tech stack</a>
</p>

</div>

---

![n8n workflow that sends Filevine case status updates by SMS and email](assets/cover.webp)

## Overview

Keeping clients updated on case status took staff time and was easy to miss. We built a custom Node.js (TypeScript) webhook service triggered by Filevine phase changes, with n8n handling the messaging. Each phase is mapped to the right update, AI writes a plain-language message in the firm's tone, it is sent by SMS and email, and deadline tasks and an activity note are logged back in Filevine.

## The challenge

Clients called for updates, and staff had to remember to write and send a message every time a case moved forward.

## The solution

A TypeScript webhook service receives Filevine phase changes and maps them to update types. n8n routes each phase, AI writes the client message, Twilio and Gmail deliver it, and the result is logged on the case.

## How it works

```mermaid
flowchart LR
    A(["Filevine phase changes"]) --> B
    B["Phase mapped<br/>and routed"] --> C
    C["AI writes<br/>the update"] --> D
    D["Sent by SMS<br/>and email"] --> E
    E(["Logged on<br/>the case"])

    classDef box fill:#1d1726,stroke:#167dfe,color:#e5e7eb
    classDef ends fill:#2e1065,stroke:#9533fa,color:#ffffff
    class B,C,D box
    class A,E ends
```

1. **Filevine phase changes.** When a case moves phase in Filevine, a webhook calls the custom Node.js service.
2. **Phase mapped and routed.** The phase is mapped to an update type and routed: discovery, mediation or settlement.
3. **AI writes the update.** AI writes a plain-English update, a reminder or a closing letter in the firm's tone.
4. **Sent by SMS and email.** The message is delivered by Twilio SMS and Gmail at the same time.
5. **Logged on the case.** A note is posted back to Filevine so the team can see exactly what the client received.

## Key features

- Case phase mapped to the right update
- AI writes a plain-language message for the client
- Update sent by SMS and email
- Deadline tasks created in Filevine
- Activity logged back on the case

## Results

- Clients stay informed at every phase
- Fewer status calls to the office
- Every update recorded on the case

## Tech stack

![Node.js](https://img.shields.io/badge/Node.js-1d1726?style=for-the-badge) ![TypeScript](https://img.shields.io/badge/TypeScript-1d1726?style=for-the-badge) ![Filevine API](https://img.shields.io/badge/Filevine%20API-1d1726?style=for-the-badge) ![n8n](https://img.shields.io/badge/n8n-1d1726?style=for-the-badge) ![OpenAI](https://img.shields.io/badge/OpenAI-1d1726?style=for-the-badge) ![Twilio SMS](https://img.shields.io/badge/Twilio%20SMS-1d1726?style=for-the-badge) ![Gmail](https://img.shields.io/badge/Gmail-1d1726?style=for-the-badge)

## Screens

![How Filevine Case Status & Deadline Automation works: Filevine phase change, Node.js webhook service, AI writes the update, SMS and email sent, Note logged in Filevine](assets/screen-1.webp)

![Filevine Case Status & Deadline Automation: before and after](assets/screen-2.webp)

## Privacy

Client names and records are confidential. Every screen in this repository uses sample data, and source code that belongs to the client is not published.

## Links

- Case study on Lexvaxa: https://lexvaxa.com/work/filevine-case-status-automation

---

<div align="center">

**Built by [Ch Muhammad Samiullah](https://github.com/samiullah156-creator)** · AI Automation Engineer and Full-Stack Developer at [Lexvaxa](https://lexvaxa.com)

<a href="https://github.com/samiullah156-creator"><img src="https://img.shields.io/badge/More%20projects-181717?style=for-the-badge&logo=github&logoColor=white" alt="More projects" /></a>
<a href="https://lexvaxa.com/contact"><img src="https://img.shields.io/badge/Work%20with%20me-167dfe?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Work with me" /></a>
<a href="https://www.linkedin.com/in/sami-lexvaxa/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>

<sub>⭐ Star this repo if you found it useful</sub>

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:9533fa,50:167dfe,100:1d1726&height=110&section=footer" width="100%" alt="" />
