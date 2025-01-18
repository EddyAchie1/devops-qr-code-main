# Use a slim Python image
FROM python:3.9-slim

# Set working directory
WORKDIR /usr/src/app

# Install dependencies in a separate step for better caching
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

# Copy application files
COPY . .


# Default command
CMD ["uvicorn", "main.app", "--host", "0.0.0.0", "--port", "80"]
