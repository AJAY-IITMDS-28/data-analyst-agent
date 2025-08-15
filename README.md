# Data Analyst Agent API

This project provides a FastAPI-based API endpoint for automated data analysis using LLMs, DuckDB, Pandas, and Matplotlib.

## Features
- Accepts POST requests at `/api/` with `questions.txt` and optional data files
- Uses LLMs (OpenAI API) to interpret and answer questions
- Supports web scraping, CSV/Parquet/JSON analysis, DuckDB SQL queries
- Generates visualizations as base64-encoded images
- Returns answers in JSON format

## Usage
Send a POST request to `/api/` with multipart/form-data:

```
curl "https://app.example.com/api/" -F "questions.txt=@question.txt" -F "data.csv=@data.csv"
```

## Setup
1. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
2. Run the API:
   ```
   uvicorn main:app --host 0.0.0.0 --port 8000
   ```

## License
MIT
