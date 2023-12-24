# Awesome-LLM-Prune
Awesome list for LLM pruning. I will comment over the following paper once I really got the idea. Please leave comments on issue once you are interested. 

- LLM-KICK: COMPRESSING LLMS: THE TRUTH IS RARELY PURE AND NEVER SIMPLE
    - Author: Ajay Jaiswal, Zhe Gan, etc
    - Link: https://arxiv.org/pdf/2310.01382.pdf
    - Code: Not available
    - Pub: Arxiv
    - Summary: Re-define the evaluation protocol for compressed LLMs; Observation: SoTA Pruning methods suffer significant performance degradation, despite negligible changes in perplexity. SoTA Pruning do not work well for N:M structured pruning. Quantization methods are more successful.
    - Comment: This paper question the performance of LLM after pruning, which provide us a new perspective besides pure perplexity
- PRUNING LARGE LANGUAGE MODELS VIA ACCURACY PREDICTOR
    - Author: Yupeng Ji, Yibo Cao, Jiucai Liu 
    - Link: https://arxiv.org/pdf/2309.09507.pdf 
    - Code: Not available 
    - Pub: Arxiv 
    - Summary: Formulate the pruning LLM as NAS problem. The search space is the prunining ratio, layer type, etc. By utilizing GBDT accuracy predictor, this paper take the layer-wise importance as input and predict the PPL. 
    - Comment: With 525 architecture-accuracy pair, this paper train the GBDT with 7:3 ratio. 
- LLM-Pruner: On the Strucutal Pruning of Large Language Models 
    - Author: Xinyin Ma, Gongfan Fang, Xinchao Wang 
    - Link: https://arxiv.org/pdf/2305.11627.pdf 
    - Code: https://github.com/horseee/LLM-Pruner
    - Pub: NeurIPS 2023 
    - Summary: This paper endeavor find the copuled structures (Dependency Graph) in LLaMA and proposed Groupded Importance Estimation like Vector-wise, Element-wise, and Group Importance. 
    - Comment: Impressive work. This work is similar to MMRazor, which can handle CNN-based model. 
- SparseGPT: Massive Language Models Can be Accurately Pruned in One-shot 
    - Author: Elias Frantar, Dan Alistarh
    - Link: https://arxiv.org/pdf/2301.00774.pdf 
    - Code: https://github.com/IST-DASLab/sparsegpt 
    - Pub: ICML 2023
    - Summary: First to prune GPT with at least 50% sparsity without any training. SparseGPT is entirely local, which only focus on weight updates without any global gradient information. 
    - Comment: TBD 
- The Emergence of Essential Sparsity in Large Pre-trained Models: The Weights that Matter
    - Author: Ajay Jaiswal, Shiwei Liu, Tianlong Chen, Zhangyang Wang
    - Link: https://arxiv.org/pdf/2306.03805.pdf
    - Code: https://github.com/VITA-Group/essential_sparsity
    - Pub: NeurIPS 2023 
    - Summary: This paper propose the existence of – “essential sparsity” defined with a sharp dropping point beyond which the performance declines much faster w.r.t the rise of sparsity level, when we directly remove weights with the smallest magnitudes in one-shot.
    - Comment: TBD 
- Wanda: A SIMPLE AND EFFECTIVE PRUNING APPROACH FOR LARGE LANGUAGE MODELS
    - Author: Mingjie Sun, Zhuang Liu, Anna Bair, etc.
    - Link: https://arxiv.org/pdf/2306.11695.pdf 
    - Code: https://github.com/locuslab/wanda
    - Pub: Arxiv 
    - Summary: 

- COMPRESSO: STRUCTURED PRUNING WITH COLLABORATIVE PROMPTING LEARNS COMPACT LARGE LANGUAGE MODELS
    - Author: Song Guo, Jiahang Xu, Li Lyna Zhang, Mao Yang 
    - Link: https://arxiv.org/pdf/2310.05015.pdf 
    - Code: https://github.com/microsoft/Moonlit/tree/main/Compresso
    - Pub: Under Review 
    - Summary: Combing instruction tuning with training-based Pruning. LoRA is incorporated to achieve memory-efficient. Collaborative pruning prompt encourage LLMs to better align with the pruning algorithm. 
    - Comment: The prompt is really interesting, which is "Attention! LLM".
- The Truth is in There: Improving Reasoning in Language Models with Layer-Selective Rank Reduction
	- Author: Pratyusha Sharma, Jordan T. Ash, Dipendra Misra 
	- Link: https://arxiv.org/pdf/2312.13558.pdf 
	- Code: Not available 
	- Pub: ICLR Under review 
	- Summary: This paper is not related to Pruning but to Low-rank decomposition. They find that removing higher-order component of weight matrics in MLP and attention can significantly improve the performance of LLMs. 