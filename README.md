### LoRA Fine-Tuning: Qwen2.5-0.5B on Alpaca

* Fine-tuned **Qwen2.5-0.5B** using LoRA, targeting the `q_proj` and `v_proj` layers with `r=8`. Only about **0.11% of the model parameters** were trained.
* Used **1,000 Alpaca examples** for training and kept **100 separate examples** for testing.
* After **2 epochs (250 training steps)** on a free Google Colab T4 GPU, test loss decreased from **2.02 to 1.71**.
* This was a small practice experiment with a single training run and a limited test set. Although the test loss improved, the generated answers did not consistently improve. Some outputs became repetitive and did not stop cleanly.
* The likely causes are the current loss setup and **greedy decoding**. These issues have not been fixed yet.

