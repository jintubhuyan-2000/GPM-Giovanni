# NASA Giovanni Area-Averaged Time Series

A desktop application for extracting and visualizing **area-averaged time-series data from NASA Giovanni** using user-defined geographic regions. The application is designed to simplify the process of selecting an Area of Interest (AOI), querying NASA Earthdata/Giovanni, processing the returned data, and generating time-series visualizations and outputs.

---

## 🌎 Overview

**NASA Giovanni Area-Averaged Time Series** provides a graphical interface for analyzing satellite and Earth observation datasets available through NASA Giovanni.

The application allows users to:

* Select an Area of Interest (AOI)
* Load **KML/KMZ** boundaries
* Generate spatial grids over an AOI
* Authenticate with **NASA Earthdata**
* Query NASA Giovanni services
* Extract area-averaged time-series data
* Visualize temporal variations
* Export results for further analysis
* Generate spatial/temporal outputs for Earth observation applications

The application is particularly useful for **remote sensing, environmental monitoring, climate analysis, disaster management, and geospatial research**.

---

## ✨ Key Features

### 🗺️ Area of Interest

The application supports:

* KML files
* KMZ files
* Polygon-based AOIs
* Point-based analysis
* User-defined spatial regions

### 🌐 NASA Earthdata Authentication

Users can authenticate using their NASA Earthdata credentials to access available Giovanni services and datasets.

### 📊 Area-Averaged Time Series

The application retrieves temporal information over the selected region and provides time-series visualization for analysis.

### 📈 Visualization

The application provides graphical visualization of retrieved time-series data, making it easier to identify:

* Temporal trends
* Seasonal variations
* Extreme events
* Changes in environmental variables
* Long-term patterns

### 📁 Data Export

Processed results can be exported for further analysis and reporting.

Supported output workflows include spreadsheet-based analysis and graphical outputs.

### 🌍 Geospatial Processing

The application uses geospatial libraries for:

* Polygon processing
* Spatial operations
* Grid generation
* Coordinate handling
* AOI processing

---

# 🖥️ Application Workflow

```text
                    NASA Giovanni
                         │
                         ▼
                 Launch Application
                         │
                         ▼
                 NASA Earthdata Login
                         │
                         ▼
                  Select / Load AOI
                         │
                 ┌───────┴────────┐
                 │                │
                KML              KMZ
                 │                │
                 └───────┬────────┘
                         ▼
                  Process Geometry
                         │
                         ▼
                  Generate Grid
                         │
                         ▼
                 Select Parameters
                         │
                         ▼
                  Query Giovanni
                         │
                         ▼
                 Retrieve Results
                         │
                         ▼
                 Process Time Series
                         │
                         ▼
                  Visualization
                         │
                         ▼
                 Export Results
```

---

# 🧰 Technologies Used

The application is developed using **Python** and several scientific, geospatial, visualization, and NASA Earthdata-related libraries.

| Component             | Technology     |
| --------------------- | -------------- |
| Programming Language  | Python         |
| GUI                   | Tkinter        |
| Numerical Processing  | NumPy          |
| Data Processing       | Pandas         |
| Visualization         | Matplotlib     |
| Geospatial Processing | Shapely        |
| NASA Data Access      | Earthaccess    |
| Spreadsheet Output    | OpenPyXL       |
| Data Source           | NASA Giovanni  |
| Authentication        | NASA Earthdata |
| Packaging             | PyInstaller    |
| Installer             | Inno Setup     |

---

# 📦 Installation

## Windows Executable

A standalone Windows executable can be generated using PyInstaller.

The recommended build is a **one-directory (`onedir`) application**, particularly because the application uses several large scientific and geospatial Python libraries.

Example:

```bash
pyinstaller --clean --noconfirm --onedir --windowed \
--name "NASA_Giovanni_TimeSeries" \
"Giovanni_GUI_with_Professional_Splash_Deepseek.py"
```

The executable will be generated under:

```text
dist/
└── NASA_Giovanni_TimeSeries/
    └── NASA_Giovanni_TimeSeries.exe
```

---

# 🔐 NASA Earthdata Account

The application requires access to NASA Earthdata/Giovanni services.

Users should have an active NASA Earthdata account before using authenticated services.

NASA Earthdata:

[NASA Earthdata](https://www.earthdata.nasa.gov/?utm_source=chatgpt.com)

---

# 🚀 Running the Application

After installation, launch:

```text
NASA_Giovanni_TimeSeries.exe
```

The application displays a startup screen while the required components are initialized.

After initialization, the main Giovanni interface is displayed.

---

# 📂 Input Data

The application can work with geographic boundaries provided as:

```text
.kml
.kmz
```

A typical workflow is:

```text
KML/KMZ
   ↓
AOI extraction
   ↓
Geometry processing
   ↓
Spatial grid
   ↓
Giovanni query
```

---

# 📊 Typical Applications

The tool can be used for Earth observation and environmental studies such as:

* 🌧️ Rainfall analysis
* 🌡️ Land surface temperature analysis
* 🌿 Vegetation monitoring
* 🔥 Fire and climate analysis
* 🌊 Flood-related environmental analysis
* 🌍 Climate variability studies
* ☁️ Atmospheric analysis
* 🌾 Agricultural monitoring
* 🛰️ Satellite-based environmental assessment

---

# 🛰️ NASA Giovanni

The application is designed around NASA Giovanni, which provides a web-based environment for exploring and analyzing NASA Earth science data.

NASA Giovanni:

[NASA Giovanni](https://giovanni.gsfc.nasa.gov/giovanni/?utm_source=chatgpt.com)

---

# 📋 Example Workflow

### Step 1 — Start the application

Launch:

```text
NASA_Giovanni_TimeSeries.exe
```

### Step 2 — Authenticate

Enter the required NASA Earthdata credentials.

### Step 3 — Select AOI

Load a:

```text
KML / KMZ
```

file.

### Step 4 — Define analysis parameters

Select the required temporal and spatial parameters.

### Step 5 — Query NASA Giovanni

The application retrieves the required data.

### Step 6 — Generate time series

The returned data are processed into an area-averaged temporal dataset.

### Step 7 — Visualize

The application generates the corresponding time-series graph.

### Step 8 — Export

Results can be saved for additional analysis and reporting.

---

# 🔧 Development

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/NASA-Giovanni-TimeSeries.git
```

Navigate to the project:

```bash
cd NASA-Giovanni-TimeSeries
```

Install dependencies:

```bash
pip install numpy pandas matplotlib shapely earthaccess openpyxl
```

Run the application:

```bash
python Giovanni_GUI_with_Professional_Splash_Deepseek.py
```

---

# 📦 Building the Windows Application

For a production Windows executable:

```bash
pyinstaller --clean --noconfirm --onedir --windowed \
--name "NASA_Giovanni_TimeSeries" \
"Giovanni_GUI_with_Professional_Splash_Deepseek.py"
```

The resulting application will be available in:

```text
dist/NASA_Giovanni_TimeSeries/
```

---

# 🛠️ Packaging with Inno Setup

The generated PyInstaller application can be distributed using **Inno Setup**.

Recommended structure:

```text
dist/
└── NASA_Giovanni_TimeSeries/
    ├── NASA_Giovanni_TimeSeries.exe
    ├── Python runtime
    ├── NumPy
    ├── Pandas
    ├── Matplotlib
    ├── Shapely
    ├── Earthaccess
    └── Dependencies
```

The complete directory should be included in the installer.

---

# ⚠️ Notes

* An active NASA Earthdata account may be required for authenticated data access.
* Internet connectivity is required for remote NASA services.
* Application startup time can depend on the packaged Python environment and installed scientific libraries.
* Do not distribute NASA Earthdata usernames or passwords with the application.
* Users should provide their own authentication credentials.

---

# 👨‍💻 Author

**Jintu Moni Bhuyan**

Research Scientist
North Eastern Regional Node for Disaster Risk Reduction (NER-DRR)
North Eastern Space Applications Centre (NESAC)
Department of Space, Government of India

### Research Interests

* Remote Sensing
* GIS
* Earth Observation
* Satellite Data Analysis
* Forest Carbon Dynamics
* Environmental Monitoring
* Disaster Risk Reduction
* Geospatial Analysis
* Machine Learning

---

# 📜 License

Add your preferred license here, for example:

```text
MIT License
```

If this repository is intended for institutional or research use, select the license according to the applicable institutional/data-source requirements.

---

# 🙏 Acknowledgements

This application makes use of NASA Earth science data and services, including NASA Giovanni and NASA Earthdata.

The developers and contributors of the open-source Python libraries used by this project are also gratefully acknowledged.

---

## ⭐ If you find this project useful

If this tool helps with your **remote sensing, environmental monitoring, or Earth observation research**, please consider starring the repository and sharing it with other researchers.
