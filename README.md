# Braid HTTP

This project implements the Braid-HTTP protocol over standard HTTP, allowing direct, serverless state synchronization between peers or traditional client-server environments.

## Braid HTTP Integration
The crate manages state synchronization on top of standard networking stacks. When a peer updates a resource, the change is versioned and a delta is generated. This update is then propagated to subscribers. The system supports:
- Subscriptions: Peers establish persistent subscriptions to resources using Braid-HTTP semantics.
- Differential Synchronization: Updates are transmitted as precise patches rather than full state, minimizing overhead.
- Version History: Each resource maintains a graph of versions, allowing strict conflict resolution.

## Applications
This library forms the foundational networking layer for any Braid-compatible application. It handles request generation, parsing, and streaming of patch updates.

## Technology Stack
- Language: Rust
- Networking: reqwest, HTTP parsing
- Protocol: Braid-HTTP (State Synchronization, Versioning)

## Testing Status
Tests are currently being migrated and expanded. Unit tests for parsing and formatting HTTP headers are planned for future versions.

## Using the Crate
Add `braid-http` to your dependencies to build Braid compliant clients and servers. Use the provided serializers and constants to properly configure your HTTP requests.
