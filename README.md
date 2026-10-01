# Bruce Kashani

**Solution architect and consultant — distributed systems, blockchain, and cloud (Google Cloud, AWS).**
Toronto, Canada · [InnoVista Tech](https://innovistatech.ca) · bkashani@gmail.com

I design and build systems that have to be correct under adversarial
conditions — ledgers, payment flows, shared records between organisations —
and I write them so that other engineers can read them. I work through
[InnoVista Tech](https://innovistatech.ca), a Toronto consultancy.

## Services

- **Consulting** — an architect on call: design reviews, platform and vendor
  selection, "do we need a blockchain?" answered honestly, due diligence, and
  support during delivery. By the day or on a monthly retainer.
- **Solution architecture** — from a business problem to a system design a
  team can build: data model, trust boundaries, failure modes, deployment
  topology on Google Cloud or AWS, operations, cost.
- **Private and consortium ledgers** — a shared, tamper-evident record that
  several organisations write to and none can quietly rewrite, without a public
  token or a heavyweight framework. Fixed price, with a runbook and operator
  training.
- **Architecture review** — a written report on an existing system: what can
  go wrong, ranked; what to fix first; what is fine and why.
- **Training** — a self-paced course where engineers implement a real
  blockchain's rules with its own tests as the judge, and live workshops for
  teams.

Details, pricing shape and the contact form: **https://innovistatech.ca**

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
- JSON-RPC over TLS, Prometheus metrics, Docker and Kubernetes packaging —
  deployed and tested on Google Cloud (GKE)
- 622 tests, a large share of them explicit attacks; a public
  [threat model](https://github.com/behrouzbk/plainchain/blob/main/docs/THREAT-MODEL.md)
  covering about 60 threats, each tied to code and a test

Built test-first over four stages with the engineering conventions documented
in the repository. Open source. Not yet independently audited, and the
repository says so.

## Working with me

Write to **bkashani@gmail.com**, or use the form at
[innovistatech.ca/contact](https://innovistatech.ca/contact.html), with a
paragraph about the problem. You will get a first opinion within two business
days — including "you may not need this".
