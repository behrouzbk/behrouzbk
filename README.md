# Bruce Banaei

**Solution architect for AI and blockchain — AI systems that stay affordable in production, and ledgers that stay correct under attack.**
Toronto, Canada · Axieo Technologies Inc. · info@axieo.ca

I design and build systems where mistakes are expensive: AI applications whose
cost grows with every call, and ledgers, payment flows and shared records
between organisations that have to stay correct under adversarial conditions.
I write them so that other engineers can read them. I work through Axieo
Technologies Inc., based in Toronto.

## Services

- **Consulting** — an architect on call: design reviews, model, platform and
  vendor selection, "do we need an LLM for this?" and "do we need a
  blockchain?" answered honestly, due diligence, and support during delivery.
  By the day or on a monthly retainer.
- **Solution architecture** — from a business problem to a system design a
  team can build: data model, trust boundaries, failure modes, deployment
  topology on Google Cloud or AWS, operations, cost.
- **AI cost review** — where your LLM spend actually goes: prompts, model
  choice, caching, retrieval and output size, ranked by savings, with a plan to
  cut the bill without losing quality.
- **Private and consortium ledgers** — a shared, tamper-evident record that
  several organisations write to and none can quietly rewrite, without a public
  token or a heavyweight framework. Fixed price, with a runbook and operator
  training.
- **Architecture review** — a written report on an existing system: what can
  go wrong, ranked; what to fix first; what is fine and why.
- **Training** — a self-paced course where engineers implement a real
  blockchain's rules with its own tests as the judge, and live workshops for
  teams.

## tokensaver

[**tokensaver**](https://github.com/behrouzbk/tokensaver) is an open-source
command-line tool that shows what a prompt costs on 20 OpenAI, Anthropic and
Google models, and exactly which changes make it cheaper. Each suggestion
comes with its reason and the tokens and dollars it saves.

- Runs fully offline: the prompt never leaves the machine, and the tokenizer
  files ship inside the package, checked against their published hashes
- Exact counts for OpenAI models; Claude, Gemini and GPT-6 shown as clearly
  labelled estimates, never as exact
- Six rule-based optimizers (JSON minification, duplicates, repeated
  instructions, filler, whitespace, long few-shot examples). Safe changes are
  applied by default; anything that could change meaning waits for review
- Every saving is measured before and after on the chosen model: the bundled
  example prompt drops by 20% on GPT-4o
- Python, 149 tests, CI on Windows, macOS and Linux

The rules are heuristics, and the README says exactly what is exact and what
is estimated.

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

Write to **info@axieo.ca** with a paragraph about the problem. You will get a
first opinion within two business days — including "you may not need this".
