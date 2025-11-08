# Use an official Python runtime
FROM python:3.10-slim

# Set working directory
WORKDIR /app

# Copy dependency files
COPY requirements.txt .
COPY pyproject.toml ./

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the application source
COPY trading_calendar ./trading_calendar

# Expose port
EXPOSE 10000

# Command to run the app
CMD ["uvicorn", "trading_calendar.main:app", "--host", "0.0.0.0", "--port", "10000"]

