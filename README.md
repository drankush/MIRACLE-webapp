# MIRACLE-WebApp 🌟
## Pediatric CMR Reference Calculator

[![SCMR 2026](https://img.shields.io/badge/SCMR-2026%20Submission-red.svg)](https://scmr.org)
[![Open Source](https://img.shields.io/badge/Open-Source-green.svg)](https://github.com/drankush/MIRACLE)
[![License: MIT](https://img.shields.io/badge/License-MIT-crimson.svg)](https://opensource.org/licenses/MIT)
[![MIRACLE API](https://img.shields.io/badge/Powered%20by-MIRACLE%20API-blue)](https://miracleapi.readme.io/)
[![Surge Demo](https://img.shields.io/badge/WebApp-Surge-yellow.svg)](https://miracle-app.surge.sh)

> A web-based calculator demonstrating the application of MIRACLE API for pediatric cardiac MRI reference values. Part of SCMR 2026 Innovative Open Source Submission.

**Live Demo**: [miracle-app.surge.sh](https://miracle-app.surge.sh/)

## 🎯 Overview

This web application demonstrates the practical implementation of the MIRACLE API for calculating z-scores and percentiles for pediatric cardiac MRI measurements. While this demo focuses on volumetric references, the MIRACLE API offers many more endpoints for comprehensive cardiovascular MRI analysis.

🔗 [View Full API Documentation](https://miracleapi.readme.io/)

## ✨ Features

- 📏 Input cardiac measurements in preferred units (cm/in, kg/lb)
- 🧮 Automatic BSA calculation using Haycock formula
- 📊 Instant z-scores and percentile calculations
- 📈 Reference ranges (3rd, 50th, 97th percentiles)
- 🖨️ Print-friendly reports with patient details

## 🛠️ How It Works

### API Integration
The application makes REST calls to two MIRACLE API endpoints:
```javascript
const ATRIAL_API_URL = 'https://script.google.com/macros/s/...';
const VENTRICULAR_API_URL = 'https://script.google.com/macros/s/...';
```

### Calculating Z-Scores
```javascript
const response = await fetch(
    `${VENTRICULAR_API_URL}?domain=Pediatric_Ventricle&parameter=${param}&gender=${gender}&measured=${value}&ht_cm=${ht_cm}&wt_kg=${wt_kg}`
);
```

### Print Function
Generates a professional report with:
- Patient demographics
- BSA calculation
- Measurement results
- Reference ranges
```javascript
function printResults() {
    const { ht_cm, wt_kg } = convertToMetric();
    const bsa = calculateBSA(ht_cm, wt_kg);
    // Creates printable report
}
```

## 🎯 Use Cases

1. **Clinical Practice**
   - Quick reference value lookup during CMR reporting
   - Standardized reporting with z-scores
   - Printable reports for patient records

2. **Research**
   - Batch processing of measurements
   - Standardized data collection
   - Easy integration with research workflows

3. **Education**
   - Teaching tool for trainees
   - Understanding normal ranges
   - Demonstrating the impact of BSA indexing

## 🔮 Available Endpoints

This demo showcases only volumetric measurements. The MIRACLE API offers many more endpoints including:
- Flow measurements
- Myocardial strain
- T1/T2 mapping
- And more...

Visit [MIRACLE API Documentation](https://miracleapi.readme.io/) for the complete list.

## 🚀 Getting Started

1. Clone the repository
2. Open `index.html` in a browser
3. Enter patient details and measurements
4. Click "Calculate Z-scores"
5. Print or save results as needed

## 📄 License

MIT License - feel free to use and modify for your needs.

## 🙏 Acknowledgments

- MIRACLE API developers
- SCMR Open Source Initiative
- Contributors and testers

## 📧 Contact

For questions about:
- MIRACLE API: [API Documentation](https://miracleapi.readme.io/)
- This Web App: [GitHub Issues](https://github.com/drankush/MIRACLE-webapp/issues)
