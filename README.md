# Cross-Architecture Knowledge Distillation
Can We **Induce Desirable Properties** into Models via Cross-Architecture Knowledge Distillation?
Authors: Muhammad Huraira Anwer, Adeen Ali Khan – LUMS, Pakistan

## 🚀 Overview
In this project, we explored whether key inductive biases (like **shape bias, locality, and permutation invariance**) can be transferred across different neural network architectures using knowledge distillation (KD).

More specifically, we focused on distilling attention-based Vision Transformers (**ViT**) into convolutional models (**CNNs**) and vice versa—something that's rarely studied. Our goal was to see not just if performance transfers, but if model behavior and biases do too.

## 🎯 Objectives
We structured our work around three guiding questions:

Can **architectural biases** (e.g., shape, texture, locality) be **transferred** through KD across ViTs and CNNs?

Do **transformer properties** like permutation invariance **survive** in student CNNs?

How do various **distillation methods** affect the **efficiency** and behavior of students under noisy and perturbed inputs?

## Contributions
We created custom test datasets with stylized textures, scrambled patches, and added noise to stress-test learned biases.

We designed two major pipelines:

**CNN ➡️ ViT** Distillation using methods like Cumulative Spatial Knowledge Distillation (**CSKD**) and Visual Linguistic Feature Knowledge Distillation (**VLFKD**).

**ViT ➡️ CNN** Distillation using methods like Contrastive Representation Distillation (**CRD**), Self Supervised Knowledge Distillation (**SSKD**), and Cross Architecture Projection Distillation (**CAPD**).

To control compute costs, all models were trained on **CIFAR-10** under limited epochs (≤ **5**).

We evaluated each model on accuracy as well as **bias metrics** that quantify model reliance on texture, shape, or global structure.

### 🔍 Key Design Decisions
Separate distillation methods were chosen based on architecture direction (CNN-to-ViT vs ViT-to-CNN), due to incompatible feature representations.

We used **baseline** "independent" models (trained without a teacher) to judge how much actual knowledge was transferred.

We explicitly limited training epochs to simulate low-compute deployment settings, emphasizing **practical feasibility** over perfect accuracy.

## Highlights & Insights
### CNN ➡️ ViT
**CSKD** emerged as the most efficient and effective method, excelling in transferring texture bias and noise robustness.

However, ViTs struggled to inherit CNN's locality bias, and improvements over the independent baseline were mild.

Suggests CNNs may be **inherently less effective** as teachers for behavior-focused distillation.

### ViT ➡️ CNN
**CRD** and **SSKD** were both effective at instilling shape bias and permutation invariance into student CNNs.

The improvements were significant compared to the independent baseline—highlighting the power of ViTs as behavior-rich teachers.

Despite higher compute costs, these methods offer promising robustness gains for real-world deployment.

## Limitations
We operated under strict training budgets (≤ 5 epochs), which likely capped the full potential of the distillation methods.

Some methods like CAPD underperformed simply because they didn’t converge under such limited training.

Future work should explore:

Longer training schedules

Broader datasets

Mechanisms to avoid **over-distilling undesirable properties** (e.g., ViT’s weak texture awareness into CNNs)

## 💡 Takeaways
**ViT**s make **powerful teachers**, capable of transferring abstract, global properties like permutation invariance.

**CNN**s are **efficient learners**, but might struggle to adopt attention-like behaviors unless the method is designed very carefully.

Cross-architecture KD isn't just viable—it can yield more robust, generalizable models when done thoughtfully.


## 📚 References

- **CRD**: Tian, Y., Krishnan, D., & Isola, P. (2019). *Contrastive Representation Distillation*. [arXiv:1910.10699](https://arxiv.org/abs/1910.10699)
- **CSKD**: Zhao, B., Song, R., & Liang, J. (2023). *Cumulative Spatial Knowledge Distillation for Vision Transformers*. [arXiv:2307.08500](https://arxiv.org/abs/2307.08500)
- **SSKD**: Xu, G., Liu, Z., Li, X., & Loy, C. C. (2020). *Knowledge Distillation Meets Self-Supervision*. [arXiv:2006.07114](https://arxiv.org/abs/2006.07114)
- **CAPD**: Liu, Y., Cao, J., Li, B., Hu, W., Ding, J., & Li, L. (2022). *Cross-Architecture Knowledge Distillation*. [arXiv:2207.05273](https://arxiv.org/abs/2207.05273)
- **VLFKD**: Zheng, X., Luo, Y., Zhou, P., & Wang, L. (2023). *Distilling Efficient Vision Transformers from CNNs for Semantic Segmentation*. [arXiv:2310.07265](https://arxiv.org/abs/2310.07265)

---
