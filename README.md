# MLX_Finetune_mistral7B


# Model Training Guide

이 문서는 `mistralai/Mistral-7B-Instruct-v0.2` 모델을 미세 조정하기 위한 가이드를 제공합니다. LoRA(Low-Rank Adaptation) 기법을 사용하여 미세 조정을 진행하는 과정을 설명합니다.

## Prerequisites
- macbook m1/m2/m3 노트북 준비
- Python 3.X 이상 설치
- 필요한 Python 라이브러리 설치 (아래 설치 방법 참조)
- 학습, 검증, 테스트 데이터셋 준비 (`train.jsonl`, `valid.jsonl`, `test.jsonl`)

## Installation

필요한 Python 패키지를 설치하기 위해, 아래 단계를 따르세요:

[MLX 프레임워크 설치](https://github.com/ml-explore)
```bash
pip install mlx
```
mlx-examples git clone 해오기
```bash
git clone https://github.com/ml-explore/mlx-examples
```
1. `mlx-examples` 디렉토리로 이동:

```bash
cd mlx-examples
```
2. `LoRA` 디렉토리로 이동후 필요한 라이브러리 설치 :
```bash
cd lora
pip install -r requirements.txt
```
