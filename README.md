# Bazm — Independently Benchmarking Small Language Models as Tool-Using Agents

Bazm is a small, opinionated benchmark built to particularly test **small language models (SLMs)** as **agents that can act**.

We care about models that can:
- run on low-to-mid machines,
- follow tool APIs (any format that's defined by user at runtime) reliably,
- and actually *do things* under these tight constraints.

In simple words: Bazm focuses on whether a **3B-parameter model can solve a task with 20 moves without any support.**

---

We wanted a benchmark that:
1. focuses on **tiny models**
2. measures full-on **agentic ability**
3. is transparent enough to discuss openly (ping us up for anything about this.)
4. isn’t already part of or baked into someone's training dataset
5. doesn’t assume cloud GPUs or large GPU home computers.

This is a long-term community effort, we'll iterate based on feedback.  
Right now it’s simple by design.

Our goal is simple:
1. Just open a page
2. Pick a weight class (Check which ones below)
3. Check out the best performing model at the top if you want to use / build something agentic.
4. Search for a specific model and its current ranking if you want to see one of em.
5. Discuss with the people doing the benchmarks so you can suggest improvements, challenge their methodology, give your own set of data / evidence to suggest otherwise and anything else.

---

## 🔍 What Bazm Measures

| Capability | Description |
|-----------|-------------|
| **Action Efficiency** | Can the model solve tasks within strict step limits? |
| **Custom Tool API reliability** | Does it stick to the API user gives instead of reverting to default training biases? |
| **Short-Term Planning** | Does it recover from mistakes or loop forever? |
| **Agent-style Reasoning** | Action guided by reasoning |

All models are evaluated under same constraints.

---

## 🧪 Evaluation Setup (Summary)

| Aspect | Specification |
|--------|--------------|
| Environment | TextWorld |
| Episodes per model | 30 |
| Step budget | 20 steps/episode |
| Command validation | Regex-based |
| Hardware | Local low-VRAM setup (baseline focused on accessibility) |

---

## 🏆 Leaderboard

The current results and ranking are published at:

### 🔗 **https://adapt-robotics.github.io/Bazm**

This page includes:
- Model-wise performance
- Success rates
- Efficiency metrics
- Notes and evaluation logs

We currently categorize by model size:
- **<1B**
- **2B–5B**
- **6B–10B**
- (not focusing on >10B yet — they already have enough attention)

Results are updated continuously as new models are tested.

---

## 🗣 Contributing
Suggest a model, ask questions, or challenge the methodology:

→ Open an Issue:  
https://github.com/Adapt-Robotics/Bazm/issues

We’ll open contributions once the pipeline stabilizes.

---

## 📜 License

This benchmark is released under the **MIT License**.

---

**© 2025 Adapt Robotics — because small models are cool too.**


