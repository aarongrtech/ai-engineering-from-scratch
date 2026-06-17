# My Progress — AI Engineering from Scratch

Personal log of lessons as I work through the curriculum.
Tracked on the `my-progress` branch of my fork (`aarongrtech/ai-engineering-from-scratch`).

## Phase 00 — Setup & Tooling
- [x] **01 — Dev Environment** — `verify.py` 7/7 core + 2/2 GPU. Python 3.12 + course `.venv` (numpy, matplotlib, jupyter, torch 2.6.0+cu124), Node 22 (nvm) + pnpm, Rust 1.96. GPU: 2× NVIDIA RTX A2000 12GB via WSL2 (CUDA available in PyTorch).
- [x] **02 — Git & Collaboration** — forked upstream, added a `fork` remote alongside `origin` (upstream), and practiced the full loop: branch → add → commit → push.

## Notes
- Concept that clicked in lesson 1: an inference endpoint (my llama.cpp server) is *not* local PyTorch/CUDA — it's an HTTP service you call as a client.
- The fork model (lesson 2): contribute to a repo you don't own by pushing to *your* fork, then opening a PR upstream.
- WSL GPU access (lesson 1 redo): the `/usr/lib/wsl/lib` driver libs are *projected from the Windows driver*, never installed inside WSL. A stale projection (WSL 595.71.01 vs Windows 596.36) broke GPU-PV with `dxgkio_query_adapter_info: Ioctl failed: -2`. Fix was a full **Windows reboot** (not just `wsl --shutdown`) to resync, plus switching GPU 0 out of TCC mode (`nvidia-smi -i 0 -dm 0`) so WSL could see it.
