## 📊 Prometheus Monitoring Glossary
| 🌟 **Term**                   | 📘 **Definition (Simple)**                      | 💡 **Example / Explanation**                          |
| ----------------------------- | ----------------------------------------------- | ----------------------------------------------------- |
| 📊 **Prometheus**             | Open-source monitoring and alerting system      | Collects metrics from applications and infrastructure |
| 📈 **Monitoring**             | Tracking system health and performance          | CPU, Memory, Disk monitoring                          |
| 🚨 **Alerting**               | Sending notifications when issues occur         | High CPU usage alert                                  |
| 📡 **Metrics**                | Numerical measurements collected over time      | CPU usage = 75%                                       |
| ⏰ **Time Series Data**        | Metrics stored with timestamps                  | CPU usage every 15 seconds                            |
| 🎯 **Target**                 | Endpoint monitored by Prometheus                | Node Exporter server                                  |
| 🔍 **Scraping**               | Process of collecting metrics from targets      | Prometheus pulls metrics every 15s                    |
| 🌐 **Endpoint**               | URL exposing metrics                            | `/metrics`                                            |
| 🏷️ **Label**                 | Key-value metadata attached to metrics          | `instance="server1"`                                  |
| 📦 **Metric Name**            | Unique name of a metric                         | `node_cpu_seconds_total`                              |
| 📜 **Sample**                 | Single metric value at a specific time          | CPU=45 at 10:00 AM                                    |
| 🧠 **TSDB**                   | Time Series Database used by Prometheus         | Stores collected metrics                              |
| 🔢 **Counter**                | Value that only increases                       | Total HTTP requests                                   |
| 📊 **Gauge**                  | Value that can increase or decrease             | CPU utilization                                       |
| 📈 **Histogram**              | Measures distribution of values                 | Request latency                                       |
| 🎯 **Bucket**                 | Range used inside histogram                     | 100ms, 500ms, 1s                                      |
| 📉 **Summary**                | Similar to histogram with percentiles           | 95th percentile latency                               |
| 🎲 **Quantile**               | Statistical percentile                          | P95 Response Time                                     |
| 🖥️ **Prometheus Server**     | Main component that collects and stores metrics | Central monitoring server                             |
| 📡 **Exporter**               | Tool that exposes metrics from systems          | Node Exporter                                         |
| 📥 **Pull Model**             | Prometheus pulls metrics from targets           | Default behavior                                      |
| 📤 **Push Model**             | Applications push metrics                       | Pushgateway                                           |
| 🚪 **Pushgateway**            | Allows short-lived jobs to expose metrics       | Batch jobs                                            |
| 🔄 **Service Discovery**      | Automatically discovers targets                 | Kubernetes Pods                                       |
| 📋 **Scrape Config**          | Defines what Prometheus monitors                | `prometheus.yml`                                      |
| 📜 **Prometheus YAML**        | Configuration file                              | Scrape intervals and targets                          |
| 🖥️ **Node Exporter**         | Collects Linux server metrics                   | CPU, Memory, Disk                                     |
| ☕ **JMX Exporter**            | Monitors Java applications                      | JVM Metrics                                           |
| 🐳 **cAdvisor**               | Collects Docker container metrics               | Container CPU & Memory                                |
| ☸️ **kube-state-metrics**     | Kubernetes object metrics                       | Deployments, Pods                                     |
| 🗄️ **MySQL Exporter**        | MySQL monitoring exporter                       | DB connections                                        |
| 🐘 **PostgreSQL Exporter**    | PostgreSQL monitoring exporter                  | Query statistics                                      |
| 🌐 **Blackbox Exporter**      | Monitors endpoints externally                   | HTTP, TCP, DNS checks                                 |
| 🔗 **SNMP Exporter**          | Network device monitoring                       | Switches, Routers                                     |
| ☁️ **CloudWatch Exporter**    | AWS metrics exporter                            | EC2, RDS metrics                                      |
| 🔍 **PromQL**                 | Query language used to analyze metrics          | Similar to SQL for metrics                            |
| 📈 **Metrics Server**         | Resource metrics provider                       | HPA metrics                                           |
| 🔄 **HPA**                    | Horizontal Pod Autoscaler                       | Scale based on CPU                                    |
| 🚀 **Helm Chart**             | Package to install Prometheus                   | kube-prometheus-stack                                 |
| 💾 **Retention Period**       | How long metrics are stored                     | 15 days                                               |
| 📦 **Local Storage**          | Metrics stored on disk                          | Prometheus TSDB                                       |


---

## 📊 Grafana Monitoring Glossary
| 🌟 **Term**                      | 📘 **Definition (Simple)**                             | 💡 **Example / Explanation**              |
| -------------------------------- | ------------------------------------------------------ | ----------------------------------------- |
| 📊 **Grafana**                   | Open-source visualization and monitoring platform      | Create dashboards from Prometheus metrics |
| 📈 **Dashboard**                 | Collection of graphs, panels, and visualizations       | Kubernetes Monitoring Dashboard           |
| 🖼️ **Panel**                    | Individual visualization component                     | CPU Usage Graph                           |
| 📋 **Row**                       | Group of panels within a dashboard                     | Infrastructure Metrics Row                |
| 📡 **Data Source**               | Backend system that provides data to Grafana           | Prometheus, Loki, Elasticsearch           |
| 🎯 **Query**                     | Request sent to a data source                          | PromQL query for CPU usage                |
| 🔍 **Explore**                   | Grafana feature for ad-hoc queries and troubleshooting | Investigate high CPU usage                |
| 📊 **Visualization**             | Graphical representation of data                       | Line chart, Pie chart                     |
| 📈 **Time Series Panel**         | Displays metric trends over time                       | CPU usage over 24 hours                   |
| 🥧 **Pie Chart**                 | Shows percentage distribution                          | Resource usage breakdown                  |
| 📋 **Table Panel**               | Displays data in table format                          | Pod status table                          |
| 🌍 **Geomap Panel**              | Visualizes geographic data                             | Multi-region monitoring                   |
| ⏰ **Time Range**                 | Period displayed on dashboard                          | Last 1 Hour                               |
| 🔍 **Time Picker**               | Tool to select dashboard time range                    | Last 24 Hours                             |
| 🔄 **Auto Refresh**              | Automatically refresh dashboard data                   | Refresh every 30 seconds                  |
| 📜 **JSON Model**                | Dashboard configuration format                         | Dashboard export/import                   |
| 📊 **Prometheus Data Source**    | Connect Grafana to Prometheus                          | Kubernetes metrics                        |
| ☁️ **CloudWatch Data Source**    | Connect AWS metrics                                    | EC2 Monitoring                            |
| 📈 **InfluxDB Data Source**      | Time-series database integration                       | IoT metrics                               |
| 🗄️ **MySQL Data Source**        | Query MySQL databases                                  | Business reports                          |
| 🐘 **PostgreSQL Data Source**    | Query PostgreSQL databases                             | Application analytics                     |
| 📊 **PromQL**                    | Query language for Prometheus                          | CPU usage query                           |
| 📡 **Webhook**                   | HTTP endpoint for notifications                        | Send alert to custom API                  |
| 💬 **Slack Notification**        | Send alerts to Slack                                   | DevOps channel alert                      |
| 👥 **Microsoft Teams Alert**     | Send alerts to Teams                                   | Operations team                           |
| 👤 **User**                      | Grafana account holder                                 | DevOps Engineer                           |
| 👥 **Team**                      | Group of Grafana users                                 | SRE Team                                  |
| 🛡️ **Role**                     | Access control level                                   | Admin, Editor, Viewer                     |
| 👀 **Viewer**                    | Read-only dashboard access                             | Monitoring team                           |
| ✏️ **Editor**                    | Can create and modify dashboards                       | DevOps Engineer                           |
| 👑 **Admin**                     | Full Grafana administration access                     | Grafana Administrator                     |
| 🔒 **RBAC**                      | Role-Based Access Control                              | Fine-grained permissions                  |
| 🔑 **API Key**                   | Authentication token for API access                    | Dashboard automation                      |
| 📜 **Provisioning**              | Automated Grafana configuration                        | Auto-create dashboards                    |
| 🧵 **Tracing**                   | Track requests across services                         | Microservices debugging                   |
| 📜 **Logs**                      | Application and system records                         | Error logs                                |
| 📡 **Metrics**                   | Numerical monitoring data                              | CPU usage                                 |
| 🔭 **Observability**             | Metrics + Logs + Traces                                | Full system visibility                    |
| 🚨 **Incident Dashboard**        | Dashboard for outage analysis                          | Production incident tracking              |
| 📊 **Business Dashboard**        | Dashboard for business KPIs                            | Revenue monitoring                        |
| 🏥 **Health Dashboard**          | Dashboard for infrastructure health                    | Cluster status                            |
