# Minimal Python ReAct Infra Agent

A minimal Python ReAct (Reason + Act) agent that diagnoses simulated infrastructure health issues such as high CPU usage, disk pressure, and Kubernetes pod crashes.

The agent follows the ReAct workflow:

Thought → Action → Observation → Answer

---

## Features

- Step-by-step reasoning
- Tool calling simulation
- Infrastructure issue diagnosis
- Structured incident report generation
- Google Colab compatible
- Simple and beginner-friendly implementation

---

## Simulated Infra Checks

The agent uses mock tools to simulate infrastructure monitoring:

- `check_cpu()`
- `check_disk()`
- `get_pod_status()`

---

## ReAct Workflow

Example reasoning chain:

```text
Thought:
CPU usage may be causing service instability.

Action:
check_cpu()

Observation:
{'cpu_usage': '92%', 'status': 'high'}

Thought:
High CPU can affect pod health. Check pod status.

Action:
get_pod_status()

Observation:
{'pod_name': 'payment-service', 'status': 'CrashLoopBackOff'}

Answer:
Root cause identified as high CPU and disk pressure.
