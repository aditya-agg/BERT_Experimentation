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

# To run BERT, BERT Large and BERT with Extra Self Attention Layer
# Run the python notebook as it is, BERT Base model has been uploaded in the repo, you only need to use that if you want to use the BERT Base Model. For Adding Extra Self Attention Layer, you can change the config file, and use the bert_config_extra.json for that, present in uncased_L-12_H-768_A-12/