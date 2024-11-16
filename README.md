# nlp_LoRA
LLM finetuning

## 과제 overview

### Fine-tuning

- **Q1**: `meta-llama/Llama-3.2-1B-Instruct` 모델을 사용하여 미세 조정 수행
- **Q2**: 2,800개의 샘플만을 미세 조정에 사용, 나머지 200개는 검증에 사용
    - 제공된 `llm-modeling-lab.jsonl` 파일에서 데이터를 분리
- **Q3**: 미세 조정된 LoRA 어댑터를 Hugging Face Hub에 업로드하고 모델 ID를 기록
    - Hugging Face Hub의 API를 사용하여 업로드

### Validation
- **Q4**: Hugging Face Hub에서 업로드한 어댑터 모델을 로드
- **Q5**: 검증 세트와 생성된 출력 간의 BLEU 점수를 sacrebleu 라이브러리를 사용하여 계산
