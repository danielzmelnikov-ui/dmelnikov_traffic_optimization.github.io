# Traffic Signal Optimization | Daniel Melnikov

Independent mathematical and simulation research on queue-aware traffic signal control, based on one hour of vehicle observations at Lincoln Street and Green Bay Road in Evanston, Illinois.

## Findings

- **3,122 vehicle arrivals observed** during the studied hour.
- **42.02% lower modeled cumulative queue delay** using queue-aware control versus the optimized fixed-timing baseline in the Phase II model.
- **16.77% lower modeled cumulative queue delay** versus an arrival-only adaptive controller.
- **83,890 modeled vehicle-seconds saved** versus optimized fixed timing, equivalent to approximately 23.3 vehicle-hours in the one-hour model.

These figures are *simulation results using field-observation inputs*, not performance measured after deploying a signal controller.

## Economic scenarios

The website includes an interactive hypothetical impact calculator, a value-of-time sensitivity graph, and conditional fuel/emissions estimates. A sample 25-intersection scenario illustrates network-scale stakes, **not validated citywide savings**. It assumes the same hourly modeled benefit repeated at each site for 500 equivalent hours annually. All calculations and limitations are explained in the complete report.

## Files

- [`Traffic_Signal_Optimization_Full_Report.pdf`](Traffic_Signal_Optimization_Full_Report.pdf): complete **24-page** research report with appended economic-impact analysis.
- [`Traffic_Signal_Optimization_Original_21pages.pdf`](Traffic_Signal_Optimization_Original_21pages.pdf): earlier expanded research report.
- [`index.html`](index.html): standalone responsive project webpage.
- [`assets/`](assets/): figures used on the website and in the new appendix.

## Run the website

Open `index.html` in a browser or enable GitHub Pages (Settings → Pages → Deploy from branch → `main` → `/root`). No build process or external libraries are required.

## Research boundaries

The cameras are a proposed sensing framework, not a deployed computer-vision system. The main traffic input is a single one-hour field observation. The nine geometry scenarios and the new city-scale economic extrapolations are hypothetical. Modeling excludes full traffic-engineering phasing and many real-world constraints. Dollar figures represent hypothetical social time value and fuel costs, **not revenue or verified savings**.
