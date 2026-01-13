# Awesome Korean TTS (Local)

한국어를 지원하며, 로컬 환경에서 실행 가능한 TTS(Text-to-Speech) 모델들을 정리한 Awesome 리스트입니다.

> Criteria  
> - 🇰🇷 Korean supported  
> - 🖥️ Runs locally (no mandatory cloud API)  

---

## Contents
- [Overview](#overview)
- [Open-Source Models](#open-source-models)
- [Research / Academic Models](#research--academic-models)
- [Lightweight / Edge Models](#lightweight--edge-models)
- [Commercial but Local SDK](#commercial-but-local-sdk)
- [Toolkits & Frameworks](#toolkits--frameworks)
- [Benchmarks](#benchmarks)
- [Datasets (Korean)](#datasets-korean)

---

## Overview

이 저장소는 다음 조건을 만족하는 TTS 모델만을 수록합니다.

- 한국어 음성 합성이 가능할 것  
- 로컬 PC, 서버, 혹은 엣지 디바이스에서 직접 실행 가능할 것  
- 모델, 코드, 혹은 실행 방식이 공개되어 있을 것  

---

## Open-Source Models

| Name | Language | License | Inference | Link | Notes |
|------|----------|---------|-----------|------|-------|
| Coqui TTS (Korean) | KO | MPL-2.0 | CPU / GPU | link | Multi-speaker |
| VITS-Korean | KO | MIT | GPU | link | Research-based |
| … | | | | | |

---

## Research / Academic Models

- **VITS (Korean fine-tuned)**  
  - Paper:  
  - Code:  
  - 특징: 고품질, 연구 목적  

- **FastSpeech2 (Korean)**  
  - Paper:  
  - Code:  

---

## Lightweight / Edge Models

라즈베리파이, Jetson, 노트북 등에서 실시간 실행이 가능한 모델들

- PicoTTS (Korean fork)  
- Custom ONNX-based TTS  
- …

---

## Commercial but Local SDK

클라우드 API가 아닌, 로컬 SDK 형태로 제공되는 엔진

- Supertonic (Local inference)
- …

---

## Toolkits & Frameworks

- Coqui TTS  
- ESPnet  
- NVIDIA NeMo  
- OpenVoice  
- …

---

## Benchmarks

| Model | MOS | Latency | Device | Notes |
|-------|-----|---------|--------|-------|
| Model A | 4.2 | 120ms | RTX 3060 | |
| Model B | 3.8 | 40ms | CPU | |

---

## Datasets (Korean)

- KSS Dataset  
- Zeroth-Korean  
- AI Hub Speech Dataset  
- …

---