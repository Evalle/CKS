# Certified Kubernetes Security Specialist Exam Preparation Guide

This guide is intended to be a point of knowledge for everyone who wants to pass Certified Kubernetes Security Specialist (CKS) Exam. 
The main idea is to provide links to every topic in each domain. Preference will always be the official documentation but feel free to add other useful links.

**The Exam itself will be available in November 2020**

## Introduction (Read carefully)

A Certified Kubernetes Security Specialist is an accomplished Kubernetes practitioner (**as evidenced by holding the CKA credential**) who has demonstrated competence on a broad range of best practices for securing container-based applications and Kubernetes platforms during build, deployment and runtime.

Certified Kubernetes Security Specialist (CKS) candidates must have taken and passed the [Certified Kubernetes Administrator (CKA)](https://www.cncf.io/certification/cka/) exam prior to attempting the CKS exam. The CKS may be scheduled but not taken until CKA certification has been achieved.

## Exam Details

This exam is an online, proctored, performance-based test that requires solving multiple tasks from a command line running Kubernetes. Candidates have 2 hours to complete the tasks.

The exam is based on Kubernetes v1.19

Certified Kubernetes Security Specialist (CKS) candidates must have taken and passed the Certified Kubernetes Administrator (CKA) exam prior to attempting the CKS exam. The CKS may be scheduled but not taken until CKA certification has been achieved.


## Table of Contents

1. [Cluster Setup](https://github.com/Evalle/CKS/blob/master/README.md#Cluster-Setup)
1. [Cluster Hardening](https://github.com/Evalle/CKS/blob/master/README.md#Cluster-Hardening)
1. [System Hardening](https://github.com/Evalle/CKS/blob/master/README.md#System-Hardening)
1. [Minimize Microservice Vulerabilities](https://github.com/Evalle/CKS/blob/master/README.md#Minimize-Microservice-Vulnerabilities)
1. [Supply Chain Security](https://github.com/Evalle/CKS/blob/master/README.md#Supply-Chain-Security)
1. [Monitoring, Logging and Runtime Security](https://github.com/Evalle/CKS/blob/master/README.md#Monitoring-Logging-and-Runtime-Security)
1. [Links](https://github.com/Evalle/CKS/blob/master/README.md#Links)

## Cluster Setup

- [Use Network security policies to restrict cluster level access](https://kubernetes.io/docs/concepts/services-networking/network-policies/)
- [Use CIS benchmark to review the security configuration of Kubernetes components (etcd, kubelet, kubedns, kubeapi)](https://github.com/aquasecurity/kube-bench)
- [Properly set up Ingress objects with security control](https://kubernetes.io/docs/concepts/services-networking/ingress/#tls)
- Protect node metadata and endpoints
- [Minimize use of, and access to, GUI elements](https://github.com/kubernetes/dashboard#getting-started)
- Verify platform binaries before deploying, use md5 checks against [official binaries](https://github.com/kubernetes/kubernetes/releases)

## Cluster Hardening

- [Restrict access to Kubernetes API](https://kubernetes.io/docs/reference/access-authn-authz/controlling-access/)
- [Use Role Based Access Controls to minimize exposure](https://kubernetes.io/docs/reference/access-authn-authz/rbac/)
- Exercise caution in using service accounts e.g. disable defaults, minimize permissions on newly created ones
- [Update Kubernetes frequently](https://kubernetes.io/docs/tasks/administer-cluster/kubeadm/kubeadm-upgrade/)

## System Hardening

- Minimize host OS footprint (reduce attack surface)
- Minimize IAM roles
- Minimize external access to the network
- Appropriately use kernel hardening tools such as AppArmor, seccomp

## Minimize Microservice Vulnerabilities

- Setup appropriate OS level security domains e.g. using [PSP](https://kubernetes.io/docs/concepts/policy/pod-security-policy/), [OPA](https://www.openpolicyagent.org/), [security contexts](https://kubernetes.io/docs/tasks/configure-pod-container/security-context/)
- Manage Kubernetes secrets
- Use container runtime sandboxes in multi-tenant environments (e.g. gvisor, kata containers)
- Implement pod to pod encryption by use of mTLS

## Supply Chain Security

- Minimize base image footprint
- Secure your supply chain: whitelist allowed registries, sign and validate images
- Use static analysis of user workloads (e.g.Kubernetes resources, Docker files)
- Scan images for known vulnerabilities ([clair](https://coreos.com/clair/docs/latest/), [trivy](https://github.com/aquasecurity/trivy))

## Monitoring Logging and Runtime Security 

- Perform behavioral analytics of syscall process and file activities at the host and container level to detect malicious activities
- Detect threats within physical infrastructure, apps, networks, data, users and workloads
- Detect all phases of attack regardless where it occurs and how it spreads
- Perform deep analytical investigation and identification of bad actors within environment
- Ensure immutability of containers at runtime
- Use Audit Logs to monitor access

## Useful Links

### Courses
- [Configuring and Managing Kubernetes Security](https://app.pluralsight.com/library/courses/configuring-managing-kubernetes-security/table-of-contents)
- [Kubernetes CKS 2020 Complete Course + Simulator (UDEMY)](https://www.udemy.com/course/certified-kubernetes-security-specialist/)

### Info
- [Exam info](https://training.linuxfoundation.org/certification/certified-kubernetes-security-specialist/?utm_source=lftraining&utm_medium=pr&utm_campaign=cks0720)
- [Exam Curriculum (November 2020)](https://github.com/cncf/curriculum/blob/master/CKS_Curriculum_%20v1.19%20Coming%20Soon%20November%202020.pdf)



