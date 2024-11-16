# Use an official Python runtime as a parent image
FROM python:3.9

# Set the working directory
WORKDIR /app

# Copy the requirements file and install dependencies
COPY requirements.txt .
# Install dependencies with pip retry logic and cleanup
RUN pip install --upgrade pip && \
    python -m pip install --no-cache-dir -r requirements.txt --use-feature=2020-resolver || \
    python -m pip install --no-cache-dir -r requirements.txt --no-deps


# Copy the application code
COPY . .

# Expose the port the app runs on
EXPOSE 8000

# Command to run the FastAPI server
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]