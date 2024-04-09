# MLX_Finetune_mistral7B


## Model

이 문서는 `mistralai/Mistral-7B-Instruct-v0.2` 모델을 미세 조정하기 위한 가이드를 제공합니다. LoRA(Low-Rank Adaptation) 기법을 사용하여 미세 조정을 진행하는 과정을 설명합니다.
- `llama`,`mistral`,`mixtral`,`gguf_llm`,`mlx_llm`, 기타 LLM trask 외에도 다양한 모델이 존재합니다.

## 준비

- macbook m1/m2/m3 노트북 준비
- Python 3.X 이상 설치
- 필요한 Python 라이브러리 설치 (아래 설치 방법 참조)
- 학습, 검증, 테스트 데이터셋 준비 (`train.jsonl`, `valid.jsonl`, `test.jsonl`)

## 셋팅

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

## 데이터셋 준비

학습(`train.jsonl`), 검증(`valid.jsonl`), 테스트(`test.jsonl`) 데이터셋은 data 폴더 내에 위치해야 합니다. 각 파일은 유효한 JSONL 형식을 따라야 하며, 각 라인은 JSON 객체를 포함해야 합니다.
- Hugging Face / AI HuB 를 통해 원하는 Downstream task 를 받아옵니다.
- `train.ipynb` 에 데이터 전처리 코드가 있습니다.
  
