# Weather Dashboard
Building a Python-based Weather Data Collection dashboard that fetches real-time weather data from OpenWeather API and stores it in AWS S3 for multiple cities.

## Features

- Fetches current weather data including temperature, humidity, and conditions
- Supports multiple cities (currently Philadelphia, Seattle, and New York)
- Automatically creates and manages AWS S3 storage
- Saves historical weather data with timestamps
- Uses environment variables for secure credential management

## Prerequisites

- Python 3.x
- OpenWeather API key
- AWS account with S3 access
- Required Python packages

## Installation

1. Clone the repository:
```bash
git clone https://github.com/your-username/Weather-dashboard-demo.git
cd Weather-dashboard-demo


2. Install required packages:
```bash
pip install boto3 requests python-dotenv
```

3. Create a `.env` file in the project root with your credentials:
```plaintext
OPENWEATHER_API_KEY=your_openweather_api_key_here
AWS_BUCKET_NAME=your_bucket_name_here
AWS_ACCESS_KEY_ID=your_aws_access_key_here
AWS_SECRET_ACCESS_KEY=your_aws_secret_key_here
```

## Usage

Run the dashboard:
```bash
python src/weather_dashboard.py
```

The script will:
1. Create an S3 bucket if it doesn't exist
2. Fetch current weather data for configured cities
3. Display weather information in the console
4. Save the data to S3 with timestamps

## Project Structure

```
Weather-dashboard-demo/
├── src/
│   └── weather_dashboard.py
├── .env
└── README.md
```

## Output Example

Fetching weather for Philadelphia...
Temperature: 28.83°F
Feels like: 19.04°F
Humidity:  86%
Conditions: light snow
Successfully saved data for Philadelphia to S3
Weather data for Philadelphia saved to S3!

## Data Storage

Weather data is stored in the S3 bucket with the following structure:
- File path: `weather-data/<city>-<timestamp>.json`
- Format: JSON with weather data and timestamp
- Updated: Every time the script runs






