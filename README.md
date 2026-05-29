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
| 📊 **Instant Query**          | Current metric value                            | CPU usage now                                         |
| ⏳ **Range Query**             | Metric values over time                         | CPU last 1 hour                                       |
| ➕ **sum()**                   | Adds metric values                              | Total CPU usage                                       |
| 📈 **avg()**                  | Calculates average                              | Average memory usage                                  |
| 🔝 **max()**                  | Highest value                                   | Peak CPU                                              |
| 🔻 **min()**                  | Lowest value                                    | Minimum latency                                       |
| 🚀 **rate()**                 | Per-second increase rate                        | Requests/sec                                          |
| ⚡ **irate()**                 | Instantaneous rate                              | Real-time request rate                                |
| 🔢 **count()**                | Counts metrics                                  | Number of pods                                        |
| 🎯 **by()**                   | Group results by label                          | By namespace                                          |
| 🚫 **without()**              | Exclude labels from grouping                    | Ignore instance label                                 |
| 🚨 **Alert Rule**             | Condition that triggers an alert                | CPU > 80%                                             |
| 📜 **Alertmanager**           | Manages and routes alerts                       | Sends email alerts                                    |
| 📧 **Receiver**               | Alert destination                               | Email, Slack                                          |
| 🔇 **Silence**                | Temporarily suppress alerts                     | Maintenance window                                    |
| 🔀 **Routing**                | Send alerts to different teams                  | DB Team alerts                                        |
| 🏷️ **Alert Labels**          | Metadata attached to alerts                     | Severity=Critical                                     |
| 📝 **Annotations**            | Additional alert information                    | Alert description                                     |
| 🔥 **Firing Alert**           | Active alert condition                          | CPU high                                              |
| ✅ **Resolved Alert**          | Alert condition cleared                         | CPU normal                                            |
| ☸️ **Prometheus Operator**    | Kubernetes operator for Prometheus              | Simplifies deployment                                 |
| 📦 **ServiceMonitor**         | Defines services to monitor                     | Monitor application service                           |
| 🎯 **PodMonitor**             | Defines pods to monitor                         | Monitor pod metrics                                   |
| 📜 **Prometheus CRD**         | Custom resource for Prometheus                  | Operator-managed config                               |
| 📈 **Metrics Server**         | Resource metrics provider                       | HPA metrics                                           |
| 🔄 **HPA**                    | Horizontal Pod Autoscaler                       | Scale based on CPU                                    |
| 🚀 **Helm Chart**             | Package to install Prometheus                   | kube-prometheus-stack                                 |
| 💾 **Retention Period**       | How long metrics are stored                     | 15 days                                               |
| 📦 **Local Storage**          | Metrics stored on disk                          | Prometheus TSDB                                       |
| 🗃️ **Remote Storage**        | External metric storage                         | Thanos, Cortex                                        |
| 🔄 **Remote Write**           | Send metrics elsewhere                          | Thanos                                                |
| 📥 **Remote Read**            | Read metrics from external storage              | Historical data                                       |
| 🧹 **Compaction**             | Optimizes stored data                           | Reduces disk usage                                    |
| ♻️ **High Availability (HA)** | Multiple Prometheus servers                     | Avoid single point of failure                         |
| 🌍 **Federation**             | Prometheus server scraping another Prometheus   | Central monitoring                                    |
| 📈 **Sharding**               | Split monitoring load across servers            | Large environments                                    |
| ☁️ **Thanos**                 | Long-term storage & global querying             | Multi-cluster monitoring                              |
| 🏗️ **Cortex**                | Horizontally scalable Prometheus backend        | Enterprise monitoring                                 |
| 🚀 **Mimir**                  | Grafana scalable metrics backend                | Large-scale monitoring                                |
| 📊 **Grafana**                | Visualization tool for metrics                  | Monitoring dashboards                                 |
| 📋 **Dashboard**              | Collection of monitoring graphs                 | Kubernetes dashboard                                  |
| 📈 **Panel**                  | Single graph or visualization                   | CPU chart                                             |
| 🎨 **Template Variable**      | Dynamic dashboard filter                        | Select namespace                                      |
| 🔔 **Grafana Alerting**       | Alerts created in Grafana                       | Memory alert                                          |

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
| 📉 **Stat Panel**                | Shows a single metric value                            | Current Memory Usage                      |
| 🎛️ **Gauge Panel**              | Displays value within a range                          | CPU utilization gauge                     |
| 🥧 **Pie Chart**                 | Shows percentage distribution                          | Resource usage breakdown                  |
| 📋 **Table Panel**               | Displays data in table format                          | Pod status table                          |
| 🌍 **Geomap Panel**              | Visualizes geographic data                             | Multi-region monitoring                   |
| 🔥 **Heatmap**                   | Shows value density over time                          | Request latency distribution              |
| 🧭 **Canvas Panel**              | Custom visual dashboards                               | Infrastructure topology                   |
| 🎨 **Theme**                     | Dashboard appearance setting                           | Dark Mode, Light Mode                     |
| 🏷️ **Template Variable**        | Dynamic filter for dashboards                          | Select Namespace                          |
| 🔄 **Variable Query**            | Query used to populate variables                       | List all Kubernetes namespaces            |
| 📝 **Annotations**               | Events marked on graphs                                | Deployment happened at 2 PM               |
| ⏰ **Time Range**                 | Period displayed on dashboard                          | Last 1 Hour                               |
| 🔍 **Time Picker**               | Tool to select dashboard time range                    | Last 24 Hours                             |
| 🔄 **Auto Refresh**              | Automatically refresh dashboard data                   | Refresh every 30 seconds                  |
| 📜 **JSON Model**                | Dashboard configuration format                         | Dashboard export/import                   |
| 📦 **Folder**                    | Organizes dashboards                                   | Production Dashboards Folder              |
| ⭐ **Starred Dashboard**          | Favorite dashboard                                     | Frequently used dashboard                 |
| 📤 **Dashboard Export**          | Save dashboard as JSON                                 | Backup dashboard                          |
| 📥 **Dashboard Import**          | Load dashboard from JSON                               | Import community dashboard                |
| 🌐 **Public Dashboard**          | Share dashboard publicly                               | Public monitoring view                    |
| 🔗 **Dashboard Link**            | Link between dashboards                                | Navigate to detailed dashboard            |
| 📊 **Prometheus Data Source**    | Connect Grafana to Prometheus                          | Kubernetes metrics                        |
| 📜 **Loki Data Source**          | Connect Grafana to Loki                                | Application logs                          |
| 🔍 **Elasticsearch Data Source** | Connect to Elasticsearch                               | Log analytics                             |
| ☁️ **CloudWatch Data Source**    | Connect AWS metrics                                    | EC2 Monitoring                            |
| 📈 **InfluxDB Data Source**      | Time-series database integration                       | IoT metrics                               |
| 🗄️ **MySQL Data Source**        | Query MySQL databases                                  | Business reports                          |
| 🐘 **PostgreSQL Data Source**    | Query PostgreSQL databases                             | Application analytics                     |
| 📊 **PromQL**                    | Query language for Prometheus                          | CPU usage query                           |
| 🔎 **LogQL**                     | Query language for Loki                                | Search application logs                   |
| 📈 **Metric Query**              | Query retrieving metrics                               | Memory utilization                        |
| 📜 **Log Query**                 | Query retrieving logs                                  | Error logs                                |
| 🚨 **Alert Rule**                | Condition that triggers an alert                       | CPU > 80%                                 |
| 🔔 **Alerting**                  | Grafana feature for notifications                      | Email alert                               |
| 📧 **Contact Point**             | Alert destination                                      | Email, Slack, Teams                       |
| 🔀 **Notification Policy**       | Routes alerts to recipients                            | Send DB alerts to DBA team                |
| 🏷️ **Alert Labels**             | Metadata attached to alerts                            | Severity=Critical                         |
| 📝 **Alert Annotations**         | Additional alert information                           | Description and runbook                   |
| 🔥 **Firing Alert**              | Active alert condition                                 | High CPU                                  |
| ✅ **Resolved Alert**             | Alert condition cleared                                | CPU normal                                |
| ⏳ **Pending Alert**              | Alert waiting before firing                            | CPU high for 2 minutes                    |
| 📢 **Alert Instance**            | Specific occurrence of an alert                        | CPU alert on server-01                    |
| 📡 **Webhook**                   | HTTP endpoint for notifications                        | Send alert to custom API                  |
| 💬 **Slack Notification**        | Send alerts to Slack                                   | DevOps channel alert                      |
| 👥 **Microsoft Teams Alert**     | Send alerts to Teams                                   | Operations team                           |
| 📱 **PagerDuty Integration**     | Incident management integration                        | Critical production alerts                |
| 📧 **Email Notification**        | Email-based alerting                                   | Alert to admins                           |
| 🔐 **Organization**              | Multi-tenant Grafana environment                       | Separate Dev and Prod teams               |
| 👤 **User**                      | Grafana account holder                                 | DevOps Engineer                           |
| 👥 **Team**                      | Group of Grafana users                                 | SRE Team                                  |
| 🛡️ **Role**                     | Access control level                                   | Admin, Editor, Viewer                     |
| 👀 **Viewer**                    | Read-only dashboard access                             | Monitoring team                           |
| ✏️ **Editor**                    | Can create and modify dashboards                       | DevOps Engineer                           |
| 👑 **Admin**                     | Full Grafana administration access                     | Grafana Administrator                     |
| 🔒 **RBAC**                      | Role-Based Access Control                              | Fine-grained permissions                  |
| 🔑 **API Key**                   | Authentication token for API access                    | Dashboard automation                      |
| 🌐 **SSO**                       | Single Sign-On integration                             | Azure AD Login                            |
| 🔐 **OAuth**                     | External authentication method                         | GitHub Login                              |
| ☸️ **Grafana Operator**          | Kubernetes operator for Grafana                        | Automated deployment                      |
| 🚀 **Helm Chart**                | Package for Grafana installation                       | Install Grafana on Kubernetes             |
| 📦 **Grafana Agent**             | Lightweight telemetry collector                        | Send metrics and logs                     |
| 📜 **Provisioning**              | Automated Grafana configuration                        | Auto-create dashboards                    |
| ⚙️ **Configuration File**        | Grafana settings file                                  | `grafana.ini`                             |
| ☁️ **Grafana Cloud**             | Managed Grafana service                                | SaaS monitoring platform                  |
| 📊 **Loki**                      | Grafana log aggregation system                         | Centralized logging                       |
| 🔍 **Tempo**                     | Grafana distributed tracing backend                    | Request tracing                           |
| 📈 **Mimir**                     | Grafana metrics backend                                | Large-scale Prometheus storage            |
| 🧵 **Tracing**                   | Track requests across services                         | Microservices debugging                   |
| 📜 **Logs**                      | Application and system records                         | Error logs                                |
| 📡 **Metrics**                   | Numerical monitoring data                              | CPU usage                                 |
| 🔭 **Observability**             | Metrics + Logs + Traces                                | Full system visibility                    |
| 🚀 **Unified Monitoring**        | Single pane of glass monitoring                        | Metrics, logs, traces together            |
| 📉 **SLI**                       | Service Level Indicator                                | API response time                         |
| 🎯 **SLO**                       | Service Level Objective                                | 99.9% uptime target                       |
| 📜 **SLA**                       | Service Level Agreement                                | Customer uptime commitment                |
| 🚨 **Incident Dashboard**        | Dashboard for outage analysis                          | Production incident tracking              |
| 📊 **Business Dashboard**        | Dashboard for business KPIs                            | Revenue monitoring                        |
| 🏥 **Health Dashboard**          | Dashboard for infrastructure health                    | Cluster status                            |
| 🔄 **Refresh Interval**          | Frequency of dashboard updates                         | Every 15 seconds                          |
| 📦 **Library Panel**             | Reusable panel across dashboards                       | Common CPU panel                          |
| 🎨 **Dashboard Templating**      | Dynamic dashboards using variables                     | Environment selection                     |
| 🧩 **Plugin**                    | Extension for Grafana functionality                    | New visualization type                    |
| 🏪 **Plugin Marketplace**        | Repository of Grafana plugins                          | Install community plugins                 |
| 🌍 **Multi-Tenancy**             | Support multiple teams/orgs                            | Shared Grafana instance                   |
| ♻️ **High Availability (HA)**    | Multiple Grafana instances                             | No single point of failure                |

