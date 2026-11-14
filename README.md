# EV Market Performance & Insights Platform

A Flask web application that presents Electric Vehicle (EV) market analysis in one web page: an embedded Tableau Public dashboard, a guided Tableau story, and a project overview for non-technical stakeholders.

Maintained by **Narendra Gade**.

## 🛠️ Tech Stack
*   **Backend:** Python, Flask
*   **Frontend:** HTML5, CSS3, Bootstrap 5, JavaScript (BootstrapMade "Instant" template)
*   **Data Preparation:** Pandas
*   **Data Visualization:** Tableau Public (embedded)

## 🚀 Features
*   Responsive single-page web interface.
*   Embedded Tableau dashboard (EV market performance).
*   Embedded Tableau story for a chronological data narrative.

## ⚙️ How to Run Locally
1. Clone the repository:
   ```bash
   git clone https://github.com/narendra-08-gade/EV-Market-Performance-Insights.git
   cd EV-Market-Performance-Insights
   ```
2. Create and activate a virtual environment (optional but recommended):
   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   ```
   On macOS/Linux use `source .venv/bin/activate`.
3. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Start the app:
   ```bash
   python app.py
   ```
5. Open `http://127.0.0.1:5000` in your browser.

The Tableau dashboard and story are loaded from `public.tableau.com`, so an internet connection is needed to view them.

## 📁 Repository Structure
*   `app.py` – Flask app; serves `templates/index.html` at `/`.
*   `templates/index.html` – Main page (hero, insights, features, Tableau dashboard and story, contact form).
*   `static/` – CSS, JavaScript, images and vendored front-end libraries.
*   `forms/contact.php` – Original PHP contact-form handler (not used by the Flask app; see limitations).
*   `service-details.html`, `starter-page.html` – Template sample pages from BootstrapMade (not linked from the app).
*   `ev_market_train.csv` – EV dataset file (an Excel workbook; see Dataset below).
*   `Phases/` – Project documentation from the original course project (templates, reports, design phases).
*   `Final_Report.pdf` – Final project report.

## 📊 Dataset and Data Source
*   **Dataset:** [Kaggle – Electric Vehicle Market Classification Dataset](https://www.kaggle.com/datasets/tharishreddy22/electric-vehicle-market-classification-dataset)
*   The file `ev_market_train.csv` is stored in Excel (`.xlsx`) format despite its extension. Open it with Excel or with `pandas.read_excel(..., engine="openpyxl")`. The Flask app does not read it directly; the dashboards are built from it in Tableau.

## ⚠️ Known Limitations
*   The Tableau dashboard and story are hosted on a Tableau Public profile that belongs to the original project. They are not republished under this repository's owner, so the embeds show the original dashboards.
*   The contact form posts to `forms/contact.php`, which depends on the paid "PHP Email Form" library and is not served by Flask. The form will not send email when run with `python app.py`.
*   The social-media links in the footer are placeholders.
*   Some marketing text and statistics on the landing page were carried over from the original template and have not been re-verified against the dataset.

## 🔗 Project Links
*   **Maintainer:** Narendra Gade ([GitHub](https://github.com/narendra-08-gade))
*   **Interactive Dashboard (Tableau Public):** [EV Market Performance Dashboard](https://public.tableau.com/app/profile/siddharth.raghuwanshi6833/viz/EV_Market_Performance_Dashboard2/Dashboard2)
*   **Data Story (Tableau Public):** [EV Market Performance Story](https://public.tableau.com/app/profile/siddharth.raghuwanshi6833/viz/EV_Market_Performance_story2/Story2)
*   **Final Report:** [View the Final Report PDF](./Final_Report.pdf)

## 📄 License and Acknowledgements
*   Licensed under the MIT License – see [LICENSE](./LICENSE). The original copyright notice is kept as the MIT License requires.
*   Front-end template: "Instant" by [BootstrapMade](https://bootstrapmade.com/newtemplate-bootstrap-website-template/) – see its [license](https://bootstrapmade.com/license/). Credit line retained in the page footer.
*   Dataset: Kaggle, by tharishreddy22 – see the dataset page for its license terms.
