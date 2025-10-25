🎵 Real-Time Music Data Pipeline using Flask & Last.fm API
📘 Overview

This project demonstrates a complete end-to-end data engineering pipeline built using Flask, Pandas, and the Last.fm API.
It extracts real-time global music chart data, transforms it into a clean structured format, and serves it via a Flask REST API or visualizes it through CLI analysis and charts.

The project highlights every stage of the data lifecycle — Extraction, Transformation, Loading, Analysis, and Visualization — making it a perfect example of a practical data engineering workflow.

🧩 Features

✅ Real-time data ingestion from Last.fm API
✅ Data cleaning, transformation, and structuring with Pandas
✅ REST API endpoints built using Flask
✅ Interactive CLI mode for on-demand data analysis
✅ Matplotlib visualizations (Pie charts of top categories)
✅ Lightweight, modular, and beginner-friendly project

🏗️ Architecture Overview
          ┌────────────────────────┐
          │     Last.fm API        │
          └──────────┬─────────────┘
                     │  (requests)
                     ▼
          ┌────────────────────────┐
          │   Data Extraction       │
          │ (fetch_lastfm_data)    │
          └──────────┬─────────────┘
                     │  (Pandas)
                     ▼
          ┌────────────────────────┐
          │   Data Transformation   │
          │  (Cleaning & Struct.)  │
          └──────────┬─────────────┘
                     │  (Flask API)
                     ▼
          ┌────────────────────────┐
          │     Data Serving        │
          │   (/api/lastfm route)  │
          └──────────┬─────────────┘
                     │  (Matplotlib / CLI)
                     ▼
          ┌────────────────────────┐
          │  Analysis & Visualization │
          └────────────────────────┘

⚙️ Tech Stack
Component	Technology Used
Backend Framework	Flask
Data Processing	Pandas
API Communication	Requests
Visualization	Matplotlib
Data Source	Last.fm API
🚀 How to Run
1️⃣ Clone the Repository
git clone https://github.com/your-username/flask-lastfm-data-pipeline.git
cd flask-lastfm-data-pipeline

2️⃣ Install Dependencies
pip install -r requirements.txt

3️⃣ Run the Application
python main.py

4️⃣ Choose the Mode

Type 'web' → Launches Flask web app at http://127.0.0.1:5000

Type 'cli' → Opens interactive command-line analysis mode

🌐 Flask Endpoints
Endpoint	Method	Description
/	GET	Renders the homepage (index.html)
/api/lastfm	GET	Returns real-time top tracks data as JSON

Example Response:

[
  {
    "rank": 1,
    "name": "Vampire",
    "artist": "Olivia Rodrigo",
    "listeners": 987654,
    "playcount": 1200456,
    "chart": "Last.fm Global Chart"
  },
  ...
]

🧠 CLI Mode Features

Choose a column (track name, artist, listeners, etc.)

View top N categories based on frequency or counts

Generate pie charts for visual analysis

Great for quick insights and exploration

📊 Example Output

CLI Mode Sample:

Top 10 'artist' categories:
Taylor Swift    5
Ed Sheeran      4
The Weeknd      3
...


Pie Chart Output:
Displays distribution of top artists or tracks interactively.

💡 Why This Project is Helpful

Demonstrates real-world ETL pipeline design.

Helps beginners understand API integration, data cleaning, and serving.

Combines data engineering and data visualization concepts in one project.

Serves as a foundation for advanced projects using databases or dashboards.

📁 Folder Structure
📂 flask-lastfm-data-pipeline
 ┣ 📜 main.py
 ┣ 📜 index.html
 ┣ 📜 requirements.txt
 ┗ 📜 README.md

✨ Future Enhancements

🔹 Store transformed data in a database (e.g., SQLite, PostgreSQL).
🔹 Add interactive charts on the web UI.
🔹 Integrate a dashboard using Plotly or Streamlit.

👨‍💻 Author

Vikyatha Shreyas Kamma
Data Engineering Enthusiast

📜 License

This project is open-source and available under the MIT License
.
