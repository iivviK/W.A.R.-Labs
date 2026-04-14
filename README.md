
# W.A.R. Labs (Web Attack & Response Lab)

A controlled environment for simulating real-world attack and defense scenarios (Red Team vs Blue Team).

## 🎯 Purpose

W.A.R. Labs was designed to bridge the gap between offensive security (pentesting) and defensive security (detection & response).

The goal is not only to exploit vulnerabilities, but to understand:

* how attacks are performed
* how they are detected
* how systems respond under real conditions

## 🧠 Approach

The lab follows a full security cycle:

Red Team → Attack
Blue Team → Detect & Analyze
Purple Team → Learn & Improve

This enables deep understanding of both attack techniques and defensive visibility.

---

## 🧱 Architecture

The environment is built as an isolated infrastructure:

* **Proxmox (bare metal)** → virtualization layer
* **Ubuntu VMs** → host systems
* **Docker** → vulnerable application container
* **OWASP Juice Shop** → target application
* **Nginx** → reverse proxy (traffic entry point)
* **VPN** → restricted access (no public exposure)
* **Wazuh** → centralized logging & monitoring

### 🔄 Traffic Flow

Attacker → Nginx (proxy) → Vulnerable App → Logs → Wazuh

* All HTTP traffic passes through the proxy layer
* Logging and monitoring are attached to the proxy (visibility point)
* Blue Team analyzes behavior based on real attack traffic

---

## 🔴 Red Team (Offensive)

* Exploits vulnerabilities in the target application
* Uses real-world attack techniques
* Focuses on gaining access and chaining vulnerabilities

## 🔵 Blue Team (Defensive)

* Monitors logs and traffic via Wazuh
* Detects anomalies and attack patterns
* Reconstructs attack paths and suggests mitigations

## 🟣 Purple Team (Collaboration)

* Joint analysis after each session
* Comparison of:

  * attack techniques vs detection capability
* Identification of gaps in both offense and defense

---

## 🔐 Security & Isolation

* The environment is fully isolated (VPN-only access)
* No external systems are targeted
* All activity is restricted to lab infrastructure

---

## 🧪 What This Demonstrates

* Understanding of full attack lifecycle
* Ability to simulate real-world security scenarios
* Knowledge of:

  * web application attacks
  * traffic analysis
  * log-based detection
* Hands-on experience with infrastructure and monitoring

---

## 🚀 Project Direction

W.A.R. Labs is being developed into a platform for:

* real-time attack/defense scenarios
* hands-on security training
* collaborative red/blue exercises

---

## 📌 Key Insight

Security is not only about finding vulnerabilities.

It is about understanding:

* how systems behave under attack
* how attacks are detected
* and where visibility breaks down
