<div align="center">

<img src="./assets/hero.svg" alt="Bootstrap Data — Own your first-party data. Govern it by default. Activate it everywhere." width="100%">

<br/>

<p align="center"><b>Bootstrap Data is the privacy-first control plane for first-party customer data.</b><br/>
One place to capture every signal your product emits, decide exactly what is allowed to flow — and&nbsp;where — then route it to your lakes, warehouses, and the tools your teams live in.<br/>
<b>Governed. Audited. Consent-aware.</b> By design, not by patch.</p>

<br/>

![Java](https://img.shields.io/badge/Java-21-7C3AED?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-4-8145EE?style=for-the-badge&logo=springboot&logoColor=white)
![React](https://img.shields.io/badge/React-Microfrontends-8B45F0?style=for-the-badge&logo=react&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-jsonb-9852F3?style=for-the-badge&logo=postgresql&logoColor=white)
![Keycloak](https://img.shields.io/badge/Auth-OIDC%20%2F%20OAuth2-A855F7?style=for-the-badge&logo=keycloak&logoColor=white)
![Privacy](https://img.shields.io/badge/Privacy-by%20Default-A855F7?style=for-the-badge&logo=shieldsdotio&logoColor=white)

</div>

<br/>

<h2 align="center">💡&nbsp;&nbsp;The problem we solve</h2>

<p align="justify">Every product is a firehose of first-party signals — taps, views, purchases, identities. That data is your most valuable asset <b>and</b> your biggest liability. Most teams are forced into an impossible trade-off:</p>

> Move fast and risk leaking PII, breaking consent, and losing the trust you spent years earning — **or** lock everything down and starve your growth, analytics, and activation teams of the data they need.

<p align="justify"><b>Bootstrap Data refuses that trade-off.</b> We make governance the <i>fast</i> path — so shipping data responsibly is easier than shipping it recklessly.</p>

<br/>

<h2 align="center">🌊&nbsp;&nbsp;The data journey</h2>

<p align="justify">From the moment an event is born to the moment it powers a campaign, every hop is deliberate, inspected, and logged.</p>

```mermaid
flowchart LR
    subgraph ingest["① INGEST"]
        src["Sources<br/>Android · iOS · JS<br/>Unity · Direct API"]
    end
    subgraph govern["② GOVERN"]
        pol["Propagation Policy<br/>Allow · Block · Omit"]
        match["Matchers<br/>PII / SPII detection"]
        consent["Consent Categories"]
    end
    subgraph store["③ STORE"]
        lake[("Data Lakes<br/>JSON · Parquet")]
        wh[("Warehouses<br/>Databricks")]
    end
    subgraph activate["④ ACTIVATE"]
        dst["Destinations<br/>Braze · Mixpanel"]
    end

    src ==> govern ==> store ==> activate
    match -.->|"gate"| dst
    consent -.->|"gate"| dst

    classDef stage fill:#7C3AED,stroke:#4C1D95,color:#fff;
    classDef data fill:#A855F7,stroke:#4C1D95,color:#fff;
    class src,pol,match,consent,dst stage;
    class lake,wh data;
```

<p align="justify"><b>①&nbsp;&nbsp;Ingest</b> &nbsp;—&nbsp; Register a <b>Source</b> for every channel — Android, iOS, JavaScript, Unity, Direct API — each with its own write key and configuration. Turn any product surface into a governed data stream in minutes.</p>

<p align="justify"><b>②&nbsp;&nbsp;Govern</b> &nbsp;—&nbsp; This is our heart. Every source carries a mandatory <b>Propagation Policy</b> that decides — per concern — whether to <b>Allow, Block, or Omit</b> unplanned events, unplanned attributes, schema violations, <b>PII</b>, and <b>SPII</b>. <b>Matchers</b> scan keys and values to classify sensitive data automatically, and <b>Consent Categories</b> decide which destinations that data is ever allowed to reach. Governance lives <i>at the point of ingestion</i> — so nothing ungoverned ever gets downstream.</p>

<p align="justify"><b>③&nbsp;&nbsp;Store</b> &nbsp;—&nbsp; <b>Data Lakes</b> define object-store sinks (bucket, format, compression, retention); <b>Warehouses</b> connect compute targets like Databricks. Your data, in your infrastructure, on your terms.</p>

<p align="justify"><b>④&nbsp;&nbsp;Activate</b> &nbsp;—&nbsp; <b>Destinations</b> like Braze and Mixpanel receive exactly the sources you choose, reshaped by field-level <b>Mappings</b> into precisely what each downstream tool expects — and never anything a user hasn't consented to.</p>

<br/>

<h2 align="center">✨&nbsp;&nbsp;What makes it different</h2>

<table>
<tr>
<td width="33%" valign="top" align="center">
<h3>🛡️ Privacy is the model</h3>
<p align="center">PII/SPII classification, consent gating, and propagation rules aren't a compliance bolt-on — they're <b>first-class entities</b> in the domain. If it isn't allowed, it doesn't move.</p>
</td>
<td width="33%" valign="top" align="center">
<h3>🧭 Governance at the edge</h3>
<p align="center">Policies attach to the <b>source itself</b>. Ungoverned data can't sneak in downstream, because there is no downstream without a policy.</p>
</td>
<td width="33%" valign="top" align="center">
<h3>🧾 Nothing is invisible</h3>
<p align="center">Every change to every entity is <b>version-tracked and audited</b>. Full history, full accountability, zero guesswork about who changed what.</p>
</td>
</tr>
</table>

<br/>

<h2 align="center">🚀&nbsp;&nbsp;The vision</h2>

<p align="justify">Today Bootstrap Data governs the flow of first-party data. Tomorrow it becomes the <b>trust layer for the entire customer-data lifecycle</b>:</p>

| Horizon | What it unlocks |
| :-- | :-- |
| 🔴 &nbsp;**Real-time activation** | Governed streams that light up destinations the instant a signal lands — not hours later. |
| 🧠 &nbsp;**Consent as code** | User consent that propagates across every lake, warehouse, and destination — revocable everywhere in one action. |
| 🤖 &nbsp;**AI-assisted governance** | Describe intent in plain language; the platform proposes matchers, policies, and mappings, then keeps schemas honest as your product evolves. |
| 🔌 &nbsp;**Open connector ecosystem** | Every major product SDK on one side, every marketing and analytics tool on the other — all speaking one governed contract. |
| 🏛️ &nbsp;**Provable compliance** | Turn "are we compliant?" from a quarterly scramble into a live, queryable answer. |

<p align="justify"><b>The north star</b> &nbsp;—&nbsp; make responsible use of customer data the <i>default</i>, so great teams can move fast <i>because</i> they respect their users, not despite it.</p>

<br/>

<h2 align="center">🧩&nbsp;&nbsp;The architecture</h2>

<p align="justify">Bootstrap Data is composed of focused, independently-evolving building blocks that separate <i>deciding what's allowed</i> from <i>doing the work</i> — a classic control-plane / data-plane split, wrapped in trust.</p>

```mermaid
flowchart TB
    subgraph experience["🖥️ Experience Layer"]
        console["Operator Console<br/>configure sources, policies & activation"]
    end
    subgraph control["🏛️ Control Plane"]
        edge["Edge Gateway<br/>routing · OIDC login"]
        registry["Metadata Registry<br/>system of record + audit"]
    end
    subgraph runtime["⚙️ Data Plane"]
        ingestapi["Ingest API<br/>event contract + SDKs"]
        engine["Governance & Activation Engine<br/>policy enforcement on live data"]
    end
    subgraph foundation["🧱 Trust Foundation"]
        identity["Identity & Access<br/>OIDC · tokens · consent"]
        design["Design System<br/>shared UI & brand"]
        quality["Quality & Assurance<br/>automated end-to-end testing"]
    end

    console --> control
    control --> runtime
    foundation -.-> control
    foundation -.-> runtime

    classDef box fill:#7C3AED,stroke:#4C1D95,color:#fff;
    class console,edge,registry,ingestapi,engine,identity,design,quality box;
```

| Component | Role in the platform |
| :-- | :-- |
| 🖥️ &nbsp;**Operator Console** | The single pane of glass where teams register sources, author governance policies, and wire up activation — no code required. |
| 🏛️ &nbsp;**Edge Gateway** | The one secure front door: authenticates every visitor, then routes traffic to the right service. |
| 📇 &nbsp;**Metadata Registry** | The system of record for every source, policy, matcher, mapping, and destination — fully validated and version-audited. |
| 📜 &nbsp;**Ingest API** | The governed contract (and SDKs) every product uses to stream first-party events into the platform. |
| ⚙️ &nbsp;**Governance &amp; Activation Engine** | The runtime that enforces propagation policies and consent on live data, then routes it to lakes, warehouses, and destinations. |
| 🔐 &nbsp;**Identity &amp; Access** | OIDC authentication, personal access tokens, and consent — the trust primitives woven through every layer. |
| 🎨 &nbsp;**Design System** | Shared, accessible UI components and brand that give every surface one consistent, polished feel. |
| 🧪 &nbsp;**Quality &amp; Assurance** | Continuous end-to-end and API testing that keeps the whole platform honest, release after release. |

<br/>

<h2 align="center">🛠️&nbsp;&nbsp;The stack</h2>

| Layer | Technologies |
| :-- | :-- |
| ⚙️ &nbsp;**Backend** | Java 21 · Spring Boot · Spring Cloud Gateway · JHipster · PostgreSQL (`jsonb`) · Redis · Consul · Keycloak (OIDC / OAuth2) |
| 🎨 &nbsp;**Frontend** | React microfrontends (Module Federation) · Redux · shadcn/ui · Tailwind CSS · TanStack Table · i18n (English · Hindi · Japanese) |
| 🛡️ &nbsp;**Trust &amp; Quality** | Validated domain constraints · filtering, pagination &amp; search on every list · complete audit history · automated CI &amp; end-to-end testing |

<br/>

---

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/logo-mark.svg">
  <img src="./assets/logo-mark.svg" alt="Bootstrap Data" width="46">
</picture>

<br/>

<b>Bootstrap Data</b> &nbsp;—&nbsp; first-party data, governed end to end.
<br/>
<sub><i>Built with intention. Private by default.</i></sub>

</div>
