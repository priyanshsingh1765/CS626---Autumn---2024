# CS626 Course project
- The project is an implementation and exploration of the research on debiasing in language models as done in the following paper: [Counterfactually Aware Fair Text
 Generation](https://ojs.aaai.org/index.php/AAAI/article/view/29719).
# Research Topic
- The research paper aims to achieve fair and equitable outputs in language models, which tend to be biased due to inherent biases in conventional training datasets.
- The interesting contribution of this specific solution, called "CAFIE" is that it eliminates the need of model-retraining.
- It is an "inference-time framework", that is, it makes the model outputs unbiased during inference.
- It does this by modifying the output probability distribution of the LM over the model training vocabulary, making it unbiased, while also maintainig the language modelling ability of the LM.
# References
- The research paper, published in AAAI-24: [Counterfactually Aware Fair Text Generation](https://ojs.aaai.org/index.php/AAAI/article/view/29719).
- Special thanks to the authors: Pragyan Banerjee, Abhinav Java, Surgan Jandial, Simra Shahid, Shaz Furniturewala, Balaji Krishnamurthy, Sumit Bhatia
- The code for CAFIE was referred to from [Pragyan Banerjee's official github page](https://github.com/banerjeepragyan), the rpository for the same being: [CAFIE](https://github.com/banerjeepragyan/CAFIE).
