# QLoRA-Fine-Tuning-of-Open-Sourced-LLMs

Fine tuning open sourced LLMs like llama, gemma, qwen, etc using QLoRA technique using huggingface ecosystem of libraries

## TODO:

1. Run fine tuning using mixed precision (bfloat16). Currently not able to perform, as colab and kaggle notebook gpus don't support bf16 natively
2. Reduce memory requirements of fine tuning further somehow. Some techniques to explore:-
   - use qlora
   - reduce batch size, use gradient accumulation
   - enable gradient checkpointing
   - use mixed precision training
   - keep clearing cache regularly during training
   - optimize the dataloader, load batch in memory when needed, store in storage otherwise
   - don't perform evaluation during training, limit the logging
