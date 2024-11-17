# Use an official Python runtime as a parent image
FROM python:3.9

# Set the working directory
WORKDIR /app

# Install dependencies directly (list your dependencies here)
RUN pip install --upgrade pip && \
    pip install fastapi uvicorn  # Replace these with your actual dependencies

# Copy the application code
COPY . .

# Expose the port the app runs on
EXPOSE 8000

# Command to run the FastAPI server
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]