# 🌊 Eco-Intelligence Lab
## AI-Driven Water Education & Stewardship

**Miami Dade College — Kendall Campus Environmental Center**

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Google Colab](https://img.shields.io/badge/Platform-Google%20Colab-F9AB00?logo=googlecolab)](https://colab.research.google.com/)
[![Python 3.10+](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)](https://python.org)

---

## About the Project

The Eco-Intelligence Lab is a two-year environmental education project (2027–2028) funded by the EPA Environmental Education Grant Program. The project combines real-time water-quality monitoring with responsible AI tools to build environmental literacy across three audiences: **college students**, **K-12 students**, and **community members**.

All activities are based at the MDC Kendall Campus Environmental Center — a nine-acre site with a three-acre limestone lake sitting directly above the **Biscayne Aquifer**, the primary drinking water source for the Miami region.

### What We Do

- **Monitor:** Real-time water-quality monitoring stations continuously collect sensor data (pH, temperature, turbidity, dissolved oxygen, conductivity, nutrients)
- **Analyze:** College students clean, visualize, and analyze environmental data using Python and AI techniques
- **Communicate:** A public-facing dashboard translates findings into accessible visualizations for the community
- **Teach:** K-12 students explore data through guided AI workshops; community members engage through monthly science events
- **Share:** All instructional materials are open-access for other institutions to adopt and adapt

### Environmental Context

South Florida faces critical water challenges. The Biscayne Aquifer — our sole drinking water source — is extremely vulnerable due to porous limestone bedrock. Contaminants can reach the water table in hours. Sea-level rise drives saltwater intrusion, stormwater carries pollutants through porous limestone, and nearly 900 new Florida residents arrive daily, increasing demand on water infrastructure. This project grounds AI education in these real, local challenges.

---

## Repository Structure

```
mdc-eco-intelligence-lab/
│
├── docs/                          # Project documentation
│   ├── PRD.md                     # Product Requirements Document
│   └── ...                        # Additional planning documents
│
├── notebooks/                     # Google Colab notebooks (college level)
│   ├── 01-data-exploration/       # D1: Data wrangling & visualization
│   ├── 02-classification/         # D2: Water quality classification models
│   ├── 03-anomaly-detection/      # D3: Sensor anomaly vs. environmental events
│   ├── 04-time-series-forecasting/# D4: Seasonal trend prediction
│   └── 05-responsible-ai/         # D5: Bias, limitations, ethics, validation
│
├── workshops/                     # Scaffolded materials for non-college audiences
│   ├── high-school/               # D7: No-code-prerequisite Colab notebooks
│   └── community/                 # Materials for community science events
│
├── dashboard/                     # D6: Public dashboard source and documentation
│
├── data/                          # Datasets
│   ├── raw/                       # Unprocessed sensor data (when available)
│   ├── processed/                 # Cleaned, analysis-ready datasets
│   └── public-sources/            # Public water quality data for prototyping
│
├── mentor-training/               # D8: Facilitator guides and training materials
│
├── assessments/                   # Pre/post assessments, rubrics, scenario evaluations
│
├── slides/                        # Presentation materials
│
└── images/                        # Diagrams, screenshots, visual assets
```

---

## Technical Stack

| Tool | Purpose |
|------|---------|
| **Python 3.10+** | Primary programming language |
| **Google Colab** | Cloud-based notebook platform (free, no installation required) |
| **pandas / NumPy** | Data wrangling and numerical computation |
| **Matplotlib / Seaborn** | Data visualization |
| **scikit-learn** | Classification, anomaly detection, preprocessing |
| **TensorFlow / Keras** | Time-series forecasting (LSTM models) |
| **Prophet** | Accessible time-series forecasting |
| **Dashboard platform** | TBD (evaluation in progress) |

---

## Who This Is For

### College Students
Work through the notebooks in the `notebooks/` folder sequentially. Each notebook is designed to open in Google Colab — click the badge at the top of any notebook to launch it directly.

### K-12 Educators & Students
Find scaffolded, no-coding-prerequisite workshops in the `workshops/high-school/` folder. These are designed to be facilitated by trained mentors, not self-guided.

### Community Members
The public dashboard (coming 2027) will provide accessible, bilingual water quality information. Community event materials are in `workshops/community/`.

### Other Educators & Institutions
This repository is designed for adoption and adaptation. All materials are licensed under CC BY-NC-SA 4.0. If you're building a similar environmental monitoring + AI education project, start with the `docs/` folder for our approach, then adapt the notebooks for your local water systems.

---

## Project Timeline

| Phase | Period | Focus |
|-------|--------|-------|
| **Phase 0** | 2026 | Pre-grant prototyping through existing courses |
| **Phase 1** | Jan–Jun 2027 | Core AI curriculum + Responsible AI module |
| **Phase 2** | Jul–Dec 2027 | Dashboard launch + K-12 workshops + mentor training |
| **Phase 3** | Jan–Dec 2028 | Full delivery, iteration, open-access packaging |

---

## Project Goals & EPA Alignment

| Goal | Audience | Target |
|------|----------|--------|
| **Goal 1** | College students | 50+ students skilled in environmental data analysis and responsible AI |
| **Goal 2** | K-12 students | 100+ students with 40%+ improvement in water quality and AI literacy |
| **Goal 3** | Community members | 200+ participants accessing and interpreting environmental data |

**EPA Educational Priority:** Artificial Intelligence  
**EPA Environmental Priority:** Ensuring Clean and Safe Water

---

## License

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

You are free to share and adapt these materials for non-commercial purposes, provided you give appropriate credit and distribute your contributions under the same license.

---

## Acknowledgments

This project is funded by the **U.S. Environmental Protection Agency** Environmental Education Grant Program (EPA-EE-25-01).

**Miami Dade College** — Kendall Campus  
**Earth Ethics Institute**

---

## Contact

Professor Carlos Marquez  
Applied AI and Data Analytics  
Miami Dade College — Kendall Campus  
cmarque1@mdc.edu

---

*This repository is under active development. Content will be populated as the project progresses through its planned phases.*
