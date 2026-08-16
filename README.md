# Capital and Capability: What AI Investment Does and Does Not Buy
Author: Rachita Mehta

### Project Overview
This research examines whether AI venture-capital investment is a reliable proxy for national AI capability. Governments and investors increasingly treat AI investment totals as a shorthand for national AI strength, but investment and capability are not necessarily the same thing. This paper tests that assumption across ten leading AI economies, separating the amount of capital a country attracts from the breadth and strength of its underlying AI ecosystem.

### Key Research Questions
Is higher AI investment associated with stronger overall national AI ecosystems?
Is AI investment associated with how broadly that capability is distributed across research, talent, governance, infrastructure, and other dimensions, rather than with its aggregate level?

### Data Description
The study covers the ten countries at the top of Stanford HAI's 2024 Global AI Vibrancy Ranking: the United States, China, India, South Korea, the United Kingdom, Singapore, Spain, the United Arab Emirates, Japan, and Canada. Both data sources are benchmarked to 2024 so that investment and capability describe the same period.

Variables included: AI venture-capital investment (USD millions); seven Stanford Vibrancy pillar scores (R&D, Responsible AI, Economy, Talent, Policy and Governance, Public Opinion, Infrastructure); a derived Non-Economic AI Ecosystem Score; and a derived Herfindahl–Hirschman concentration index (HHI) measuring how evenly capability is distributed across pillars.

### Data Sources
Stanford HAI Global AI Vibrancy Tool (2024 pillar-level indicators) and the OECD AI Policy Observatory, VC Investments in AI by Country (Preqin deal data, 2024).

### Methodology
The research constructs a Non-Economic AI Ecosystem Score by excluding Stanford's Economy pillar, which itself incorporates AI private investment, to avoid circularity between the independent and dependent variables. Ecosystem breadth is measured using an HHI applied descriptively to each country's own distribution of capability across six non-economic pillars. Association between investment and each measure is tested using Spearman's rank correlation, appropriate for a small, right-skewed sample.

The Model: Ecosystem Score = (R&D + Responsible AI + Talent + Policy & Governance + Public Opinion + Infrastructure) / 6
The Breadth Measure: HHI = Σ(pillar score / total)² across the six non-economic pillars.

### Principal Findings
Level: AI investment has a positive but statistically insignificant association with overall ecosystem strength (Spearman ρ = 0.41, p = 0.24, N = 10).
Breadth: AI investment has a stronger, statistically significant association with how evenly capability is distributed across the ecosystem (Spearman ρ = −0.64, p = 0.048, N = 10).
Interpretation: Investment appears more informative about the breadth of a country's AI ecosystem than about its aggregate strength. Countries with substantially different investment levels can reach similar ecosystem scores through different combinations of research, talent, governance, and infrastructure.
Note: This research is cross-sectional and descriptive; it does not establish that investment causes broader ecosystem development. The analysis also distinguishes ecosystem capability from strategic autonomy, since a country can develop substantial domestic AI capability while remaining dependent on foreign firms for critical technologies such as semiconductors and cloud infrastructure.

### Repository Contents
`AI_Investment_and_National_AI_Capability_analysis.ipynb` — full analysis notebook, run start to finish: loads the investment data, builds the Ecosystem Score and HHI, produces all five figures, and runs the Spearman correlations reported above.

`AI_Investment_and_National_AI_Capability_data.xlsx` — country-level dataset (pillar scores, Ecosystem Score, HHI, investment totals) with a Notes & Sources tab documenting where every column comes from and how the derived columns are calculated.

`oecd_ai_investment_data.xlsx` — the underlying OECD/Preqin investment dataset used by the notebook.

`AI Investment and National AI Capability.pdf` — the full written paper.
