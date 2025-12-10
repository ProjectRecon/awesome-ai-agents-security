# Awesome AI Agents Security 
[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](http://creativecommons.org/publicdomain/zero/1.0/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/ProjectRecon/awesome-ai-agents-security/blob/main/CONTRIBUTING.md)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/ProjectRecon/awesome-ai-agents-security/graphs/commit-activity)

A curated list of open-source tools, frameworks, and resources for securing autonomous AI agents.

This list is organized by the **security lifecycle** of an autonomous agent, covering red teaming, runtime protection, sandboxing, and governance.

## 📖 Table of Contents

- [Agent Firewalls & Gateways (Runtime Protection)](#-agent-firewalls--gateways-runtime-protection)
- [Red Teaming & Vulnerability Scanners](#-red-teaming--vulnerability-scanners)
- [Static Analysis & Linters](#-static-analysis--linters)
- [Sandboxing & Isolation Environments](#-sandboxing--isolation-environments)
- [Guardrails & Compliance](#-guardrails--compliance)
- [Benchmarks & Datasets](#-benchmarks--datasets)
- [Identity & Authentication](#-identity--authentication)
- [Contributing](#-contributing)

---

## 🛡️ Agent Firewalls & Gateways (Runtime Protection)
*Tools that sit between the agent and the world to filter traffic, prevent unauthorized tool access, and block prompt injections.*

- **[AgentGateway](https://github.com/agentgateway/agentgateway)** - A Linux Foundation project providing an AI-native proxy for secure connectivity (A2A & MCP protocols). It adds RBAC, observability, and policy enforcement to agent-tool interactions.
- **[Envoy AI Gateway](https://gateway.envoyproxy.io/)** - An Envoy-based gateway that manages request traffic to GenAI services, providing a control point for rate limiting and policy enforcement.

## ⚔️ Red Teaming & Vulnerability Scanners
*Offensive tools to test agents for security flaws, loop conditions, and unauthorized actions.*

- **[Strix](https://github.com/usestrix/strix)** - An autonomous AI agent designed for penetration testing. It runs inside a docker sandbox to actively probe applications and generate verified exploit capabilities.
- **[PyRIT](https://github.com/Azure/PyRIT)** - Microsoft’s open-source red teaming framework for generative AI. It automates multi-turn adversarial attacks to test if an agent can be coerced into harmful behavior.
- **[Agentic Security](https://github.com/msoedov/agentic_security)** - A dedicated vulnerability scanner for agent workflows and LLMs capable of running multi-step jailbreaks and fuzzing attacks against agent logic.
- **[Garak](https://github.com/leondz/garak)** - The "Nmap for LLMs." A vulnerability scanner that probes models for hallucination, data leakage, and prompt injection susceptibilities.
- **[A2A Scanner](https://github.com/cisco-ai-defense/a2a-scanner)** - A scanner by Cisco designed to inspect "Agent-to-Agent" communication protocols for threats, validating agent identities and ensuring compliance with communication specs.
- **[Cybersecurity AI (CAI)](https://github.com/aliasrobotics/cai)** - A framework for building specialized security agents for offensive and defensive operations, often used in CTF (Capture The Flag) scenarios.

## 🔍 Static Analysis & Linters
*Tools to analyze agent configuration and logic code before deployment.*

- **[Agentic Radar](https://github.com/splx-ai/agentic-radar)** - A static analysis tool that visualizes agent workflows (LangGraph, CrewAI, AutoGen). It detects risky tool usage, permission loops, and maps them to known vulnerabilities.
- **[Agent Bound](https://github.com/ElPaisano/agent-bound)** - A design-time analysis tool that calculates "Agentic Entropy"—a metric to quantify the unpredictability and risk of infinite loops or unconstrained actions in agent architectures.
- **[Checkov](https://github.com/bridgecrewio/checkov)** - While primarily for IaC, Checkov includes policies for scanning AI infrastructure and configurations to prevent misconfigurations in deployment.

## 📦 Sandboxing & Isolation Environments
*Secure runtimes to prevent agents from damaging the host system during code execution.*

- **[SandboxAI](https://github.com/substratusai/sandboxai)** - An open-source runtime for executing AI-generated code (Python/Shell) in isolated containers with granular permission controls.
- **[Kubernetes Agent Sandbox](https://github.com/kubernetes-sigs/agent-sandbox)** - A Kubernetes Native project providing a Sandbox Custom Resource Definition (CRD) to manage isolated, stateful workloads for AI agents.
- **[Agent-Infra Sandbox](https://github.com/agent-infra/sandbox)** - An "All-In-One" sandbox combining Browser, Shell, VSCode, and File System access in a single Docker container, optimized for agentic tasks.
- **[OpenHands](https://github.com/All-Hands-AI/OpenHands)** - Formerly OpenDevin, this platform includes a secure runtime environment for autonomous coding agents to operate without accessing the host machine's sensitive files.

## 🚧 Guardrails & Compliance
*Middleware to enforce business logic and safety policies on inputs and outputs.*

- **[NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails)** - NVIDIA’s toolkit for adding programmable rails to LLM-based apps. It ensures agents stay on topic, avoid jailbreaks, and adhere to defined safety policies.
- **[Guardrails](https://github.com/guardrails-ai/guardrails)** - A Python framework for validating LLM outputs against structural and semantic rules (e.g., "must return valid JSON," "must not contain PII").
- **[LiteLLM Guardrails](https://github.com/BerriAI/litellm)** - While known for model proxying, LiteLLM includes built-in guardrail features to filter requests and responses across multiple LLM providers.

## 📊 Benchmarks & Datasets
*Resources to evaluate agent security performance.*

- **[CVE Bench](https://github.com/uiuc-kang-lab/cve-bench)** - A benchmark for evaluating an AI agent's ability to exploit real-world web application vulnerabilities (useful for testing defensive agents).

## 🆔 Identity & Authentication
*Tools to manage agent identity (non-human identities).*

- **[WSO2](https://github.com/wso2)** - An identity management solution that treats AI agents as first-class identities, enabling secure authentication and authorization for agent actions.

---

## 🤝 Contributing

Contributions are welcome! Please read the contribution guidelines first.

1. Fork the project.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.
