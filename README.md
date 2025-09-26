# System Design Learning

## Table of Contents

1. [Foundations & Fundamentals](#1-foundations--fundamentals)
   - 1.1 [System Design Introduction](#11-system-design-introduction)
   - 1.2 [Performance Metrics & Trade-offs](#12-performance-metrics--trade-offs)

2. [Networking & Communication Fundamentals](#2-networking--communication-fundamentals)
   - 2.1 [Network Basics](#21-network-basics)
   - 2.2 [DNS & Domain Resolution](#22-dns--domain-resolution)
   - 2.3 [HTTP & Web Protocols](#23-http--web-protocols)
   - 2.4 [Proxy & Gateway Patterns](#24-proxy--gateway-patterns)

3. [APIs & Communication Patterns](#3-apis--communication-patterns)
   - 3.1 [API Design Patterns](#31-api-design-patterns)
   - 3.2 [Real-time Communication](#32-real-time-communication)
   - 3.3 [API Management](#33-api-management)

4. [Databases & Data Storage](#4-databases--data-storage)
   - 4.1 [Database Fundamentals](#41-database-fundamentals)
   - 4.2 [Database Design & Optimization](#42-database-design--optimization)
   - 4.3 [Transactions & Consistency](#43-transactions--consistency)
   - 4.4 [Database Scaling Strategies](#44-database-scaling-strategies)
   - 4.5 [Database Internals](#45-database-internals)

5. [Caching Strategies](#5-caching-strategies)
   - 5.1 [Caching Fundamentals](#51-caching-fundamentals)
   - 5.2 [Caching Patterns](#52-caching-patterns)
   - 5.3 [Cache Policies & Management](#53-cache-policies--management)
   - 5.4 [Caching Infrastructure](#54-caching-infrastructure)

6. [Load Balancing & Scaling](#6-load-balancing--scaling)
   - 6.1 [Scaling Approaches](#61-scaling-approaches)
   - 6.2 [Load Balancing](#62-load-balancing)
   - 6.3 [Advanced Scaling Patterns](#63-advanced-scaling-patterns)

7. [System Architecture Patterns](#7-system-architecture-patterns)
   - 7.1 [Architectural Styles](#71-architectural-styles)
   - 7.2 [Communication Patterns](#72-communication-patterns)
   - 7.3 [Advanced Patterns](#73-advanced-patterns)

8. [Message Queues & Event Systems](#8-message-queues--event-systems)
   - 8.1 [Asynchronous Communication](#81-asynchronous-communication)
   - 8.2 [Message Queue Systems](#82-message-queue-systems)
   - 8.3 [Event Streaming Platforms](#83-event-streaming-platforms)
   - 8.4 [Enterprise Integration](#84-enterprise-integration)

9. [Distributed Systems Concepts](#9-distributed-systems-concepts)
   - 9.1 [Distributed Systems Fundamentals](#91-distributed-systems-fundamentals)
   - 9.2 [Consensus & Coordination](#92-consensus--coordination)
   - 9.3 [Time & Ordering](#93-time--ordering)
   - 9.4 [Fault Tolerance & Reliability](#94-fault-tolerance--reliability)
   - 9.5 [Advanced Distributed Concepts](#95-advanced-distributed-concepts)

10. [Data Structures & Algorithms for Systems](#10-data-structures--algorithms-for-systems)
    - 10.1 [Specialized Data Structures](#101-specialized-data-structures)
    - 10.2 [Tree Structures](#102-tree-structures)
    - 10.3 [Hashing & Partitioning](#103-hashing--partitioning)
    - 10.4 [Search & Indexing](#104-search--indexing)

11. [Big Data & Analytics](#11-big-data--analytics)
    - 11.1 [Data Processing Paradigms](#111-data-processing-paradigms)
    - 11.2 [Big Data Technologies](#112-big-data-technologies)
    - 11.3 [Data Storage Systems](#113-data-storage-systems)

12. [Security](#12-security)
    - 12.1 [Authentication & Authorization](#121-authentication--authorization)
    - 12.2 [Security Protocols & Standards](#122-security-protocols--standards)
    - 12.3 [Network Security](#123-network-security)
    - 12.4 [Application Security](#124-application-security)
    - 12.5 [Data Security](#125-data-security)

13. [Cloud & Infrastructure](#13-cloud--infrastructure)
    - 13.1 [Cloud Computing Models](#131-cloud-computing-models)
    - 13.2 [Containerization & Orchestration](#132-containerization--orchestration)
    - 13.3 [Cloud Storage](#133-cloud-storage)
    - 13.4 [Infrastructure as Code](#134-infrastructure-as-code)

14. [Observability & Operations](#14-observability--operations)
    - 14.1 [Logging](#141-logging)
    - 14.2 [Monitoring & Metrics](#142-monitoring--metrics)
    - 14.3 [Distributed Tracing](#143-distributed-tracing)
    - 14.4 [Alerting & Incident Response](#144-alerting--incident-response)
    - 14.5 [Reliability Engineering](#145-reliability-engineering)

15. [Advanced System Design Patterns](#15-advanced-system-design-patterns)
    - 15.1 [Fan Patterns](#151-fan-patterns)
    - 15.2 [Retry & Resilience Patterns](#152-retry--resilience-patterns)
    - 15.3 [Data Synchronization](#153-data-synchronization)

16. [System Design Trade-offs & Decisions](#16-system-design-trade-offs--decisions)
    - 16.1 [Common Trade-offs](#161-common-trade-offs)
    - 16.2 [Decision Frameworks](#162-decision-frameworks)
      
17. [System Design Interview Problems](#17-system-design-interview-problems)

18. [System Design Interview Template](#18-system-design-interview-template)
    - [Requirements](#181-requirements)
      - [Functional Requirements](#1811-functional-requirements)
      - [Non Functional Requirements](#1812-non-functional-requirements)
      - [Capacity Estimation](#1813-capacity-estimation)
    - [Core Entities](#182-core-entities)
    - [API or Interface](#183-api-or-interface)
    - [Data Flow](#184-data-flow)
    - [High Level Design](#185-high-level-design)
    - [Deep Dives](#186-deep-dives)

20. [System Design Practice Problems](#19-system-design-practice-problems)
    - 19.1 [Design a Rate Limiter](#191-design-a-rate-limiter)
    - 19.2 [Design a URL Shortener (Bitly)](#192-design-a-url-shortener-bitly)
    - 19.3 [Design a Twitter / Feed System](#193-design-a-twitter--feed-system)
    - 19.4 [Design WhatsApp / Messaging App](#194-design-whatsapp--messaging-app)
    - 19.5 [Design Instagram / Photo Sharing](#195-design-instagram--photo-sharing)
    - 19.6 [Design YouTube / Video Streaming](#196-design-youtube--video-streaming)
    - 19.7 [Design an E-commerce Platform](#197-design-an-e-commerce-platform)
    - 19.8 [Design Uber / Ride-Sharing](#198-design-uber--ride-sharing)
    - 19.9 [Design a Notification System](#199-design-a-notification-system)
    - 19.10 [Design an Online Collaborative Editor](#1910-design-an-online-collaborative-editor)
    - 19.11 [Design a File Storage System (Dropbox / Google Drive)](#1911-design-a-file-storage-system-dropbox--google-drive)
    - 19.12 [Design a Leaderboard / Ranking System](#1912-design-a-leaderboard--ranking-system)
    - 19.13 [Design a Search Engine / Autocomplete](#1913-design-a-search-engine--autocomplete)
    - 19.14 [Design a Payment Gateway](#1914-design-a-payment-gateway)
    - 19.15 [Design a Job Scheduler](#1915-design-a-job-scheduler)



## 1. Foundations & Fundamentals

### 1.1 System Design Introduction
- What is System Design?
- Why is System Design Important?
- High-Level Design vs Low-Level Design
- System Design Interview Process
- Key System Characteristics (Scalability, Performance, Reliability, Availability, Maintainability, Security)

### 1.2 Performance Metrics & Trade-offs
- Latency vs Throughput vs Bandwidth
- Response Time, Processing Time, Queue Time
- Performance vs Cost Trade-offs
- Quality Attributes (FURPS+)

## 2. Networking & Communication Fundamentals

### 2.1 Network Basics
- OSI Model & TCP/IP Stack
- IP Addresses (IPv4/IPv6, Public/Private, Static/Dynamic)
- Subnets and CIDR
- NAT (Network Address Translation)
- TCP vs UDP (Connection-oriented vs Connectionless)

### 2.2 DNS & Domain Resolution
- DNS (Domain Name System)
- DNS Resolution Flow
- DNS Records (A, AAAA, CNAME, MX, TXT)
- DNS Load Balancing
- GeoDNS

### 2.3 HTTP & Web Protocols
- HTTP vs HTTPS
- HTTP Methods & Status Codes
- HTTP Headers & Cookies
- HTTP/1.1 vs HTTP/2 vs HTTP/3
- Keep-Alive Connections
- SSL/TLS Handshake

### 2.4 Proxy & Gateway Patterns
- Forward Proxy vs Reverse Proxy
- API Gateway
- Application Load Balancer vs Network Load Balancer
- CDN (Content Delivery Network)

## 3. APIs & Communication Patterns

### 3.1 API Design Patterns
- REST API Design Principles
- RESTful Resource Naming
- GraphQL (Query Language & Schema)
- gRPC (Protocol Buffers & Streaming)
- API Versioning Strategies

### 3.2 Real-time Communication
- WebSockets vs Server-Sent Events (SSE)
- Long Polling vs Short Polling
- WebRTC (Peer-to-Peer Communication)
- Push Notifications

### 3.3 API Management
- Rate Limiting & Throttling
- API Authentication & Authorization
- Idempotency
- Pagination
- Error Handling & Status Codes
- Webhooks

## 4. Databases & Data Storage

### 4.1 Database Fundamentals
- DBMS Basics
- SQL vs NoSQL Trade-offs
- Database Types:
  - Relational (RDBMS)
  - Document (MongoDB, CouchDB)
  - Key-Value (Redis, DynamoDB)
  - Wide-Column (Cassandra, HBase)
  - Graph (Neo4j, Amazon Neptune)
  - Time-Series (InfluxDB, TimescaleDB)
  - NewSQL (CockroachDB, Spanner)

### 4.2 Database Design & Optimization
- Database Schema Design
- Normalization (1NF, 2NF, 3NF) vs Denormalization
- Database Indexing (B-tree, Hash, Bitmap, Full-text)
- Query Optimization
- Database Constraints & Referential Integrity

### 4.3 Transactions & Consistency
- ACID Properties
- Transaction Isolation Levels
- Distributed Transactions
- Two-Phase Commit (2PC) vs Saga Pattern
- Optimistic vs Pessimistic Locking

### 4.4 Database Scaling Strategies
- Vertical Scaling (Scale Up)
- Horizontal Scaling:
  - Database Replication (Master-Slave, Master-Master)
  - Database Sharding (Horizontal Partitioning)
  - Vertical Partitioning
- Database Federation
- Change Data Capture (CDC)
- Global Secondary Indexes (GSI)

### 4.5 Database Internals
- Storage Engines (InnoDB, MyISAM)
- Write-Ahead Logging (WAL)
- LSM Trees vs B-Trees
- Buffer Pool Management
- How Databases Ensure Durability

## 5. Caching Strategies

### 5.1 Caching Fundamentals
- What is Caching & Why Cache?
- Cache Hit vs Cache Miss
- Cache Locality (Temporal & Spatial)

### 5.2 Caching Patterns
- Cache-Aside (Lazy Loading)
- Write-Through
- Write-Back (Write-Behind)
- Write-Around
- Refresh-Ahead

### 5.3 Cache Policies & Management
- Cache Eviction Policies (LRU, LFU, FIFO, Random)
- Cache Coherence
- Cache Invalidation Strategies
- TTL (Time to Live)

### 5.4 Caching Infrastructure
- In-Memory Caching (Redis, Memcached)
- Distributed Caching
- CDN (Content Delivery Network)
- Browser Caching
- Database Query Result Caching
- Application-Level Caching

## 6. Load Balancing & Scaling

### 6.1 Scaling Approaches
- Vertical Scaling vs Horizontal Scaling
- Stateful vs Stateless Applications
- Auto-scaling Strategies

### 6.2 Load Balancing
- Load Balancer Types (L4 vs L7)
- Load Balancing Algorithms:
  - Round Robin (Weighted)
  - Least Connections
  - IP Hash
  - Geographic
  - Health Check-based
- Sticky Sessions vs Session Affinity
- Health Checks & Circuit Breakers

### 6.3 Advanced Scaling Patterns
- Clustering & High Availability
- Blue-Green Deployment
- Canary Deployment
- Feature Flags

## 7. System Architecture Patterns

### 7.1 Architectural Styles
- Monolithic Architecture
- Microservices Architecture
- Service-Oriented Architecture (SOA)
- Serverless Architecture (FaaS)
- Jamstack Architecture

### 7.2 Communication Patterns
- Client-Server Architecture
- N-Tier Architecture
- Peer-to-Peer (P2P)
- Event-Driven Architecture
- Request-Response vs Publish-Subscribe

### 7.3 Advanced Patterns
- CQRS (Command Query Responsibility Segregation)
- Event Sourcing
- Saga Pattern (Choreography vs Orchestration)
- Strangler Fig Pattern
- Bulkhead Pattern
- Sidecar Pattern
- Service Mesh

## 8. Message Queues & Event Systems

### 8.1 Asynchronous Communication
- Synchronous vs Asynchronous Communication
- Message Queues vs Publish-Subscribe
- Point-to-Point vs Publish-Subscribe Models

### 8.2 Message Queue Systems
- Message Broker Architecture
- Queue vs Topic
- Message Ordering & Delivery Guarantees
- Dead Letter Queues
- Message Acknowledgment Patterns

### 8.3 Event Streaming Platforms
- Apache Kafka Architecture
- Event Streaming vs Message Queuing
- Event Sourcing Implementation
- Stream Processing

### 8.4 Enterprise Integration
- Enterprise Service Bus (ESB)
- Message Transformation
- Content-Based Routing

## 9. Distributed Systems Concepts

### 9.1 Distributed Systems Fundamentals
- CAP Theorem (Consistency, Availability, Partition Tolerance)
- PACELC Theorem
- Consistency Models:
  - Strong Consistency
  - Eventual Consistency
  - Causal Consistency
  - Session Consistency

### 9.2 Consensus & Coordination
- Consensus Algorithms:
  - Paxos
  - Raft
  - PBFT (Practical Byzantine Fault Tolerance)
- Leader Election
- Distributed Locking
- Service Discovery & Service Registry

### 9.3 Time & Ordering
- Vector Clocks & Logical Clocks
- Lamport Timestamps
- Event Ordering in Distributed Systems
- Clock Synchronization (NTP)

### 9.4 Fault Tolerance & Reliability
- Byzantine Fault Tolerance
- Split-Brain Problem
- Quorum-based Systems
- Gossip Protocol
- Heartbeats & Failure Detection
- Circuit Breaker Pattern

### 9.5 Advanced Distributed Concepts
- CRDTs (Conflict-Free Replicated Data Types)
- Merkle Trees
- Consistent Hashing
- Distributed Hash Tables (DHT)

## 10. Data Structures & Algorithms for Systems

### 10.1 Specialized Data Structures
- Bloom Filters (Membership Testing)
- Count-Min Sketch (Frequency Estimation)
- HyperLogLog (Cardinality Estimation)
- Trie (Prefix Trees)
- Skip Lists

### 10.2 Tree Structures
- B-Trees & B+ Trees
- LSM Trees (Log-Structured Merge Trees)
- Quad Trees (Spatial Indexing)
- R-Trees (Spatial Data)

### 10.3 Hashing & Partitioning
- Consistent Hashing
- Rendezvous Hashing
- Geohashing (Location Services)
- Hash Ring

### 10.4 Search & Indexing
- Inverted Index (Full-text Search)
- Elasticsearch Architecture
- Search Ranking Algorithms

## 11. Big Data & Analytics

### 11.1 Data Processing Paradigms
- Batch Processing vs Stream Processing vs Micro-batching
- ETL vs ELT Pipelines
- Lambda Architecture vs Kappa Architecture

### 11.2 Big Data Technologies
- MapReduce Programming Model
- Apache Spark (RDDs, DataFrames)
- Apache Flink (Stream Processing)
- Apache Storm

### 11.3 Data Storage Systems
- Data Warehouses vs Data Lakes vs Data Lakehouse
- OLTP vs OLAP
- Columnar Storage (Parquet, ORC)
- Data Partitioning Strategies

## 12. Security

### 12.1 Authentication & Authorization
- Authentication vs Authorization
- Multi-Factor Authentication (MFA)
- Single Sign-On (SSO)
- Identity Providers (IdP)

### 12.2 Security Protocols & Standards
- OAuth 2.0 & OpenID Connect (OIDC)
- SAML (Security Assertion Markup Language)
- JWT (JSON Web Tokens)
- Session Management

### 12.3 Network Security
- SSL/TLS & mTLS (mutual TLS)
- Certificate Management
- Public Key Infrastructure (PKI)
- VPN & Zero Trust Architecture

### 12.4 Application Security
- Role-Based Access Control (RBAC)
- Attribute-Based Access Control (ABAC)
- SQL Injection Prevention
- XSS & CSRF Protection
- API Security Best Practices
- Rate Limiting & DDoS Protection

### 12.5 Data Security
- Data Encryption (at Rest & in Transit)
- Key Management Systems
- Data Masking & Anonymization
- Compliance (GDPR, HIPAA, PCI-DSS)

## 13. Cloud & Infrastructure

### 13.1 Cloud Computing Models
- IaaS vs PaaS vs SaaS
- Public vs Private vs Hybrid Cloud
- Multi-Cloud vs Vendor Lock-in

### 13.2 Containerization & Orchestration
- Virtual Machines vs Containers
- Docker Architecture
- Kubernetes Architecture
- Container Registries
- Service Mesh (Istio, Linkerd)

### 13.3 Cloud Storage
- Object Storage (S3, Azure Blob, GCS)
- Block Storage vs File Storage
- Data Durability & Availability
- Storage Classes & Lifecycle Policies

### 13.4 Infrastructure as Code
- Configuration Management
- Infrastructure Provisioning
- Immutable Infrastructure
- GitOps

## 14. Observability & Operations

### 14.1 Logging
- Structured vs Unstructured Logging
- Log Levels & Log Rotation
- Centralized Logging
- Log Aggregation (ELK Stack, Fluentd)

### 14.2 Monitoring & Metrics
- Application vs Infrastructure Monitoring
- Time Series Databases (Prometheus, Grafana)
- Key Performance Indicators (KPIs)
- SLA vs SLO vs SLI

### 14.3 Distributed Tracing
- Trace Context Propagation
- Span & Trace Relationships
- Sampling Strategies
- Jaeger, Zipkin

### 14.4 Alerting & Incident Response
- Alert Fatigue & Alert Optimization
- On-call Rotations
- Incident Response Procedures
- Post-mortem Analysis

### 14.5 Reliability Engineering
- Error Budgets
- Chaos Engineering
- Disaster Recovery Planning
- Business Continuity

## 15. Advanced System Design Patterns

### 15.1 Fan Patterns
- Fan-Out Pattern (Broadcast)
- Fan-In Pattern (Aggregation)
- Scatter-Gather Pattern

### 15.2 Retry & Resilience Patterns
- Exponential Backoff
- Jitter in Retry Logic
- Bulkhead Isolation
- Timeout Patterns

### 15.3 Data Synchronization
- Master-Master Replication
- Conflict Resolution
- Multi-Region Data Consistency

## 16. System Design Trade-offs & Decisions

### 16.1 Common Trade-offs
- Consistency vs Availability
- Latency vs Throughput
- Storage vs Computation
- Simplicity vs Performance
- Monolith vs Microservices
- SQL vs NoSQL
- Synchronous vs Asynchronous
- Push vs Pull Models

### 16.2 Decision Frameworks
- Technology Selection Criteria
- Performance vs Cost Analysis
- Risk Assessment
- Scalability Planning


## 17. System Design Interview Problems

### 17.1 High-Frequency System Design Problems

| # | System | Key Focus Areas | Difficulty |
|---|--------|-----------------|------------|
| 1 | **Twitter / Feed System** | Timeline generation, fan-out vs fan-in, caching, database sharding, rate limits | Medium |
| 2 | **Instagram / Photo Sharing** | Image upload & storage, CDN, feed generation, likes/comments, database indexing | Medium |
| 3 | **WhatsApp / Messaging App** | Real-time delivery, message queue, end-to-end encryption, offline support, read receipts | Hard |
| 4 | **Facebook News Feed** | Ranking algorithms, caching, personalization, batch vs real-time processing | Hard |
| 5 | **YouTube / Video Streaming** | Video storage, streaming, transcoding, CDN, recommendation engine | Hard |
| 6 | **Netflix / Video Streaming** | Adaptive streaming, caching, load balancing, recommendation engine | Hard |
| 7 | **Uber / Ride-Sharing** | Geo-location, matching algorithm, surge pricing, real-time updates, distributed systems | Hard |
| 8 | **Food Delivery System** | Menu management, orders, delivery tracking, notifications, database design | Medium |
| 9 | **E-commerce Platform (Amazon)** | Product catalog, search, order management, payment system, inventory tracking | Hard |
| 10 | **URL Shortener (Bitly)** | Unique key generation, database schema, caching, redirection latency, analytics | Easy |
| 11 | **Online Collaborative Editor (Google Docs)** | Real-time collaboration, operational transformation / CRDTs, conflict resolution | Hard |
| 12 | **File Storage System (Dropbox / Google Drive)** | File upload/download, versioning, replication, deduplication, consistency | Medium |
| 13 | **Recommendation System** | Collaborative filtering, content-based filtering, caching, personalization, ML integration | Medium |
| 14 | **Notification System** | Push/email/SMS, fan-out, queueing, retries, rate limiting | Medium |
| 15 | **Payment Gateway (PayPal / Stripe)** | ACID transactions, consistency, fraud detection, high availability | Hard |
| 16 | **Leaderboard / Ranking System** | Real-time updates, caching, sorting large datasets, distributed counters | Medium |
| 17 | **URL Caching / CDN Design** | Caching strategy, TTL, cache invalidation, geo-replication, performance | Medium |
| 18 | **Logging / Analytics System** | Event ingestion, batching, storage, indexing, query optimization | Medium |
| 19 | **Search Engine / Autocomplete** | Indexing, query processing, ranking, caching, sharding, latency optimization | Hard |
| 20 | **Online Multiplayer Game Server** | State synchronization, matchmaking, latency handling, consistency | Hard |
| 21 | **Email / SMS Queue System** | Queueing, retries, batching, deduplication, throughput scaling | Medium |
| 22 | **Job Scheduler (Airflow-like)** | Cron jobs, DAG execution, retries, distributed execution, monitoring | Medium |
| 23 | **Stock Trading System** | Real-time updates, order matching, high throughput, consistency, latency | Hard |
| 24 | **Pastebin / Gist** | Data storage, unique key generation, expiration, scaling reads/writes | Easy |
| 25 | **Event Ticketing System** | Seat reservation, concurrency, high availability, payment integration, scaling | Medium |

### 17.2 Problem Categories

#### Social Networks & Messaging
- Twitter / Feed System
- Instagram / Photo Sharing
- WhatsApp / Messaging App
- Facebook News Feed

#### Content & Streaming Platforms
- YouTube / Video Streaming
- Netflix / Video Streaming
- File Storage System (Dropbox / Google Drive)

#### Real-time & Location Services
- Uber / Ride-Sharing
- Food Delivery System
- Online Multiplayer Game Server

#### E-commerce & Marketplace
- E-commerce Platform (Amazon)
- Payment Gateway (PayPal / Stripe)
- Event Ticketing System

#### Search & Discovery
- Search Engine / Autocomplete
- Recommendation System
- URL Shortener (like TinyURL, Bitly) – hashing, redirection, DB sharding

#### Infrastructure & Backend Services
- Notification System
- Logging / Analytics System
- Job Scheduler (Airflow-like)
- Email / SMS Queue System
- URL Caching / CDN Design
- Rate Limiter (API gateway level) – token bucket, sliding window, Redis.

#### Specialized Systems
- Online Collaborative Editor (Google Docs)
- Leaderboard / Ranking System
- Stock Trading System
- Pastebin / Gist

### 17.3 Interview Preparation Strategy

#### By Difficulty Level
- **Start with Easy (2 problems)**: URL Shortener, Pastebin
- **Progress to Medium (11 problems)**: Instagram, Food Delivery, File Storage, Recommendation System, Notification System, Leaderboard, CDN Design, Analytics System, Email Queue, Job Scheduler
- **Master Hard (12 problems)**: Twitter, WhatsApp, Facebook Feed, YouTube, Netflix, Uber, E-commerce, Google Docs, Payment Gateway, Search Engine, Game Server, Stock Trading

#### Key Preparation Areas
1. **Database Design**: Focus on problems 1, 2, 8, 9, 12, 15
2. **Caching Strategies**: Focus on problems 1, 4, 6, 10, 16, 17
3. **Real-time Systems**: Focus on problems 3, 7, 11, 14, 20, 23
4. **Scalability**: Focus on problems 5, 9, 18, 19, 21, 22

## Learning Path Recommendations:

1. **Beginner**: Focus on sections 1-6 (Foundations through Load Balancing)
2. **Intermediate**: Add sections 7-10 (Architecture Patterns through Data Structures)
3. **Advanced**: Complete with sections 11-16 (Big Data through Trade-offs)
4. **Interview Prep**: Emphasize sections 4 (Databases), 6 (Scaling), 9 (Distributed Systems), and 16 (Trade-offs)

## 18. System Design Interview Template

<img width="4823" height="1870" alt="system design2" src="https://github.com/user-attachments/assets/f9ef0da1-86e7-4821-ab41-ef0cc11d047c" />

> ⚠️ **Note:**  Data Flow (step 4) is optional and only needed for data processing systems.
### 18.1 Requirements

### 18.1.1 Functional Requirements

### What does the system DO?

#### Core Features
- What are the primary features users need?
- What actions can users perform?
- What data does the system process?
- What workflows must be supported?

#### User Interactions
- Who are the different types of users?
- What can each user type do?
- How do users authenticate and authorize?
- What permissions/roles are needed?

#### Data Operations
- What data needs to be created, read, updated, deleted?
- How is data structured and related?
- What business rules govern the data?
- What validations are required?

#### Integration & APIs
- What external systems need integration?
- What APIs need to be exposed?
- What data formats are required (JSON, XML)?
- What third-party services are needed?

#### Example Questions for Different Systems

**Social Media Platform:**
- Can users post text, images, videos?
- How do users follow/unfollow others?
- What privacy controls exist?
- How does the feed algorithm work?

**E-commerce:**
- How do users search and filter products?
- What's the checkout process?
- How are payments processed?
- What inventory management is needed?

**Chat Application:**
- What message types are supported?
- How do group chats work?
- Are there message reactions/replies?
- What about file sharing?

### 18.1.2 Non Functional Requirements

### HOW WELL does the system perform?

#### Performance & Scalability
- **Users**: How many daily/monthly active users?
- **Traffic**: What's the expected requests per second?
- **Response Time**: What latency is acceptable?
- **Throughput**: How much data volume per day?
- **Growth**: What's the expected growth rate?

**Key Questions:**
- What's the peak traffic multiplier?
- Are there seasonal/event-driven spikes?
- What's acceptable response time for different operations?
- How much data will be processed daily?

#### Availability & Reliability
- **Uptime**: What availability percentage is required?
- **Disaster Recovery**: How quickly must system recover?
- **Data Loss**: What's acceptable data loss tolerance?
- **Failure Handling**: How should failures be managed?

**Key Questions:**
- Is this a mission-critical system?
- What's the cost of downtime?
- Are there maintenance windows?
- What backup and recovery needs exist?

#### Security & Privacy
- **Authentication**: How do users prove identity?
- **Authorization**: What access controls are needed?
- **Data Protection**: What data needs encryption?
- **Compliance**: What regulations apply (GDPR, HIPAA)?

**Key Questions:**
- What sensitive data is handled?
- Are there geographic data restrictions?
- What audit logging is required?
- How long is data retained?

#### Consistency & Data Integrity
- **ACID**: Are database transactions required?
- **CAP Theorem**: Consistency vs Availability trade-offs?
- **Eventual Consistency**: Is delayed consistency acceptable?
- **Data Validation**: What integrity checks are needed?

**Key Questions:**
- Is real-time consistency critical?
- Can you tolerate stale data for performance?
- What happens during network partitions?
- How important is data accuracy vs speed?

## Question Framework by System Type

### Real-Time Systems (Chat, Gaming)
**Functional:**
- What real-time features are needed?
- How do you handle message ordering?
- What offline capabilities exist?

**Non-Functional:**
- What's acceptable message delay?
- How many concurrent connections?
- Is global real-time sync needed?

### Data-Heavy Systems (Analytics, Search)
**Functional:**
- What queries/searches are supported?
- How is data aggregated and reported?
- What export/import capabilities exist?

**Non-Functional:**
- How much data volume daily?
- What query response times are acceptable?
- How often is data updated?

### Content Systems (Social Media, Video)
**Functional:**
- What content types are supported?
- How is content moderated?
- What recommendation features exist?

**Non-Functional:**
- What's the read:write ratio?
- How is content distributed globally?
- What bandwidth requirements exist?

### For System Design Interviews

**Opening Questions:**
- "What's the main purpose of this system?"
- "Who are the primary users?"
- "What's the expected scale (users, data)?"

**Functional Deep Dive:**
- "Walk me through a typical user flow"
- "What are the core features we must support?"
- "Are there any complex business rules?"

**Non-Functional Clarification:**
- "What's more important: consistency or availability?"
- "What response time do users expect?"
- "How much downtime is acceptable?"

**Scope Management:**
- "What can we defer to v2?"
- "Are there existing systems to integrate with?"
- "What's out of scope for this design?"

## Red Flags & Follow-up Questions

### When Requirements Are Vague
- "Can you give me a specific example?"
- "What would a typical user session look like?"
- "What happens in the worst-case scenario?"

### When Scale Is Unclear
- "How many users in year 1 vs year 3?"
- "What's the peak traffic pattern?"
- "How much data do you expect to store?"

### When Priorities Conflict
- "If we had to choose between X and Y, which is more critical?"
- "What's the business impact if this feature is delayed?"
- "Can we start simple and add complexity later?"

## Quick Reference

### Functional = WHAT
- Features, workflows, business logic
- User interactions and permissions
- Data operations and validations
- API endpoints and integrations

### Non-Functional = HOW WELL
- Performance (speed, throughput)
- Scalability (growth handling)
- Reliability (uptime, recovery)
- Security (protection, compliance)
- Usability (user experience)
- Maintainability (code quality, docs)

### 18.1.3 Capacity Estimation

Capacity estimation is a critical skill for system design interviews and real-world system planning. This guide provides formulas, examples, and practical tips for estimating the resources your system will need.

## 1. Traffic / Requests Per Second (RPS)

### Goal
Estimate how many requests your system handles per second.

### Formula
```
RPS = Total Requests per Day / (24 × 3600)
```

### Example
- 1M DAU (Daily Active Users)
- 10 requests per user per day

```
1,000,000 × 10 = 10,000,000 requests/day
RPS = 10,000,000 / 86400 ≈ 116 req/sec
```

### Key Considerations
- **Peak Factor**: Multiply RPS by 2–5× to account for traffic spikes
- **Read vs Write Ratio**: Often 100:1 for social media, 10:1 for e-commerce
- **Geographic Distribution**: Consider time zones for global applications

### Common Traffic Patterns
- **Social Media**: High evening peaks, weekend spikes
- **Business Apps**: Weekday 9-5 patterns
- **Entertainment**: Evening and weekend heavy
- **E-commerce**: Holiday and sale event spikes

## 2. Storage Estimation

### Goal
Estimate the total data stored over time.

### Formulas
```
Storage per Day = Number of Items per Day × Size per Item
Total Storage = Storage per Day × Retention Days
```

### Example
- 1M photos/day, each 3 MB

```
1,000,000 × 3 MB = 3,000,000 MB/day ≈ 3 TB/day
1-year retention ≈ 3 TB/day × 365 ≈ 1,095 TB ≈ 1.1 PB
```

### Storage Types & Considerations

#### Hot vs Cold Storage
- **Hot Storage**: Frequently accessed (last 30 days) - expensive, fast
- **Warm Storage**: Occasionally accessed (30 days - 1 year) - moderate cost
- **Cold Storage**: Rarely accessed (>1 year) - cheap, slow retrieval

#### Data Growth Patterns
- **Linear Growth**: Consistent daily additions (logs, user data)
- **Exponential Growth**: Viral content, social networks
- **Seasonal Growth**: E-commerce, entertainment platforms

### Common File Sizes
- **Text post**: 1-10 KB
- **Image (compressed)**: 100 KB - 5 MB
- **Video (1080p, 1 min)**: 50-100 MB
- **Audio (MP3, 3 min)**: 3-5 MB
- **Document (PDF)**: 100 KB - 10 MB

## 3. Bandwidth / Network Throughput

### Goal
Estimate required network bandwidth for data transfer.

### Formula
```
Bandwidth (Bytes/sec) = RPS × Average Request Size
```

### Example
- RPS = 1000
- Each request = 100 KB

```
1000 × 100 KB = 100,000 KB/s ≈ 97.7 MB/s
```

### Bandwidth Considerations
- **CDN Usage**: Reduces origin server bandwidth by 80-95%
- **Compression**: Gzip can reduce text by 60-80%
- **Regional Distribution**: Multiple data centers reduce per-region bandwidth
- **Peak vs Average**: Plan for 3-5× peak bandwidth

### Network Latency Impact
- **Same datacenter**: 0.5-2 ms
- **Same region**: 5-20 ms
- **Cross-continent**: 100-300 ms
- **Satellite**: 500-700 ms

## 4. Compute / CPU Requirements

### Goal
Estimate processing power required to handle the load.

### Formulas
```
CPU-seconds/sec = RPS × CPU time per request (seconds)
Number of CPUs required = CPU-seconds/sec / CPU capacity per core
```

### Example
- RPS = 500
- CPU time per request = 50 ms = 0.05 s

```
500 × 0.05 = 25 CPU-seconds/sec
If 1 CPU core = 1 CPU-second/sec, need 25 cores
```

### CPU Estimation Guidelines

#### Operation Complexity
- **Simple CRUD**: 10-50 ms CPU time
- **Complex queries**: 100-500 ms
- **Image processing**: 1-10 seconds
- **ML inference**: 100 ms - 10 seconds
- **Video encoding**: 10 seconds - minutes

#### Scaling Factors
- **Algorithm complexity**: O(1) vs O(n) vs O(log n)
- **Database optimization**: Indexes, query optimization
- **Caching hit rate**: 80-95% cache hits dramatically reduce CPU

### Modern CPU Considerations
- **Multi-core scaling**: Not all tasks parallelize perfectly
- **Hyperthreading**: ~30% performance boost
- **CPU architecture**: ARM vs x86 performance differences
- **Containerization overhead**: 5-10% performance impact

## 5. Memory Requirements

### Goal
Estimate RAM usage for in-memory data, caches, and active sessions.

### Formula
```
Memory = Number of Concurrent Items × Size per Item
```

### Example
- 10k concurrent sessions
- Each session ~1 KB

```
10,000 × 1 KB = 10 MB
```

### Memory Usage Patterns

#### Application Memory
- **JVM heap**: 2-8 GB typical
- **Node.js**: 100 MB - 2 GB
- **Python**: 50-500 MB
- **Go**: 10-200 MB
- **C++**: 10-100 MB

#### Caching Strategy
- **Redis/Memcached**: 80% of memory for data
- **Cache hit ratio**: Target 95%+ for hot data
- **Cache eviction**: LRU, LFU, TTL-based

#### Memory Estimation Rules
- **Session data**: 1-10 KB per active user
- **Database connections**: 1-10 MB per connection
- **Cache memory**: 20-50% of total data for optimal hit rate
- **OS overhead**: Reserve 10-20% for system processes

## 6. System Design Interview Workflow

### Step-by-Step Process

#### 1. Define Scope
- What specific feature or operation?
- What are the constraints?
- What's the expected scale?

#### 2. Estimate Traffic
```
DAU → Daily Requests → RPS → Peak RPS
```

#### 3. Estimate Storage
```
Data per day × Retention period = Total storage
```

#### 4. Estimate Bandwidth
```
RPS × Average response size = Bandwidth needed
```

#### 5. Estimate Compute & Memory
```
CPU time per request × RPS = Total CPU needed
Concurrent users × Memory per user = Total memory
```

#### 6. Add Safety Margins
- **Traffic**: 2-5× for peak handling
- **Storage**: 20-30% for overhead and growth
- **Compute**: 50-100% for redundancy
- **Memory**: 30-50% for garbage collection and buffers

## 7. Reference Numbers & Quick Calculations

### Availability and Reliability
| Availability | Downtime per Year |
|--------------|------------------|
| 99%          | 3.6 days         |
| 99.9%        | 8.8 hours        |
| 99.99%       | 52 minutes       |
| 99.999%      | 5 minutes        |
| 99.9999%     | 31 seconds       |

### Operation Latencies
| Operation | Time |
|-----------|------|
| L1 cache reference | 0.5 ns |
| Main memory reference | 100 ns |
| Send 1KB over 1 Gbps network | 10 μs |
| Read 4KB randomly from SSD | 150 μs |
| Round trip within datacenter | 500 μs |
| Read 1MB sequentially from SSD | 1 ms |
| HDD seek | 10 ms |
| Send packet CA→Netherlands→CA | 150 ms |

### Data Size Powers of 10
| Power | Approximate Value | Full Name | Short Name |
|-------|------------------|-----------|------------|
| 10³   | 1 Thousand       | 1 Kilobyte | 1 KB |
| 10⁶   | 1 Million        | 1 Megabyte | 1 MB |
| 10⁹   | 1 Billion        | 1 Gigabyte | 1 GB |
| 10¹²  | 1 Trillion       | 1 Terabyte | 1 TB |
| 10¹⁵  | 1 Quadrillion    | 1 Petabyte | 1 PB |

## 8. Advanced Estimation Techniques

### Probabilistic Models
- **Poisson distribution** for request arrivals
- **Pareto principle** (80/20 rule) for data access patterns
- **Normal distribution** for response times

### Machine Learning Workloads
```
Training: GPU hours = Dataset size × Model complexity × Epochs
Inference: CPU/GPU time = Model size × Input size × Batch size
```

### Database Sizing
```
IOPS needed = (Reads/sec × Read IOPS) + (Writes/sec × Write IOPS)
Connection pool size = (Average response time × RPS) / 1000
```

### Microservices Considerations
- **Service mesh overhead**: 10-15% latency increase
- **Network calls**: Each hop adds 1-5ms
- **Circuit breaker**: Plan for 95-99% upstream availability

## 9. Common Estimation Mistakes to Avoid

### Underestimating Factors
- **Peak traffic**: Using average instead of peak
- **Data growth**: Linear vs exponential growth patterns
- **Failure scenarios**: Not accounting for redundancy needs
- **Operational overhead**: Monitoring, logging, backups

### Overestimating Factors
- **Perfect scaling**: Assuming linear scalability
- **Cache hit rates**: Assuming unrealistic 99%+ hit rates
- **Network efficiency**: Ignoring protocol overhead
- **Compression ratios**: Overestimating compression benefits

### Real-World Adjustments
- **Safety margins**: Always add 2-3× capacity buffer
- **Geographic distribution**: Account for data locality
- **Regulatory requirements**: Data residency, audit logs
- **Business growth**: Plan for 2-5 years of growth

## 10. Practical Examples

### Social Media Platform
```
100M DAU, 50 posts viewed per day
RPS: 100M × 50 / 86400 ≈ 58K requests/sec
Peak: 58K × 3 ≈ 174K requests/sec
Storage: 100M users × 1MB profile + posts = 100TB
Bandwidth: 174K × 10KB response ≈ 1.7GB/sec
```

### Video Streaming Service
```
10M concurrent viewers, 5Mbps average bitrate
Bandwidth: 10M × 5Mbps = 50Tbps
Storage: 100K hours content × 10GB/hour = 1PB
CDN: 95% cache hit rate reduces origin load by 20×
```

### E-commerce Platform
```
1M DAU, 20 page views, 5% conversion
RPS: 1M × 20 / 86400 ≈ 231 requests/sec
Peak (Black Friday): 231 × 10 = 2310 requests/sec
Orders: 1M × 0.05 = 50K orders/day
Database: 50K × 5KB order = 250MB/day
```

## Summary

Capacity estimation is both an art and a science. Start with basic calculations, add realistic safety margins, and always validate assumptions with actual measurements. Remember that systems rarely fail due to average load—they fail during peak traffic, so always plan for the worst-case scenarios.

### Key Takeaways
1. **Start simple**: Use powers of 10 for quick mental math
2. **Be realistic**: Add safety margins for peaks and growth
3. **Think end-to-end**: Consider all system components
4. **Validate assumptions**: Real-world data beats estimates
5. **Plan for failure**: Design for redundancy and scaling

### 18.2 Core Entities
### 18.3 API or Interface
### 18.4 Data Flow
### 18.5 High Level Design
### 18.6 Deep Dives

## 19. System Design Practice Problems

### 19.1 Design a Rate Limiter
- Handle request limits per user/IP.
- Discuss fixed window, sliding window, token bucket, leaky bucket.
- Scaling across distributed servers.

### 19.2 Design a URL Shortener (Bitly)
- Unique key generation, database schema, redirection latency.
- Analytics, caching, handling collisions.

### 19.3 Design a Twitter / Feed System
- Timeline generation, fan-out vs fan-in, caching.
- Database sharding, read/write scaling.

### 19.4 Design WhatsApp / Messaging App
- Real-time message delivery, offline messages.
- End-to-end encryption, group messaging, message queues.

### 19.5 Design Instagram / Photo Sharing
- Image upload & storage, CDN, feed generation.
- Likes, comments, indexing, caching.

### 19.6 Design YouTube / Video Streaming
- Video storage, transcoding, adaptive streaming.
- CDN, recommendation engine, search indexing.

### 19.7 Design an E-commerce Platform
- Product catalog, search, order management.
- Inventory tracking, payment gateway integration, caching.

### 19.8 Design Uber / Ride-Sharing
- Geo-location, real-time matching, surge pricing.
- Distributed system design, scaling riders & drivers.

### 19.9 Design a Notification System
- Push/email/SMS, fan-out, queueing.
- Retry mechanism, rate limiting, scalability.

### 19.10 Design an Online Collaborative Editor
- Real-time collaboration, operational transforms / CRDTs.
- Conflict resolution, consistency across multiple users.

### 19.11 Design a File Storage System (Dropbox / Google Drive)
- Upload/download, versioning, replication, deduplication.
- Consistency, latency, scaling reads/writes.

### 19.12 Design a Leaderboard / Ranking System
- Real-time updates, sorting, caching.
- Distributed counters, scale considerations.

### 19.13 Design a Search Engine / Autocomplete
- Indexing, query processing, ranking.
- Caching, sharding, low-latency suggestions.

### 19.14 Design a Payment Gateway
- ACID transactions, consistency, high availability.
- Fraud detection, scaling with many concurrent transactions.

### 19.15 Design a Job Scheduler
- Cron jobs, DAG execution, retries.
- Distributed execution, monitoring, fault tolerance.

