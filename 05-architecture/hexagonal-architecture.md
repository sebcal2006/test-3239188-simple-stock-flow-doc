# Hexagonal Architecture — Simple Stock Flow

## 1. Ports and Adapters
The architecture strictly separates the application core from the outside world via ports (interfaces) and adapters (implementations).

### Driving / Inbound Ports
* Represented by use cases or application services that expose permitted operations in the system (e.g., record sale, update stock, query catalog).
* Invoked by inbound adapters (ASP.NET Core Controllers / REST API).

### Driven / Outbound Ports
* Interfaces defined in the domain or application to abstract persistence and external services (e.g., product repositories, sale repositories).
* Implemented in the infrastructure layer using Entity Framework Core connected to the PostgreSQL engine (`simple_stock_flow`).

## 2. Dependency Rule
Dependencies always point inwards. Infrastructure knows about application and domain; application knows about domain; **the domain knows nothing external**.
