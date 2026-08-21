# Tripvisito - Backend Platform Layer (Super Repository)

## Mandatory Student & GCP Information
- **Student Name:** Lithira Jayanaka
- **Student Number:** 241722002
- **GCP Project ID:** project-a4f7bad0-3923-4cdb-b9b

---

## Project Description
This is the **parent (super) repository** containing the core platform-level infrastructure microservices of the Tripvisito platform. It aggregates the platform service components as **Git submodules** to support a polyrepo architecture as required by the ECA project guidelines.

### Associated Submodules
1. **[config-server](config-server)**: Centralizes application configurations.
2. **[service-registry](service-registry)**: Discovery server (Netflix Eureka).
3. **[api-gateway](api-gateway)**: Single gateway interface with JWT auth filters.

## Technology Stack
- **Spring Cloud Platform Suite**
- **Git Submodules**

## Setup / Getting Started Instructions

### Cloning with Submodules
Since this repository relies on Git submodules, you must clone it using the `--recursive` flag or initialize submodules after cloning:
```bash
# Option A: Clone recursively
git clone --recursive git@github:LithiraJK/tripvisito-backend-platform.git

# Option B: Initialize submodules post-cloning
git clone git@github.com:LithiraJK/tripvisito-backend-platform.git
cd tripvisito-backend-platform
git submodule update --init --recursive
```

### Build & Run
To run the platform services, refer to the README files located inside each submodule folder. The services must be started in order:
1. `config-server` (Port `8888`)
2. `service-registry` (Port `8761`)
3. `api-gateway` (Port `8080`)
