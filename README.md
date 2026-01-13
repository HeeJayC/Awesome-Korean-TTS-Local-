# Awesome Korean TTS (Local)

한국어를 지원하며, 로컬 환경에서 실행 가능한 TTS(Text-to-Speech) 모델들을 정리한 Awesome 리스트입니다.

> Criteria  
> - 🇰🇷 Korean supported
> - Runs locally (no mandatory cloud API)  

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

| Name | Lang | License | Infer | Link | Notes |
|------|------|---------|-------|------|-------|
| Supertonic | KO | Open | CPU/GPU | [GitHub](https://github.com/supertone-inc/supertonic) | Lightweight local TTS |
| MMS TTS (kor) | KO | Open (NC) | CPU/GPU | [HF](https://huggingface.co/facebook/mms-tts-kor) | Meta MMS Korean TTS model |
| MeloTTS (ko) | KO | Open | CPU | [HF](https://huggingface.co/myshell-ai/MeloTTS-Korean) | Multi-lingual TTS library |
| RealTime Zero-shot TTS (ko) | KO | Open | CPU/GPU | [GitHub](https://github.com/Nyan-SouthKorea/RealTime_zeroshot_TTS_ko) | Zero-shot TTS supporting custom voices |
| Orpheus-3B (ko, Q8) | KO | Open | GPU/Quant | [HF](https://huggingface.co/lex-au/Orpheus-3b-Korean-FT-Q8_0.gguf) | Quantised high-quality TTS |
| Kokoro-82M | Multi (incl. KO) | Apache-2.0 | CPU/GPU | [HF](https://huggingface.co/hexgrad/Kokoro-82M) | Lightweight model family |
| Coqui XTTS-v2 | Multi (incl. KO) | MPL-2.0 | CPU/GPU | [GitHub](https://github.com/coqui-ai/tts) / [HF](https://huggingface.co/coqui/XTTS-v2) | Multi-speaker, Korean support |

## Open-Source Models — Details

이 섹션은 한국어 TTS 오픈소스 모델들의 **라이선스, 추론 환경, 사용 목적**을 중심으로 정리합니다.  
실제 적용 전에 참고할 수 있도록 **실무 관점**에서 기술합니다.

---

### Supertonic

- **License**
  - Sample Code: MIT License
  - Model Weights: OpenRAIL-M License
- **Inference**: CPU / GPU (ONNX)
- **Description**
  - 로컬 실행에 최적화된 경량 TTS 엔진
  - JSON 기반 음성 스타일을 통한 멀티 보이스 지원
  - 스트리밍 및 실시간 TTS 파이프라인 구성에 적합
- **Recommended Use**
  - 로봇, 온프레미스 TTS, 실서비스
- **Notes**
  - 상업적 사용 가능
  - 단, OpenRAIL-M 책임 기반 사용 제한 준수 필요

---

### MMS TTS (kor)

- **License**: CC-BY-NC 4.0
- **Inference**: CPU / GPU
- **Description**
  - Meta MMS 기반 다국어 TTS 모델
  - 한국어 음성 품질이 안정적
- **Recommended Use**
  - 연구, 실험, 데모
- **Notes**
  - ❌ 상업적 사용 불가
  - 출처 명시 필수

---

### MeloTTS (ko)

- **License**: Apache-2.0
- **Inference**: CPU
- **Description**
  - 경량 구조의 다국어 TTS
  - 빠른 추론 속도와 단순한 사용성
- **Recommended Use**
  - 로컬 테스트, 경량 환경
- **Notes**
  - 음질은 최신 대형 모델 대비 보통 수준

---

### RealTime Zero-shot TTS (ko)

- **License**: Open (Non-Commercial 계열, 프로젝트별 상이)
- **Inference**: CPU / GPU
- **Description**
  - Zero-shot TTS 지원
  - 참조 음성을 이용한 커스텀 보이스 생성
- **Recommended Use**
  - 연구, 실험, 음성 클로닝 테스트
- **Notes**
  - 실시간성은 하드웨어 및 설정에 따라 편차 존재
  - 라이선스 세부 조건 확인 필요

---

### Orpheus-3B (ko, Q8)

- **License**: OpenRAIL 계열
- **Inference**: GPU (Quantized)
- **Description**
  - 대형 파라미터 기반 고품질 TTS
  - Q8 양자화를 통한 추론 비용 절감
- **Recommended Use**
  - 고음질 데모, 연구 목적
- **Notes**
  - GPU 필수
  - 실시간 서비스에는 다소 무거움

---

### Kokoro-82M

- **License**: Apache-2.0
- **Inference**: CPU / GPU
- **Description**
  - 비교적 작은 파라미터 수의 경량 모델
  - 다국어 지원 (한국어 포함)
- **Recommended Use**
  - 경량 실험, 엣지 디바이스
- **Notes**
  - 음질은 경량 모델 수준

---

### Coqui XTTS-v2

- **License**: MPL-2.0
- **Inference**: CPU / GPU
- **Description**
  - 멀티스피커 및 Zero-shot TTS 지원
  - 한국어 포함 다국어 음성 합성 가능
- **Recommended Use**
  - 음성 클로닝, 멀티 보이스 실험
- **Notes**
  - 실시간성은 하드웨어 및 설정 영향 큼
  - MPL-2.0 라이선스 조건 확인 필요


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