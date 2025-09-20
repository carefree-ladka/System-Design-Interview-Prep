# System Design Learning

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

---

## Learning Path Recommendations:

1. **Beginner**: Focus on sections 1-6 (Foundations through Load Balancing)
2. **Intermediate**: Add sections 7-10 (Architecture Patterns through Data Structures)
3. **Advanced**: Complete with sections 11-16 (Big Data through Trade-offs)
4. **Interview Prep**: Emphasize sections 4 (Databases), 6 (Scaling), 9 (Distributed Systems), and 16 (Trade-offs)
