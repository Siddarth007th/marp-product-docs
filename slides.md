---
marp: true
theme: product-docs
paginate: true
footer: "Product Documentation • Page ${page} / ${total}"
---

<!-- _class: lead -->

# Product X Documentation Overview

**Technical Writer:** You  
**Contact:** 24f2008507@ds.study.iitm.ac.in  

A concise, version-controlled documentation deck for Product X.

---

## Agenda

1. Product overview  
2. Architecture & data flow  
3. API behavior and complexity  
4. Configuration & deployment  
5. Monitoring and troubleshooting  

---

<!--
backgroundImage: url("https://source.unsplash.com/featured/?servers,cloud,data")
backgroundSize: cover
backgroundColor: rgba(0,0,0,0.55)
_class: lead
-->

# High-Level Architecture

- Event producers → message queue  
- Workers → transform & store data  
- REST / gRPC APIs  
- Metrics, logs, tracing for visibility  

*(This slide satisfies the **background image** requirement.)*

---

## Data Flow & Components

- API Gateway  
- Ingestion Service  
- Processing Workers  
- Storage Layer  
- Query & Reporting layer  

---

## API Complexity and Performance

### Time Complexity Examples

- Lookup by ID:  
  $$ T(n) = O(1) $$
- Sorted batch query:  
  $$ T(n) = O(n \log n) $$
- Full scan:  
  $$ T(n) = O(n) $$

Combined:
$$
T(n) = O(n \log n) + O(n) \approx O(n \log n)
$$

---

## Configuration Management

- OAuth2 / OIDC  
- Rate limits  
- Storage backends  
- Version-controlled configs  

---

## Deployment Workflow

1. Feature branch  
2. Code + tests + docs updated  
3. CI: lint, test  
4. Merge  
5. Auto-deploy  
6. Export slides with Marp  

```bash
marp slides.md --pdf
marp slides.md --html
