[update-readmes]   Mode: rewrite — migrating to template structure...
# rust-hypervisor-firmware

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/rust-hypervisor-firmware)

<!-- AI:start:what-it-does -->
This project provides a minimal, lightweight firmware implementation for hypervisors, written in Rust. It targets multiple architectures, including x86_64, AArch64, and RISC-V, and is designed to initialize virtual machines by setting up the required hardware state and bootstrapping the guest operating system. It is used by developers building virtualization platforms or custom hypervisor solutions.
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
The project is structured as a Rust-based firmware for hypervisors, supporting multiple architectures (x86_64, aarch64, riscv64). It uses a modular design with architecture-specific dependencies and configurations. The main components include:

1. **Core Logic**: Located in `src/`, this directory contains the primary implementation of the firmware.
2. **Architecture-Specific Configurations**: Files like `x86_64-unknown-none.json`, `aarch64-unknown-none.json`, and `riscv64gcv-unknown-none-elf.json` define target-specific settings.
3. **Build Scripts**: `build.rs` handles custom build steps.
4. **Resources**: The `resources/` directory contains additional assets required during the build or runtime.
5. **Scripts**: Utility scripts are stored in the `scripts/` directory.
6. **Configuration Files**: Files like `Cargo.toml`, `rust-toolchain.toml`, and `.github/` workflows manage dependencies, toolchains, and CI/CD pipelines.

The components interact through Rust's module system and conditional compilation, enabling architecture-specific code paths. The directory structure is as follows:

```plaintext
.
├── .github/
├── resources/
├── scripts/
├── src/
│   ├── arch/
│   ├── drivers/
│   ├── firmware/
│   └── main.rs
├── Cargo.toml
├── build.rs
├── rust-toolchain.toml
├── x86_64-unknown-none.json
├── aarch64-unknown-none.json
└── riscv64gcv-unknown-none-elf.json
```
<!-- AI:end:architecture -->

## Install

<!-- Add installation instructions here. This section is yours — the AI will not modify it. -->

```bash
git clone https://github.com/Interested-Deving-1896/rust-hypervisor-firmware.git
cd rust-hypervisor-firmware
```

## Usage

<!-- Add usage examples here. This section is yours — the AI will not modify it. -->

## Configuration

<!-- Document configuration options here. This section is yours — the AI will not modify it. -->

## CI

<!-- AI:start:ci -->
- **build.yaml**: Runs `cargo build` and `cargo clippy` for all supported targets (x86_64, aarch64, riscv64). Ensures code compiles and adheres to linting rules. No secrets required.

- **dco.yaml**: Verifies that all commits are signed with a Developer Certificate of Origin (DCO). No secrets required.

- **docker-image.yaml**: Builds and optionally pushes a Docker image containing the project. Requires `DOCKER_USERNAME` and `DOCKER_PASSWORD` secrets for pushing images.

- **integration-windows.yaml**: Executes integration tests on a Windows environment. Ensures compatibility with Windows systems. No secrets required.

- **release.yaml**: Builds and publishes release artifacts for supported targets. Requires `GITHUB_TOKEN` (provided by default in GitHub Actions) for publishing releases.

- **tests.yaml**: Runs unit tests and integration tests for all supported targets. Ensures correctness of the codebase. No secrets required.
<!-- AI:end:ci -->

## Mirror chain

<!-- AI:start:mirror-chain -->
This repo is maintained in [`Interested-Deving-1896/rust-hypervisor-firmware`](https://github.com/Interested-Deving-1896/rust-hypervisor-firmware) and mirrored through:

```
Interested-Deving-1896/rust-hypervisor-firmware  ──►  OpenOS-Project-OSP/rust-hypervisor-firmware  ──►  OpenOS-Project-Ecosystem-OOC/rust-hypervisor-firmware
```

Changes flow downstream automatically via the hourly mirror chain in
[`fork-sync-all`](https://github.com/Interested-Deving-1896/fork-sync-all).
Direct commits to OSP or OOC are detected and opened as PRs back to `Interested-Deving-1896`.
<!-- AI:end:mirror-chain -->

## Contributors

<!-- AI:start:contributors -->
[@retrage](https://github.com/retrage) (243 commits)  
[@rbradford](https://github.com/rbradford) (196 commits)  
[@dependabot[bot]](https://github.com/dependabot[bot]) (146 commits)  
[@josephlr](https://github.com/josephlr) (67 commits)  
[@dependabot-preview[bot]](https://github.com/dependabot-preview[bot]) (20 commits)  
[@jongwu](https://github.com/jongwu) (11 commits)  
[@benmaddison](https://github.com/benmaddison) (4 commits)  
[@yuuzi41](https://github.com/yuuzi41) (1 commit)  
[@shpark](https://github.com/shpark) (1 commit)  
[@rveerama1](https://github.com/rveerama1) (1 commit)  
[@ning-yang](https://github.com/ning-yang) (1 commit)  
[@edigaryev](https://github.com/edigaryev) (1 commit)  
[@MrXinWang](https://github.com/MrXinWang) (1 commit)  
[@henryksloan](https://github.com/henryksloan) (1 commit)  
[@fdr](https://github.com/fdr) (1 commit)  
[@Lencerf](https://github.com/Lencerf) (1 commit)  
[@thenewwazoo](https://github.com/thenewwazoo) (1 commit)  
[@acarp-crusoe](https://github.com/acarp-crusoe) (1 commit)  

This repository may be a mirror. Please refer to the upstream source for additional contributions and updates.
<!-- AI:end:contributors -->

## Origins

<!-- AI:start:origins -->
_Original project — no upstream fork._
<!-- AI:end:origins -->

## Resources

<!-- AI:start:resources -->
_No additional resource files found._
<!-- AI:end:resources -->

## License

<!-- AI:start:license -->
[Apache-2.0](https://github.com/Interested-Deving-1896/rust-hypervisor-firmware/blob/main/LICENSE) © 2026 [Interested-Deving-1896](https://github.com/Interested-Deving-1896)
<!-- AI:end:license -->
