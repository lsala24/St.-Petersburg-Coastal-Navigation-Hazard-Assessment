# St. Petersburg Coastal Navigation & Hazard Assessment

## 🔗 Project Link
**[View the Interactive StoryMap](https://arcgis.com/stories/3cf9f1975e864b81ba28269a39451c1f)**

<img width="846" height="577" alt="Capture1" src="https://github.com/user-attachments/assets/c3b23354-bad3-4e25-b939-d0f8296f64c1" />

## 📌 Project Summary
This project demonstrates a full-cycle GIS workflow, transforming raw, legacy-encoded maritime data into a modernized, web-ready spatial interface. Focused on the coastal waters of **St. Petersburg, Florida**, the analysis provides a **Common Operating Picture** for identifying navigation assets and submerged hazards. 

By bridging the gap between complex **S-57** data standards and intuitive web cartography, this repository showcases skills in data engineering, schema refactoring, and workflow automation.

## 🛠️ Tech Stack & Skills
* **GIS Software:** QGIS 3.x, ArcGIS Online
* **Workflow Automation:** QGIS Graphical Modeler (Spatial Logic & Batch Processing)
* **Data Engineering:** SQL (CASE Expressions), Schema Mapping, Attribute Refactoring
* **Database Management:** OGC GeoPackage (.gpkg) Optimization
* **Narrative Design:** ArcGIS StoryMaps

## 🚀 Key Workflow Phases

### 1. Schema Refactoring & Logic
Initial S-57 hydrographic data utilized numeric legacy encoding (e.g., `BOYSHP` values as integers). I performed a comprehensive refactoring of these attribute tables using **CASE WHEN** logic in QGIS to map these codes into human-readable categories such as "Pillar," "Can," and "Conical" buoy structures.

### 2. Attribute Optimization
To ensure the data was stakeholder-ready, I addressed database constraints by configuring **Field Aliases**. This step corrected truncated headers and transformed cryptic database shorthand into professional, descriptive titles.

### 3. Spatial Logic Automation
To identify high-risk areas, I developed a custom **Graphical Model** within QGIS. This visual workflow automates the intersection of bathymetric thresholds and navigation hazards:
* **Bathymetric Extraction:** The model filters contours to a critical **5.4-meter** depth, defining the nearshore transition zone.
* **Proximity Analysis:** By automating an intersection between **30-meter hazard buffers** and the bathymetry shelf, the workflow isolates the most significant obstacles to maritime safety.
* **Consistency:** This approach ensures the analysis is repeatable and can be rapidly re-run as hydrographic data is updated.

<img width="702" height="451" alt="Navigation_hazard_zone_tool" src="https://github.com/user-attachments/assets/00a922c6-26fb-40be-81ac-0c488b13cdc8" />

### 4. Data Portability & Storage
To prioritize data integrity, all processed layers—including **Navigation Assets**, **Safety Hazards**, and **Bathymetry**—were exported into a unified **OGC GeoPackage**. This approach ensures a centralized, cross-platform spatial database ready for deployment.

### 5. Interactive Web Deployment
The final data was hosted via **ArcGIS Online** and integrated into a high-contrast web map. By utilizing the **ArcGIS Oceans** basemap and professional symbology, the map provides immediate clarity for maritime risk assessment and asset management.

## 📊 Data Sources
* **S-57 Hydrographic Data:** NOAA Office of Coast Survey
* **Basemap Integration:** Esri ArcGIS Oceans
* **Study Area:** St. Petersburg Coastal Environment, FL
