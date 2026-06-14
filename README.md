# SOC-Lite Monitoring Stack

A production-style monitoring and alerting stack built on Docker, designed to monitor Linux server infrastructure in real time.

## Stack Components

| Component | Purpose | Port |
|-----------|---------|------|
| Prometheus | Metrics collection and alert evaluation | 9090 |
| Grafana | Dashboard visualisation | 3000 |
| Alertmanager | Alert routing and email notification | 9093 |
| Node Exporter | Linux system metrics exporter | 9100 |

## Features

- Real-time monitoring of CPU, memory, disk, and network
- Three alert rules: HighCPUUsage, HighMemoryUsage, LowDiskSpace
- Email notifications via Gmail SMTP when thresholds are breached
- Alert resolution notifications when systems recover
- Persistent Grafana dashboard storage via Docker volumes

## Quick Start

```bash
git clone https://github.com/Brightkakatech/soc-monitoring-stack.git
cd soc-monitoring-stack
docker compose up -d
```

Access Grafana at `http://YOUR_SERVER_IP:3000` (default login: admin/admin)

## Alert Rules

| Alert | Condition | Severity |
|-------|-----------|---------|
| HighCPUUsage | CPU > 80% for 1 minute | Warning |
| HighMemoryUsage | Memory > 85% for 1 minute | Warning |
| LowDiskSpace | Disk < 20% free for 1 minute | Critical |

## Author

Bright Amalahu — Systems Administrator and Cloud Engineer  
[Medium](https://medium.com/@brightkakatech) | [GitHub](https://github.com/Brightkakatech)
