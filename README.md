# Bruce Kashani

**Solution architect and consultant — distributed systems, blockchain, and cloud.**
Toronto, Canada · bkashani@gmail.com

I design and build systems that have to be correct under adversarial
conditions, and I write them so that other engineers can read them. Available
for consulting and solution-architecture engagements from late 2026.

## What I do

- **Solution architecture** — from a business problem to a system design a
  team can build: data model, consensus and trust boundaries, deployment
  topology, operations, cost.
- **Private and consortium ledgers** — a shared, tamper-evident record that
  several organisations write to and none can quietly rewrite, without a public
  token or a heavyweight framework.
- **Security-minded engineering** — threat models where every rule points at
  the code that enforces it and the test that shows the attack failing.
- **Cloud and delivery** — Google Cloud, Kubernetes, Docker, CI/CD; TypeScript
  and Node.js, C# and .NET.

## PlainChain

[**PlainChain**](https://github.com/behrouzbk/plainchain) is a complete Layer 1
blockchain node written from scratch in TypeScript — small enough to read in an
afternoon. No blockchain SDKs: every hash, signature and Merkle tree comes from
Node's built-in `crypto`, and there are three runtime dependencies.

- Proof of work with fork-aware retargeting, **or** a Clique-style proof of
  authority for consortium chains
- UTXO ledger with crash-atomic reorganisations, header-first sync, checkpoints
- Replace-by-fee mempool; wallet with BIP-39 phrases, watch-only files and an
  SPV light client
- JSON-RPC over TLS, Prometheus metrics, Docker and Kubernetes packaging (run
  on GKE)
- 576 tests, a large share of them explicit attacks; a public
  [threat model](https://github.com/behrouzbk/plainchain/blob/main/docs/THREAT-MODEL.md)
  covering about 55 threats, each tied to code and a test

Built test-first over four stages with the engineering conventions documented
in the repository. Apache 2.0.

## Working with me

Email **bkashani@gmail.com** with a paragraph about the problem. Typical
engagements: a discovery and design phase, a private-chain deployment with a
runbook and operator training, or an architecture review of an existing system.
