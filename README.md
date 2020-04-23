# BERT_Experimentation


Command to run the scripts:
  python [run_bert_onlstm.py, run_bert_tcn.py, run_bert_lstm.py] \
    --model_type bert \
    --model_name_or_path bert-base-uncased \
    --do_train \
    --do_eval \
    --version_2_with_negative \
    --train_file PATH_TO_SQUAD2.0_TRAIN_FILE \
    --predict_file ATH_TO_SQUAD2.0_EVAL_FILE \
    --learning_rate 3e-5 \
    --num_train_epochs 4 \
    --max_seq_length 384 \
    --doc_stride 128 \
    --output_dir ./[bert_orig, bert_lstm, bert_onlstm, bert_tcn]/ \
    --per_gpu_eval_batch_size=10  \
    --per_gpu_train_batch_size=10   \
    --save_steps 500 \
    --evaluate_during_training
