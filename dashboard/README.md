# Public Dashboard

Web-based environmental data dashboard providing real-time water quality information for the MDC Kendall Campus Environmental Center.

## Dual-Audience Design

The dashboard serves two audiences through layered architecture:

- **Public layer:** Traffic-light water quality status, plain-language explanations, bilingual (English/Spanish), mobile-responsive
- **Technical layer:** Full parameter detail, historical trends, AI-generated anomaly alerts, downloadable data

## Platform Decision

Dashboard platform is under evaluation. Candidates include:

| Platform | Pros | Cons |
|----------|------|------|
| **Power BI** | Familiar to instructor; strong visualization; embeddable | Licensing considerations; less flexible for custom AI integration |
| **Streamlit** | Python-native; free; excellent for data apps; easy Colab integration | Requires hosting; less polished out-of-box |
| **Custom (Flask/Dash)** | Maximum flexibility; full control | Highest development effort; maintenance burden |

Decision target: End of Phase 1 (June 2027)

## Features (Planned)

- Real-time sensor data display
- Historical trend visualizations
- AI-generated anomaly alerts with plain-language explanations
- Quarterly validation reports (dashboard vs. manual measurements)
- Kiosk mode for Environmental Center, Library, and Student Union displays
- QR code access for mobile viewing
- Bilingual support (English/Spanish)

*Development begins Phase 1, v1 launch targeted for Phase 2 (Jul–Dec 2027).*
