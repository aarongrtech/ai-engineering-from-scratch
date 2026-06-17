# My Progress — AI Engineering from Scratch

Personal log of lessons as I work through the curriculum.
Tracked on the `my-progress` branch of my fork (`aarongrtech/ai-engineering-from-scratch`).

## Phase 00 — Setup & Tooling
- [x] **01 — Dev Environment** — `verify.py` 7/7. Python 3.12 + course `.venv` (numpy, matplotlib, jupyter), Node 20, Rust 1.96. No local GPU — running on CPU.
- [x] **02 — Git & Collaboration** — forked upstream, added a `fork` remote alongside `origin` (upstream), and practiced the full loop: branch → add → commit → push.

## Notes
- Concept that clicked in lesson 1: an inference endpoint (my llama.cpp server) is *not* local PyTorch/CUDA — it's an HTTP service you call as a client.
- The fork model (lesson 2): contribute to a repo you don't own by pushing to *your* fork, then opening a PR upstream.
