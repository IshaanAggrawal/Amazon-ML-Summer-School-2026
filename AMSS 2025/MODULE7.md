<h1 align="center">AMSS 2025 Module 7</h1>
<h2 align="center">Causal Inference</h2>
<h3 align="center">Session Date: Aug 30, 2025</h3>

# Causal Inference: Foundations, Challenges, and Methods

## Introduction
Causal inference is concerned with understanding cause-and-effect relationships. Unlike models that focus only on correlation, it seeks to answer how a treatment or intervention influences an outcome. This topic is central to fields like healthcare, economics, policy, and the social sciences, where the aim is not just prediction but explanation and decision-making.

## Core Concepts and Methodologies

### 1. Motivations and Real-World Questions
- Distinguishing true causes from misleading correlations. For example, higher income is associated with marriage, but marriage itself may not increase income.  
- Business applications such as measuring the true impact of an advertisement on purchase decisions.  
- Public policy questions such as whether reducing the number of firefighters lowers fire incidents, where simple correlations may be misleading.  

### 2. Fundamental Challenges
- **Confounding variables**: Hidden factors affect both the treatment and the outcome, creating false links.  
- **Counterfactuals**: We cannot observe what would have happened under an alternative treatment for the same person.  
- **Selection bias**: When treatment assignment is not random, estimates can be systematically skewed.  

### 3. Frameworks and Assumptions
- **Potential Outcomes Model (Rubin Causal Model)**: Each individual has potential outcomes under different treatments, with the causal effect defined as the difference between them.  
- **Key assumptions**:  
  - Stable Unit Treatment Value Assumption (SUTVA): One individual’s treatment does not influence another’s outcome.  
  - Ignorability: After adjusting for confounders, treatment assignment is independent of potential outcomes.  
  - Positivity: Every individual has a non-zero chance of receiving each treatment.  

When these assumptions fail, bias enters. For example, unmeasured socioeconomic status can confound treatment effects.

## Applications and Future Directions
Causal inference provides the foundation for evaluation in science, policy, and medicine. Classical methods such as **propensity score matching**, **inverse weighting**, and **stratification** remain widely used. Modern approaches use machine learning to improve flexibility and reduce bias in high-dimensional data:  

- Neural network models (TARNet, DragonNet) that learn balanced representations.  
- Causal forests that extend decision trees to estimate heterogeneous effects.  
- Matching and subclassification methods that group individuals by their likelihood of treatment to approximate randomized experiments.  

Open challenges remain, especially when assumptions such as ignorability or positivity are violated. Tools like **instrumental variables**, **synthetic controls**, and new causal discovery methods are being developed to address these issues.

## Summary Table: Key Concepts and Methods

| Aspect | Description | Techniques |
|--------|-------------|------------|
| Goal | Measure how treatments affect outcomes | ATE, CATE, ITE |
| Assumptions | Needed for unbiased estimates | SUTVA, Ignorability, Positivity |
| Challenges | Hidden factors, bias, limited overlap | Sensitivity analysis, instrumental variables |
| Classical Methods | Work with simple confounders | Propensity scores, IPW, Stratification |
| Modern Methods | Handle complex, high-dimensional data | Representation learning, Causal forests, Neural networks |
| Applications | Broad scientific and practical use | Medicine, economics, marketing, policy |

>[!NOTE]
>Causal inference is a vital tool for understanding the world in terms of cause and effect. It moves us beyond correlations to meaningful explanations, helping guide sound decisions. The combination of traditional statistics with modern machine learning has created powerful methods, but the reliability of results always depends on the strength of the underlying assumptions. As research continues, more robust and interpretable tools will shape the future of causal analysis across many fields.