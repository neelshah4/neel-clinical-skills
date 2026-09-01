# Neel Clinical Skills

Eleven interactive teaching tools for pediatric and adult critical care. Each one is a single
self-contained HTML page: open it, move the inputs, and watch the physiology or the diagnostic
reasoning change. No install, no account, no server. Nothing you type leaves your browser.

**Live site: https://neelshah4.github.io/neel-clinical-skills/**

Every tool is independently linkable. You can send a colleague one URL and they get exactly that tool.

> These are teaching tools, not medical devices, and not for autonomous clinical decision-making.
> Read [DISCLAIMER.md](DISCLAIMER.md) before using any of them with a patient in mind.

## The tools

| Tool | What it does |
|---|---|
| [V-V ECMO Oxygenation Calculator](tools/vv-ecmo-oxygenation-calculator.html) | Solves the venovenous mixing equation in both directions. Enter cardiac output and it predicts arterial saturation; enter a measured SaO2 and it solves for cardiac output. Recirculation fraction, hemoglobin, and oxygen delivery are all live inputs. |
| [CO2 Gap and ScvO2 Interpreter](tools/co2-gap-scvo2-interpreter.html) | Reads PaCO2, PvCO2, ScvO2 and lactate through three stacked tiers: the venoarterial CO2 gap, the macrocirculatory versus microcirculatory pattern, and anaerobic stratification. Returns a verdict, the edge cases that break the gap, and what to do next. |
| [ICU CBC Interpreter](tools/icu-cbc-interpreter.html) | Bedside CBC interpretation through a sepsis lens, with the evidence graded per finding and nine confounders you can switch on: steroids, G-CSF, recent chemotherapy, asplenia, hematologic malignancy, recent seizure, late pregnancy, beta-agonist infusion, recent transfusion. |
| [Pediatric AKI Risk Tool](tools/pediatric-aki-risk-tool.html) | Renal angina index tracked day by day, with a Bayesian layer that moves a pretest severe-AKI rate to a posttest probability using urinary NGAL and cystatin C. |
| [Albuterol Delivery During HFNC](tools/albuterol-hfnc-delivery.html) | Charts inhaled lung dose as a percentage of the nominal nebulizer dose against high-flow nasal cannula flow rate, so the flow-versus-delivery tradeoff is visible rather than asserted. |
| [PRx, CPPopt and the MAP Challenge](tools/prx-cppopt-map-challenge.html) | Cerebral autoregulation made concrete: animated pressure-reactivity waveforms, a PRx versus CPP U-curve you can move, a norepinephrine and MAP challenge simulator, and a walkthrough of the protocol. |
| [The Venous Return Wars](tools/venous-return-wars.html) | An interactive teaching essay on the Guyton versus Brengelmann dispute, with three live rigs you drive yourself: two tanks and a pump, a venous return curve you can reshape, and a vasodilate-then-defend-blood-pressure sequence. |
| [Critical Asthma: Drugs, Noninvasive Support, and the Ventilator](tools/asthma-critical-care.html) | Ten agents in one pharmacology table that shows where its sources disagree rather than averaging them, a toxicity matrix for what stacks when three drugs run at once, an interactive Campbell diagram for CPAP and BiPAP, and two PEEP schematics built from adult physiology that is labelled as adult. |
| [Ventilator Fundamentals](tools/ventilator-fundamentals.html) | The equation of motion, made movable. Pressure, flow and volume are solved live rather than drawn, so changing compliance or resistance redraws real curves. Covers holds and what each measures, volume control against pressure control and PRVC, trigger types, and how inspiratory time, rise time and cycle-off work. |
| [Ventilator Advanced](tools/ventilator-advanced.html) | Patient effort graphed against ventilator pressure; why PRVC withdraws support as the patient works harder while pressure control holds it constant; the decremental trial that finds best-compliance PEEP; and deadspace against shunt. |
| [ARDS Inflammatory Subphenotypes](tools/ards-subphenotype-explorer.html) | Exploratory only. Runs the published hypo- and hyperinflammatory classifiers that print their coefficients, refuses the ones that do not, and reports a range rather than a number when an input is missing. Pediatric results carry how poorly the adult signature transports to children. |

## How to use them

Open the live site and pick a tool, or click any link above. Everything runs client side.

To run them offline, clone the repository and open any file in `tools/` directly. A few pages pull
fonts or a charting library from a CDN, so a page opened without a network connection will fall back
to system fonts and, in two cases, will not draw its figures.

```bash
git clone https://github.com/neelshah4/neel-clinical-skills.git
open neel-clinical-skills/index.html
```

## How the evidence is handled

Every quantitative claim in these tools was put through a literature refresh and then independently
audited by agents that did not write the file. Identifiers are resolved against PubMed and Crossref
rather than recalled, and a sample of every tool's verified identifiers is re-fetched blind and
compared before release.

Some numbers here never had a citation to begin with: consensus thresholds, likelihood ratios derived
from a pooled AUROC, delivery percentages synthesized across bench studies. Those are kept and
labelled as derived rather than deleted or dressed up as directly reported. Where a tool says a number
is an approximation, believe it.

If you find an error, open an issue. Corrections to clinical content are the most useful contribution
anyone can make here.

## Contributing

Issues and pull requests are welcome, particularly for clinical accuracy. Please keep each tool a
single self-contained HTML file with no build step, and keep the disclaimer and the evidence labelling
intact.

## License

[CC BY-NC 4.0](LICENSE). Attribution required, non-commercial use only.

Neel Shah, MD, Pediatric Critical Care Medicine, Washington University in St. Louis.
