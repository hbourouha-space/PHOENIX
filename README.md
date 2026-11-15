
# PHOENIX
### Proactive Hazard Observation, Isolation and Extinction Network for eXtreme Environments

**DETECT EARLY. ASSESS THE RISK. PROTECT THE CREW.**

## The Challenge

A small ignition event inside a spacecraft can develop into a serious threat to crew safety. In confined spacecraft environments, fire behavior is affected by material properties, oxygen concentration, pressure, airflow, geometry and ventilation.

NASA has conducted numerous combustion investigations in space. However, locating, comparing and interpreting the scientific evidence across these investigations can be challenging.

## Our Solution

PHOENIX is a research and engineering decision-support prototype designed to organize NASA combustion science and translate experimental evidence into insights relevant to spacecraft fire safety. AI-assisted interpretation is part of the intended architecture, but a generative-AI model is not connected in the current prototype.

It focuses on three interconnected priorities:

1. **Prevention:** Understand ignition conditions and material-specific fire behavior.
2. **Detection:** Interpret combustion products, smoke characteristics and sensor evidence.
3. **Suppression:** Evaluate extinction, flame displacement, reignition and potential secondary ignition.

## NASA Research Foundation

PHOENIX uses NASA's Physical Sciences Informatics (PSI) repository as its primary research reference.

Featured investigations include:

- **BASS-II:** Solid-fuel ignition, flame spread and extinction in microgravity.
- **SAFFIRE-I:** Spacecraft-scale fire behavior and combustion measurements.
- **SAME-R:** Smoke aerosol characteristics and detector response.
- **SPICE:** Solid- and gaseous-fuel combustion research in a fan-driven duct configuration; review each test's fuel, geometry and flow conditions.
- **ACME:** Combustion experiments aboard the International Space Station.
- **FLEX:** Flame-extinguishment research examining CO₂ and helium dilution. Do not conflate it with separate droplet-combustion investigations.

NASA source: https://psi.nasa.gov/physci/repo/

## Engineering Approach

PHOENIX emphasizes material-specific analysis rather than applying one generic fire model to every spacecraft material.

Relevant variables include:

- Material composition and geometry
- Thickness and orientation
- Oxygen concentration and partial pressure
- Total pressure
- Airflow and ventilation configuration
- Ignition conditions
- Flame propagation and extinction observations
- Smoke and combustion-product measurements

## Two Engineering Domains

### 1. Internal Fire Intelligence

Focuses on cabin materials, ignition, flame propagation, smoke generation, detection and suppression.

### 2. External Integrity Intelligence

Explores spacecraft thermal-protection integrity, including thermal protection systems, insulation and impact-related damage. This is a separate engineering domain and requires different models and evidence.

## PHOENIX Architecture

The intended architecture combines:

- NASA research discovery and source traceability
- Structured experimental metadata
- Scientific comparison and engineering analysis
- A planned AI scientific interpreter grounded in retrieved research (not connected in this prototype)
- Mission-oriented research applications

**Physics models calculate. Research tools organize. AI-assisted interpretation is a future development direction. PHOENIX makes the evidence easier to examine.**

## Live Demonstration

Open the PHOENIX prototype: https://hbourouha-space.github.io/PHOENIX/app/

The application is organized into an overview, internal fire evidence screen, BASS-II experimental comparison, external integrity screen, materials dashboard, NASA research links, curated scientific interpreter, an interactive SI Research Dashboard and engineering workflow.

The NASA PSI Research and Scientific Interpreter sections include keyword-search links that open matching investigation results directly on NASA PSI. The SI Research Dashboard provides transparent, rule-based relevance ranking across curated investigation families based on the selected mission environment and fire-safety question. Its scores indicate topic relevance only—not experimental quality, material safety, flammability or mission risk. The prototype does not automatically ingest PSI records or use a connected generative-AI model. Users should verify findings against original NASA records and cite the investigation DOI where available.

The BASS-II comparison panel presents a NASA-reported PMMA rod example and includes an interactive metadata compatibility check. The check flags selected differences and missing fields; it is not a predictive combustion model.

## Current Prototype Status

The current GitHub prototype includes an interactive research catalogue, investigation links, guided scientific interpretation prompts, a curated rule-based relevance-ranking dashboard and engineering principles.

The live NASA repository connection and generative AI backend remain development objectives and are not represented as operational features in this version.

## Scientific Integrity and Limitations

PHOENIX is a research prototype, not a certified spacecraft fire-safety system.

- Experimental conditions must be preserved when comparing investigations.
- Unknown measurements must remain unknown.
- Results from gaseous flames, liquid droplets and solid materials must not be treated as interchangeable.
- Blowoff must not automatically be interpreted as extinction.
- Any future AI-generated interpretations must be traceable to original scientific evidence.
- Mission-specific safety decisions require validated engineering models and qualified review.

## Project Repository

GitHub: https://github.com/hbourouha-space/PHOENIX

NASA PSI: https://psi.nasa.gov/physci/repo/

---

**PHOENIX — Turning combustion science into crew protection.**
