# **Coin Flip Metrics Service**

## **What is this Project?**

This project is a simple coin-flip simulation web service built using **FastAPI**, designed to demonstrate the integration of APIs with monitoring and metrics collection. It includes endpoints to perform simulated coin flips and expose real-time metrics compatible with **Prometheus** for monitoring.

---

## **What Does It Do?**

1. **Simulate Coin Flips:**
   - Users can specify the number of coin flips via an API call.
   - The service returns the count of `heads` and `tails` for the specified number of trials.

2. **Track Metrics:**
   - The service tracks metrics such as:
     - Number of heads flipped.
     - Number of tails flipped.
     - Total number of flips.
   - Metrics are exposed in a Prometheus-compatible format for real-time monitoring.

3. **Monitor with Prometheus:**
   - Metrics data can be visualized and analyzed using Prometheus or any compatible monitoring tool.
   - Includes a pre-configured `prometheus.yml` for easy setup.

   ![Prometheus Metrics Output](https://github.com/richiectr360/FastAPIServerWithPrometheus/blob/main/screenshots/1.png)
   ![Prometheus Graph Example](https://github.com/richiectr360/FastAPIServerWithPrometheus/blob/main/screenshots/2.png)

---

## **Tech Stack**

### **Core Technologies:**
- **FastAPI:** A modern, fast (high-performance) web framework for building APIs with Python.
- **Prometheus:** An open-source systems monitoring and alerting toolkit.
- **Python:** Backend logic written in Python, with libraries for metrics and web service handling.

### **Key Libraries:**
- `fastapi`: Web framework for creating API endpoints.
- `uvicorn`: ASGI server to run the FastAPI application.
- `prometheus-client`: Exposes metrics in a format compatible with Prometheus.
- `Jinja2`: Dependency for FastAPI templates.

### **Containerization and Deployment:**
- **Docker:** Used to containerize the application and Prometheus.
- **Docker Compose:** Simplifies multi-container setup, allowing the application and Prometheus to run seamlessly.

---

## **How to Use It**

### **Running the Project**

1. **Using Python (Local Development):**
   - Install the dependencies:
     ```bash
     pip install -r requirements.txt
     ```
   - Run the server:
     ```bash
     python server.py
     ```
   - API Endpoints:
     - `/flip-coins?times=<number>`: Simulate coin flips.
     - `/metrics`: Expose metrics for Prometheus.

    ![Coin Flip API Example](https://github.com/richiectr360/FastAPIServerWithPrometheus/blob/main/screenshots/3.png)

2. **Using Docker (Production):**
   - Build and start the services:
     ```bash
     docker-compose up --build
     ```
   - Access endpoints at:
     - `http://localhost:5000/flip-coins`
     - `http://localhost:5000/metrics`

### **Prometheus Integration**
- Start Prometheus with the included `docker-compose.yml`:
  ```bash
  docker-compose up


## **Why Use This Project?**

- **Educational Tool:** Learn how to integrate FastAPI services with monitoring tools like Prometheus.
- **Metrics Collection:** Demonstrates how to expose custom metrics for any web application.
- **Modern Tech Stack:** Uses popular, high-performance tools for creating and monitoring web services.
