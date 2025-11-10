# Unity Network Protocols Guide

## Introduction
This repository provides guidance and simple code reference for connecting Unity client to backend server, such as Python, using different network protocol. Unity has its own limitation in supporting specific task, so offloading these task to a backend service is recommended. Choosing the right protocol for communication ensures efficient and reliable interaction between Unity and the backend.

## Network Protocol
| Protocol | Type | Strength | Limitation |
| ------------- | -------------------- | --------------------------------------------------------------- | --------------------------------------------------------- |
| **TCP** | Connection-oriented | Reliable delivery, ordered data | Slower than UDP, introduce lag for real-time update |
| **UDP** | Connectionless | Low-latency update | No delivery guarantee or order, possible some packet loss |
| **WebSocket** | Full-duplex over TCP | Real-time chat, dashboard, collaborative feature | Require a server, built on top of TCP, not suitable for ultra-low-latency task |
| **WebRTC** | Peer-to-peer | Real-time audio, video, etc | More complicated to setup, require signaling server to exchange connection information before peer can communicate directly |
| **gRPC** | RPC over HTTP/2 | Structured, type-safe API call, backend service, non-real-time AI inference | Not optimized for ultra-low-latency real-time update |
| **HTTP/REST** | Request-response | Non-real-time backend task, configuration, database queries | Slower, not suitable for continuous streaming |
