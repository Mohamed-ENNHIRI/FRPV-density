# FRPV Explorer - 3D France (Commune Level)

This repository hosts the **FRPV Explorer**, an interactive web application that visualizes the density of photovoltaic (PV) rooftops across communes in France in a 3D map. It allows users to explore PV penetration rates and total rooftop counts at a granular level, providing insights into the distribution of solar installations.

---

## Project Overview

The FRPV Explorer aims to provide a clear and interactive visualization of PV rooftop density in France. By leveraging geographic data and rooftop analysis, the tool helps understand the current landscape of solar energy adoption at the commune level. The 3D representation enhances the spatial understanding of PV penetration across the French territory.

---

## Features

* **Interactive 3D Map:** Explore France's communes with a 3D visualization of PV rooftop counts.
* **Commune-Level Data:** View detailed statistics for each commune, including:
    * INSEE Code
    * Total Rooftops
    * PV Rooftops Count
    * PV Penetration Rate
* **Color-Coded Density:** Communes are colored based on their PV rooftop count, with a gradient from low to high density.
* **Height-Based Representation:** The height of each commune's extrusion on the map is proportional to its PV rooftop count, offering an intuitive visual cue of density.
* **Search Functionality:** Easily search for specific communes by name or INSEE code.
* **Responsive Information Panel:** Details about the hovered or selected commune are displayed in real-time.
* **Credits and Information Modal:** Provides details on data sources, original research, and tool development.
* **Dynamic Data Loading:** Efficiently loads geographic (GeoJSON) and PV count (CSV) data.
* **Paris, Lyon, Marseille Aggregation:** Arrondissements of Paris, Lyon, and Marseille are aggregated into their respective main commune codes for a consolidated view.

---

## Technologies Used

* **MapLibre GL JS:** For interactive 3D map rendering.
* **Tailwind CSS:** For modern and responsive UI styling.
* **PapaParse:** For parsing CSV data.
* **Turf.js:** For geospatial analysis, particularly for combining geometries of arrondissements.
* **HTML, CSS, JavaScript:** Core web technologies for the application.

---

## Data Sources

The data visualized on this map is derived from:

* **GeoJSON files:** Processed geographic data for French communes.
* **CSV files:** Containing counts of total and PV-equipped rooftops for each commune.

The original research and data processing are attributed to:

* **Martin Thebault & Boris Nerot:** For their work published in Applied Energy.
    * DOI: [10.1016/j.apenergy.2025.125630](https://doi.org/10.1016/j.apenergy.2025.125630)
    * © 2025 The Author(s). Published by Elsevier Ltd. This is an open access article under the CC BY license.
* **Mohamed ENNHIRI:** For the creation of the original FRPV Explorer tool and the underlying data analysis.

---

## Getting Started

To run the FRPV Explorer locally:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/Mohamed-ENNHIRI/FRPV-density.git](https://github.com/Mohamed-ENNHIRI/FRPV-density.git)
    cd FRPV-density
    ```
2.  **Ensure you have the necessary data files:**
    * `communes-avec-outre-mer.geojson` (should be available from `https://raw.githubusercontent.com/gregoiredavid/france-geojson/master/communes-avec-outre-mer.geojson`)
    * `commune_pv_counts.csv` (this file is expected to be in the root directory or adjust the `PV_COUNTS_CSV_URL` in `count.html`)
3.  **Open `count.html` in your web browser.**

    You can simply open the `count.html` file directly in your browser, or serve it using a local web server (e.g., Python's `http.server`):
    ```bash
    python -m http.server
    ```
    Then, navigate to `http://localhost:8000/count.html` in your browser.

---

## Project Structure
.
├── count.html                  # The main HTML file for the FRPV Explorer web application
├── commune_pv_counts.csv       # CSV file containing PV rooftop counts per commune (expected data)
└── README.md                   # This README file

---

## Contributing

Contributions to improve the FRPV Explorer are welcome! Please feel free to open issues or submit pull requests.

---

## License

This project is open source. Please refer to the specific licenses of the underlying data sources as mentioned in the credits.

---

## Contact

For any questions or further information, please refer to the contact details provided in the original research or associated repository.
