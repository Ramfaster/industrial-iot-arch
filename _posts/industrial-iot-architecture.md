---
layout: post
title: "Designing SCADA OPC-UA to Architecture on AWS"
date: 2026-03-02
categories: Industrial IoT, Architecture, AWS
tags: OPC-UA, Kafka, MSK, EKS, SCADA, High Availability
---

## 1. Introduction

In industrial IoT systems, OPC-UA is commonly used to collect data from SCADA systems.

This article explains how to design a reliable data pipeline using:

- SCADA Historina Server Architecture
- SCADA & OPC-UA Server ↔ OPC-UA Client Integration 
- AWS Architecture (EC2, SG, EKS, MSK, VPN, etc..)
- Time-Series Database Influx
- Industrial Streaming Systems
- High Availability Architecture
- Energy & Manufacturing Data Modeling

Designed for real-world industrial environments.

---

## 2. Architecture Overview

SCADA → OPC-UA → Collector → IoT OPC-UA Client → AWS EKS (Stream Processor) → TSDB → Dashboard

---

## 3. Key Design Considerations

### 1) Designed for real-world industrial environments.
Industrial systems require stable data ingestion even under network degradation.

### 2) High Availability Requirements
Unlike typical web systems, downtime impacts physical operations.

---

## High Availability Strategy

- Multi-AZ MSK cluster  
- Redundant OPC-UA collectors  
- Health-checked Kubernetes pods  
- Database replication strategy  

Reliability is not optional in industrial systems.

### 3) Security & Network
SCADA F/W Network & AWS VPN Tunnel
Industrial networks often restrict outbound connectivity.  
Architecture must respect operational policies.

### 4) Scalability
Containerized collectors deployed on AWS EKS.

---

## 4. Conclusion

Industrial IoT architecture must prioritize:

- Reliability  
- Operational continuity  
- Secure boundary management  
- Clear separation between OT and IT
  
OT-IT integration requires careful architecture design.
Scalability comes second to resilience.
More deep-dives will follow in upcoming articles.

---

More detailed architecture breakdown will follow.
