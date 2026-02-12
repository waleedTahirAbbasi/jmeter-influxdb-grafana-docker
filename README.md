# 🚀 JMeter Live Monitoring Stack

A plug-and-play solution to visualize Apache JMeter performance test results in real-time using **InfluxDB** and **Grafana**. 

Stop relying on static spreadsheets and raw logs. This stack allows you to monitor response times, error rates, and throughput as they happen.

---

## 📖 Overview

This setup uses a "Time-Series" approach to performance monitoring:
1. **JMeter** generates the load and streams metrics.
2. **InfluxDB (1.8)** stores the metrics in a time-series database.
3. **Grafana** queries InfluxDB to display beautiful, live dashboards.

### Why use this?
* **Real-time Insights:** Catch 429 (Too Many Requests) or 500 errors the second they spike.
* **Stakeholder Ready:** Professional dashboards for high-level summaries.
* **Comparison:** Easily compare different test runs (baselines) side-by-side.

---

## 🏗 Architecture

```text
[ JMeter ]  ---- (Write Metrics) ----> [ InfluxDB 1.8 ]
    |                                       |
    | (Simulate Load)                       | (Query Data)
    v                                       v
[ Target App ]                       [ Grafana Dashboard ]
