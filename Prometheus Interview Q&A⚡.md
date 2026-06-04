## ⚡ Prometheus in Kubernetes — Rapid Fire Interview Q&A
| #️⃣    | ❓ Interview Question                                     | ✅ Answer                                                                                               |
| ------ | -------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| 1️⃣    | 📊 What is Prometheus?                                   | 🚀 Open-source monitoring and alerting toolkit used to collect and store metrics.                      |
| 2️⃣    | ☸️ Why is Prometheus popular in Kubernetes?              | 🎯 Native Kubernetes integration and automatic service discovery.                                      |
| 3️⃣    | 🔍 Main purpose of Prometheus?                           | 📈 Monitor applications, infrastructure, and Kubernetes resources.                                     |
| 4️⃣    | 🏗️ Who created Prometheus?                              | 🚀 SoundCloud                                                                                          |
| 5️⃣    | 🌟 What is the CNCF status of Prometheus?                | 🏆 Graduated CNCF project.                                                                             |
| 6️⃣    | 📦 What type of data does Prometheus collect?            | 📊 Time-series metrics.                                                                                |
| 7️⃣    | ⏱️ What is a time-series metric?                         | 📈 Metric value stored with a timestamp.                                                               |
| 8️⃣    | 🔄 How does Prometheus collect metrics?                  | 🎯 Pull-based model (scraping targets).                                                                |
| 9️⃣    | 📥 What is Scraping?                                     | 🔍 Pulling metrics from targets periodically.                                                          |
| 🔟     | 🌐 Default Prometheus port?                              | 🚪 9090                                                                                                |
| 1️⃣1️⃣ | 📋 What are the main Prometheus components?              | 📊 Prometheus Server, 🚨 Alertmanager, 📈 Grafana, 🎯 Exporters                                        |
| 1️⃣2️⃣ | 🎯 What is a Target?                                     | 📡 Endpoint from which Prometheus collects metrics.                                                    |
| 1️⃣3️⃣ | 📊 What is a Metric?                                     | 🔢 Measured value like CPU, memory, requests.                                                          |
| 1️⃣4️⃣ | 🏷️ What are Labels in Prometheus?                       | 🔖 Key-value pairs used to identify metrics.                                                           |
| 1️⃣5️⃣ | 📈 Example Label?                                        | `pod="nginx-123"`                                                                                      |
| 1️⃣6️⃣ | 🔎 What is PromQL?                                       | 🧮 Prometheus Query Language used to query metrics.                                                    |
| 1️⃣7️⃣ | 📊 Example PromQL query?                                 | `up`                                                                                                   |
| 1️⃣8️⃣ | 🖥️ Query CPU usage example?                             | `rate(container_cpu_usage_seconds_total[5m])`                                                          |
| 1️⃣9️⃣ | 📦 What is an Exporter?                                  | 📡 Component exposing metrics for Prometheus.                                                          |
| 2️⃣0️⃣ | 🐧 Popular Linux exporter?                               | 🎯 Node Exporter                                                                                       |
| 2️⃣1️⃣ | ☸️ What is kube-state-metrics?                           | 📊 Exposes Kubernetes object metrics.                                                                  |
| 2️⃣2️⃣ | 🖥️ What does Node Exporter monitor?                     | CPU, Memory, Disk, Network.                                                                            |
| 2️⃣3️⃣ | ☸️ What does kube-state-metrics monitor?                 | Pods, Deployments, Nodes, StatefulSets.                                                                |
| 2️⃣4️⃣ | 🔔 What is Alertmanager?                                 | 🚨 Handles alerts from Prometheus.                                                                     |
| 2️⃣5️⃣ | 📧 Alertmanager notification channels?                   | 📧 Email, 💬 Slack, 📱 PagerDuty, 🌐 Webhooks                                                          |
| 2️⃣6️⃣ | 🚨 What is an Alert Rule?                                | 📋 Condition triggering an alert.                                                                      |
| 2️⃣7️⃣ | 📈 Example alert?                                        | CPU usage > 80% for 5 minutes.                                                                         |
| 2️⃣8️⃣ | 📊 What is Grafana?                                      | 📈 Visualization tool for Prometheus metrics.                                                          |
| 2️⃣9️⃣ | 🔗 How does Grafana connect to Prometheus?               | 📡 Prometheus acts as a data source.                                                                   |
| 3️⃣0️⃣ | ☸️ How is Prometheus usually installed in Kubernetes?    | 📦 Helm Chart (kube-prometheus-stack).                                                                 |
| 3️⃣1️⃣ | 🎯 Popular Helm chart?                                   | 🚀 kube-prometheus-stack                                                                               |
| 3️⃣2️⃣ | 📡 What is Service Discovery?                            | 🔍 Automatic discovery of monitoring targets.                                                          |
| 3️⃣3️⃣ | ☸️ Does Prometheus support Kubernetes Service Discovery? | ✅ Yes                                                                                                  |
| 3️⃣4️⃣ | 📋 What is a ServiceMonitor?                             | 🎯 CRD used to define scrape targets.                                                                  |
| 3️⃣5️⃣ | 📋 What is PodMonitor?                                   | 📦 CRD used to scrape pod metrics directly.                                                            |
| 3️⃣6️⃣ | 🎯 Which operator manages ServiceMonitor?                | 🚀 Prometheus Operator                                                                                 |
| 3️⃣7️⃣ | ⚙️ What is Prometheus Operator?                          | 🤖 Automates Prometheus deployment and management.                                                     |
| 3️⃣8️⃣ | 📊 What Kubernetes metrics are commonly monitored?       | CPU, Memory, Pods, Nodes, Storage, Network.                                                            |
| 3️⃣9️⃣ | 🖥️ Metric to check node status?                         | `kube_node_status_condition`                                                                           |
| 4️⃣0️⃣ | 📦 Metric to check pod count?                            | `kube_pod_info`                                                                                        |
| 4️⃣1️⃣ | 💾 Monitor PVC usage using?                              | `kubelet_volume_stats_used_bytes`                                                                      |
| 4️⃣2️⃣ | 📉 What is Retention Period?                             | ⏳ How long metrics are stored.                                                                         |
| 4️⃣3️⃣ | 💽 Where does Prometheus store data?                     | 📦 Local TSDB (Time-Series Database).                                                                  |
| 4️⃣4️⃣ | 🔒 Is Prometheus storage persistent by default?          | ❌ No, configure PVC.                                                                                   |
| 4️⃣5️⃣ | 📦 Why use PVC for Prometheus?                           | 💾 Persist monitoring data.                                                                            |
| 4️⃣6️⃣ | 🚀 What is Remote Write?                                 | 📡 Send metrics to external storage.                                                                   |
| 4️⃣7️⃣ | ☁️ Examples of long-term storage?                        | 🏗️ Thanos, Cortex, Mimir                                                                              |
| 4️⃣8️⃣ | 📈 Why use Thanos?                                       | 🌍 Long-term storage and HA Prometheus.                                                                |
| 4️⃣9️⃣ | 🚨 Pod restarted unexpectedly. What should you check?    | 📊 Prometheus metrics and alerts.                                                                      |
| 5️⃣0️⃣ | 📦 Pod in CrashLoopBackOff. Which metrics help?          | CPU, Memory, Restart Count.                                                                            |
| 5️⃣1️⃣ | 🧠 High memory usage in pod. Which metric?               | `container_memory_usage_bytes`                                                                         |
| 5️⃣2️⃣ | 💻 High CPU usage in pod. Which metric?                  | `container_cpu_usage_seconds_total`                                                                    |
| 5️⃣3️⃣ | 📉 Node under pressure. What check?                      | CPU, Memory, Disk metrics.                                                                             |
| 5️⃣4️⃣ | 🚨 Cluster suddenly slow. What investigate?              | Node metrics, API Server metrics, etcd metrics.                                                        |
| 5️⃣5️⃣ | 📡 Service not reachable. Prometheus helps how?          | Check service availability metrics.                                                                    |
| 5️⃣6️⃣ | 🌐 Which metric shows target health?                     | `up`                                                                                                   |
| 5️⃣7️⃣ | ❌ `up = 0` means?                                        | 🚨 Target unreachable.                                                                                 |
| 5️⃣8️⃣ | 📊 Which component monitors Kubernetes API Server?       | 🎯 Prometheus                                                                                          |
| 5️⃣9️⃣ | 🛡️ Can Prometheus monitor etcd?                         | ✅ Yes                                                                                                  |
| 6️⃣0️⃣ | 🛡️ Can Prometheus monitor CoreDNS?                      | ✅ Yes                                                                                                  |
| 6️⃣1️⃣ | 🛡️ Can Prometheus monitor Ingress Controllers?          | ✅ Yes                                                                                                  |
| 6️⃣2️⃣ | 📈 Why monitor kubelet?                                  | 🔍 Node and pod performance metrics.                                                                   |
| 6️⃣3️⃣ | 📦 Which metric shows pod restarts?                      | `kube_pod_container_status_restarts_total`                                                             |
| 6️⃣4️⃣ | 🚀 Why is Prometheus important in DevOps?                | 📊 Observability and proactive monitoring.                                                             |
| 6️⃣5️⃣ | 🔄 Prometheus Pull vs Push?                              | 📥 Pull-based by default.                                                                              |
| 6️⃣6️⃣ | 📤 When use Pushgateway?                                 | 🕒 Short-lived batch jobs.                                                                             |
| 6️⃣7️⃣ | 🎯 What is Pushgateway?                                  | 📡 Allows ephemeral jobs to push metrics.                                                              |
| 6️⃣8️⃣ | 📊 Prometheus vs CloudWatch?                             | ☸️ Prometheus = Kubernetes/Open Source, ☁️ CloudWatch = AWS-native monitoring.                         |
| 6️⃣9️⃣ | 📊 Prometheus vs Grafana?                                | 📈 Prometheus collects metrics; Grafana visualizes metrics.                                            |
| 7️⃣0️⃣ | 🚨 Most common Prometheus production issue?              | 💾 Storage exhaustion and high cardinality metrics.                                                    |
| 7️⃣1️⃣ | ⚠️ What is High Cardinality?                             | 🔖 Too many unique labels causing performance issues.                                                  |
| 7️⃣2️⃣ | 🏆 Best practice for Prometheus?                         | 📦 Use PVC, Alertmanager, Grafana, and retention tuning.                                               |
| 7️⃣3️⃣ | 🏆 Best Kubernetes monitoring stack?                     | 🚀 Prometheus + Grafana + Alertmanager                                                                 |
| 7️⃣4️⃣ | 🎯 Interview Gold: Prometheus in one line?               | 📊 Open-source monitoring system that collects and stores Kubernetes metrics using a pull-based model. |
| 7️⃣5️⃣ | 🎯 Interview Gold: Real-world architecture?              | ☸️ Kubernetes → Exporters → Prometheus → Alertmanager → Grafana → Slack/Email Alerts                   |

