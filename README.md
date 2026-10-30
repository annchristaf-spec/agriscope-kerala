
# AgriScope Kerala — Agricultural Yield & Climate Pattern Analysis

A responsive, GitHub Pages-ready academic project dashboard inspired by the Kerala Data Portal's agriculture sector page. It provides crop analytics, district comparisons, climate visualizations, dataset downloads, live weather information, and a visual Big Data processing pipeline.

## Features

- Interactive dashboard with animated KPI counters and charts
- Crop analytics with search and district filters
- District-wise comparison and CSV export
- Climate trends with monthly rainfall and temperature visualizations
- Live current weather using the public Open-Meteo API
- Dataset explorer with downloadable CSV files generated in the browser
- Big Data workflow visualization and explanation of the 5 Vs
- Responsive sidebar and navigation for mobile and desktop
- GitHub Pages deployment support

## Run Locally

No build tools or package installation are required.

1. Download or clone this repository.
2. Open `index.html` in a web browser.
3. For best results, run a local static server, such as the VS Code Live Server extension.
4. Ensure you have an internet connection for live weather information and externally loaded chart libraries.

## Publish Using GitHub Pages

1. Create a new GitHub repository, for example `agriscope-kerala`.
2. Upload all project files and folders directly to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Choose branch `main` and folder `/ (root)`.
6. Click **Save**.
7. Wait for GitHub Pages to finish deployment.
8. Open the published website using the URL shown in the Pages settings.

Your website URL will follow this format:

`https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`

A GitHub Actions workflow is included at `.github/workflows/pages.yml` for static website deployment.

## Data Sources and Academic Integrity

### Live Weather Data

- **Source:** Open-Meteo Forecast API
- **Location:** Thiruvananthapuram, Kerala
- **Latitude:** 8.5241
- **Longitude:** 76.9366
- **API:** https://api.open-meteo.com/
- **API key:** Not required for the public endpoint used by this project.

Internet access is required to retrieve live weather information.

### Agricultural Data Source

The Kerala Data Portal provides access to government datasets related to agriculture.

Source: https://datahub.kerala.gov.in/sector/agriculture

### Sample Dashboard Data

Crop production, district indicators, monthly rainfall and monthly temperature values in the starter project are illustrative demonstration values. They are not official Kerala statistics and must not be presented as measured findings.

Before the final project demonstration:

1. Download relevant datasets from the Kerala Data Portal or other authoritative government sources.
2. Replace the illustrative data arrays in `app.js` with verified datasets.
3. Preserve the dataset's source, units, year and geographic coverage.
4. Document any data cleaning, missing-value handling and transformations.
5. Cite the original data sources in your project report and presentation.

## Project Architecture

AgriScope Kerala follows a modular web-based architecture that integrates data input, processing, visualization and deployment.

### System Architecture

```text
                  AGRISCOPE KERALA
                          |
                  GITHUB PAGES HOSTING
                          |
                     USER BROWSER
                          |
           +--------------+--------------+
           |              |              |
       index.html      style.css       app.js
           |              |              |
       Dashboard       UI Design     Data Processing
       Structure       Animations         |
                                       +--+----------+
                                       |  |          |
                                     Charts Filters CSV Export
                                       |
                               +-------+--------+
                               |                |
                           Sample Data      Open-Meteo API
                               |                |
                         Crop and Climate   Live Weather
                         Demonstrations       Data

                  DATA STORAGE / FUTURE INPUT
                               |
                           data folder
                               |
                     Official Kerala Datasets
                               |
                      Data Cleaning and
                        Preparation

                   FUTURE BIG DATA EXTENSION
                               |
                          Hadoop / HDFS
                               |
                          Apache Hive
                               |
                     Data Cleaning, Joining
                       and Aggregation
                               |
                       Aggregated CSV/JSON
                               |
                       AgriScope Dashboard
```

### Architecture Components

**1. Frontend Layer**

HTML5 defines the dashboard structure and content. CSS3 provides responsive layouts, styling and animations. JavaScript supports user interactions and dashboard functionality.

**2. Data Processing Layer**

JavaScript manages the dashboard's data arrays, filtering, calculations, chart updates and CSV export.

**3. Visualization Layer**

Chart.js is used to display charts and visual comparisons, helping users explore agricultural and climate patterns.

**4. External Data Layer**

The Open-Meteo API supplies live weather information for Thiruvananthapuram. The application requires an internet connection to retrieve this information.

**5. Data Storage Layer**

The `data/` directory contains dataset-related documentation and is reserved for source datasets and future data integration.

**6. Big Data Processing Layer — Proposed Extension**

Hadoop Distributed File System (HDFS) and Apache Hive can be integrated to store, clean, join and aggregate large agricultural datasets. The processed results can be exported to CSV or JSON and used by the dashboard.

**7. Deployment Layer**

GitHub Pages hosts the static website and makes it accessible through a public URL.

### Current Implementation vs Proposed Extension

| Component | Status |
|---|---|
| HTML, CSS and JavaScript dashboard | Implemented |
| Interactive charts and filters | Implemented |
| CSV export | Implemented |
| Live Open-Meteo weather | Implemented |
| Hadoop and HDFS integration | Proposed extension |
| Apache Hive processing | Proposed extension |
| Automated pipeline from Hive to dashboard | Proposed extension |

**Important:** Hadoop and Hive are proposed extensions and are not currently implemented in this website. The current dashboard processes its demonstration data in the browser.

## Big Data Concepts

The project can demonstrate how agricultural data analysis relates to the 5 Vs of Big Data.

- **Volume:** Large amounts of agricultural production, rainfall and temperature records.
- **Velocity:** Weather observations and newly collected agricultural records arriving over time.
- **Variety:** Structured datasets containing crop types, locations, production values and climate measurements.
- **Veracity:** Data quality, accuracy, consistency and reliability of the source.
- **Value:** Useful insights into agricultural yield and climate patterns to support further analysis.

These concepts describe the project's analytical goals. A production-scale Big Data implementation would require the proposed distributed storage and processing components.

## Proposed Hadoop and Hive Workflow

1. Collect verified agricultural and climate datasets.
2. Upload the source files to HDFS.
3. Create Hive tables for the agricultural and climate datasets.
4. Clean records and handle missing or inconsistent values.
5. Join datasets using appropriate location and time fields.
6. Calculate summaries and aggregates, such as district-wise crop production and rainfall averages.
7. Export the aggregated results to CSV or JSON.
8. Load the processed results into the AgriScope Kerala dashboard.

This workflow describes a possible extension; it is not part of the currently implemented static website.

## Technology

- HTML5
- CSS3
- JavaScript
- Chart.js
- Open-Meteo API
- GitHub Pages
- Hadoop and HDFS — proposed extension
- Apache Hive — proposed extension

## Future Enhancements

- Integration of verified government agricultural datasets
- Hadoop and Hive-based distributed data processing
- Historical climate and crop yield trend analysis
- More district-wise and crop-wise comparisons
- Improved data validation and missing-value handling
- Predictive analytics using suitable statistical or machine learning models
- Automated data updates and dashboard refreshes

## License and Attribution

This is an independent academic demonstration and is not affiliated with or endorsed by the Government of Kerala.

The Kerala Data Portal is referenced as a potential source of official datasets. Follow the relevant attribution, licensing and reuse conditions when incorporating its data.

Open-Meteo is used for live weather information. Refer to its official website for API documentation and applicable usage terms:

https://open-meteo.com/
