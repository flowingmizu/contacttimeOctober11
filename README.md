Mizuverse Labs · Chlorine Contact Time (CT) Simulator
Module 4 · Disinfect: an interactive training simulator that teaches how water treatment operators prove disinfection with one number:
CT = C × T₁₀
Learners run a virtual clearwell, work through real operator math, set chlorine doses across three seasons, and live with the consequences.
Stay curious. Stay clear.
🔗 Live demo: https://flowingmizu.github.io/REPO-NAME/ 🧭 Guided tour: add #tour to the end of the link, e.g. https://flowingmizu.github.io/REPO-NAME/#tour
Why this exists
Experienced water operators are retiring, and new operators rarely get a safe place to practise lab work and dosing decisions before they touch real equipment. Mizuverse Labs closes that gap with simulations that connect textbook calculations to real plant decisions.
Every module follows the same learning loop: Observe → Experiment → Interpret → Decide → See consequences.
The Mizuverse Labs pathway
One river, one connected story: the same seasonal source water runs through every module.
#	Module	Focus
1	Stock Solution	Dilution math, C₁V₁ = C₂V₂
2	Alkalinity Titration	pH vs alkalinity, buffering capacity
3	Jar Test	Coagulation optimisation, alum dosing
4	Chlorine Contact Time	Disinfection, CT compliance
Roadmap	Chloramines · UV · Ozone · Distribution	
What's inside this module
Warm-up quiz: three questions, with lab equipment rewards.
Learn
An animated tracer study: release dye into an unbaffled or a serpentine-baffled clearwell and watch short-circuiting happen.
EPA baffling factors (0.1 to 1.0) and what T₁₀ means.
A pH slider showing the HOCl / OCl⁻ split.
Worked math: HDT → T₁₀ → CT on the same plant used in the challenge.
Operator practice: 10 randomised problems (flow conversion, HDT, T₁₀, CT, feed rate, demand, HOCl %). Answers within 2% count.
Seasonal disinfection challenge: set the chlorine dose for three seasons:
Spring Snowmelt (6 °C, pH 7.2): cold water raises the CT required.
Summer Dry (24 °C, pH 8.1): residual decays before the first customer.
Autumn Rain (14 °C, pH 6.8): organics raise chlorine demand and by-product risk.
Each decision is judged at the worst case (peak flow, minimum clearwell level) and graded from CT failure to Optimised. Learners must also defend their dose.
Compare seasons: a table and chart of CT calculated vs CT required.
Final quiz: 15 exam-style questions drawn from a bank of 27, covering concepts and operator calculations. 70% (11/15) is a pass; 13+ earns the tardigrade badge.
Training summary: an operator-readiness profile (Dose Selection, Process Control, Water Quality Interpretation, Treatment Optimisation), plus study notes.
Extras
A "My Lab" equipment shelf to collect: gloves, DPD kit, colorimeter, tracer dye, sample bottle.
Progress saves automatically in the browser.
Key formulas used
Quantity	Formula
Flow conversion	gpm = MGD × 1,000,000 ÷ 1,440
Hydraulic detention time	HDT = volume (gal) ÷ flow (gpm)
Credited contact time	T₁₀ = HDT × baffling factor
Contact value	CT = residual C (mg/L) × T₁₀ (min)
Compliance	CT calculated ≥ CT required
Chlorine feed rate	lb/day = dose (mg/L) × flow (MGD) × 8.34
Chlorine demand	demand = dose − residual
How to run
The simulator is a single self-contained HTML file. No build step and no install.
Online: open the GitHub Pages link above.
Locally: download index.html and open it in any modern browser.
For GitHub Pages: go to Settings → Pages → Deploy from branch → main / root. Keep the file named index.html.
Tech
Plain HTML, CSS and JavaScript in one file.
Chart.js 4.4.1 via the cdnjs CDN, for the residual decay and season comparison charts.
Lexend via Google Fonts.
Progress is stored in localStorage, wrapped in try/catch so the page still works in private windows.
Responsive layout for laptops, tablets and phones.
Model notes and assumptions
All plant constants live in one CONFIG object at the top of the script, so instructors can review and adjust them.
Plant: 1.2 MGD average, 2.0 MGD peak flow. Clearwell 120,000 / 160,000 / 200,000 gal (minimum / normal / high). Tracer-study baffling factor 0.3.
Log credit: 0.5-log Giardia inactivation is required from disinfection, assuming conventional filtration earns 2.5 of the 3 logs required by the Surface Water Treatment Rule.
CT required: calculated with the EPA regression equation for free chlorine and Giardia. ⚠️ Verify against the SWTR Guidance Manual CT tables before classroom release.
HOCl fraction: a temperature-adjusted pKa.
Chlorine decay, demand and by-product risk: simplified teaching models, not plant-specific predictions.
Residual targets: at least 0.2 mg/L at the first customer, and below the 4.0 mg/L MRDL.
Disclaimer
This simulator is for educational practice only. It supplements, but does not replace, hands-on laboratory and plant training. It does not award certification. Always follow your state regulations, your utility's procedures, and the official EPA guidance.
About
Mizuverse Labs creates interactive water treatment learning tools for high school and trade school students, entry-level operators and workforce programs. Developed during a water treatment internship at Clackamas Community College (WET 280).
Mascot: Tardi the tardigrade 🐻💧
© 2026 Irene Susanto · Mizuverse Labs. All rights reserved.

