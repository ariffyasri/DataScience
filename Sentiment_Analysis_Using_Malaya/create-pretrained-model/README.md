## Files needed:
* tokenization.py 

    - https://github.com/google-research/bert/blob/master/tokenization.py
    - https://github.com/google-research/electra/blob/master/model/tokenization.py
    - https://github.com/huseinzol05/Malaya/blob/dc2160711625740573b5feb48d9d970dc704e763/pretrained-model/bert/tokenization.py

* optimization.py
    - https://github.com/google-research/electra/blob/master/model/optimization.py

* modeling.py
    - https://github.com/huseinzol05/Malaya/blob/99dcd5f154f737b7a7a289fda8fcbf167292c0dc/malaya/transformers/electra/modeling.py
    - https://github.com/google-research/electra/blob/master/model/modeling.py

* custom_optimization.py
    - https://github.com/huseinzol05/Malaya/blob/dc2160711625740573b5feb48d9d970dc704e763/pretrained-model/bert/custom_optimization.py

* create_pretraining_data.py
    - https://github.com/huseinzol05/Malaya/blob/dc2160711625740573b5feb48d9d970dc704e763/pretrained-model/bert/create_pretraining_data.py

* BASE_config.json
    - https://raw.githubusercontent.com/huseinzol05/Malaya/dc2160711625740573b5feb48d9d970dc704e763/pretrained-model/bert/config/BASE_config.json

## Steps:

* 1-build-wordpiece.ipynb
* 2-create-pretraining-data.py
    - ```properties
        python 2-create-pretraining-data.py
        ```
* 3-multigpu_pretraining.py
    - ```properties
        python 3-multigpu_pretraining.py --input_file=tfrecord/bert-*.tfrecord --output_dir=pretraining_output --do_train=True --do_eval=False --bert_config_file=config/BASE_config.json --train_batch_size=150 --max_seq_length=128 --max_predictions_per_seq=20 --num_train_steps=1000000 --num_warmup_steps=10 --learning_rate=2e-5 --save_checkpoints_steps=200000 --use_gpu=True --num_gpu_cores=1 --eval_batch_size=12
        ```
