<div align="center">

# Mohit Chahal

**Lead Software Engineer · Backends and real-time systems**

6 years building software, 4 of them full-time. I design APIs, data models and real-time systems<br>
in Node.js, NestJS, PostgreSQL and Redis, and I lead the engineers who build on them.

<a href="https://mohitchahal.com/"><img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=astro&logoColor=white" alt="Portfolio: mohitchahal.com"></a>
<a href="https://www.linkedin.com/in/itsmohitchahal/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
<a href="mailto:contact@mohitchahal.com"><img src="https://img.shields.io/badge/Email-C14438?style=for-the-badge" alt="Email: contact@mohitchahal.com"></a>

</div>

<br>

## What I do

- **Lead engineering** at Innovizia Technologies across several projects at once: backend architecture, infrastructure planning, and design and code reviews for frontend and backend engineers
- **Build APIs that serve live production traffic**, then load-test them with simulated real users and go after the slow tail until the p95 and p99 come down
- **Ship the whole slice** when a project needs it: the schema, the API, the React and Next.js front-ends, Docker and the CI/CD pipeline

## Open source: Gym Ledger

<table>
<tr>
<td width="250" valign="top">
<a href="https://github.com/gym-ledger/web"><img src="https://raw.githubusercontent.com/gym-ledger/web/main/.github/assets/demo.gif" width="250" alt="Gym Ledger on a phone: home, progress, muscle map, body weight and logging a set"></a>
</td>
<td valign="top">

**A self-hostable workout tracker for lifters.** Log every set at the gym, even with no signal, follow and edit training plans, and watch your strength and body weight move over time.

- **Offline-first PWA:** sets logged without signal queue on the phone and sync in batches when the connection returns
- **Sessions done properly:** passwordless OTP, one session per device, refresh tokens that rotate on every use with reuse detection
- **Live notifications over SSE:** each stream lives no longer than its access token and closes the moment its session is signed out
- **Hardened API:** strict zod validation on every route, Redis-backed rate limits, a self-hosted proof-of-work CAPTCHA, an audit log of admin changes
- **Privacy built in:** data export, account deletion with a 30-day grace period, AI check-ins only on opt-in
- **Ops included:** one-command Docker stack, CI and deploys with GitHub Actions, encrypted nightly backups and an optional streaming standby

| | |
|---|---|
| [**gym-ledger/api**](https://github.com/gym-ledger/api) | The REST API · Express 5, TypeScript, PostgreSQL, Redis |
| [**gym-ledger/web**](https://github.com/gym-ledger/web) | The app people train with · Next.js 16, React 19, Tailwind CSS |
| [**gym-ledger/admin**](https://github.com/gym-ledger/admin) | The admin panel · exercise library, versioned program builder, analytics |

</td>
</tr>
</table>

## Building next: Restaurant OS

A multi-tenant platform for restaurant groups: one API serves the counter, the kitchen, online ordering and the people running the business. **Open-sourcing soon.**

- Offline-first point of sale: orders are saved on the device during service and synced in the background, so a dropped connection never loses a bill
- Kitchen and online-ordering APIs with real-time updates over WebSocket
- A self-hosted OpenStreetMap geocoder behind a gateway with per-project allowlists, so there are no paid map keys or quotas
- Load-tested with a simulated restaurant group (POS terminals going offline and back, kitchen screens, dashboards, QR ordering):

| Throughput | p95 latency | p99 latency |
|:---:|:---:|:---:|
| **100 req/s** | **27 ms** | **101 ms** |

<sub>On a 2 vCPU / 8 GB server that was also running two other live projects. Method: <a href="https://mohitchahal.com/#testing">how I load-test</a>.</sub>

## Stack

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=ts,nodejs,nestjs,express,postgres,prisma,redis,mongodb,docker,githubactions,cloudflare,linux,react,nextjs,tailwind,astro,js,py,git&perline=10&theme=dark">
  <img alt="TypeScript, Node.js, NestJS, Express, PostgreSQL, Prisma, Redis, MongoDB, Docker, GitHub Actions, Cloudflare, Linux, React, Next.js, Tailwind CSS, Astro, JavaScript, Python, Git" src="https://skillicons.dev/icons?i=ts,nodejs,nestjs,express,postgres,prisma,redis,mongodb,docker,githubactions,cloudflare,linux,react,nextjs,tailwind,astro,js,py,git&perline=10&theme=light">
</picture>

Also: Drizzle, Fastify, WebSocket, SSE, Zod.
