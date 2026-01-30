# Section 1 – On-Premises Architecture Diagram

```mermaid
flowchart LR
    User --> Firewall
    Firewall --> WebServer
    WebServer --> Database-Server
    WebServer --> File-Storage-Server
    WebServer --> Email-Server
```
