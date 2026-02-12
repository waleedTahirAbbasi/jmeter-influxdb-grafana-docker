🚀 JMeter Live Monitoring Stack
This repository provides a "plug-and-play" infrastructure to transform raw JMeter results into professional, real-time dashboards using InfluxDB and Grafana.

---

## ✅ Overview

This setup allows you to:

- Run **JMeter performance tests**
- Automatically push live metrics to **InfluxDB**
- Visualize results in **Grafana dashboards**
- Monitor performance in real time during test execution

### Why this stack?

| Tool | Purpose |
|------|--------|
| JMeter | Load generation & performance testing |
| InfluxDB | Time-series metrics storage |
| Grafana | Real-time dashboards & visualization |

This architecture gives you:

- Live performance feedback
- Historical trend analysis
- Shareable dashboards
- Production-like observability

---

## ✅ Architecture

    JMeter Test
        |
        v
 Backend Listener
        |
        v
    InfluxDB
        |
        v
     Grafana
  (Dashboards)


Flow:

1. JMeter executes load test
2. Backend Listener sends metrics to InfluxDB
3. Grafana reads metrics from InfluxDB
4. Dashboards visualize performance in real time

---

## ✅ Prerequisites

Install the following:

- Docker ≥ 20.x
- Docker Compose ≥ v2
- JMeter ≥ 5.5 (installed locally)

### Ports used

| Service | Port |
|--------|------|
| InfluxDB | 8086 |
| Grafana | 3000 |

Make sure these ports are free.

### System requirements

- 4 GB RAM minimum
- 2 CPU cores recommended
- Linux / macOS / Windows supported

---
