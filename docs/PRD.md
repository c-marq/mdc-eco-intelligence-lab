# Eco-Intelligence Lab — Product Requirements Document
## AI & Data Analytics Deliverables

**Project:** Eco-Intelligence Lab: AI-Driven Water Education & Stewardship  
**Grant:** EPA-EE-25-01  
**AI Lead:** Professor Carlos Marquez, Miami Dade College  
**Document Version:** 1.0 (Draft — Sections 1–5)  
**Created:** February 21, 2026  
**Status:** Pre-approval planning

---

## Table of Contents

1. [Project Overview](#1-project-overview)
2. [Stakeholder Map](#2-stakeholder-map)
3. [Phase Overview](#3-phase-overview)
4. [Deliverable Registry](#4-deliverable-registry)
5. [Dependency Map](#5-dependency-map)

---

## Sections Planned for v2.0

6. Hour Budget (250 grant hours + Phase 0 teaching hours)
7. Partner Integration Points
8. Risk Register
9. Success Metrics & EPA Evaluation Alignment

---

## 1. Project Overview

### Mission

The Eco-Intelligence Lab installs real-time water-quality monitoring stations on the MDC Kendall Campus Environmental Center — a nine-acre site with a three-acre limestone lake sitting directly above the Biscayne Aquifer. College students build and maintain the stations, analyze the data using AI and data analytics techniques, develop a public-facing dashboard, and receive responsible AI instruction. The project extends to K-12 students through guided workshops and to the community through monthly engagement events.

### Scope of This Document

This PRD covers **only the AI and Data Analytics deliverables** — the subset of the project under Professor Marquez's direct responsibility. Other project components (station hardware deployment, field methods training, community event logistics, K-12 field visits) are led by other faculty and staff. This document interfaces with those components where data handoffs or curriculum dependencies exist.

### Constraints

| Constraint | Detail |
|---|---|
| **Faculty Hours** | 250 total grant-funded hours over 2 years (~125/year, ~2.5 hrs/week) |
| **Project Period** | January 4, 2027 – December 31, 2028 |
| **Technical Platform** | Python, Google Colab (free tier), scikit-learn, TensorFlow |
| **Student Skill Level — Python** | Introductory to intermediate (pandas, visualization, basic scripting) |
| **Student Skill Level — ML/DL** | Guided application of pre-built models; students train, evaluate, and interpret — they do not design model architectures from scratch |
| **Dashboard Platform** | TBD — decision required by end of Phase 1 |
| **Pre-Grant Runway** | ~10 months (March 2026 – December 2026) available for Phase 0 prototyping through existing courses at no grant cost |

### Key Assumptions

- Domain-specific environmental data science guidance is available through the Dr. Suárez advisory prompt (Tier 1 — active and operational)
- Industry partners (Tier 2) such as the Everglades Foundation lead scientist are prospective; outreach is planned but no commitments are in place. All deliverables have self-build fallback paths (Tier 3) if partnerships do not materialize.
- If Tier 2 partners provide production-grade pipelines and models, Prof. Marquez builds the **instructional scaffolding** (how to teach it); partners provide the **technical engines** (the models and pipelines themselves). If not, Prof. Marquez builds simplified but defensible versions using public data and open-source methods.
- College students identified during Phase 0 become the mentor pool for Phase 2 K-12 workshops and community events
- Monitoring station hardware is deployed and generating data by mid-Phase 1 (responsibility of other project staff); AI curriculum can begin with historical/simulated data if stations are delayed
- EPA-approved QAPP will be developed by project staff before data collection begins

---

## 2. Stakeholder Map

### Primary Audiences (Who Uses What You Build)

| Audience | What They Need | Deliverables They Touch |
|---|---|---|
| **College Students** (50+ over 2 years) | Hands-on skills in data cleaning, visualization, classification, anomaly detection, forecasting, dashboard development, and responsible AI — all applied to real environmental data | AI curriculum notebooks, Responsible AI module, Dashboard development experience |
| **K-12 Students** (100+ over 2 years) | Age-appropriate, scaffolded introduction to AI-assisted environmental data exploration with no coding prerequisite | High school workshop notebooks, Facilitator guides |
| **Community Members** (200+ over 2 years) | Accessible understanding of local water quality through the public dashboard and community events | Public dashboard, Community event data interpretation materials |
| **College Student Mentors** (subset of college students) | Training to co-facilitate high school workshops and community events | Mentor training materials, Facilitator guides |

### Internal Stakeholders

| Stakeholder | Interest |
|---|---|
| **Project Coordinator** | Overall timeline, deliverable completion, EPA reporting |
| **Michael Matthews** (Earth Ethics Institute Director) | Environmental education quality, community engagement |
| **Cristina Mateo** (Sr. Director, Campus Admin) | Budget, institutional compliance |
| **External Evaluator** (Dr. Jacqueline Peña) | Pre/post assessments, rubrics, scenario-based evaluations, dashboard analytics |
| **EPA Program Officers** | Grant deliverable compliance, QAPP adherence, measurable outcomes |

### Partner Contributors

The project relies on three tiers of advisory and partnership support. The curriculum is designed to be viable at every tier — partner contributions enhance depth and authenticity but are not blockers.

**Tier 1 — AI Domain Advisory (Active)**

| Partner | Contribution | Status |
|---|---|---|
| **Dr. Rafael Suárez** (simulated domain expert) | South Florida environmental data science expertise delivered through a structured Claude advisory prompt. Provides operationally grounded guidance on sensor data realities, South Florida hydrology, model selection, dashboard design, QA/QC considerations, and the practical difference between production-grade and education-grade approaches. | ✅ Active — prompt developed and operational |

> **Note:** Dr. Suárez is not a real person. He is a detailed expert persona prompt that allows Prof. Marquez to access domain-specific environmental data science guidance through Claude. This is documented transparently because the advisory quality is real even though the person is simulated — the prompt encodes 40 years of South Florida monitoring expertise, sensor platform knowledge, and regulatory framework awareness.

**Tier 2 — Industry Partners (Prospective)**

| Partner | Expected Contribution | Status |
|---|---|---|
| **Everglades Foundation — Lead Scientist** | Production data pipelines, water quality classification models, anomaly detection approaches, time-series forecasting models, real-world sensor data expertise | 🔜 Prospective — outreach planned, ideally pre-approval to establish relationship; formal engagement post-approval |
| **Other environmental data science professionals** (TBD) | Additional models, datasets, or domain review | 🔜 To be identified during Phase 0 |

**Tier 3 — Fallback Path (Built-In)**

If industry partnerships do not materialize or are delayed, every "acquire and adapt" deliverable (D1–D4) has a self-build alternative:

| Deliverable | Partner Path | Fallback Path |
|---|---|---|
| D1 — Data Exploration | Adapt production pipeline | Build from scratch using public water quality data (EPA STORET, USGS NWIS, SFWMD DBHYDRO) |
| D2 — Classification | Adapt production classifier | Build basic random forest classifier from scratch; less sophisticated but teachable |
| D3 — Anomaly Detection | Adapt production approach | Use statistical process control (SPC) methods; simpler but defensible |
| D4 — Time-Series Forecasting | Adapt production model | Use Prophet (simpler to teach than LSTM); reduced depth but achievable |

> **Key Insight:** The project is fully viable without Tier 2 partners. Partner contributions increase authenticity and reduce Prof. Marquez's development hours, but the fallback path produces functional, defensible curriculum using publicly available data and well-documented open-source methods.

**Institutional Partners**

| Partner | Contribution | Integration Point |
|---|---|---|
| **Other MDC Faculty** | Station hardware, field methods training, K-12 field visits, community event logistics | Data handoff: stations produce data that feeds AI curriculum |
| **Miami-Dade County Public Schools** | K-12 student access, classroom integration, teacher coordination | Receive workshop curriculum and trained mentors |

---

## 3. Phase Overview

The project follows four phases. **Phase 0 is pre-grant** — work done through existing courses at no grant cost. Phases 1–3 consume the 250 grant-funded hours.

### Phase 0: Pre-Grant Foundation

**Timeline:** March 2026 – December 2026 (~10 months)  
**Cost to Grant:** $0 (regular teaching load)  
**Goals Served:** Feeds Goal 1

**Purpose:** Build early prototypes, establish partner relationships, identify passionate students, and create a head start that makes Phases 1–3 more efficient.

**Key Activities:**

- Integrate water monitoring themes into Data Mining course projects (starting ~March 2026)
- Develop prototype Colab notebooks using publicly available water quality datasets (EPA STORET, USGS NWIS, SFWMD DBHYDRO) as stand-ins for future campus sensor data
- Establish working relationships with environmental data science partners; request access to production pipelines and models
- Identify students with interest and aptitude who may become project contributors and future mentors
- Prototype initial data exploration and visualization workflows
- Begin drafting the Responsible AI module outline based on existing CAI1001C course materials

**Phase 0 Exit Criteria:**

- [ ] At least 2 prototype notebooks exist (data exploration + basic visualization using public water quality data)
- [ ] At least 1 partner relationship established with commitment to share models/pipelines
- [ ] At least 3–5 students identified as potential project contributors
- [ ] Responsible AI module outline drafted
- [ ] Dashboard technology shortlist created (2–3 candidates evaluated)

---

### Phase 1: Infrastructure & Core Curriculum

**Timeline:** January – June 2027 (6 months)  
**Grant Hours:** ~80–90 hours  
**Goals Served:** Goal 1 (primary)

**Purpose:** Build the foundational AI curriculum that college students will use throughout the project. Establish the data pipeline from monitoring stations to analysis-ready datasets. Launch the Responsible AI module. Begin dashboard architecture.

**Key Activities:**

- Adapt partner-provided data pipelines into instructional Colab notebooks (data ingestion → cleaning → validation)
- Build the core notebook sequence: Explore → Clean → Visualize → Classify → Detect Anomalies
- Adapt partner-provided classification and anomaly detection models into student-accessible Colab notebooks with instructional scaffolding
- Deliver Responsible AI module v1 (data bias, model limitations, human-in-the-loop, ethical data sharing)
- Select dashboard platform and build architecture prototype
- Design assessment rubrics and scenario-based evaluations aligned with EPA evaluation framework
- Begin training first cohort of student mentors through hands-on co-facilitation

**Phase 1 Dependencies:**

- Monitoring stations must be deployed and generating data (or fallback to public datasets if delayed)
- Partner models/pipelines received and reviewed for adaptation feasibility
- QAPP approved before any campus data is used in instruction

**Phase 1 Exit Criteria:**

- [ ] Core notebook sequence complete and tested with students (5+ notebooks)
- [ ] Responsible AI module v1 delivered and assessed (85% mastery target)
- [ ] Dashboard platform selected with architecture prototype approved
- [ ] At least 2 student mentors in training
- [ ] Pre/post assessment instruments developed with evaluator

---

### Phase 2: Expansion & Adaptation

**Timeline:** July – December 2027 (6 months)  
**Grant Hours:** ~80–90 hours  
**Goals Served:** Goals 1, 2, 3

**Purpose:** Extend the college curriculum to include forecasting. Launch the public dashboard. Adapt college materials into K-12 workshop curriculum. Train mentors. Begin community engagement.

**Key Activities:**

- Adapt partner-provided time-series forecasting models into instructional notebooks
- Launch public dashboard v1 with real-time data, historical trends, and AI-generated alerts
- Design and build high school workshop notebooks (scaffolded, no-code-prerequisite versions of college materials)
- Create facilitator guides for each workshop
- Train and certify college student mentors; lead initial K-12 workshop sessions, then hand off to mentors
- Support first community events with data interpretation materials
- Conduct quarterly dashboard validation against manual measurements

**Phase 2 Dependencies:**

- Phase 1 core notebooks must be complete and tested
- Sufficient campus sensor data accumulated for meaningful trend analysis
- K-12 school partnerships and scheduling confirmed
- Community event calendar established by project coordinator

**Phase 2 Exit Criteria:**

- [ ] Time-series forecasting notebook complete
- [ ] Public dashboard live with real-time data feed
- [ ] At least 3 high school workshop notebooks created with facilitator guides
- [ ] At least 4 student mentors trained and delivering workshops
- [ ] First community events completed with data interpretation support
- [ ] K-12 pre/post assessments deployed

---

### Phase 3: Delivery, Refinement & Packaging

**Timeline:** January – December 2028 (12 months)  
**Grant Hours:** ~70–80 hours  
**Goals Served:** Goals 1, 2, 3

**Purpose:** Full delivery cycle across all audiences. Iterate on all materials based on assessment data and user feedback. Refine dashboard. Package everything for the open-access repository.

**Key Activities:**

- Continue delivering AI curriculum to new college student cohorts; refine based on assessment data
- Expand and refine K-12 workshops based on first delivery cycle feedback
- Maintain and improve public dashboard (seasonal pattern updates, new alert types, accessibility improvements)
- Continue community event support with increasingly mentor-led delivery
- Compile all notebooks, curriculum, facilitator guides, and assessment instruments into the open-access public repository
- Document lessons learned, pedagogical approach, and replication guidance
- Support final project evaluation and EPA reporting

**Phase 3 Dependencies:**

- All Phase 2 deliverables operational
- Assessment data from Phase 2 available for iteration
- Full year of sensor data available for seasonal pattern analysis

**Phase 3 Exit Criteria:**

- [ ] All curriculum refined through at least 2 delivery cycles
- [ ] Dashboard operational with 4+ quarters of validated data
- [ ] 50+ college students served, 100+ K-12 students served, 200+ community members engaged
- [ ] Open-access repository published with complete materials
- [ ] Final evaluation data collected and reported to EPA

---

## 4. Deliverable Registry

Each deliverable is tagged with its source (build in-house vs. acquire and adapt), the goal(s) it serves, its target phase, and what it depends on.

### Legend

- **🔧 BUILD** = Designed and built in-house by Prof. Marquez
- **🔄 ADAPT** = Acquired from partners, adapted and scaffolded for instruction
- **Goal Tags:** G1 = College Students, G2 = K-12 Students, G3 = Community

---

### D1 — Data Exploration & Visualization Notebooks

| Field | Detail |
|---|---|
| **ID** | D1 |
| **Description** | Series of Colab notebooks teaching students to inspect, clean, and visualize water quality sensor data. Students develop intuition for what "normal" looks like before any modeling begins. Covers pandas operations, Seaborn/Matplotlib visualizations, missing data handling, and sensor drift awareness. |
| **Source** | 🔄 ADAPT — Partner provides production data pipeline; Prof. Marquez strips to essentials and adds instructional scaffolding |
| **Audience** | College students |
| **Goals** | G1 |
| **Phase** | Prototype in Phase 0, finalize in Phase 1 |
| **Depends On** | Sensor data (or public water quality data as fallback) |
| **Format** | Google Colab notebooks (.ipynb) hosted on GitHub |
| **Estimated Count** | 3–4 notebooks in sequence |
| **Acceptance Criteria** | Students can load raw sensor data, identify and handle missing values, create time-series visualizations, and articulate what constitutes "normal" readings for the Kendall Campus lake |

---

### D2 — Classification Model Notebooks

| Field | Detail |
|---|---|
| **ID** | D2 |
| **Description** | Notebooks where students apply classification algorithms (random forest, gradient boosting) to categorize water conditions as safe/advisory/impaired based on multi-parameter sensor readings. Students learn model training, evaluation, and interpretation. |
| **Source** | 🔄 ADAPT — Partner provides production classification model(s); Prof. Marquez simplifies and scaffolds |
| **Audience** | College students |
| **Goals** | G1 |
| **Phase** | Phase 1 |
| **Depends On** | D1 (students must understand the data before modeling it) |
| **Format** | Google Colab notebooks (.ipynb) hosted on GitHub |
| **Estimated Count** | 2–3 notebooks |
| **Acceptance Criteria** | Students can train a classifier on labeled water quality data, evaluate accuracy with appropriate metrics, and explain what the model's predictions mean in environmental context |

---

### D3 — Anomaly Detection Notebooks

| Field | Detail |
|---|---|
| **ID** | D3 |
| **Description** | Notebooks teaching students to detect unusual readings in sensor data — distinguishing genuine environmental events (contamination, algal blooms) from sensor malfunctions (fouling, drift, calibration failure). Uses isolation forests and/or statistical methods. |
| **Source** | 🔄 ADAPT — Partner provides production anomaly detection approach; Prof. Marquez adapts |
| **Audience** | College students |
| **Goals** | G1 |
| **Phase** | Phase 1 |
| **Depends On** | D1 (baseline understanding of "normal"), D2 (modeling fundamentals) |
| **Format** | Google Colab notebooks (.ipynb) hosted on GitHub |
| **Estimated Count** | 1–2 notebooks |
| **Acceptance Criteria** | Students can run anomaly detection on sensor data, flag outliers, and articulate a hypothesis for each anomaly (environmental event vs. sensor issue) supported by evidence from the data |

---

### D4 — Time-Series Forecasting Notebooks

| Field | Detail |
|---|---|
| **ID** | D4 |
| **Description** | Notebooks applying time-series models (ARIMA/Prophet and/or LSTM) to predict seasonal water quality trends — nutrient loading cycles, dry-season salinity patterns, post-storm recovery curves. Requires sufficient historical data. |
| **Source** | 🔄 ADAPT — Partner provides production forecasting model(s); Prof. Marquez adapts |
| **Audience** | College students |
| **Goals** | G1 |
| **Phase** | Phase 2 (requires accumulated sensor data) |
| **Depends On** | D1, D2, D3 (full exploration → modeling progression), 6+ months of sensor data |
| **Format** | Google Colab notebooks (.ipynb) hosted on GitHub |
| **Estimated Count** | 1–2 notebooks |
| **Acceptance Criteria** | Students can fit a time-series model to seasonal sensor data, generate forecasts, evaluate forecast accuracy, and explain predictions in the context of South Florida seasonal hydrology |

---

### D5 — Responsible AI Module

| Field | Detail |
|---|---|
| **ID** | D5 |
| **Description** | Structured instructional module covering four competency areas: (1) data bias recognition in environmental monitoring, (2) model limitation and uncertainty analysis, (3) human-in-the-loop validation comparing AI outputs with manual sampling, (4) ethical data sharing and public communication. Assessed through scenario-based evaluation with 85% mastery target. |
| **Source** | 🔧 BUILD — Designed and built in-house; draws on Prof. Marquez's CAI1001C materials and EPA-specific ethical considerations |
| **Audience** | College students (primary), adapted for K-12 and community awareness |
| **Goals** | G1, G2, G3 |
| **Phase** | Draft outline in Phase 0, v1 in Phase 1, refined in Phase 3 |
| **Depends On** | D1 (needs real data examples to ground bias discussions); can begin outline before data is available |
| **Format** | Colab notebook + supplementary readings/slides; scenario-based assessment instrument |
| **Estimated Count** | 1 core module with 4 units + assessment |
| **Acceptance Criteria** | 85% of participating students demonstrate mastery on scenario-based evaluation; students can identify bias in a given environmental dataset, articulate model limitations, validate AI output against manual data, and evaluate an ethical data-sharing scenario |

---

### D6 — Public Dashboard

| Field | Detail |
|---|---|
| **ID** | D6 |
| **Description** | Web-based dashboard translating real-time sensor data and AI outputs into accessible visualizations. Serves dual audiences: public-facing layer (traffic-light water quality status, plain-language explanations, bilingual English/Spanish) and technical layer (full parameter detail, historical trends, AI-generated anomaly alerts). Hosted on MDC web platform with kiosk and mobile access. |
| **Source** | 🔧 BUILD — Prof. Marquez provides technical direction; students build iteratively |
| **Audience** | Community members (primary), college students (builders), K-12 students (viewers), regulatory partners |
| **Goals** | G1, G2, G3 |
| **Phase** | Architecture in Phase 1, v1 launch in Phase 2, iteration in Phase 3 |
| **Depends On** | D1 (data pipeline must exist), monitoring station data feed, platform decision |
| **Format** | Web application (platform TBD — Power BI, Streamlit, or custom; decision by end Phase 1) |
| **Estimated Count** | 1 dashboard with iterative releases |
| **Acceptance Criteria** | Dashboard displays real-time data, historical trends, and AI-generated alerts; quarterly validation shows alignment with manual measurements; community survey shows 50%+ report increased understanding; accessible in English and Spanish; mobile-responsive |

---

### D7 — High School Workshop Notebooks

| Field | Detail |
|---|---|
| **ID** | D7 |
| **Description** | Pre-configured, heavily scaffolded Colab notebooks designed for high school students with no coding prerequisite. Students visualize water quality trends, run pre-built models, compare AI predictions with sensor readings, and reflect on results. Adapted from college-level notebooks (D1–D4) with reduced complexity, more guided steps, and age-appropriate framing. |
| **Source** | 🔧 BUILD — Adapted in-house from college notebooks; requires significant instructional redesign for age-appropriate delivery |
| **Audience** | K-12 students (high school) |
| **Goals** | G2 |
| **Phase** | Phase 2 |
| **Depends On** | D1, D2, D3 (college versions must be tested before adaptation); facilitator guides (D8) |
| **Format** | Google Colab notebooks (.ipynb) with pre-run outputs visible; hosted on GitHub |
| **Estimated Count** | 3–4 workshop notebooks |
| **Acceptance Criteria** | High school students with no coding experience can complete each workshop in 60–90 minutes with mentor facilitation; 40%+ improvement on pre/post assessments; trained mentors can deliver without faculty present |

---

### D8 — Mentor Training Materials

| Field | Detail |
|---|---|
| **ID** | D8 |
| **Description** | Training program for college students who will co-facilitate K-12 workshops (D7) and community events (Goal 3). Includes facilitator guides for each workshop, troubleshooting playbooks, facilitation techniques, and assessment administration procedures. Must be thorough enough that mentors deliver reliably without faculty present. |
| **Source** | 🔧 BUILD — Designed and built in-house |
| **Audience** | College student mentors |
| **Goals** | G1 (mentor development), G2 (workshop delivery), G3 (community event support) |
| **Phase** | Begin in Phase 1 (initial mentor identification), primary development in Phase 2 |
| **Depends On** | D7 (workshop notebooks must exist before facilitator guides can be written); D5 (mentors need responsible AI training) |
| **Format** | Facilitator guides (Markdown/PDF), troubleshooting playbooks, observation checklists |
| **Estimated Count** | 1 mentor training program + 1 facilitator guide per workshop notebook |
| **Acceptance Criteria** | Trained mentors independently deliver workshops observed to be at or above quality threshold; mentors can handle the 5 most common student questions/issues without faculty intervention |

---

### D9 — Open-Access Repository

| Field | Detail |
|---|---|
| **ID** | D9 |
| **Description** | Public GitHub repository containing all project notebooks, curriculum materials, facilitator guides, assessment instruments, datasets (where shareable), and replication guidance. Designed for other institutions to adopt or adapt the Eco-Intelligence Lab model. |
| **Source** | 🔧 BUILD — Compilation and documentation of all other deliverables |
| **Audience** | Other educators, institutions, EPA, public |
| **Goals** | G1, G2, G3 (all materials packaged) |
| **Phase** | Ongoing structure from Phase 0; final packaging in Phase 3 |
| **Depends On** | All other deliverables (D1–D8) |
| **Format** | GitHub repository with README, structured folders, licensing, and usage documentation |
| **Estimated Count** | 1 repository |
| **Acceptance Criteria** | An educator at another institution can clone the repository and understand how to adapt the materials for their own water quality monitoring context; all notebooks run in Colab without modification (except dataset URLs); documentation is complete |

---

## 5. Dependency Map

### Build Sequence — What Must Exist Before What

The deliverables follow a strict dependency chain. This is the order in which work must proceed:

```
PHASE 0 (Pre-Grant — No Cost)
│
├── D1 Prototypes ──── Data exploration notebooks using public datasets
├── D5 Outline ─────── Responsible AI module outline from CAI1001C materials
├── D6 Shortlist ───── Dashboard platform candidates evaluated
└── D9 Structure ───── Repository structure created on GitHub
│
▼
PHASE 1 (Jan–Jun 2027)
│
├── D1 Final ──────────── Data exploration & visualization (finalized with real sensor data)
│     │
│     ├── D2 ──────────── Classification models (requires D1)
│     │     │
│     │     └── D3 ────── Anomaly detection (requires D1 + D2 foundations)
│     │
│     └── D5 v1 ───────── Responsible AI module v1 (requires D1 for real data examples)
│
├── D6 Architecture ───── Dashboard architecture prototype + platform decision
│
└── D8 Begin ──────────── Identify and begin training first mentors
│
▼
PHASE 2 (Jul–Dec 2027)
│
├── D4 ────────────────── Time-series forecasting (requires D1-D3 + 6 months data)
│
├── D6 v1 Launch ──────── Public dashboard goes live (requires D1 pipeline + data feed)
│
├── D7 ────────────────── High school workshop notebooks (adapted from D1, D2, D3)
│     │
│     └── D8 Final ────── Facilitator guides + mentor certification (requires D7)
│
└── Community materials ── Data interpretation materials for Goal 3 events
│
▼
PHASE 3 (Jan–Dec 2028)
│
├── Iterate all ───────── Refine D1-D8 based on assessment data and feedback
├── D6 Mature ─────────── Dashboard seasonal updates + accessibility improvements
├── D5 v2 ─────────────── Responsible AI module refined with real project examples
└── D9 Final ──────────── Open-access repository packaged and published
```

### Critical Path

The **critical path** — the sequence where any delay cascades to downstream deliverables — runs through:

**Partner model acquisition → D1 (exploration) → D2 (classification) → D3 (anomaly detection) → D7 (high school adaptation) → D8 (mentor training)**

If partner models are delayed, D1 can proceed using public datasets (fallback already planned in Phase 0). If monitoring stations are delayed, the same fallback applies. The forecasting notebooks (D4) are on a parallel path constrained by data accumulation, not by the main curriculum sequence.

The **Responsible AI module (D5)** runs in parallel to the technical notebooks — it can begin from outline as early as Phase 0 and doesn't block any other deliverable, but it enriches all of them when integrated.

The **Dashboard (D6)** is semi-independent — its architecture can be designed in Phase 1 while notebooks are being built, but it can't launch until the data pipeline (from D1) and real sensor data are available.

### Partner Integration Dependencies (Tier 2 — Prospective)

These dependencies assume Tier 2 industry partners are secured. If not, the Tier 3 fallback path activates automatically.

| What You Need from Partners | When You Need It | Fallback If Unavailable |
|---|---|---|
| Production data cleaning/wrangling pipeline | Phase 0 (ideal) or early Phase 1 | Build simplified pipeline from scratch using public water quality data (EPA STORET, USGS NWIS, SFWMD DBHYDRO) |
| Classification model(s) for water quality categorization | Phase 1 (by ~March 2027) | Build basic random forest classifier from scratch; less sophisticated but teachable |
| Anomaly detection approach | Phase 1 (by ~April 2027) | Use statistical process control (SPC) methods; simpler but defensible |
| Time-series forecasting model(s) | Phase 2 (by ~July 2027) | Use Prophet (simpler to teach than LSTM); reduced depth but achievable |

**Phase 0 Action Item:** Initiate outreach to Everglades Foundation lead scientist and other prospective partners. Goal is to establish relationships pre-approval so formal engagement can begin immediately when the grant is confirmed.

---

## What's Next (Sections 6–9)

The following sections will be developed in a subsequent session:

- **Section 6 — Hour Budget:** Detailed allocation of 250 grant hours across phases and deliverables, plus estimated Phase 0 hours from regular teaching load
- **Section 7 — Partner Integration Points:** Specific ask documents for each partner type, including what to request, what format it should arrive in, and how it will be adapted
- **Section 8 — Risk Register:** Identified risks, probability, impact, and mitigation strategies
- **Section 9 — Success Metrics:** Mapping each deliverable to EPA evaluation criteria and measurable outcomes

---

*Document maintained in the Eco-Intelligence Lab GitHub repository. Version history tracked via Git.*
