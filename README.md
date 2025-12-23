\# OpenShift Voting Application



A production-style voting application deployed on OpenShift using CodeReady Containers (CRC).  

This project focuses on understanding core OpenShift and Kubernetes concepts through hands-on deployment and troubleshooting.



---




## Architecture (Current)

- PostgreSQL (StatefulSet + PVC)
- Redis (StatefulSet)
- Vote API (Deployment)
- Internal communication via ClusterIP Services


---



\## Current Progress ✅



\### PostgreSQL Deployment

\- Deployed PostgreSQL using a StatefulSet

\- Configured persistent storage using PersistentVolumeClaims (PVC)

\- Fixed CrashLoopBackOff by correctly configuring `PGDATA`

\- Validated data persistence across pod restarts

\- Exposed PostgreSQL internally using a ClusterIP Service



---




## Concepts Covered

- OpenShift Projects (Namespaces)
- Deployments vs StatefulSets
- PersistentVolumeClaims (PVC)
- Service discovery using Kubernetes DNS
- Environment variable based configuration
- OpenShift non-root container security model
- Debugging CrashLoopBackOff issues
- Overriding container command and arguments
- Using oc CLI for logs and troubleshooting



---



\## Tools \& Platform



\- OpenShift 4.x (CodeReady Containers)

\- Kubernetes

\- PostgreSQL

\- Git \& GitHub

\- Windows + PowerShell



---



\## Next Steps 🚀



\- Deploy Redis

\- Deploy Vote API

\- Deploy Vote UI

\- Expose application using OpenShift Routes

\- Add basic NetworkPolicies

\- Final cleanup and documentation



---



\## Why This Project?



This project is designed to:

\- Learn OpenShift fundamentals deeply

\- Practice real-world troubleshooting

\- Build a resume-ready OpenShift project

-------------------------------------------

## Current Progress ✅

### PostgreSQL
- Deployed PostgreSQL using a StatefulSet
- Configured persistent storage using PersistentVolumeClaims (PVC)
- Fixed CrashLoopBackOff by correctly configuring `PGDATA`
- Verified data persistence across pod restarts

### Redis
- Deployed Redis using a StatefulSet
- Exposed Redis internally using a ClusterIP Service
- Verified connectivity using `redis-cli`

### Vote API
- Deployed a stateless Vote API using a Deployment
- Connected the API to PostgreSQL and Redis using Kubernetes Service DNS
- Troubleshot CrashLoopBackOff caused by OpenShift non-root security constraints
- Fixed privileged port binding issue by overriding the container command to run on port 8080


## Frontend Status (Current)

The original demo voting UI container images were found to be unstable and incompatible
with OpenShift’s restricted security model (non-root execution and PodSecurity enforcement).

To validate OpenShift routing, TLS termination, and security compliance, a hardened
NGINX-based frontend was deployed temporarily.

A custom lightweight voting UI will be implemented next to interact directly with the Vote API.




