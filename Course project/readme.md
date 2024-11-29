# CS626 Course project
- The project is an implementation and exploration of the research on debiasing in language models as done in the following paper: [Counterfactually Aware Fair Text
 Generation](https://ojs.aaai.org/index.php/AAAI/article/view/29719).
# Research Topic
- The research paper aims to achieve fair and equitable outputs in language models, which tend to be biased due to inherent biases in conventional training datasets.
- The interesting contribution of this specific solution, called "CAFIE" is that it eliminates the need of model-retraining.
- It is an "inference-time framework", that is, it makes the model outputs unbiased during inference.
- It does this by modifying the output probability distribution of the LM over the model training vocabulary, making it unbiased, while also maintainig the language modelling ability of the LM.
# Modifications/Improvements to the solution
## Modification 1 - Extremeness term
- We added a term to the weight calculation that models the "extremeness" of the probability distribution corresponding to each counterfactual context.
- This term helps improve the language modelling ability of CAFIE.
- But a tradeoff we observed was a reduction in the fairness of the model output against an improvement in the language modelling ability.
## Modification 2 - Adding a bias attribute in the Indian context - Caste
- CAFIE can't identify caste based terms as being sensitive, we added a few such terms and evaluated the model with the updated sensitive token list.
-  The caste based tokens and sentences for evaluation were taken from the [IndiBias Dataset](https://github.com/sahoonihar/IndiBias)
-  This dataset was prepared by collaborators from [CFILT IIT Bombay](https://www.cfilt.iitb.ac.in/): Nihar Ranjan Sahoo, Pranamya Prashant Kulkarni, Narjis Asad, Arif Ahmad, Tanu Goyal, Aparna Garimella, Pushpak Bhattacharyya.
-  We observed an overall improvement in CAFIE fairness after updating the list of sensitive tokens
# Results
- Our findings, analysis and improvement results can be found in the presentation for the project.
# References
- The research paper, published in AAAI-24: [Counterfactually Aware Fair Text Generation](https://ojs.aaai.org/index.php/AAAI/article/view/29719).
- Special thanks to the authors: Pragyan Banerjee, Abhinav Java, Surgan Jandial, Simra Shahid, Shaz Furniturewala, Balaji Krishnamurthy, Sumit Bhatia
- The code for CAFIE was referred to from [Pragyan Banerjee's official github page](https://github.com/banerjeepragyan), the repository for the same being: [CAFIE](https://github.com/banerjeepragyan/CAFIE).
