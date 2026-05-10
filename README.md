
<p align="left"> <img src="https://komarev.com/ghpvc/?username=ritish134&label=Profile%20views&color=0e75b6&style=flat" alt="ritish134" /> </p>


<h3 align="left">Languages and Tools:</h3>
<table>
<tr>
<td><a href="https://www.linux.org"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" width="40"/></a></td>
<td><a href="https://www.gnu.org/software/bash/"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/bash/bash-original.svg" width="40"/></a></td>
<td><a href="https://www.docker.com"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original.svg" width="40"/></a></td>
<td><a href="https://kubernetes.io"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/kubernetes/kubernetes-plain.svg" width="40"/></a></td>
<td><a href="https://azure.microsoft.com"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/azure/azure-original.svg" width="40"/></a></td>
<td><a href="https://grafana.com"><img src="https://raw.githubusercontent.com/grafana/grafana/main/public/img/grafana_icon.svg" width="40"/></a></td>
<td><a href="https://prometheus.io"><img src="https://raw.githubusercontent.com/prometheus/prometheus/main/documentation/images/prometheus-logo.svg" width="40"/></a></td>
<td><a href="https://grafana.com/oss/loki/"><img src="https://github.com/grafana/loki/blob/main/docs/sources/logo.png" width="40"/></a></td>
<td><a href="https://www.jenkins.io/"><img src="https://www.vectorlogo.zone/logos/jenkins/jenkins-icon.svg" width="40"/></a></td>
<td><a href="https://www.w3schools.com/cpp/"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" width="40"/></a></td>
<td><a href="https://golang.org"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/go/go-original.svg" width="40"/></a></td>
<td><a href="https://www.mysql.com/"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" width="40"/></a></td>
<td><a href="https://cmake.org/"><img width="48" height="48" alt="image" src="https://github.com/user-attachments/assets/355b8fbe-4a6b-42f0-96c6-18495038b549" />
</a></td>
<td><a href="https://www.rust-lang.org/"><img width="48" height="48" alt="image" src="https://github.com/user-attachments/assets/2e0f35dc-8490-40ef-9ecb-01a19ce6d61b" />
</a></td>
</tr>
</table>


---

## Contributions
### 🛠️ Compilers & Static Analysis

| Project | PR | Concept |
|---|---|---|
| **[llvm/llvm-project](https://github.com/llvm/llvm-project)** *(38k ⭐)* | [#196783](https://github.com/llvm/llvm-project/pull/196783) | `readability-delete-null-pointer` clang-tidy check warned about unnecessary `if (ptr) { delete ptr; }` with an else branch but generated no fix-it (FIXME in source). Implemented the transformation that strips the if/else structure and unwraps both bodies — safe because deleting null is a no-op per C++ [expr.delete]. |
### 🦀 Database Internals & Distributed Systems

| Project | PR | Concept |
|---|---|---|
| **[tursodatabase/turso](https://github.com/tursodatabase/turso)** *(18k ⭐)* | [#6193](https://github.com/tursodatabase/turso/pull/6193)  | B-tree splits allocate new pages - during balancing, those pages must be registered in the pointer map so autovacuum can track and relocate them. |
| **[superfly/corrosion](https://github.com/superfly/corrosion)** *(1.7k ⭐)* | [#459](https://github.com/superfly/corrosion/pull/459)  | Config validation and builder pattern for gossip MTU settings. |
| **[superfly/corrosion](https://github.com/superfly/corrosion)** | [#460](https://github.com/superfly/corrosion/pull/460)  | SWIM gossip packet sizing - how UDP datagrams must fit within the MTU after subtracting QUIC header overhead. |
| **[superfly/corrosion](https://github.com/superfly/corrosion)** | [#470](https://github.com/superfly/corrosion/pull/470)  | Replacing magic string literals with named constants across a distributed query response path. |

> *turso* is a from-scratch SQLite-compatible database in Rust. *corrosion* is Fly.io's distributed SQLite over QUIC.

---

### ☸️ Kubernetes & Cloud Native

| Project | PR | Concept |
|---|---|---|
| **[portainer/kubesolo](https://github.com/portainer/kubesolo)** *(485 ⭐)* | [#118](https://github.com/portainer/kubesolo/pull/118)  | Webhook hot path optimization - JSON marshal/unmarshal at startup once vs. decoding static data on every pod admission request. Dropped from 1873 ns/op to 0.63 ns/op, 20 allocs → 0. |
| **[portainer/kubesolo](https://github.com/portainer/kubesolo)** | [#112](https://github.com/portainer/kubesolo/pull/112)  | Cross-compilation for ARM musl targets - static linking, no glibc, verified across runc, CNI plugins, and container image manifests. |
| **[kube-burner/kube-burner](https://github.com/kube-burner/kube-burner)** | [#896](https://github.com/kube-burner/kube-burner/pull/896)  | Rate limiter config validation - invalid QPS/Burst values caused a panic inside the Kubernetes client rather than a clean error. |

---

### 🔒 Security & Supply Chain

| Project | PR | Concept |
|---|---|---|
| **[chainguard-dev/malcontent](https://github.com/chainguard-dev/malcontent)** *(652 ⭐)* | [#992](https://github.com/chainguard-dev/malcontent/pull/992)  | Refactoring a large report generation function - how to decompose a monolith into focused helpers without breaking behavior across pledges, syscalls, and capability metadata. |
| **[chainguard-dev/malcontent](https://github.com/chainguard-dev/malcontent)** | [#1045](https://github.com/chainguard-dev/malcontent/pull/1045)  | Reducing allocations in a hot path - replacing `strings.Split` + `fmt.Sprintf` with index lookups and string slicing when scanning large file sets. |
| **[chainguard-dev/malcontent](https://github.com/chainguard-dev/malcontent)** | [#1068](https://github.com/chainguard-dev/malcontent/pull/1068)  | CLI flag ordering in a `urfave/cli` app - global flags must come before the subcommand, not after. |
| **[chainguard-dev/dfc](https://github.com/chainguard-dev/dfc)** | [#108](https://github.com/chainguard-dev/dfc/pull/108)  | Path validation for user-supplied YAML files - blocking directory traversal and enforcing safe extensions at the CLI layer. |
| **[wolfi-dev/os](https://github.com/wolfi-dev/os)** *(1.2k ⭐)* | [#78677](https://github.com/wolfi-dev/os/pull/78677) · [#78676](https://github.com/wolfi-dev/os/pull/78676) · [#77400](https://github.com/wolfi-dev/os/pull/77400) | Package maintenance on Chainguard's Wolfi Linux - version bumps and cleanup of carried patches. |

---

### 🔐 Secure Communication & CI

| Project | PR | Concept |
|---|---|---|
| **[build-trust/ockam](https://github.com/build-trust/ockam)** *(4.6k ⭐)* | [#6525](https://github.com/build-trust/ockam/pull/6525) · [#6590](https://github.com/build-trust/ockam/pull/6590)  | Composite GitHub Actions - renaming and wiring a reusable action across dozens of CI workflows. |

---

### 🌱 Where it started

| [tungbq/LocalEnv #31](https://github.com/tungbq/LocalEnv/pull/31) | [tungbq/AWSHub #177](https://github.com/tungbq/AWSHub/pull/177) | [TheMagnificent11/lewee #175](https://github.com/TheMagnificent11/lewee/pull/175) |
|---|---|---|
|  Added Java environment support |  Documentation |  .NET code contribution |

---

## 🛠️ What I'm comfortable with

`Rust` · `Go`· `cmake`· `build-systems` · `Kubernetes` · `distributed systems` · `database internals` · `CI/CD` · `Linux`

---
