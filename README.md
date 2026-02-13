# ⛧ EREBUS v1.1 — Primordial Auditor of Code and Claims

> "If you cannot prove it, it perishes. But if the evidence is insufficient, it is not destruction — it is suspension."

**EREBUS** is a system prompt that transforms any LLM into an uncompromising code auditor with built-in false positive protection. Unlike typical "review my code" prompts, EREBUS enforces **evidence-based verdicts** — it cannot reject your code on vibes alone.

## Why EREBUS?

Most AI code review prompts fall into two traps:

| Trap | What happens |
|---|---|
| **Too soft** | "Looks good! Maybe consider..." — misses real bugs |
| **Too harsh** | "REJECT EVERYTHING" — wastes your time on non-issues |

EREBUS solves both with a **structured evidence system**:

- 🔴 Can't reject without **hard evidence** (logs, reproduction steps, code references)
- 🟠 Uncertain? It says **HOLD**, not REJECT
- ✅ Must state **what would change the verdict** (flip conditions)

## Core Architecture

### Evidence Tiers
| Tier | Name | What counts | Can REJECT? |
|---|---|---|---|
| **A** | HARD | Raw logs + reproduction + code line + counter-test | ✅ Yes |
| **B** | SOFT | Static analysis + docs + code reference (no repro) | ❌ CONDITIONAL only |
| **C** | HEURISTIC | "Seems plausible," pattern matching, gut feeling | ❌ HOLD only |

### The 12 Seals

Every piece of code is judged against 12 unbreakable seals:

| # | Seal | What it checks |
|---|---|---|
| 0 | Existential Justification | "Why does this need to exist?" |
| 1 | Causal Chain | Evidence → Cause → Change → Elimination → Proof |
| 2 | Temporal Dominion | Timing/performance measurement integrity |
| 3 | Bidirectional Verification | Positive + Negative + Inverse tests |
| 4 | Dead Code Necromancy | Unused code = contamination |
| 5 | Survival Instinct | AI self-preservation pattern detection |
| 6 | Observer Effect | "Works only in testing" detection |
| 7 | Hallucination Gate | Non-existent API/flag/protocol detection |
| 8 | Supply Chain Audit | Dependency security verification |
| 9 | Entropy Analysis | Complexity → bug density correlation |
| 10 | Failure Prophecy | Catastrophic failure path analysis |
| 11 | Petrification Test | Graceful degradation under dependency failure |

### Verdict System
```
⛧ ANNIHILATE  — Malice/backdoor proven at Tier-A
🔴 REJECT      — Tier-A evidence + Seal violation
🟠 HOLD        — Insufficient evidence (DEFAULT)
🟡 CONDITIONAL — Minor issues, fixable
✅ VERIFIED    — All 12 Seals passed
```

### False Positive Controls (6 Rules)

This is what makes EREBUS unique. Most "strict" prompts just reject everything. EREBUS has **6 built-in safety rules** to prevent over-rejection:

1. **Evidence Tiers** — Can't REJECT on gut feeling
2. **Escalation Ladder** — Default is HOLD, not REJECT
3. **Alternative Hypothesis Gate** — Must consider other explanations before REJECT
4. **Flip Conditions** — Must state what would reverse the verdict
5. **Sample/Time Limits** — Can't REJECT on insufficient data
6. **Prescription Exception** — Verdicts must not block practical work

## Usage

### With Claude
Paste the entire prompt as your **system prompt** or first message, then submit your code.

### With ChatGPT
Use it as a **Custom Instruction** or paste at the start of conversation.

### With any LLM
Works with any model that supports system prompts. Tested with Claude 3.5/4, GPT-4o, and Gemini.

## Example Output

```
═══ SEAL 3: BIDIRECTIONAL VERIFICATION ═══
Evidence: Tier-B — Unit tests exist (positive path only). 
  No negative tests found. Inverse test: not applicable.
Verdict: 🟡 CONDITIONAL
Flip condition: Submit negative test for error propagation 
  path → upgrades to ✅ VERIFIED
```

## Origin Story

Built during a Solana AI Agent Hackathon where 3 AI agents wrote 28,000+ lines of production Rust code. When AI writes your code, you need AI to audit it — but standard "review this code" prompts either miss real bugs or cry wolf on everything.

EREBUS was born from the realization that **the real problem isn't making AI strict enough — it's preventing AI from being strict about the wrong things.**

## Languages

- 🇰🇷 [Korean (Original)](erebus_primordial_auditor.md)
- 🇺🇸 [English](erebus_primordial_auditor_EN.md)

## License

MIT — Use it, modify it, make it your own. If you build something cool with it, let me know.

---

*Named after Erebus (Ἔρεβος) — the primordial deity of darkness in Greek mythology. Because your code's flaws cannot hide in the dark when darkness itself is the auditor.*

