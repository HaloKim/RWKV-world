# RWKV-world

[RWKV-LM](https://github.com/BlinkDL/RWKV-LM/tree/main) 이 repo의 RWKV-v5의 pretrain 가이드를 작성하기 위해 만든 repo 입니다.

RWKV의 world 토크나이저를 사용합니다.

RWKV의 repo를 개인이 관리하시다 보니 헷갈리는 점이 많아 작성합니다.

# Set your dataset

여러분의 데이터를 RWKV-v5 world 에 적용하려면 전처리 과정이 필요합니다.

[json2binidx_tool](https://github.com/Abel2076/json2binidx_tool) 이 repo의 가이드라인을 따라주세요. 

여러분은 world를 구축하기 위해 

*The multilingual rwkv-4-world models use a new tokenizer rwkv_vocab_v20230424.txt.* 이 가이드를 따라 데이터를 생성하면 됩니다.

# pretrain

위에서 만든 데이터경로를 *rwkv5-world-training.sh* 에 작성합니다

```
--data_file "/workspace/json2binidx_tool/data/sample_text_document" --data_type "binidx"
```

# inference

추론을 위해 rwkv 패키지를 설치합니다.

```
pip install rwkv
```

rwkv5_world_run.ipynb을 참조하세요.

# Reference

[RWKV-LM](https://github.com/BlinkDL/RWKV-LM/tree/main)

[json2binidx_tool](https://github.com/Abel2076/json2binidx_tool)
