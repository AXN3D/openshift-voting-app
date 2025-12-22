\# OpenShift Voting Application



A production-style voting application deployed on OpenShift using CodeReady Containers (CRC).  

This project focuses on understanding core OpenShift and Kubernetes concepts through hands-on deployment and troubleshooting.



---



\## Architecture (Simplified)



\- PostgreSQL (StatefulSet + Persistent Storage)

\- Redis (StatefulSet – upcoming)

\- Vote API (Deployment – upcoming)

\- Vote UI (Deployment + Route – upcoming)



---



\## Current Progress ✅



\### PostgreSQL Deployment

\- Deployed PostgreSQL using a StatefulSet

\- Configured persistent storage using PersistentVolumeClaims (PVC)

\- Fixed CrashLoopBackOff by correctly configuring `PGDATA`

\- Validated data persistence across pod restarts

\- Exposed PostgreSQL internally using a ClusterIP Service



---



\## Concepts Covered So Far



\- OpenShift Projects (Namespaces)

\- StatefulSets vs Deployments

\- PersistentVolumeClaims (PVC)

\- Pod lifecycle and restarts

\- Troubleshooting CrashLoopBackOff

\- DiskPressure issues in CRC

\- OpenShift CLI (`oc`) usage



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



