# AgriScope Kerala — Agricultural Yield & Climate Pattern Analysis

A responsive, GitHub Pages-ready academic project dashboard inspired by the Kerala Data Portal's agriculture sector page. It adds crop analytics, district comparisons, climate visualizations, dataset downloads and a visual big-data pipeline.

## Features

- Dashboard with animated KPI counters and interactive charts
- Crop analytics with search and district filter
- District-wise comparison and CSV export
- Climate trends (illustrative monthly rainfall and temperature)
- Live current weather card using the public Open-Meteo API
- Dataset explorer with downloadable CSV files generated in-browser
- Big data workflow and the 5 Vs
- Responsive sidebar/navigation for mobile and desktop

## Run locally

No build tools or package installation required.

1. Download or clone this repository.
2. Open `index.html` in a browser.
3. For best results, run a local static server (for example, VS Code Live Server).

## Publish using GitHub Pages

1. Create a new GitHub repository, for example `agriscope-kerala`.
2. Upload all files and folders from this project to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Choose branch **main** and folder **/(root)**, then Save.
6. Wait for the deployment workflow to finish. Your website will be available at `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`.

A GitHub Actions workflow is included at `.github/workflows/pages.yml` to publish the static site.

## Data sources and academic integrity

- **Live weather:** Open-Meteo Forecast API, current conditions for Thiruvananthapuram (latitude 8.5241, longitude 76.9366). No API key is required for this public endpoint. Internet access is required.
- **Agricultural reference portal:** [Kerala Data Portal — Agriculture](https://datahub.kerala.gov.in/sector/agriculture).
- **Sample dashboard data:** Crop production, district indicators, monthly rainfall and monthly temperature values in this starter project are illustrative demonstration values. They are NOT official Kerala statistics and should not be cited as measured findings.

Before your final project demonstration, replace sample arrays in `app.js` with verified datasets downloaded from the Kerala Data Portal or other authoritative government sources. Preserve each dataset's source, units, year and geographic coverage in your report.

## Project architecture

```text
Browser
  ├── index.html       Dashboard structure and sections
  ├── style.css        Responsive visual design and animations
  └── app.js           Data arrays, filters, charts, CSV export
          └── Open-Meteo API (live current weather)
```

For a Hadoop/Hive extension, use the same source datasets as input to HDFS, create Hive external tables, clean and aggregate records, and export aggregated results to CSV/JSON for this dashboard.

## Technology

HTML5 · CSS3 · JavaScript · Chart.js · Open-Meteo API · GitHub Pages

## License / attribution

This is an independent academic demonstration and is not affiliated with or endorsed by the Government of Kerala. The Kerala Data Portal is linked as a source for official datasets; follow its attribution and reuse conditions when incorporating its data.
