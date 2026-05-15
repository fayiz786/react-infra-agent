# Advanced Python ReAct Infra Agent

A minimal yet enhanced Python ReAct (Reason + Act) agent that simulates infrastructure health diagnosis using step-by-step reasoning, tool execution, and structured incident reporting.

The project demonstrates how an AI agent can inspect infrastructure metrics such as CPU usage, disk pressure, memory utilization, and Kubernetes pod health to identify operational issues.

---

# Features

- ReAct reasoning workflow
- Multiple issue simulation
- Colored terminal logs
- Infrastructure diagnostics
- Structured incident report generation
- Google Colab compatible
- Beginner-friendly implementation

---

# ReAct Workflow

The agent follows the ReAct pattern:

```text
Thought → Action → Observation → Answer

# EXAMPLE

THOUGHT:
CPU usage may be causing instability.

ACTION:
check_cpu()

OBSERVATION:
{'cpu_usage': '94%', 'status': 'high'}

THOUGHT:
High CPU may affect Kubernetes pods.

ACTION:
get_pod_status()

OBSERVATION:
{'pod_name': 'payment-service', 'status': 'CrashLoopBackOff'}

FINAL INCIDENT REPORT:
Infrastructure resource exhaustion detected.