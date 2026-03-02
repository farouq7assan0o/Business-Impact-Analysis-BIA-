# Business Impact Analysis (BIA)

**Author:** Farouq Hassan
**Organization:** Bazaarjo
**Scenario:** 2-hour website outage following breach & service disruption
**Objective:** Identify critical processes, assess impact severity, and define recovery priorities

📄 Source: 

---

# 1 Scenario Overview

Following a confirmed breach and temporary service disruption, Bazaarjo conducted a **Business Impact Analysis (BIA)** to:

* Identify mission-critical business processes
* Quantify financial, customer, and regulatory impact
* Define RTO (Recovery Time Objective)
* Define RPO (Recovery Point Objective)
* Rank recovery priorities

This BIA supports:

* Disaster Recovery Planning (DRP)
* Incident Response alignment
* Executive-level recovery prioritization
* PCI-DSS and regulatory continuity requirements

---

# 2 Identified Critical Business Processes

Six critical business functions were identified (Page 1 ):

1. Online Order Processing
2. Payment Processing
3. Merchant Portal Operations
4. Customer Support & Refund Management
5. Product Catalog & Inventory Management
6. Incident Response & Monitoring

These represent revenue generation, compliance exposure, operational continuity, and reputational risk domains.

---

# 3 Completed BIA Table

The structured BIA table (Pages 1–2 ) evaluated each process across:

* Key systems
* Key personnel
* Key vendors
* Financial impact
* Customer impact
* Regulatory/legal impact
* RTO
* RPO

Below is the reconstructed analysis.

---

## 3.1 Online Order Processing

**Key Systems:**

* Web Application
* Order Database
* API Gateway

**Key People:**

* DevOps
* Backend Developers

**Key Vendor:**

* Cloud Hosting Provider

**Impact Assessment:**

* Financial Impact: High
* Customer Impact: High
* Regulatory Impact: Medium

**RTO:** 30 minutes
**RPO:** 5 minutes

### Justification (Page 2 )

* Revenue stops immediately during outage
* Data loss must be minimal to prevent duplicate/lost orders

---

## 3.2 Payment Processing

**Key Systems:**

* Payment Gateway
* Transaction Database

**Key People:**

* DevOps
* Security Team

**Key Vendors:**

* Payment Processor
* Bank

**Impact Assessment:**

* Financial Impact: High
* Customer Impact: High
* Regulatory Impact: High

**RTO:** 15 minutes
**RPO:** 0–5 minutes

### Justification (Pages 2–3 )

* PCI-DSS obligations
* Financial reconciliation sensitivity
* Near zero tolerance for data loss

---

## 3.3 Merchant Portal Operations

**Key Systems:**

* Merchant Dashboard
* Authentication System

**Key People:**

* Merchant Support
* Dev Team

**Key Vendor:**

* Identity Provider

**Impact Assessment:**

* Financial Impact: Medium
* Customer Impact: High
* Regulatory Impact: Low

**RTO:** 1 hour
**RPO:** 15 minutes

Merchants tolerate brief disruption but prolonged outage increases complaints and churn.

---

## 3.4 Customer Support & Refund Management

**Key Systems:**

* CRM
* Ticketing System

**Key People:**

* Support Agents
* Finance Team

**Key Vendor:**

* Refund Processor

**Impact Assessment:**

* Financial Impact: Medium
* Customer Impact: High
* Regulatory Impact: Medium

**RTO:** 2 hours
**RPO:** 30 minutes

### Justification

* Critical post-incident trust management
* Refund records must remain intact
* Limited ticket data loss acceptable

---

## 3.5 Product Catalog & Inventory Management

**Key Systems:**

* Inventory Database
* CMS

**Key People:**

* Product Operations Team

**Key Vendor:**

* Logistics Partner

**Impact Assessment:**

* Financial Impact: Medium
* Customer Impact: Medium
* Regulatory Impact: Low

**RTO:** 4 hours
**RPO:** 1 hour

Orders may proceed briefly using cached inventory data.

---

## 3.6 Incident Response & Monitoring

**Key Systems:**

* SIEM
* Monitoring Tools

**Key People:**

* SOC
* DevOps

**Key Vendor:**

* MSSP

**Impact Assessment:**

* Financial Impact: Low
* Customer Impact: Medium
* Regulatory Impact: High

**RTO:** 15 minutes
**RPO:** 0 minutes

### Justification (Page 3 )

* Essential for breach containment
* No log loss acceptable (legal & forensic requirements)

---

# 4 RTO & RPO Justification Summary

| Process            | RTO    | RPO     | Rationale                          |
| ------------------ | ------ | ------- | ---------------------------------- |
| Payment Processing | 15 min | 0–5 min | PCI-DSS + financial integrity      |
| Online Orders      | 30 min | 5 min   | Core revenue engine                |
| Incident Response  | 15 min | 0 min   | Forensic & regulatory preservation |
| Customer Support   | 2 hrs  | 30 min  | Trust recovery function            |
| Merchant Portal    | 1 hr   | 15 min  | Partner continuity                 |
| Product Catalog    | 4 hrs  | 1 hr    | Short-term resilience via cache    |

---

# 5 Process Ranking (Recovery Priority)

As defined on Page 3 :

1. Payment Processing (Highest Criticality)
2. Online Order Processing
3. Incident Response & Monitoring
4. Customer Support & Refunds
5. Merchant Portal Operations
6. Product Catalog & Inventory

---

# 6 Top 3 Critical Processes (Executive View)

## 1 Payment Processing

* Immediate financial exposure
* PCI-DSS regulatory implications
* Zero tolerance for transaction data loss

---

## 2 Online Order Processing

* Core revenue engine
* High customer visibility
* Social media backlash risk

---

## 3 Incident Response & Monitoring

* Enables breach containment
* Protects forensic evidence
* Prevents repeated compromise

---

# 7 Strategic Observations

This BIA demonstrates:

* Regulatory impact drives prioritization
* Payment and logging systems require near-zero RPO
* Revenue functions demand low RTO
* Support functions tolerate longer recovery
* Monitoring capability is critical during breach containment

---

# 8 Business Continuity Themes Identified

| Domain                 | Priority Theme                    |
| ---------------------- | --------------------------------- |
| Financial Systems      | Near real-time recovery           |
| Revenue Systems        | Rapid restoration                 |
| Security Monitoring    | Zero data loss tolerance          |
| Customer Trust         | Post-incident stabilization       |
| Operational Resilience | Controlled degradation acceptable |

---

# 9 Skills Demonstrated

* Business Impact Analysis (BIA) development
* RTO/RPO calculation & justification
* Critical process identification
* Regulatory continuity alignment
* Recovery prioritization methodology
* Executive-level recovery ranking
* Financial vs operational impact comparison
* Disaster recovery planning support

---

# 🔐 Final Determination

The Bazaarjo BIA establishes a clear recovery hierarchy aligned with:

* Revenue protection
* PCI-DSS compliance
* Regulatory evidence preservation
* Customer trust management

The defined RTOs and RPOs provide a measurable foundation for:

* Disaster Recovery Plan (DRP) implementation
* Backup architecture validation
* Incident recovery simulations
* Executive decision-making during outages
