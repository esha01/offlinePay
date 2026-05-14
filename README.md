# OfflinePay Network

Offline-first decentralized payment simulation platform enabling secure peer-to-peer money transfer in low-connectivity environments using mesh propagation.

## Overview

OfflinePay Network is a distributed systems prototype that explores how digital payments could function in environments with unreliable or unavailable internet connectivity.

The project simulates encrypted payment packets traveling device-to-device across a mesh network until a bridge node with internet connectivity uploads the transaction to a backend settlement service.

This project was built as an experiment in:
- offline-first systems
- distributed transaction propagation
- encrypted packet routing
- idempotent backend settlement
- mesh-network-inspired payment flows

---

## Problem Statement

Digital payment systems heavily depend on continuous internet connectivity.

However, connectivity failures are common in:
- metro tunnels
- crowded events
- rural areas
- disaster zones
- low-signal environments

OfflinePay explores a hypothetical system where payment instructions can propagate locally between nearby devices without requiring the sender to have direct internet access.

---

## How It Works

1. Sender creates a payment packet
2. Packet is encrypted using hybrid encryption
3. Packet propagates across nearby mesh devices
4. Intermediate nodes relay packets without decrypting them
5. Any device with internet access becomes a bridge node
6. Bridge node uploads packet to backend
7. Backend settles transaction exactly once using idempotency protection

---

## System Architecture

```text
Sender Device
      ↓
Mesh Devices
      ↓
Bridge Node
      ↓
Spring Boot Backend
      ↓
Transaction Settlement
```

---

## Features

- Offline payment packet simulation
- Gossip-style mesh propagation
- Bridge node synchronization
- Encrypted transaction payloads
- Duplicate packet protection
- Idempotent settlement logic
- Real-time dashboard visualization
- Transaction ledger
- Mesh device monitoring

---

## Security Concepts Simulated

- RSA-OAEP key exchange
- AES-256-GCM payload encryption
- Replay attack prevention
- Nonce-based freshness validation
- Idempotent transaction processing
- Duplicate packet dropping

---

## Tech Stack

### Backend
- Java 17
- Spring Boot 3

### Frontend
- HTML
- CSS
- Vanilla JavaScript
- Thymeleaf

### Database
- H2 Database

### Build Tools
- Maven

---

## Dashboard

The dashboard simulates:
- packet injection
- mesh propagation
- bridge uploads
- settlement tracking
- account balance updates

### Main UI Sections

- Mesh Devices
- Account Balances
- Transaction Ledger
- Activity Log

---

## Running The Project

### Clone Repository

```bash
git clone https://github.com/esha01/offlinePay.git
cd offlinePay
```

### Start Application

```bash
./mvnw spring-boot:run
```

### Open Browser

```text
http://localhost:8080
```

---

## API Endpoints

| Endpoint | Description |
|---|---|
| `/api/demo/send` | Inject payment packet |
| `/api/mesh/gossip` | Simulate mesh propagation |
| `/api/mesh/flush` | Upload packets through bridge nodes |
| `/api/mesh/reset` | Reset simulation state |
| `/api/accounts` | Fetch account balances |
| `/api/transactions` | Fetch transaction ledger |

---

## Future Improvements

- Real Bluetooth communication
- WebSocket-based live synchronization
- PostgreSQL integration
- JWT authentication
- Mobile client simulation
- Network latency simulation
- Packet TTL expiry visualization
- React frontend migration

---

## Learning Outcomes

This project helped explore:
- distributed systems fundamentals
- offline-first architecture
- backend API design
- frontend dashboard engineering
- transaction consistency challenges
- idempotent processing
- mesh-network-inspired communication systems

---

## Disclaimer

This project is an educational systems prototype and not a production-ready financial infrastructure implementation.

It is intended to demonstrate distributed systems and offline transaction flow concepts.

---

## References & Inspiration

Research and systems related to offline-first mesh communication and offline payment infrastructure:  
- LNMesh offline payment research :contentReference[oaicite:0]{index=0}
- Mesh-based offline communication systems :contentReference[oaicite:1]{index=1}
- Offline payment infrastructure concepts :contentReference[oaicite:2]{index=2}