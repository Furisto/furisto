## Work

Currently at Ona working on Cloud Development Environments and agents. Some of my work:

**[Automations](https://ona.com/docs/ona/configuration/automations/overview)**
Built automation system for triggering actions based on workspace lifecycle events (e.g., running tasks on workspace start, executing scripts on prebuild completion).

**[Single Sign-On](https://ona.com/docs/ona/sso/overview)**
Implemented SSO integration enabling enterprise customers to use their identity providers for authentication.

**[Source Control Providers](https://ona.com/docs/ona/source-control/overview)**
Integrated GitLab, Bitbucket, and Microsoft Azure DevOps as source control providers, enabling users to connect repositories from multiple platforms.

**[Billing System](https://ona.com/docs/ona/billing/overview)**
Built billing infrastructure for usage-based pricing and subscription management.

## Open Source

### Youki - Container Runtime in Rust
[github.com/youki-dev/youki](https://github.com/youki-dev/youki) • 7.1k stars

OCI-compliant container runtime. Alternative to runc (Docker) and crun (Red Hat). Community-driven, now a CNCF sandbox project.

Early contributor to the project. My work included:
- [WebAssembly workload support](https://github.com/youki-dev/youki/pull/548)
- [cgroups v2 implementation](https://github.com/youki-dev/youki/pull/48)
- Command-line interface 
- [Library API](https://github.com/youki-dev/youki/pull/314) (making it embeddable)
- [Rootless containers](https://github.com/youki-dev/youki/pull/98)
- [Systemd resource control integration](https://github.com/youki-dev/youki/pull/451)

Docker delegates container creation to runtimes like youki, which handle namespaces, cgroups, and filesystem isolation.

### oci-spec
[github.com/youki-dev/oci-spec-rs](https://github.com/youki-dev/oci-spec-rs) • 6M downloads 

Rust implementation of OCI specifications. Wrote the initial image spec implementation and contributed heavily to the runtime spec. Used by the containerd project, Kubewarden, and others.

### Gitpod
[github.com/gitpod-io/gitpod](https://github.com/gitpod-io/gitpod) • 13.5k stars

Contributor to Gitpod's cloud development environment platform. Some of my work:

#### [Kubernetes Controller (ws-manager-mk2)](https://github.com/gitpod-io/gitpod/pulls?q=is%3Apr+is%3Aclosed+label%3A%22feature%3A+ws-manager-mk2%22)

Built controller managing workspace lifecycle for Gitpod's SaaS platform. 

Replaced gRPC-based state management with CRD-based architecture. Decoupled workspace lifecycle from pod lifecycle, enabling restarts without service interruption. 

Improved reliability from 99.9% to 99.99%.

#### [Workspace Classes](https://github.com/gitpod-io/gitpod/pulls?q=is%3Apr+is%3Aclosed+author%3AFuristo+label%3A%22feature%3A+workspace+classes%22)

Implemented resource tiering system enabling customers to select differently sized workspaces based on computational needs.

#### [DDoS Protection](https://github.com/gitpod-io/gitpod/pull/11255)

Initiated and implemented rate limiting using nftables to prevent abuse. 

Used token bucket algorithm to limit connection attempts while allowing existing connections to continue. 

Reduced on-call alerts by 34%.

#### [Pressure Stall Information (PSI)](https://github.com/gitpod-io/gitpod/pulls?q=is%3Apr+is%3Aclosed+author%3AFuristo+label%3A%22feature%3A+psi%22)

Implemented scraping of Linux PSI metrics to diagnose performance issues in customer workspaces. 

Enables troubleshooting resource contention (CPU, memory, I/O pressure).