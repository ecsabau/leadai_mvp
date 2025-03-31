# 🔍 LeadAI - Automated Lead Scoring & Reporting

![Python](https://img.shields.io/badge/python-3.11%2B-blue)
![Pandas](https://img.shields.io/badge/pandas-2.0%2B-orange)
![PDF Generation](https://img.shields.io/badge/PDF-FPDF2-green)

A Python-based system that analyzes lead data from CSV files and generates professional PDF reports with contact details, budgets, and interest categories.

## ✨ Features
- **CSV Processing**: Reads lead data (name, email, budget, interest)
- **PDF Reports**: Generates formatted, multi-column reports
- **Unicode Support**: Handles special characters (é, 汉, etc.)
- **Customizable**: Easily adapt columns or scoring logic

## 🚀 Quick Start
1. Clone the repo:
   ```bash
   git clone https://github.com/ecsabau/leadai_mvp.git
   
2. Install dependencies:
   ```bash
   pip install -r requirements.txt

3. Generate the report:
   ```bash
   python report.py

📂 File Structure:
```leadai_mvp/
├── report.py               # Main PDF generation script
├── sample_leads.csv        # Example dataset (fake data)
├── requirements.txt        # Python dependencies
├── .gitignore             # Specifies files to exclude from Git
└── leadai_report.pdf       # Sample output (generated)
```
🚀 Usage
1. Prepare Your Data:
Create a CSV file named leads.csv with these columns (or modify report.py to match your schema):
```
csv
name,email,phone,budget,interest,pages_visited,time_spent_sec
John Doe,john@example.com,555-1234,$10K,Real Estate,"['/funds','/pricing']",227
```
2. Generate Reports:
```bash
python report.py
Output will be saved as leadai_report.pdf

🧩 Customization
```
1. Modify Report Columns

Edit these lines in report.py:
```
headers = ["Name", "Email", "Budget", "Interest"]  # Change column titles
col_widths = [40, 80, 30, 40]                    # Adjust column widths
```

2. Add Scoring Logic

Insert before PDF generation:
```
# Example: Score based on time spent
df["score"] = df["time_spent_sec"] / 10
```

🛡️ Data Security
For sensitive data:

1. Add to .gitignore:
  ```bash
   echo "leads.csv" >> .gitignore
  ```
2. Use environment variables for paths:
   ```
   import os
   csv_path = os.getenv('LEADS_CSV_PATH', 'sample_leads.csv')
   ```

🤝 Contributing

Fork the repository
Create a feature branch (git checkout -b feature/improvement)
Commit changes (git commit -m 'Add new feature')
Push to branch (git push origin feature/improvement)
Open a Pull Request

📜 License
MIT License

Copyright (c) 2025 ecsabau

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
