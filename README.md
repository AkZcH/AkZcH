# Akshat Chauhan

**Systems Engineer** — low-level foundations, distributed systems on top.

---

I like the layer where things actually break: syscalls, consensus, network partitions, the 3 a.m. page nobody wants. I build systems that fail loudly in staging so they don't fail quietly in production — and when they do fail anyway, I'd rather be the person calmly reading the stack trace than the one refreshing the dashboard in a panic.

Most of what's below started as "I don't fully understand why this breaks" and turned into a project once I got annoyed enough to find out.

---

## What I actually work with

**Systems & Languages**
Rust (primary — memory management, concurrency, `ptrace`/syscall-level work), Go, C, TypeScript. Comfortable enough in Linux internals to trace a syscall by hand before reaching for a wrapper library.

**Infra I've actually run, not just read about**
Docker, Kubernetes (HPA/autoscaling), PostgreSQL (including the fun failure modes — see blog), Redis, GitHub Actions CI.

**Distributed systems concepts I'm actively building against**
Leader election, consensus (Raft/Paxos — studied and prototyped, not production-hardened yet), config propagation, WAL design, deterministic replay of non-deterministic failures.

---

## Currently going deep on

- Rust, properly this time — first-principles, not pattern-matched from tutorials
- eBPF for observability and syscall-level tracing
- Distributed config propagation and consensus (see: Herald)
- Debugging things that only break in Docker, on Windows, at the worst possible time

I don't list Terraform/Ansible/service mesh/observability-stack tooling here — I've read about them, haven't shipped with them, and I'd rather you trust the things I do claim.

---

## Featured Work

- **[Herald](https://github.com/AkZcH/Herald)** — Self-hosted distributed config propagation engine, Go. Built to survive the kind of partial-failure scenarios that take down config-driven systems silently.
- **[SysRift](https://github.com/AkZcH/SysRift)** — `ptrace`-based syscall recorder/replayer for deterministic debugging of non-deterministic bugs. Rust, multi-process tracing via `PTRACE_O_TRACEFORK`.
- **[RavenMQ](https://github.com/AkZcH/SmartQueue)** — Distributed task scheduler: leader election via Postgres advisory locks, Kubernetes-native autoscaling, LSTM-based load prediction.
- **[EchoTrap](https://github.com/AkZcH/EchoTrap)** — Async TCP honeypot in Tokio for attack detection and evasion behavior.

---

## Writing

I write up the incidents, not just the wins. Recent: debugging why Postgres 16's SCRAM-SHA-256 change silently broke Go connections on Windows/Docker Desktop, and what that says about assuming your auth stack hasn't changed under you.

[Blog →](https://akshatsystems.vercel.app/writings/)

---

## Contact

[LinkedIn](https://linkedin.com/in/akshat-chauhan) · akshatchauhan.dev@gmail.com

> Make it work, make it right, make it fast — and write down what broke along the way.
