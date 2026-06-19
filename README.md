# PBC Miner — Privacy Bank Chain

> ### *"Private money that works for you."*

![Status](https://img.shields.io/badge/status-pre--launch%20preview-orange)
![Algorithm](https://img.shields.io/badge/algo-RandomX%20v2-8a2be2)
![Variant](https://img.shields.io/badge/variant-rx%2Fpbc-blueviolet)
![Mining](https://img.shields.io/badge/mining-CPU%20only-brightgreen)
![License](https://img.shields.io/badge/license-GPL--3.0-green)

This is the official CPU miner for **Privacy Bank Chain (PBC)** — a new privacy blockchain that is **not launched yet**. The miner is open source *today* so the people who build the ecosystem — pool operators, tooling devs, early miners — can study it and be ready before mainnet goes live.

---

## Something new is coming

For years you had to choose.

**Monero** gave you real privacy — but your coins just sit there. No yield, no savings, nothing.
**DeFi** gave you yield — but every balance and position is public, and it all runs on smart contracts that have been drained for **billions**.

PBC refuses that trade-off. It brings genuine, bank-grade financial tools to a chain with **Monero-level privacy** — and every one of them is written directly into the protocol in verifiable, deterministic **C++**:

- **No smart contracts** — no virtual machine, no bytecode to exploit
- **No oracles, no custody, no admin keys**
- Just cryptography and consensus

The result is a set of native capabilities that — combined — we don't believe exist together on **any** other privacy blockchain, including protections built for the **post-quantum era**, an area where the major privacy coins still have no deployed answer.

That's all we'll say in public for now. The full picture lands at launch.

> Want to know what's actually inside before everyone else? The people who get the details first are in the community below. 👇

---

## Get a head start — this is why the miner is already public

PBC mines with **RandomX v2 (`rx/pbc`)** — CPU-only and ASIC-resistant, true to the "anyone can mine from home" philosophy. Because it's RandomX, it is **Stratum-compatible**: a pool sees a standard coinbase structure, so getting a pool ready is straightforward.

If you run a pool, build mining tools, or simply like being early — **clone it, read it, build it now**, and you'll be ready on day one.

### Build from source (Ubuntu 24.04)

The miner is an [XMRig](https://github.com/xmrig/xmrig) fork; CMake produces a binary named `xmrig`, which is renamed to `pbcminer`. RandomX is bundled in-tree — no extra package required.

```bash
sudo apt update
sudo apt install -y build-essential cmake pkg-config git libssl-dev libuv1-dev libhwloc-dev

# from the repository root:
mkdir -p build && cd build
cmake -DCMAKE_BUILD_TYPE=Release -DWITH_CUDA=OFF -DWITH_OPENCL=OFF -DWITH_NVML=OFF ..
make -j$(nproc)
mv xmrig pbcminer
```

`rx/pbc` is a CPU algorithm, so the supported build is CPU-only.

> **Pre-launch note:** there is no public network to mine against yet. Right now you can **study and compile** the miner to prepare. Configuration and connection details ship with the mainnet launch — announced first in the community below.

---

## Be first when it launches

When PBC goes live, **it is announced first inside PulseMining** — our crypto-mining community.

PulseMining is for people who like to spot good projects early and actually understand what they're mining:

- 🌍 **Fully multilingual, translated in real time (FR · EN · ES · RU)**
- 💎 **Signal over noise** — real projects, surfaced and explained, not hype
- 🛠️ **Real support** — node, wallet or miner giving you trouble? You're never on your own
- 🤝 **Builders welcome** — pool operators, devs and partners are already in

No promises of miracle gains — just people who'll help you move forward, and the launch news before anyone else.

### 👉 Join PulseMining: **https://discord.gg/BKFaXmZ2Az**

---

## Status & disclaimer

PBC is **pre-launch**. No token exists yet, nothing is for sale, and there is no public mainnet. Final network parameters (max supply, emission) are fixed before the genesis block. Nothing in this repository is financial advice or a promise of any return.

## Credits & license

PBC Miner is a fork of [XMRig](https://github.com/xmrig/xmrig), licensed under the **GNU General Public License v3.0** — see [LICENSE](LICENSE). RandomX proof-of-work by [tevador](https://github.com/tevador/RandomX). All original XMRig copyrights remain intact.
