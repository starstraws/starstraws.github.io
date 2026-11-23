---
layout: page
title: Research
permalink: /research/
description: Research in audio-language models and telecom fraud detection.
nav: true
nav_order: 2
---

## Audio-language models for telecom fraud detection

*September 2025 – September 2026*

**Background.** Spoken content is central to telecom fraud detection. Pauses, speaking rate, and accent can provide complementary evidence, but existing audio-language models may not use semantic and acoustic information effectively. Detailed acoustic annotation is also costly.

**Approach.** Built separate semantic and acoustic pathways. Fixed-Length Query Adapters (FLQ-Adapters) aggregate variable-length features into fixed-length token sequences for joint reasoning in a language model. Constructed ParaScam with synthetic audio, transcripts, and delivery-enriched scripts. Role-specific alignment first uses transcript-informed teacher analyses to align the semantic pathway, then freezes its adapter and trains the acoustic pathway using teacher analyses enriched with acoustic descriptions.

**Results.** On TeleAntiFraud, fraud-detection weighted F1 reached **98.13%**, with **88.61%** average weighted F1 across three tasks. With 500 labeled calls for downstream adaptation, fraud-type weighted F1 improved by **27.37 percentage points** over the semantic-only variant.

