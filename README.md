# Multithread - Weather API Case Study (Papua)

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Library](https://img.shields.io/badge/Library-Pandas-orange.svg)
![Concurrency](https://img.shields.io/badge/Concurrency-Multithreading-yellowgreen.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

---

### **Brief Description**
This Parallel Computing project, developed for the Parallel Computing course, FILKOM UB, implements **multithreading** utilizing `ThreadPoolExecutor`.  
The primary function is to efficiently and rapidly retrieve real-time weather data from **WeatherAPI.com** for numerous districts across **Papua Province**, Indonesia.  
The collected data is classified into a structured Excel file. The project emphasizes a comparison of execution time against the sequential (single-threading) method to clearly demonstrate the performance advantages provided by parallel computing.

---

## **Group Members**

| Name                        | Student ID (NIM) | Major                |
|------------------------------|------------------|----------------------|
| Barru Wira Yasa             | 235150301111021  | Computer Engineering |
| Muhammad Rafli Abidi Utama  | 235150301111035  | Computer Engineering |
| Muhammad Shean Elliora Ribah| 235150307111045  | Computer Engineering |

*Faculty of Computer Science, Brawijaya University*

---

## **Project Goals**

1. To develop an API-based weather data retrieval system using the Python programming language.  
2. To utilize the multithreading method to enable parallel execution of the data collection process.  
3. To achieve faster processing time compared to the sequential method (single-threading).  
4. To produce organized and accurate weather data from various districts in Papua Province.  
5. To store the weather data results in Excel format for ease of access, analysis, and utilization.

---

## **Technology & Dependencies**

- **Python 3.x**  
- **`requests`** – for making HTTP requests to the Weather API  
- **`pandas`** – for reading the Excel input file and saving processed results to the output file  
- **`concurrent.futures.ThreadPoolExecutor`** – the core module for implementing multithreading  
- **Weather API (weatherapi.com)** – provides real-time weather data (temperature, humidity, wind, UV, etc.)

---

## **Multithreading Implementation**

The project employs **multithreading** to mitigate the high I/O latency associated with numerous API calls over a network.

1. **Process Flow:** The system reads location data from the Excel input file, prepares tasks, and initiates threads.  
2. **Parallel Execution:** The `ThreadPoolExecutor` runs multiple worker threads concurrently (configured with a maximum of 10 workers).  
3. **Efficiency:** Each thread independently handles a location, processes the JSON response, and updates the shared DataFrame.  
   This concurrent processing significantly reduces total execution time compared to sequential execution.

---

## **Usage Guide**

### 1. Clone Repository
```bash
git clone <YOUR_REPOSITORY_URL>
cd <PROJECT_FOLDER_NAME>
