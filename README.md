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

## Open-Source Models — Details

이 섹션은 한국어 TTS 오픈소스 모델들의 **라이선스, 추론 환경, 사용 목적**을 중심으로 정리합니다.  
실제 적용 전에 참고할 수 있도록 **실무 관점**에서 기술합니다.

---

### Supertonic

- **License**
  - Sample Code: MIT License
  - Model Weights: OpenRAIL-M License
    - Commercial use is permitted under the OpenRAIL-M License
    - Use-based (responsible-use) restrictions must be complied with
- **Inference**: CPU / GPU (ONNX)
- **Description**
  - Text-to-Speech model released by Supertone
  - ONNX-based inference examples provided
  - Voice style files provided in JSON format

---

### MMS TTS (kor)

- **License**: CC-BY-NC 4.0
  - ❌ Commercial use not permitted
  - Attribution required
- **Inference**: CPU / GPU
- **Description**
  - Meta MMS (Massively Multilingual Speech) TTS model
  - Korean language support

---

### MeloTTS (ko)

- **License**: MIT License
  - Free for both commercial and non-commercial use
- **Inference**: Fast enough for CPU real-time inference
- **Description**
  - MeloTTS-based Korean TTS model
  - Released by MyShell

---

### RealTime Zero-shot TTS (ko)

- **License**: MIT License
  - Free for both commercial and non-commercial use
- **Inference**: Not specified
- **Description**
  - Zero-shot TTS approach
  - Uses reference audio for target speaker speech generation

---

### Orpheus-3B (ko, Q8)

- **License**: Apache-2.0
  - Free for both commercial and non-commercial use
  - Attribution and license notice required
- **Inference**: Not specified
- **Description**
  - Korean fine-tuned Orpheus-3B model
  - Q8_0 quantized GGUF checkpoint

---

## Benchmarks

Benchmark results depend heavily on hardware, runtime settings, and model configurations.
The following table is intended as a template for future evaluation.

| Model | MOS | Latency | Device | Notes |
|-------|-----|---------|--------|-------|
| Supertonic | TBD | TBD | TBD | |
| MMS TTS (kor) | TBD | TBD | TBD | Non-commercial |
| MeloTTS (ko) | TBD | TBD | TBD | CPU real-time capable |
| RealTime Zero-shot TTS (ko) | TBD | TBD | TBD | Zero-shot |
| Orpheus-3B (ko, Q8) | TBD | TBD | TBD | Quantized |

