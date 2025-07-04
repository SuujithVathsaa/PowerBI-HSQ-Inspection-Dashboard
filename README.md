# 🛠️ Health & Safety, Quality & Depot Inspection Dashboard – Power BI

This repository hosts the **Power BI Dashboard** for monitoring **Health & Safety**, **Quality**, and **Depot Inspections**. It helps operational teams improve visibility into inspection outcomes, non-conformance events, and inspector performance.

![image](https://github.com/user-attachments/assets/3e7ff6af-c04d-4e5b-bc09-d449ab170b06)
(./2e844c39-df7d-44d8-b0b5-ff04a3dc29a6.png)

---

## 📊 About the Dashboard

The dashboard integrates inspection datasets across three key domains:
- 🔍 **Health & Safety**
- 🧪 **Quality Compliance**
- 🏢 **Depot Performance Audits**

It supports:
- Issue identification by type (Minor, OFI, Major)
- Inspector accountability
- Location-based inspection results

---

## 🧠 Key Features

### 🔹 Interactive Filtering
- Dynamic date and **Business Area** slicers
- Treemap for **operative-level activity**

### 🌍 Geo-Mapping with Tooltips
- Integrated **Bing Maps**
- Colored data points for defect severity
- **Image tooltips**: Hover over location pins to preview **photos of non-conformance**

### 📈 Summary KPIs
- Total inspections
- Count of Minor, OFI, Major findings

### 💬 Inspector Comments
- Section to show notes or comments for context

### 🎨 Custom Theme
- Futuristic purple background and card-style visuals for better readability and presentation

!![image](https://github.com/user-attachments/assets/5df14e45-e436-47a5-b429-32bebde06604)
(./dashboard.png)

---


## 🧮 Key sample DAX Measures Used

### 🟣 OFI Count 

-- OFI Count
OFI Count H&S = 
COALESCE(
    CALCULATE(
        COUNTROWS('H&S'),
        FILTER('H&S', 'H&S'[defect_rating] = "OFI")
    ),
    0
)

### 🟣 Minor Count
Minor Count H&S = 
COALESCE(
    CALCULATE(
        COUNTROWS('H&S'),
        FILTER('H&S', 'H&S'[defect_rating] = "Minor")
    ),
    0
)

### 🟣 Major Count
Major Count H&S = 
COALESCE(
    CALCULATE(
        COUNTROWS('H&S'),
        FILTER('H&S', 'H&S'[defect_rating] = "Major")
    ),
    0
)


---
## 🗃️ Files

| File Name | Description |
|-----------|-------------|
| `H&S_Quality_Inspection.pbix` | Main Power BI dashboard file |
| `README.md` | This documentation |

> ⚠️ Sample data has been anonymized for demonstration. Replace with your data if replicating this dashboard in your environment.

---

## 🚀 Getting Started

1. Clone this repo or download the `.pbix` file
2. Open in **Power BI Desktop**
3. Connect your own datasets or review sample visualizations
4. Hover over map points to view **image-based tooltip**
5. Publish to Power BI Service if needed

---

## 🤝 Contributing

Contributions and ideas are welcome! Feel free to raise issues, suggest enhancements, or fork and build on this project.

---

## 📬 Contact

For questions or collaboration, feel free to reach out or connect via GitHub Discussions or 
linkdin - https://www.linkedin.com/in/sujith-vathsaa-55969416a/.

