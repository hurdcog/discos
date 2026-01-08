# DiscOS - Distributed Cognitive Operating System

**DiscOS** is a next-generation distributed operating system that combines the best features from Plan 9, Inferno, and modern distributed OS research. This repository serves as the development foundation for building an optimal distributed OS with cognitive computing capabilities.

## Vision

DiscOS aims to create a unified platform that integrates:
- **Plan 9's elegance**: 9P protocol, per-process namespaces, "everything is a file"
- **Inferno's portability**: Styx protocol, virtual machine architecture
- **Modern security**: Capability-based security, formal verification principles
- **Cognitive computing**: Native support for AGI architectures and distributed intelligence

## Repository Structure

```
discos/
├── docs/                           # Research and strategy documents
│   ├── distributed_os_comprehensive_report.md
│   ├── distributed_os_comparison.md
│   └── distributed_os_strategy.md
├── sources/
│   ├── plan9-family/              # Plan 9 family source code
│   │   ├── plan9/                 # Plan 9 from Bell Labs
│   │   ├── inferno/               # Inferno OS
│   │   ├── harvey/                # Harvey OS
│   │   └── node9/                 # Node9 (Lua/LuaJIT modernization)
│   ├── tools/                     # Supporting tools and libraries
│   │   ├── ninep/                 # Go 9P2000 implementation
│   │   ├── apex/                  # ANSI POSIX Environment
│   │   └── ventivac/              # Venti components for Inferno
│   └── modern-os/                 # Modern OS references (future)
└── README.md
```

## Source Components

### Plan 9 Family

| Component | Description | Origin |
|-----------|-------------|--------|
| **plan9** | Original Plan 9 from Bell Labs - the foundational distributed OS | plan9foundation/plan9 |
| **inferno** | Inferno OS with Limbo/Dis VM and Styx protocol | inferno-os/inferno-os |
| **harvey** | Harvey OS - Plan 9 continuation with 9P2000, Fossil, Venti | Harvey-OS/harvey |
| **node9** | Modernized Inferno with LuaJIT and libuv | jvburnes/node9 |

### Tools & Libraries

| Component | Description | Origin |
|-----------|-------------|--------|
| **ninep** | Idiomatic Go implementation of 9P/9P2000 protocols | Harvey-OS/ninep |
| **apex** | ANSI POSIX Environment for Plan 9 compatibility | Harvey-OS/apex |
| **ventivac** | Venti block storage components for Inferno | inferno-os/ventivac |

## Key Features to Integrate

### From Plan 9
- 9P protocol for unified resource access
- Per-process namespaces
- Union directories
- /proc filesystem
- rc shell

### From Inferno
- Styx protocol (refined 9P)
- Limbo concurrent programming language
- Dis virtual machine for portability
- Hosted/native dual-mode operation

### From Node9
- LuaJIT high-performance runtime
- libuv async I/O model
- Modern language accessibility

### From Harvey
- 9P2000 protocol improvements
- Fossil file system with snapshots
- Venti content-addressable storage
- Factotum authentication agent

## Development Roadmap

### Phase 1: Core System (12-18 months)
- Develop microkernel foundation
- Implement 9P-NG protocol
- Create Rust-based system SDK

### Phase 2: Basic System (9-12 months)
- Implement Go and LuaJIT runtimes
- Develop distributed scheduler
- Create content-addressable storage

### Phase 3: Full-Featured OS (12-18 months)
- Develop graphical user interface
- Implement WebAssembly runtime
- Expand driver and hardware support

## Documentation

See the `docs/` directory for detailed analysis and strategy:
- [Comprehensive Report](docs/distributed_os_comprehensive_report.md) - Full analysis of all systems
- [Comparison Guide](docs/distributed_os_comparison.md) - Quick reference comparison
- [Strategy Document](docs/distributed_os_strategy.md) - Development strategy

## License

This repository integrates code from multiple sources with different licenses:
- Plan 9: Lucent Public License / MIT
- Inferno: GPL/LGPL/MIT
- Harvey: GPL
- Node9: MIT
- ninep: BSD-3-Clause
- apex: MIT
- ventivac: MIT

Please refer to individual component directories for specific license terms.

## Contributing

Contributions are welcome! Please see the documentation for architectural guidelines and development practices.

## Acknowledgments

This project builds upon decades of distributed systems research from Bell Labs, UC Berkeley, and the open source community. Special thanks to the maintainers of Plan 9, Inferno, Harvey OS, and Node9.
