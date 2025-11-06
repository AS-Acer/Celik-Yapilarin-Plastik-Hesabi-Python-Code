


````markdown
# Steel Section Plastic & Elastic Capacity Calculator

![Python](https://img.shields.io/badge/Python-3.9%2B-3776AB.svg?style=for-the-badge&logo=python&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)
![Status](https://img.shields.io/badge/Build-Passing-brightgreen.svg?style=for-the-badge)

This project computes **elastic and plastic section properties** for selected steel cross-sections and prints formatted results while exporting them to **CSV + Excel (.xlsx)** automatically on your **Desktop** (supports both normal Desktop and OneDrive Desktop).

---

## 📐 Supported Sections

| Section | Description | Notes |
|--------|-------------|------|
| **BuiltUpI** | Welded / fabricated asymmetric I-section | Geometry fully user-defined |
| **CHS_UPE_LR** | Circular tube + 2× UPE300 (Left & Right) | Horizontal symmetry |
| **CHS_UPE_TB** | Circular tube + 2× UPE300 (Top & Bottom) | Vertical symmetry |

**Default geometry values (you can modify in code):**
- CHS: `Ø323 × 12 mm`
- UPE300 catalog values from European profiles
- Gap for Left-Right case: `gap_back = 28.9 mm`
- Vertical offset for Top-Bottom case: `y_c = 190.4 mm`

---

## 🧱 Material

| Property | Value |
|--------|------|
| Steel Grade | **S355** |
| Yield Strength (fy) | **355 MPa** |

---

## 📦 Output (Automatically Saved)

| Filename | Location | Description |
|---------|----------|-------------|
| `sections_results.csv` | Desktop | Raw results table |
| `sections_results.xlsx` | Desktop | Styled formatted Excel report |

---

## ▶️ Installation & Requirements

```bash
pip install openpyxl
````

Excel kaydı için gereklidir. Yüklemesen de CSV çalışır.

---

## ▶️ Running the Script

```bash
python sections_excel.py
```

veya:

```bash
C:\Python312\python.exe "C:\tam\yol\sections_excel.py"
```

---

## 🖥 Example Console Output

```
┌ Section 2 - CHS + 2×UPE300 (L-R) ───────────────────────────────┐
│ Computation & Results                                           │
└────────────────────────────────────────────────────────────────┘
Area                :     1.28e+04 mm²
Ix                  :     3.76e+07 mm⁴
Iy                  :     1.08e+08 mm⁴
We_x                :     2.01e+05 mm³
Wp_x                :     2.58e+05 mm³
Me_x                :     71.4 kN·m
Mp_x                :     91.8 kN·m
shape_x             :        1.28 —
...
```

---

## 📂 Directory Structure

```
project-folder/
│   sections_excel.py
│   README.md
```

---

## ✨ Features

* Automated **centroid, stiffness, elastic modulus** and **plastic modulus** computation.
* **Plastic neutral axis** location based on area balancing.
* **Shape factor** evaluation: `Wp / We`.
* Output neatly **formatted** in terminal.
* **Excel report** with:

  * Header highlighting
  * Auto column sizing
  * Grid borders

---

## 🌍 Turkish Explanation (TR)

Bu script, çelik taşıyıcı sistemlerde kullanılan **kesit plastik ve elastik dayanım hesaplarını** otomatik yapar.
CHS + UPE birleşik kesitlerde **Steiner Teoremi** doğru uygulanır ve **plastik nötr eksen** doğru konumlandırılır.

**Sonuçlar otomatik olarak masaüstüne kaydedilir.**
Hem **CSV** formatında düz veri, hem de **Excel** formatında şık tablo üretilir.

---

## 🧑‍💻 Author

Developed for **structural steel plastic design** coursework.
Contributions & improvements are welcome → feel free to open PRs or Issues.

---

## 📜 License

```
MIT License — free for academic + commercial use.
```

```

