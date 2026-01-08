# Distributed Operating Systems: Quick Reference Comparison

## Primary Systems Analyzed

| System | Repository | Status | Languages | Key Innovation |
|--------|-----------|--------|-----------|----------------|
| **Plan 9** | plan9foundation/plan9 | Active (Community) | C, Assembly, Rc | 9P protocol, per-process namespaces |
| **Inferno** | inferno-os/inferno-os | Active (Community) | Limbo, C | Styx protocol, Dis VM portability |
| **Node9** | jvburnes/node9 | Inactive (2020) | C, Lua | LuaJIT + libuv modernization |
| **Harvey OS** | Harvey-OS/harvey | Inactive (2022) | C, Assembly | 9P2000, Fossil/Venti storage |

## Organization Repositories of Interest

### Harvey-OS Organization
| Repository | Stars | Description |
|------------|-------|-------------|
| harvey | 1,448 | Main distributed OS |
| ninep | 40 | Go 9P/9P2000 implementation |
| apex | 33 | ANSI POSIX Environment |

### inferno-os Organization
| Repository | Stars | Description |
|------------|-------|-------------|
| inferno-os | 696 | Main distributed OS |
| ventivac | 6 | Venti components for Inferno |
| inferno-2e | 13 | Historical 1999 release |

## Other Notable Distributed Operating Systems

### Active Projects
| System | Type | Key Feature |
|--------|------|-------------|
| **9front** | Plan 9 fork | Most active, expanded hardware support |
| **HarmonyOS** | Commercial | Cross-device distributed experience |
| **Fuchsia** | Commercial | Capability-based security, Zircon microkernel |
| **seL4** | Research | Formally verified microkernel |
| **Genode** | Research | Component-based, capability security |
| **Redox** | Community | Rust-based, memory safety |

### Historical Systems
| System | Origin | Contribution |
|--------|--------|--------------|
| **Amoeba** | VU Amsterdam | Microkernel distributed OS, led to Python |
| **Sprite** | UC Berkeley | High-performance distributed file system |
| **LOCUS** | UCLA | Transparent distributed file system |
| **Barrelfish** | ETH Zurich/MS | Multikernel architecture |
| **MINIX 3** | VU Amsterdam | Self-healing microkernel |

## Best Features by Category

### Protocol & Communication
| Feature | Best Implementation | Why |
|---------|---------------------|-----|
| Resource protocol | Plan 9 (9P) | Simple, elegant, proven |
| Network transparency | Inferno (Styx) | Refined 9P with security |
| Cross-device | HarmonyOS | Distributed Soft Bus |

### Security
| Feature | Best Implementation | Why |
|---------|---------------------|-----|
| Formal verification | seL4 | Mathematical proof of correctness |
| Capability security | Fuchsia/Genode | Fine-grained access control |
| Authentication | Harvey (Factotum) | Centralized credential management |

### Language & Runtime
| Feature | Best Implementation | Why |
|---------|---------------------|-----|
| Memory safety | Redox (Rust) | Compile-time guarantees |
| Portability | Inferno (Dis VM) | Cross-platform bytecode |
| Performance | Node9 (LuaJIT) | Near-native JIT compilation |

### Storage
| Feature | Best Implementation | Why |
|---------|---------------------|-----|
| Content-addressable | Harvey (Venti) | Deduplication, integrity |
| Snapshots | Harvey (Fossil) | Built-in versioning |
| Distributed | Plan 9 | Network-transparent access |

## Recommended Strategy Summary

### Core Components
1. **Microkernel**: seL4-based (formally verified)
2. **Protocol**: 9P-NG (modernized 9P)
3. **Namespaces**: Per-process (Plan 9 style)
4. **Security**: Capability-based (Fuchsia/Genode style)

### Languages
1. **System**: Rust (memory safety)
2. **Applications**: Go (concurrency), LuaJIT (scripting)
3. **Portable**: WebAssembly (sandboxed execution)

### Key Subsystems
1. Distributed file system with content-addressable storage
2. Authentication agent (Factotum-inspired)
3. Distributed scheduler with load balancing
4. Capability-based security throughout

### Development Phases
| Phase | Duration | Focus |
|-------|----------|-------|
| 1 | 12-18 months | Core microkernel, 9P-NG, Rust SDK |
| 2 | 9-12 months | Scheduler, storage, Go/Lua runtimes |
| 3 | 12-18 months | GUI, Wasm, drivers, documentation |
