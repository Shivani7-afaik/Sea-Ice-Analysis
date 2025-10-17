# Sea-Ice-Analysis
Data processing and visualization of sea ice thickness trends using Python, Pandas, and Matplotlib. Used the dataset of CRYOSAT from 2010-2020.

##  Sea Ice Thickness Data Processing and Visualization  
**Outputs:** Monthly sea ice thickness | Average sea ice thickness  

**Video links:** *https://drive.google.com/file/d/1L5qrG1MpJe5cFQAjVsO3hzrflBmyrB6D/view?usp=sharing*  
*https://drive.google.com/file/d/1jHQhw4FNs5EcnRaLM9RDliZ-ppLpT1Zb/view?usp=sharing*


---

##  Project Description
This project analyzes **Southern Hemisphere sea ice thickness data (2010–2020)** using Python.  
We accessed CRYOSAT data from the **ESA Climate Change Initiative (CCI)** repository and processed **NetCDF** files to identify temporal and spatial trends in sea ice thickness.

The analysis includes data cleaning, computation of monthly and yearly averages, and multiple visualizations — including an animated video showing decadal changes.

---

##  Key Steps

### 1. Data Acquisition  
- Downloaded CRYOSAT sea ice thickness data (2010–2020) from ESA CCI repository.

### 2. Data Cleaning and Preparation  
- Used **netCDF4** and **xarray** to read and process NetCDF files.  
- Cleaned missing values, standardized timestamps, and extracted key variables such as sea ice thickness and time.

### 3. Data Analysis  
- Computed monthly and yearly averages while excluding missing data regions.  
- Calculated total sea ice thickness to track interannual trends and anomalies.

### 4. Data Visualization  
- Created **line plots**, **area plots**, and **animated visualizations** to illustrate changes in thickness over time.  
- Developed a time-based animation of sea ice thickness from 2011–2019.

---

##  Dataset Overview
- **Total files:** 114  
- **Average sea ice thickness:** 1.598 m  
- **Total sea ice thickness:** 270,872.03 m  

### Key Variables
- Spatial: `xc`, `yc`, `lat`, `lon`  
- Temporal: `time`, `time_bnds`, `nv`  
- Sea ice: `radar_freeboard`, `sea_ice_freeboard`, `sea_ice_thickness`, `sea_ice_concentration`  
- Snow cover: `snow_depth`, `snow_depth_uncertainty`  
- Quality flags and projection: `quality_flag`, `status_flag`, `Lambert_Azimuthal_Grid`, `region_code`

---

##  Analysis and Figures

### Monthly Subplots  
**Figures 1 & 2:** Monthly thickness variation (2010–2020).  
Clear seasonal cycles are visible, with complete data from 2011–2019.

### Time Series Analysis  
**Figure 3:** Monthly average thickness (2010–2020) — recurring winter peaks and summer troughs.  
**Figure 4:** Annual average thickness — general decline 2013–2019, sharp increase in 2020.

### Investigation on 2020  
- Fewer data points (13,456).  
- Mean = 1.77 m, Std = 1.05 m.  
- Right-skewed histogram due to incomplete data (only Jan–Apr 2020).  
**Figure 5:** Distribution histogram for 2020.

### Aggregate Analysis  
**Figure 6:** Yearly total sea ice thickness (2010–2020).  
Overall stability with fluctuations, an anomalous rise in 2020.

### Animated Visualization  
Animated video of average sea ice thickness (2011–2019).  
Shows decadal evolution of Antarctic ice cover.

---

##  Key Findings

1. **Data Completeness**
   - 114 files processed; incomplete years: 2010 & 2020.  
   - 5–15% data gaps after NaN removal.

2. **Temporal Patterns**
   - Seasonal peaks in October (winter), lows in March (summer).  
   - Stable baseline from 2011–2019; anomaly in 2020.

3. **Observational Limitations**
   - 2020 spike possibly due to sensor or spatial sampling differences.  
   - NaN values indicate environmental measurement challenges.

---

##  Work Cited  
ESA CCI CryoSat-2 Sea Ice Thickness Data:  
(https://catalogue.ceda.ac.uk/uuid/67b003a864cd4e9ebeccd29fbdf4447e/)

---

###  Summary
This analysis provides evidence of evolving Southern Hemisphere sea ice conditions with potential 2020 measurement anomalies.  
Further investigation into climate or observational factors is recommended.
