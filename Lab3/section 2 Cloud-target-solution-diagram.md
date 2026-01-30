flowchart LR
    User --> LoadBalancer
    LoadBalancer --> Application-Service
    AppService --> Managed-Database
    AppService --> Object-Storage
    AppService --> SaaS-Email
