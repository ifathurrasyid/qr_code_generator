# 📱 Dynamic QR Code Generator & Bulk Automator

![Branded QR Example](images/branded_qr_close_up.png)

## 🚀 Overview
Marketing and operations teams often hit bottlenecks when manually generating hundreds of custom, trackable QR codes. This project eliminates that friction entirely.

Built with **Python, Pandas, and Pillow**, this utility is a high-speed, OS-agnostic automation engine. It ingests bulk URLs from an Excel database and instantly renders hundreds of modern, branded QR codes—complete with embedded logos and automatic background transparency processing.

---

## ✨ Key Engineering Features
* **High-Speed Multi-Threading:** Utilizes `concurrent.futures.ThreadPoolExecutor` to process and render images in parallel, turning a multi-minute task into a sub-second execution.
* **Auto-Transparency (Alpha Processing):** Automatically scans JPG and PNG logos pixel-by-pixel, stripping out white backgrounds and converting them to transparent alpha channels before injection.
* **Intelligent Matrix Scaling:** Uses high error correction (`ERROR_CORRECT_H`) and mathematically calculates optimal aspect ratios to ensure logos never exceed 25% of the QR matrix, guaranteeing 100% scannability.
* **Dual-Input Architecture:** Designed with a clean execution dashboard allowing users to toggle between a hardcoded Python list (for quick one-offs) or an Excel spreadsheet (for bulk database runs).
* **Modern Aesthetic:** Bypasses standard blocky QR generation in favor of rounded modules and custom corporate color hex injections via `qrcode` styling masks.

---

## 📸 Automation Showcase

### 1. The Bottleneck vs. The Solution
Taking a raw list of campaign URLs and instantly transforming them into a directory of deployable, high-fidelity marketing assets.
![Bulk Automation](images/input_vs_output.png)

### 2. High-Fidelity Injection
Calculated logo centering with automated background removal ensures brand assets look native to the QR code, not just pasted on top.
![Branded Close Up](images/branded_qr_close_up.png)

### 3. Multi-Threaded Execution
The engine handles bulk processing effortlessly, providing clean terminal logs for every parallel thread completed.
![Terminal Execution](images/terminal_execution.png)

---

## 🛠️ Tech Stack
* **Python 3.x**
* **Pillow (PIL):** Image manipulation, alpha channel processing, and resizing.
* **qrcode:** Matrix generation and modern module styling.
* **Pandas:** Bulk data extraction and parsing from `.xlsx` files.
* **Concurrent.futures:** Multi-threading for parallel execution.

---

## ⚙️ How to Run
1. Clone the repository.
2. Install dependencies: `pip install pandas qrcode[pil] Pillow openpyxl`
3. Place your logos in an `icon/` folder and your bulk URLs in an Excel file (e.g., `socmed_links_database.xlsx`).
4. Open the Jupyter Notebook, toggle your preferred input method in the Execution Dashboard (Cell 3), and hit run!