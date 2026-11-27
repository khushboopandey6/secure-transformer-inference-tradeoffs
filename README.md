Evaluating the Accuracy–Security–Performance Trade-offs in Non-Interactive Secure Transformer Inference
Course: Cryptography Project
Team members: Khushboo Pandey and Dhruv

About the project
For this project, we want to understand how homomorphic encryption can be used to run parts of a Transformer model without first decrypting the input.

Our main reference is the paper NEXUS: Secure Transformer Inference Made Non-interactive. It explores how a server can perform computations on encrypted data while keeping the client's input private.

We plan to study the security ideas behind this approach and build a smaller version that we can test for our course project. In particular, we want to see how different CKKS settings affect the output, how long encrypted computation takes, and how close the decrypted result is to the normal, unencrypted result.

We are still deciding how much of the Transformer workflow we can implement. We will start with a small CKKS example and then choose a realistic next step.
What we want to learn
- How homomorphic encryption works, especially the CKKS scheme.
- What information is protected when a client sends encrypted data to a server.
- What the server might still observe, such as message size and execution time.
- How CKKS parameters affect computation time and numerical error.
- How encrypted results compare with normal, unencrypted computation.
Our planned approach
1. Read the NEXUS paper. Understand its protocol, security assumptions, and implementation.
2. Define the threat model. Identify what the client wants to keep private, what the server can access, and what our prototype does not protect.
3. Set up a plaintext baseline. Use a small pretrained Transformer model for a classification task so we have normal outputs for comparison.
4. Try CKKS. Use an open-source homomorphic encryption library to encrypt input values, perform a supported computation, and decrypt the result.
5. Compare the results. Measure numerical differences, prediction agreement where applicable, and execution time.
6. Test different settings. Compare a small number of valid CKKS configurations and record their security settings and performance.
7. Write up our findings. Explain the results, limitations, and possible improvements.
The exact operations we encrypt will depend on what we can implement and test. If our prototype encrypts only selected operations or a small model component, we will say so clearly. We will not describe that as fully encrypted end-to-end Transformer inference.
Tools and resources
Tool or resource	How we plan to use it
NEXUS paper	Main research reference
NEXUS source code	Understand the authors' implementation
OpenFHE	Experiment with CKKS homomorphic encryption
PyTorch	Run the machine learning baseline
Hugging Face Transformers	Load and run a pretrained model
DistilBERT SST-2	Possible starting model for sentiment classification
GLUE dataset	Possible source of SST-2 evaluation examples


We do not plan to use a paid LLM API. We will use open-source software and publicly available model weights. We plan to develop locally first. AWS is optional and will only be used if an eligible free option is available and it does not create charges.
What we plan to measure
- Time for key generation, encryption, evaluation, and decryption.
- Difference between plaintext and decrypted numerical outputs.
- Prediction agreement and classification metrics, if supported by the implemented model path.
- Size of the encrypted data sent to and returned from the server.
- Memory use during experiments.
- CKKS parameters and the security level reported for each configuration.
We will record the hardware and software versions so that our experiments can be understood and repeated.
Who is working on what?
Khushboo Pandey
- Set up the project repository and development environment.
- Explore the NEXUS implementation and its setup requirements.
- Set up OpenFHE and try a basic CKKS encrypt/evaluate/decrypt example.
- Work on the encrypted computation and experiment scripts.
- Record runtime, memory, and ciphertext-size measurements.
Dhruv
- Study the NEXUS protocol and its security assumptions.
- Prepare the threat model and explain what is and is not protected.
- Set up the plaintext Transformer model and evaluation data.
- Record baseline predictions and metrics.
- Help compare the plaintext and encrypted results.
Work we will do together
We will agree on the final implementation scope, check each other's results, review the security claims, analyze the experiments, and prepare the final report and presentation. These are our planned responsibilities, and we will update them as the project develops.
Repository layout
secure-transformer-inference-tradeoffs/
├── README.md
├── PROJECT_PLAN.md
├── docs/
│   ├── paper-notes.md
│   ├── threat-model.md
│   └── protocol-design.md
├── configs/
│   └── ckks/
├── data/
│   └── README.md
├── src/
│   ├── plaintext/
│   ├── he/
│   └── evaluation/
├── experiments/
├── results/
│   ├── raw/
│   └── figures/
├── tests/
└── report/
We will add files and folders as we need them. We will not upload large model files, private data, secret keys, or AWS credentials to GitHub.
Current progress
This repository is where we will organize our reading, implementation, and experiments. We will update this checklist as we complete each part.
- [ ] Read and take notes on the NEXUS paper.
- [ ] Write the threat model.
- [ ] Set up the development environment.
- [ ] Run the plaintext model baseline.
- [ ] Run a basic CKKS example.
- [ ] Choose and implement the first encrypted operation.
- [ ] Run the comparison experiments.
- [ ] Prepare the final report.
References
1. NEXUS: Secure Transformer Inference Made Non-interactive — NDSS
2. NEXUS source code
3. OpenFHE documentation
4. OpenFHE source code
5. DistilBERT SST-2 model
6. GLUE dataset
This README describes our current plan. We will update it as we make implementation decisions and get experimental results.
