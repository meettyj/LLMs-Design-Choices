# 📘 On The Design Choices of Next Level LLMs

Large Language Models (LLMs) have rapidly evolved across academia, industry, and public life. As the number and diversity of models increase, the design space for building high-performance, generalizable, and efficient LLMs has become more complex and strategically important.

We analyze **31 influential LLMs** developed by **12 leading institutions**, listed alphabetically: `AI2`, `Alibaba`, `Anthropic`, `Apple`, `DeepSeek`, `Google`, `Meta`, `Microsoft`, `Mistral AI`, `Moonshot AI`, `OpenAI`, and `Zhipu AI`. Our focus is to uncover the critical design choices shaping current and next-generation LLMs across three dimensions: model architecture, post-training, and optimization.

We highlight the key **Takeaway** and **Position** across the major LLM design choices, offering insights into prevailing trends and emerging best practices.

# Design Choices on Model Architecture

### 1. What Makes Decoder-only Architectures Dominant?

**Takeaway:** Decoder-only models dominate LLM design because of their ability that unifying tasks through next-token prediction, simplifying architecture for scalability, enabling efficient streaming inference, and aligning naturally with raw-text pre-training.

**Position:** The next leap may come from modular extensions on top of decoder-only models, such as multimodal encoders for perception, simulators or search interfaces for interaction, and encoder-style modules for memory and personalization.

### 2. When to Use Dense or MoE Architectures?

**Takeaway:** Dense models offer strengths such as training stability and ease of deployment, while MoE enable efficient scaling, expert specialization, and resource-aware execution. 

**Position:** Future LLMs can adopt hybrid architectures that integrate a dense core for stable general-purpose capabilities with different expert modules for scalability and specialization.


# Design Choices on Post-Training

### 3. How to Select Task and Data for Post-training?

**Takeaway:** Pretrained LLMs are unlocked to a wide range of tasks during post-training, including reasoning, modeling human preferences, tool use, and multi-modality.

**Position:** Beyond scaling model size and pre-training data, future LLMs will increasingly emphasize task-specific data-centric post-training. This approach aims to equip models with more complex behaviors that are often rare or underrepresented in the pre-training corpus.


### 4. How to Choose Post-training Strategy?

**Takeaway:** Post-training incorporates multiple training strategies and reinforcement learning algorithms, with growing reliance on rejection sampling to enhance capabilities.


**Position:** The future of post-training lies in developing multiple stages that iteratively use diverse strategies, adapting LLMs' behaviors to real-world environments and needs.



### 5. How to Obtain Reward for RL?

**Takeaway:** Reward signal used for reinforcement learning can be obtained from diverse sources, including human preference, rule-based verifications, and AI-generated feedback.


**Position:** The frontier of LLM reward modeling lies in integrating human and AI feedback with automated and verifiable evaluations. Future models should pioneer dynamic, self-improving reward modeling that adapts to new tasks based on user needs and AI capabilities.


# Design Choices on Optimization

### 6. How to Design Prompt Template?

**Takeaway:** Prompt design plays a critical role in LLM training and inference, spanning system prompting, standard prompting, and reasoning prompting.


**Position:** Unifying and systematizing prompt design, across role formatting, and reasoning scaffolds, is critical for advancing LLM reliability and generalization.


### 7. How to Minimize Memory Usage?

**Takeaway:** Memory efficiency in LLMs is achieved through a multifaceted approach involving quantization, efficient attention mechanisms, and memory-saving training tricks.

**Position:** As LLMs continue to scale and diversify in deployment environments, the next frontier in memory optimization lies in designing hardware-aware frameworks that adapt memory-saving strategies based on computational context and task requirements.


### 8. How to Obtain a Smaller Model?

**Takeaway:** Distillation has become the dominant strategy for transferring capabilities and performance from larger LLMs to smaller models. 


**Position:** As the field matures, we envision a layered LLM ecosystem: a few ever-evolving “super teacher” models pushing the boundaries of intelligence, paired with a diverse landscape of compact student models that are distilled and trained for targeted domains and tasks.


### 9. How to Accelerate Training and Inference?

**Takeaway:** Existing methods depend heavily on parallelism strategies and hardware-aware optimizations to accelerate LLM training and inference.


**Position:** The next frontier in LLM acceleration lies in integrating hardware-adaptive parallelism that aligns with model architectures and balances training and inference workloads intelligently across heterogeneous compute resources.



# 🌐 Awesome-LLMs

We list the **31 influential LLMs** covered in the paper, each accompanied by a link to the relevant research paper or blog post.

### 🏢 AI2
- **OLMo 2** [[paper]](https://arxiv.org/pdf/2501.00656)  
- **Tulu 3** [[paper]](https://arxiv.org/pdf/2411.15124)

### 🏢 Alibaba
- **Qwen2** [[paper]](https://arxiv.org/pdf/2407.10671)  
- **Qwen2.5** [[paper]](https://arxiv.org/pdf/2412.15115)
- **Qwen2.5-1M** [[paper]](https://arxiv.org/pdf/2501.15383)  
- **QwQ-32B** [[blog]](https://qwenlm.github.io/blog/qwq-32b/)
- **Qwen3** [[paper]](https://arxiv.org/pdf/2505.09388)

### 🏢 Anthropic
- **Aya 23** [[paper]](https://arxiv.org/pdf/2405.15032)
- **Claude 3** [[paper]](https://www-cdn.anthropic.com/de8ba9b01c9ab7cbabf5c33b80b7bbc618857627/Model_Card_Claude_3.pdf)
- **Claude 4** [[paper]](https://www-cdn.anthropic.com/6be99a52cb68eb70eb9572b4cafad13df32ed995.pdf)

### 🏢 Apple
- **OpenELM** [[paper]](https://arxiv.org/pdf/2404.14619)
- **DCLM** [[paper]](https://arxiv.org/pdf/2406.11794)

### 🏢 DeepSeek
- **DeepSeek-R1** [[paper]](https://arxiv.org/pdf/2501.12948)
- **DeepSeek-V3** [[paper]](https://arxiv.org/pdf/2412.19437)  

### 🏢 Google
- **Gemini 1.0** [[paper]](https://arxiv.org/pdf/2312.11805)
- **Gemini 1.5** [[paper]](https://arxiv.org/pdf/2403.05530) 
- **Gemini 2.0** [[blog]](https://blog.google/technology/google-deepmind/google-gemini-ai-update-december-2024/)
- **Gemini 2.5** [[blog]](https://blog.google/technology/google-deepmind/gemini-model-thinking-updates-march-2025/)
- **Gemma 1** [[paper]](https://arxiv.org/pdf/2403.08295)
- **Gemma 2** [[paper]](https://arxiv.org/pdf/2408.00118)
- **Gemma 3** [[paper]](https://arxiv.org/pdf/2503.19786)

### 🏢 Meta
- **Llama 3** [[paper]](https://arxiv.org/pdf/2407.21783)  
- **Llama 4** [[blog]](https://ai.meta.com/blog/llama-4-multimodal-intelligence/)

### 🏢 Microsoft
- **Phi-3** [[paper]](https://arxiv.org/pdf/2404.14219)
- **Phi-4** [[paper]](https://arxiv.org/pdf/2412.08905)
- **Phi-4-Mini** [[paper]](https://arxiv.org/pdf/2503.01743)

### 🏢 Mistral AI
- **Mistral 7B** [[paper]](https://arxiv.org/pdf/2310.06825) 
- **Mixtral 8x7B** [[paper]](https://arxiv.org/pdf/2401.04088)

### 🏢 Moonshot AI
- **Kimi K1.5** [[paper]](https://arxiv.org/pdf/2501.12599)

### 🏢 OpenAI
- **GPT-4** [[paper]](https://arxiv.org/pdf/2303.08774)

### 🏢 Zhipu AI
- **ChatGLM** [[paper]](https://arxiv.org/pdf/2406.12793)
