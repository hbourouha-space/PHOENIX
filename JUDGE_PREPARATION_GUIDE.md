# PHOENIX — Judge Preparation Guide

**Proactive Hazard Observation, Isolation and Extinction Network for eXtreme Environments**

A practical guide for judge Q&A, a short demonstration, and failed-demo recovery. Be confident about what is implemented and equally clear about what is curated, rule-based, planned, or not validated.

## 30-second opening

PHOENIX is a research and engineering decision-support prototype for spacecraft fire safety. It organizes NASA combustion research and helps users compare experimental conditions before drawing conclusions. Its central principle is that fire behavior is material- and configuration-specific: a PMMA film, rod, fabric, and wire insulation should not be treated as one generic material. PHOENIX also keeps internal cabin-fire questions separate from external thermal-protection-system integrity. It is an evidence-navigation and engineering-triage tool, not a certified fire-prediction system.

## What is actually implemented

| Area | Current capability | Boundary |
|---|---|---|
| Internal Fire Intelligence | Qualitative evidence screen for material, form, oxygen, pressure, airflow, ventilation, ignition, thickness, and suppression observations; flags missing conditions. | No validated ignition probability, flame-spread calculation, or fire-risk score. |
| BASS-II comparison | NASA-reported PMMA-rod example and metadata-compatibility check for a second case. | Does not predict a new test or establish universal material limits. |
| External Integrity | Structured inspection-evidence screen for tiles, RCC, blankets, impacts, cracks, erosion, and attachments. | Does not predict re-entry failure; separate from cabin-fire analysis. |
| Materials Dashboard | Organizes evidence fields for different material families. | No universal material safety ratings. |
| NASA PSI Research | Curated direct links and keyword search to NASA PSI. | No automatic PSI download, ingestion, or parsing. |
| Scientific Interpreter | Authored, curated guidance for selected research questions. | Not a connected generative-AI service. |
| SI Research Dashboard | Transparent, hand-authored topic-relevance ranking across curated investigation families. | Relevance is not experimental quality, material safety, flammability, or mission risk. |

## Likely judge questions and suggested answers

### 1. What problem are you solving?
Spacecraft fire behavior depends on interacting conditions—material composition and form, thickness, oxygen concentration and partial pressure, total pressure, airflow, ignition, and ventilation. Results can be misleading when tests under different conditions are compared as though they were equivalent. PHOENIX makes those conditions visible and structures the evidence review.

### 2. What makes this more than a list of NASA links?
The links are only one part. PHOENIX organizes the engineering question: what material was tested, in what form and geometry, under what atmosphere and flow, and what was actually observed? Its compatibility screen flags important mismatches and missing metadata. The goal is disciplined comparison, not link aggregation.

### 3. Which NASA research does it use?
The prototype is grounded in NASA Physical Sciences Informatics research families, including BASS/BASS-II, SAFFIRE, SAME-R, SPICE, FLEX, and ACME. It reproduces one NASA-reported BASS-II PMMA-rod comparison and links to original NASA investigation records and reports. It does not yet have an automated PSI data-ingestion pipeline, so I do not claim that full PSI datasets are integrated.

### 4. Explain the 13.6% versus 16.0% oxygen example.
The interface presents a NASA-reported example for a quarter-inch PMMA rod: steady flame spreading in BASS-II microgravity at 13.6% oxygen, compared with a reported one-g blowoff condition at 16.0%. That is a 2.4 percentage-point difference between those reported conditions. It illustrates why gravity regime and test conditions matter. It is not a universal ignition threshold, a general PMMA limit, or a prediction for another geometry or apparatus. Ignition and sustained flame propagation are different phenomena.

### 5. Why material-specific analysis?
A polymer film, slab, and rod have different geometries and thermal behavior. Fabrics, composites, and wire insulation introduce other structures and test variables. Thickness, orientation, oxygen, pressure, flow, ignition, and apparatus all matter. PHOENIX deliberately asks for those fields and warns against combining unlike experiments.

### 6. Why separate internal fire from external integrity?
They are different spacecraft-safety engineering domains. Internal fire analysis concerns ignition, flame propagation, smoke, and suppression in cabin materials. External integrity concerns thermal-protection materials and inspection evidence such as impacts, cracks, erosion, and attachments. Their physics, failure modes, and evidence requirements differ, so PHOENIX keeps them separate.

### 7. Is the dashboard using AI?
There is no connected generative-AI model in the current prototype. The Scientific Interpreter contains curated explanations, and the SI Research Dashboard uses a visible rule-based relevance rubric for a small curated set of NASA investigation families. ChatGPT assisted development—ideation, research organization, writing, and coding/debugging—but is not running as an autonomous engine inside PHOENIX.

### 8. What does the SI ranking score mean?
It is a topic-relevance score based on the selected research question, material/phenomenon, and mission context. It helps users decide which curated investigation family to inspect first. It does not evaluate experimental quality, material safety, flammability, or mission risk. The original NASA record must be reviewed.

### 9. Is the interpretation scientifically validated?
No. PHOENIX is a research-triage prototype, not a validated model. It makes missing conditions visible and directs users back to NASA sources. Validation would require source-by-source verification, expert review, a structured evidence database, and comparison against appropriately controlled experimental results.

### 10. Can it tell a crew what suppressant to use or when a vehicle is safe?
No. It does not issue operational commands, certify material safety, or recommend suppression procedures. It helps organize evidence and engineering questions. Mission decisions require validated models, vehicle-specific requirements, qualified engineering review, and established safety procedures.

### 11. What happens when evidence is incomplete?
The tool flags missing fields such as material form, thickness, measured oxygen, total pressure, airflow, ventilation, or ignition evidence. Unknown values should remain unknown; users should not infer a value or compare the test as if every condition were known.

### 12. What are the biggest limitations?
PSI access is through curated direct links rather than automatic data ingestion. The relevance dashboard is rule-based and limited to curated investigation families. The internal screen is qualitative, and the external integrity screen structures inspection questions rather than running a thermal-protection model. PHOENIX is not validated or certified for operational use.

### 13. What would you build next?
First, a traceable PSI data layer with investigation IDs, test-level metadata, documents, units, and provenance. Next, a compatibility engine that distinguishes missing values from mismatched conditions and explains why tests can or cannot be compared. Then domain-expert evaluation and verified, narrowly scoped models—without collapsing different materials or engineering domains into one generic score.

### 14. What did you learn as a builder?
I entered the challenge worried about coding, working from a Chromebook, and learning unfamiliar tools. I decided to learn by building. PHOENIX represents the engineering side of that journey: taking NASA combustion research and asking how evidence can be organized more responsibly for spacecraft safety. I learned to make assumptions visible, preserve limitations, and keep going when the tools were unfamiliar.

## Two-minute demo route

1. **Overview:** State the principle: data informs, physics constrains, tools organize, engineers review, humans decide.
2. **Internal Fire Engine:** Select a material and form. Point out oxygen, pressure, airflow, ventilation, thickness, and ignition fields. Generate the qualitative screen and show missing conditions; do not describe it as a risk score.
3. **BASS-II comparison:** Explain the NASA-reported 13.6% microgravity steady-spread and 16.0% one-g blowoff example. Change a metadata field in Case B to show the compatibility message.
4. **External Integrity:** Select an impact or crack and show inspection priorities. Explain that this is separate from cabin fire.
5. **SI Dashboard / PSI links:** Rank curated investigation families and open a NASA source. Explain that the score is relevance-only and no automatic PSI ingestion or GenAI backend is active.
6. **Close:** “The next step is a traceable experimental evidence layer and expert-reviewed validation.”

## If the live demo fails

**Say:** “The live interface is not loading reliably in this environment, so I do not want to pretend the interaction is working. I can still show the public project, explain the implemented decision logic, and walk through a specific example from the documented source.”

Recovery:
1. Try the public prototype: https://hbourouha-space.github.io/PHOENIX/app/
2. If it does not load, open the repository README: https://github.com/hbourouha-space/PHOENIX
3. Navigate to app/index.html in the repository to show the source implementation.
4. Use the README's NASA PSI and BASS-II links to show the evidence basis.
5. Walk through the BASS-II values and metadata-comparison logic verbally. Do not claim an interaction succeeded if it did not.

## Short answers for difficult moments

- **“Is this a fire simulator?”** No. It is an evidence-organization and qualitative comparison prototype, not a combustion solver.
- **“Is the PSI dashboard live?”** It opens NASA PSI search and curated investigation links; it does not ingest PSI records automatically.
- **“Is the relevance score AI?”** No. It is a transparent, hand-authored rule-based score.
- **“Can I trust 13.6% as a limit?”** No. It is one NASA-reported condition for a specific PMMA rod configuration and gravity regime.
- **“What is the most important design choice?”** Never compare unlike tests as if conditions were interchangeable, and never turn missing evidence into certainty.

## Phrases to avoid

Do not say PHOENIX predicts fire spread, calculates spacecraft fire risk, certifies materials, chooses suppression actions, connects directly to PSI datasets, uses a live generative-AI interpreter, or determines TPS re-entry safety. Those are not current capabilities.

## Reference links

- Repository: https://github.com/hbourouha-space/PHOENIX
- Prototype: https://hbourouha-space.github.io/PHOENIX/app/
- NASA PSI: https://psi.nasa.gov/physci/repo/

**Final reminder:** You do not need to defend PHOENIX as finished. Defend the engineering reasoning, the provenance of the example, the separation of unlike problems, and the honesty of the limitations.
