
# Evaluating the Accuracy–Security–Performance Trade-offs in Non-Interactive Secure Transformer Inference

## Project Information

- **Course:** Cryptography
- **Project Type:** Research and Implementation
- **Team Members:**
  - Khushboo Pandey
  - Dhruv

## About the Project

In this project, we are studying how Transformer models can be used while keeping input data private. We are focusing on a research paper called **"NEXUS: Secure Transformer Inference Made Non-interactive."**

Normally, when someone uses a machine learning model through a remote service, they need to send their input to the server. This can create privacy concerns because the server may be able to see the user's data.

One possible solution is Homomorphic Encryption (HE). It allows certain computations to be performed on encrypted data without first decrypting it.

Our goal is to understand the techniques used in the NEXUS paper and build a small prototype to explore the trade-offs between accuracy, security, and performance.

We are not trying to reproduce the complete NEXUS system. Instead, we will focus on selected operations that we can implement and evaluate within the time and resources available for this course.

## Project Objectives

Through this project, we want to:

- Understand how Homomorphic Encryption works.
- Learn about the CKKS encryption scheme and its use in machine learning.
- Study the security model and design of the NEXUS paper.
- Compare normal Transformer inference with selected encrypted computations.
- Measure the effect of encryption on accuracy and performance.
- Understand the limitations of using Homomorphic Encryption for Transformer inference.

## Our Approach

We plan to work on the project in the following stages.

### 1. Understand the Research Paper

We will first study the NEXUS paper to understand:

- The problem it is trying to solve.
- How non-interactive secure inference works.
- The role of Homomorphic Encryption.
- The security assumptions and limitations.
- The performance improvements discussed in the paper.

### 2. Set Up the Environment

We will set up the required tools and libraries on our local machines.

Our initial tools include:

- Python
- OpenFHE
- PyTorch
- Hugging Face Transformers
- Jupyter Notebook
- Git and GitHub

We will start with local CPU-based experiments and consider cloud resources only if needed.

### 3. Build a Plaintext Baseline

Before implementing encrypted computations, we will run a Transformer model without encryption.

We are considering DistilBERT fine-tuned on the SST-2 sentiment classification dataset.

This will give us a baseline for:
- Model accuracy
- Inference time
- Memory usage

### 4. Explore Homomorphic Encryption

We will study and experiment with the CKKS encryption scheme using OpenFHE.

We will explore how selected computations can be performed on encrypted values and understand the effect of encryption parameters on the results.

### 5. Implement a Small Prototype

We will try to implement selected encrypted operations related to Transformer inference.

The exact implementation scope will depend on what we can successfully support with the available libraries and resources.

We will clearly document which operations are encrypted and which operations, if any, are performed in plaintext.

### 6. Run Experiments

We will compare the plaintext baseline with our encrypted prototype.

The measurements we plan to collect include:

- Accuracy and numerical error
- Inference or computation time
- Encryption and decryption time
- Memory usage
- Ciphertext size
- Impact of different CKKS parameters

### 7. Analyze the Results

Finally, we will study the results and discuss the trade-offs between accuracy, security, and performance.

We will also document implementation challenges and limitations.

## Tools and Technologies

| Tool | Purpose |
|---|---|
| Python | Main programming language |
| OpenFHE | Homomorphic Encryption experiments |
| PyTorch | Machine learning framework |
| Hugging Face Transformers | Pretrained Transformer models |
| DistilBERT | Candidate model for sentiment classification |
| SST-2 | Sentiment classification dataset |
| Jupyter Notebook | Experiments and analysis |
| GitHub | Version control and collaboration |

## Team Responsibilities

### Khushboo Pandey

- Set up the project repository and development environment.
- Explore the NEXUS implementation and its dependencies.
- Work on the OpenFHE and CKKS experiments.
- Implement selected encrypted computations.
- Measure encryption-related performance metrics.

### Dhruv

- Study the NEXUS paper and its security model.
- Work on the plaintext Transformer baseline.
- Explore the dataset and evaluation metrics.
- Help analyze accuracy and numerical differences.
- Document the security assumptions and limitations.

### Shared Responsibilities

- Finalize the implementation scope.
- Review each other's work.
- Run and validate experiments.
- Compare the results.
- Prepare the final report and presentation.

## Repository Structure

```text
secure-transformer-inference-tradeoffs/
│
├── README.md
├── PROJECT_PLAN.md
│
├── docs/
│   ├── paper-notes.md
│   ├── threat-model.md
│   └── protocol-design.md
│
├── configs/
│   └── ckks/
│
├── data/
│   └── README.md
│
├── src/
│   ├── plaintext/
│   ├── he/
│   └── evaluation/
│
├── experiments/
│
├── results/
│   ├── raw/
│   └── figures/
│
├── tests/
│
└── report/
    └── final-report.md
```

## Current Progress

- [x] Selected the research paper.
- [x] Finalized the project topic.
- [x] Created the GitHub repository.
- [ ] Complete the detailed paper review.
- [ ] Finalize the threat model.
- [ ] Set up the development environment.
- [ ] Run the plaintext Transformer baseline.
- [ ] Explore CKKS using OpenFHE.
- [ ] Implement the selected encrypted operations.
- [ ] Run experiments and collect results.
- [ ] Analyze the accuracy, security, and performance trade-offs.
- [ ] Complete the final report and presentation.

## References

1. **NEXUS: Secure Transformer Inference Made Non-interactive**  
   https://www.ndss-symposium.org/ndss-paper/secure-transformer-inference-made-non-interactive/

2. **NEXUS GitHub Repository**  
   https://github.com/zju-abclab/NEXUS

3. **OpenFHE GitHub Repository**  
   https://github.com/openfheorg/openfhe-development

4. **OpenFHE Documentation**  
   https://openfhe-development.readthedocs.io/

5. **DistilBERT Fine-tuned on SST-2**  
   https://huggingface.co/distilbert/distilbert-base-uncased-finetuned-sst-2-english

6. **GLUE Dataset**  
   https://huggingface.co/datasets/nyu-mll/glue

---

## Note

This project is currently in the research and implementation stage. The final implementation and experiments may change depending on the results of our initial testing.

We will update this README as the project progresses.
