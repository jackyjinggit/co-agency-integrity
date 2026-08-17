# co-agency-integrity · 认知免疫工具包

**The cognitive immune system for human–AI co-agency.**

> 中文名：**认知免疫工具包** —— 一组用于在人–AI 共演中检测认知腐败（隐喻劫持、谄媚回音 FEE、价值高估、治理漂移）的可移植技能。英文 `co-agency-integrity` 保留作仓库锚名。

Everyone is shipping agent frameworks — orchestration, routing, role-playing,
multi-agent parliaments. Almost nobody is shipping the layer that stops your
AI from quietly becoming a yes-man.

This repo is a small, portable toolkit of four skills that catch the three
failure modes of human–AI *co-performance*:

| Failure mode | What goes wrong | Skill |
|---|---|---|
| Structural capture | Power metaphors (commander/soldier, parent/child, master/apprentice) silently rewrite the real collaboration into a hierarchy that was never agreed. | `metaphor-power-audit` |
| Sycophancy echo (FEE) | The AI co-signs your self-narrative, softens hard truths into agreement, and the "challenge" was never real. | `autoethnography-peer-review` |
| Value inflation | You (or the system) over-credit outcomes — counting activity as impact, ignoring effect. | `audit-quantification` |
| Governance drift | A council convenes without loading its method, skips quorum, or quietly grabs authority it was not given. | `governance-precheck` |

It is deliberately **not** another agent framework. It is the hygiene layer you
run *on top of* whatever framework you already use. See [`docs/WHY.md`](docs/WHY.md)
for the full thesis.

## What's inside

```
co-agency-integrity/
├── README.md
├── LICENSE
├── docs/
│   ├── WHY.md                 # the anti-sycophancy thesis
│   └── SELF-TEST.md           # pre-push run of every skill (proof it runs)
├── skills/
│   ├── metaphor-power-audit/      # audit power metaphors in any collaboration
│   ├── autoethnography-peer-review/  # independent blind review of co-produced output
│   ├── audit-quantification/      # IPOE model + gold-standard 0–4 gate
│   ├── governance-precheck/       # pre-flight gate before any multi-agent council
│   └── council-method/            # the generic SOP governance-precheck loads
└── examples/
    ├── metaphor-audit-example.md
    └── peer-review-example.md
```

## Install

These are [Agent Skills](https://docs.anthropic.com/en/docs/agent-skills) /
WorkBuddy-style `SKILL.md` packages. Copy any `skills/<name>/` folder into your
agent's skills directory (e.g. `~/.workbuddy/skills/` or your platform's
equivalent). No code, no API calls, no dependencies — pure method.

## Who it's for

- Builders running a long-lived AI collaborator and worried it's drifting into
  agreement rather than partnership.
- Researchers doing self-ethnography / human–AI interaction studies who need a
  repeatable dissent check.
- Teams standing up multi-agent councils who want a pre-flight gate, not a
  post-mortem.

## Provenance & Originality

- **First public release:** 2026-08-17 by Jiang Ping (蒋平).
- **Origin:** Extracted and de-personalized from the author's private PDSS
  (Protocol-Driven Symbiosis System) research on the cognitive immune system
  for human–AI co-agency. The bundled methods (metaphor-power-audit,
  FEE peer-review, IPOE quantification) were developed independently by the
  author prior to this release.
- **Authoritative prior-art anchor:** The companion paper *FEE v3.4*
  (Flattering-Echo Effect) is deposited on OSF with a DOI and server timestamp.
  That academic record — not this repo — is the canonical originality evidence.
- **Timestamp evidence (C — domestic TSA, landed):** the `v0.1.0` release
  snapshot `co-agency-integrity_v0.1.0_stampbundle.zip` (SHA-256
  `1af632dbe8b0678c2dc43f83318fc6156bc511721fc7769c693c6f1736288217`)
  is stamped by **China TSA (China Time-Stamp Authority — the national
  time-stamp root) via Unitrust (联合信任)** at `2026-08-17 18:20:23 +08:00`,
  as an RFC 3161 TimeStampToken (signer: China TSA-2). Cryptographic
  verification: parse the bundled `.tsa` with `openssl asn1parse -inform DER`;
  the `TSTInfo.MessageImprint` digest equals the zip's SHA-256 **exactly**,
  and `GeneralizedTime = 202608171820235Z`. The certificate bundle
  (`co-agency-integrity_v0.1.0_stampbundle.zip_可信时间戳证书.zip`, containing
  `.tsa` + `.pdf`) and the stamped zip MUST be kept together, unmodified —
  this is what makes the evidence verifiable later. This proves *expression*
  precedence at a fixed moment; it does **not** protect the underlying
  methods/ideas from re-expression by others.
- **Decentralized anchor (B — OpenTimestamps, optional, still pending):** a
  Bitcoin anchor via [OpenTimestamps](https://opentimestamps.org) remains
  **pending** — the local client hit a Windows/Python-3.13 runtime-library
  load error (`find_library` returns `None`; same root cause as the Chrome SxS
  issue). To complete: install the VC++ 2022 redistributable (or run on
  Linux/macOS), then `ots stamp ...` and commit the `.ots` files.

This toolkit is MIT-licensed — reuse freely with attribution. The *ideas* are
prior art the author claims; copyright protects **expression, not method**, so
we lead with first-mover narrative and continued output, not lock-down.

## License

MIT — see [`LICENSE`](LICENSE).
