
# Project Plan
## Evaluating the Accuracy–Security–Performance Trade-offs in Non-Interactive Secure Transformer Inference

### 1. Project Overview

**Course:** Cryptography  
**Research Paper:** NEXUS: Secure Transformer Inference Made Non-interactive  
**Team Members:**
- Khushboo Pandey
- Dhruv

### 2. Project Goal

The main goal of this project is to understand how Homomorphic Encryption can help protect user data during Transformer inference.

We will study the NEXUS research paper and develop a small prototype using available tools and libraries. We will compare normal inference with selected encrypted computations and evaluate the impact on accuracy, security, and performance.

We are not planning to reproduce the complete NEXUS system. Our focus is to implement and evaluate a manageable part of the problem.

---

### 3. Project Modules and Responsibilities

We have divided the project into the following modules so that each team member has clear responsibilities.

## Module 1: Research Paper Analysis and Security Understanding

**Assigned to: Dhruv**

**Tasks:**
- Read and understand the NEXUS research paper.
- Identify the main problem addressed by the paper.
- Understand how non-interactive secure inference works.
- Study the role of Homomorphic Encryption.
- Understand the CKKS encryption scheme.
- Identify the security assumptions and threat model.
- Understand what information is protected and what information may still be exposed.
- Review the limitations of the proposed approach.

**Expected Deliverables:**
- `docs/paper-notes.md`
- `docs/threat-model.md`
- Summary of the NEXUS paper.
- Explanation of the security assumptions and limitations.

## Module 2: Project Setup and Environment Configuration

**Assigned to: Khushboo Pandey**

**Tasks:**
- Set up the GitHub repository and project structure.
- Prepare the Python development environment.
- Install and configure the required libraries.
- Explore the NEXUS GitHub repository and its dependencies.
- Set up OpenFHE for Homomorphic Encryption experiments.
- Check whether the required experiments can run locally using CPU resources.
- Document installation steps and environment requirements.

**Expected Deliverables:**
- Working project environment.
- `requirements.txt` or environment configuration.
- `README.md`
- Installation and setup instructions.
- Initial OpenFHE setup test.

## Module 3: Plaintext Transformer Implementation

**Assigned to: Dhruv**

**Tasks:**
- Explore pretrained Transformer models.
- Set up DistilBERT fine-tuned on the SST-2 sentiment classification dataset.
- Load and prepare the dataset.
- Run normal inference without encryption.
- Calculate model accuracy on a fixed evaluation subset.
- Measure normal inference time.
- Record memory usage where practical.
- Save the baseline results for comparison.

**Expected Deliverables:**
- Plaintext Transformer implementation.
- Baseline accuracy results.
- Baseline inference time.
- Evaluation script or notebook.
- Results saved under `results/raw/`.

## Module 4: Homomorphic Encryption and CKKS Implementation

**Assigned to: Khushboo Pandey**

**Tasks:**
- Study the CKKS encryption scheme in more detail.
- Understand encryption, evaluation, and decryption.
- Explore OpenFHE examples and documentation.
- Test encryption and decryption using sample numerical values.
- Perform selected arithmetic operations on encrypted values.
- Explore how CKKS parameters affect numerical precision.
- Measure encryption, evaluation, and decryption time.
- Record ciphertext size and memory usage where possible.

**Expected Deliverables:**
- OpenFHE implementation.
- CKKS encryption and decryption examples.
- Selected encrypted arithmetic operations.
- Performance measurements.
- Implementation notes and limitations.

## Module 5: Secure Inference Prototype

**Assigned to: Khushboo Pandey and Dhruv**

**Tasks:**
- Review the plaintext implementation and CKKS experiments.
- Decide which Transformer-related operations can realistically be tested with encryption.
- Define the input and output flow for the prototype.
- Connect the selected encrypted operations with the plaintext baseline where appropriate.
- Test the implementation with sample inputs.
- Verify the decrypted numerical results against the corresponding plaintext computations.
- Clearly identify which operations are encrypted and which remain plaintext.

**Expected Deliverables:**
- Working prototype for the selected operations.
- Prototype architecture or workflow diagram.
- Test cases and validation results.
- Description of implementation limitations.

## Module 6: Performance and Accuracy Evaluation

**Assigned to: Khushboo Pandey and Dhruv**

**Tasks:**

**Khushboo Pandey:**
- Measure encryption time.
- Measure homomorphic evaluation time.
- Measure decryption time.
- Record ciphertext size.
- Record memory usage where practical.
- Test selected CKKS parameter configurations.

**Dhruv:**
- Measure plaintext model accuracy.
- Compare plaintext and decrypted numerical outputs.
- Calculate numerical error.
- Analyze any differences in classification results.
- Help organize the evaluation results.

**Both Members:**
- Compare plaintext and encrypted computations.
- Analyze the performance overhead.
- Discuss the impact of encryption on accuracy.
- Explain the security and privacy limitations.
- Prepare graphs and result tables.

**Expected Deliverables:**
- Performance comparison table.
- Accuracy and numerical error results.
- Experiment graphs.
- Analysis of accuracy, security, and performance trade-offs.

## Module 7: Documentation and Final Presentation

**Assigned to: Khushboo Pandey and Dhruv**

**Tasks:**

**Khushboo Pandey:**
- Document environment setup and implementation details.
- Explain the OpenFHE and CKKS experiments.
- Document performance measurements.
- Help prepare the implementation section of the report.

**Dhruv:**
- Document the research paper analysis.
- Explain the threat model and security assumptions.
- Document the plaintext baseline.
- Help prepare the evaluation and security analysis sections.

**Both Members:**
- Review and combine all project documentation.
- Prepare the final report.
- Create presentation slides.
- Review the results and conclusions.
- Prepare for questions about the implementation and research paper.

**Expected Deliverables:**
- Final project report.
- Updated GitHub repository.
- Demonstration of the prototype.

---

### 4. Responsibility Summary

| Module | Description | Owner |
|---|---|---|
| 1 | Research Paper and Security Analysis | Dhruv |
| 2 | Project Setup and Environment | Khushboo |
| 3 | Plaintext Transformer Implementation | Dhruv |
| 4 | CKKS and OpenFHE Implementation | Khushboo |
| 5 | Secure Inference Prototype | Both |
| 6 | Performance and Accuracy Evaluation | Both |
| 7 | Documentation and Presentation | Both |

---

### 5. Project Timeline

The following is our tentative timeline. We will adjust it based on implementation progress and the complexity of the experiments.

| Phase | Activities | Responsible Member |
|---|---|---|
| Phase 1 | Read NEXUS paper and understand the security model | Dhruv |
| Phase 2 | Set up repository, Python environment, and OpenFHE | Khushboo |
| Phase 3 | Implement and test plaintext Transformer baseline | Dhruv |
| Phase 4 | Explore CKKS and implement encrypted operations | Khushboo |
| Phase 5 | Develop the selected secure inference prototype | Both |
| Phase 6 | Run experiments and collect measurements | Both |
| Phase 7 | Analyze results and prepare graphs | Both |
| Phase 8 | Complete report and presentation | Both |

---

### 6. Expected Evaluation Metrics

We plan to evaluate the prototype using the following metrics:

| Metric | What We Want to Measure |
|---|---|
| Accuracy | How accurately the model performs its task |
| Numerical Error | Difference between plaintext and decrypted results |
| Encryption Time | Time required to encrypt the input |
| Evaluation Time | Time required to perform encrypted operations |
| Decryption Time | Time required to decrypt the output |
| Ciphertext Size | Size of encrypted data |
| Memory Usage | Memory consumed during experiments |
| Performance Overhead | Additional computation time caused by encryption |

---

### 7. Tools and Technologies

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| OpenFHE | Homomorphic Encryption implementation |
| CKKS | Approximate Homomorphic Encryption scheme |
| PyTorch | Machine learning framework |
| Hugging Face Transformers | Transformer model implementation |
| DistilBERT | Candidate sentiment classification model |
| SST-2 | Sentiment classification dataset |
| Jupyter Notebook | Running experiments and analysis |
| GitHub | Project collaboration and version control |

---

### 8. Repository Structure

```text
secure-transformer-inference-tradeoffs/
│
├── README.md
├── PROJECT_PLAN.md
├── requirements.txt
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

---

### 9. Important Notes

- We will first make sure that the plaintext and CKKS experiments work independently.
- We will start with small test inputs before attempting more complex Transformer-related operations.
- We will not claim that the entire Transformer model is encrypted unless the implementation actually supports that.
- We will document the security assumptions and limitations of our prototype.
- We will use the same test inputs wherever possible to make the comparison fair.
- We will keep the implementation manageable and focus on producing reproducible results.

### 10. Project Status

This project is currently in the research and initial implementation stage. The module assignments describe our planned responsibilities, not necessarily completed work. We will update the checklist as each task is completed.

- [x] Select research paper.
- [x] Finalize project title.
- [x] Create GitHub repository.
- [x] Divide project responsibilities.
- [ ] Complete research paper analysis.
- [ ] Finalize threat model.
- [ ] Complete environment setup.
- [ ] Implement plaintext baseline.
- [ ] Complete initial CKKS experiments.
- [ ] Develop secure inference prototype.
- [ ] Run performance and accuracy experiments.
- [ ] Complete final report and presentation.
