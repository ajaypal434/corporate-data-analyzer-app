# corporate-data-analyzer-app

A simple desktop tool I built to make quick data analysis easier for people who don't want to touch Excel formulas or write Python code. You give it a CSV or Excel file, pick what you want to group by and what to measure, and it builds you a report and a chart — right there in the app.

## Why I built this

While working on data analyst projects, I kept seeing the same pattern — someone has a spreadsheet, wants a quick summary by category (like total sales by region), and ends up manually messing around with pivot tables. So I built a small GUI app that does this in a few clicks: load the file, pick your columns, get your report and chart, export if you want.

## What it does

- Load a CSV or Excel file and see basic info (rows, columns, headings)
- Automatically figures out which columns are text and which are numbers (even handles numbers stored as text, like "12,000")
- Pick a column to group by, an aggregation (sum, mean, max, min, count, median), and a value column — it builds the report and shows it in a table
- Turn that report into a Bar, Column, Line, or Pie chart with one click
- Export the report to Excel or CSV, and save the chart as a PNG
- Handles bad input gracefully instead of just crashing

## Built with

Python, Tkinter (for the GUI), Pandas (for the data crunching), and Matplotlib (for the charts).

## Screenshot

<img width="1383" height="922" alt="corporate data analysis" src="https://github.com/user-attachments/assets/15cbd7b7-4933-4f9c-9edb-ed8bb188780e" />


## How to run it

```bash
git clone https://github.com/ajaypal/corporate-data-analyzer.git
cd corporate-data-analyzer
pip install -r requirements.txt
python corporate_data_analyzer.py
```

There's a sample file in `sample_data/sample_sales_data.csv` if you want to try it out without your own data.

## Turning it into a standalone .exe

```bash
pip install pyinstaller
pyinstaller --onefile --windowed corporate_data_analyzer.py
```

The finished .exe shows up in the `dist/` folder — good for sharing with someone who doesn't have Python installed.

## What I'd add next

A save-location picker for exports (right now it always saves to the same folder), and a way to handle really large files without the UI freezing.

## Conclusion

This project started as a way to practice combining Pandas, Tkinter, and Matplotlib into one working tool instead of three separate scripts. What I ended up with is something genuinely useful — a lightweight report-and-chart builder that anyone can run without knowing a single line of Python. It's not meant to replace tools like Power BI or Excel, but for quick, on-the-spot analysis of a CSV or Excel file, it does the job well. Building it also helped me get more comfortable with GUI development and thinking about how a non-technical user would actually interact with a tool like this, which is something I want to keep working on in future projects.

## Author

**Ajaypal**
Email: ajaypalajaypal23719@gmail.com
