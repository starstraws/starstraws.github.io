---
layout: page
title: Projects
permalink: /projects/
description: Engineering projects in speech processing and speaker verification.
nav: true
nav_order: 3
---

## Telecom service conversation transcription

*October 2026 – present · In progress*

**Background.** Service-counter recordings contain nearby conversations and non-speech intervals. On-site service recordings face variable environmental noise. The task requires extracting business-related dialogue and associating it with speakers, service roles, and timestamps.

**Approach.** Designed two processing pipelines. Service-counter recordings pass through FSMN-VAD and an audio-language model for transcription and contextual reconstruction. On-site recordings first use FRCRN speech enhancement, followed by FSMN-VAD and audio-language model transcription. Context supports business-dialogue selection and employee/customer role inference, while ambiguous segments are marked for review.

**Current outcome.** Built a prototype with speaker-annotated transcripts and organized business text. It retains raw transcriptions, segment start and end times, and speaker IDs for timestamp-based audio verification. Validation on real recordings and local deployment debugging are ongoing.

---

## Speaker verification for a maritime video and audio platform

*Zhenjiang Maritime Safety Administration · May 2023 – May 2024*

**Background.** Maritime enforcement recordings contain wind, waves, and other environmental noise. Speaker verification must handle distorted voice features and limited identity-labeled data.

**Contribution.** Participated in speaker verification scheme design. MFCC and ResNet-18 extract audio features. Speed perturbation and added noise create augmented samples for self-supervised pretraining with a MoCo negative-sample queue, momentum encoder, and InfoNCE loss. Word2Vec encodes textual voice attributes, which are fused with audio features by element-wise multiplication. The pretrained backbone is frozen for downstream MLP training with speaker labels. Cosine similarity and a threshold support same-speaker decisions.

**Outcome.** The scheme produces similarity scores and same-speaker decisions for pairs of recordings. Pretraining uses unlabeled audio, with speaker labels used for downstream training.

**Granted invention patent.** 一种基于动量对比学习的声纹识别方法和设备  
*A speaker recognition method and device based on momentum contrastive learning*  
Patent number: **ZL202311463284.3**.
