# Research Digest — 2026-05-21

> **Coverage window:** arXiv Thursday batch (papers submitted Tue May 19 – Wed May 20 2026, announced May 21, IDs ≥ ~2605.19000); catch-up on selected bio-ML papers with IDs 2605.01138–2605.17244 not featured in the May 14–19 run (today's arXiv q-bio.BM new-submissions window returned lower-than-usual volume); bioRxiv postings checked through May 21. Sources: arXiv (cs.LG, cs.AI, q-bio.BM, q-bio.QM, q-bio.GN, stat.ML, cs.NE), bioRxiv, medRxiv, HF Papers, Papers With Code.

---

---
TITLE: Drift Flow Matching
AUTHORS: Chenrui Ma et al.
SOURCE: arXiv | 2605.17244 | [**Link**](https://arxiv.org/abs/2605.17244)
TOPIC TAG: Flow Matching
TLDR: Drift Flow Matching (DFM) unifies one-step Drift Models — which learn direct source-to-target transport maps — with multi-step Flow Matching in a single framework, preserving one-step efficiency by default while allowing iterative refinement steps when higher quality is required.
WHY IT MATTERS: One-step generative models (consistency models, flow distillation) sacrifice sample quality for speed, while multi-step flow matching sacrifices speed for quality; DFM's unified parameterization bridges this gap, enabling a single trained model to operate on an adaptive compute budget at inference time. For biological applications — protein backbone diffusion, molecular conformer generation, single-cell transport — this means the same generative model can be run in cheap one-step mode for high-throughput screening and costly multi-step mode for final candidate selection without retraining.
CODE: Not released

---

---
TITLE: MP2D: Constrained Monte Carlo Tree-Guided Diffusion for Multi-Objective Protein Sequence Design
AUTHORS: Zitai Kong, Yifan Dong, Yixuan Wu, Zhaokang Liang, Jian Wu, Hongxia Xu
SOURCE: arXiv | 2605.05829 | [**Link**](https://arxiv.org/abs/2605.05829)
TOPIC TAG: Diffusion / Protein LM
TLDR: MP2D integrates conditional discrete diffusion with constrained Monte Carlo Tree Search (MCTS) and global iterative refinement to treat each diffusion denoising step as a sequential decision node, exploring diverse denoising trajectories guided by Pareto-based multi-property rewards for protein sequence optimization.
WHY IT MATTERS: Prior multi-objective protein sequence design methods either optimize properties independently in separate rounds or use gradient-based guidance that collapses to single Pareto solutions; MP2D's MCTS backbone explicitly explores diverse denoising trajectories with a dynamic Pareto constraint, recovering a full Pareto front of sequences satisfying conflicting objectives (e.g., binding affinity vs. stability vs. expression). The marriage of tree-search planning with diffusion denoising introduces a new class of test-time compute scaling for protein design without requiring access to differentiable property oracles.
CODE: Not released

---

---
TITLE: Expanding Functional Protein Sequence Space Using High-Entropy Generative Models
AUTHORS: Roberto Netti, Emily Hinds, Francesco Calvanese, Rama Ranganathan, Martin Weigt, Francesco Zamponi
SOURCE: arXiv | 2605.03578 | [**Link**](https://arxiv.org/abs/2605.03578)
TOPIC TAG: Protein LM
TLDR: On the Chorismate Mutase enzyme family, a maximum-entropy Boltzmann Machine model (meDCA) along the edge-decimation trajectory yields a sequence distribution that samples a viable protein space more than 15 orders of magnitude larger than standard fully-connected DCA models, while improving experimental hit rates in directed evolution campaigns.
WHY IT MATTERS: Standard DCA / Boltzmann Machine protein generative models are heavily over-constrained — their dense parameter sets fit evolutionary statistics too tightly, generating sequences clustered around known naturals and missing the broader neutral network that evolution navigates; meDCA identifies the sparsest model that satisfies all evolutionary constraints, maximizing the entropy of the generative distribution. A 15-orders-of-magnitude expansion in viable sequence space directly enlarges the effective library for wet-lab library screening and machine-learning-guided directed evolution, with implications for engineering proteins outside natural sequence families.
CODE: Not released

---

---
TITLE: A Unified Measure-Theoretic View of Diffusion, Score-Based, and Flow Matching Generative Models
AUTHORS: (arXiv 2605.06829 authors)
SOURCE: arXiv | 2605.06829 | [**Link**](https://arxiv.org/abs/2605.06829)
TOPIC TAG: Diffusion / Flow Matching
TLDR: This paper derives a single measure-theoretic framework that subsumes DDPM, score-based SDEs, and continuous normalizing flows / flow matching as special cases of a general stochastic interpolant, unifying their training objectives and sampling algorithms under one mathematical roof.
WHY IT MATTERS: Practitioners in biological generative modeling currently choose between diffusion, score-based, and flow matching models based on empirical folklore rather than principled guidance; a unified framework reveals exactly which design choices (forward process, noise schedule, parameterization) differentiate these families and enables principled combination of their strengths. The measure-theoretic view also clarifies when biological data geometry (discrete sequences, SE(3) structures, count data) requires departing from the standard Euclidean assumptions shared by all three families.
CODE: Not released

---

---
TITLE: Kaczmarz Linear Attention
AUTHORS: Jiaxuan Zou et al.
SOURCE: arXiv | 2605.08587 | [**Link**](https://arxiv.org/abs/2605.08587)
TOPIC TAG: Architecture / SSM
TLDR: Revisiting the online-regression formulation underlying Gated DeltaNet, the authors derive a key-norm-normalized dynamic step size inspired by the Kaczmarz projection method, yielding a linear recurrent attention variant with improved state maintenance for long-context sequence modeling without quadratic memory cost.
WHY IT MATTERS: Linear recurrent models (Mamba, Hyena, DeltaNet) are critical for making genomic and protein language models practical at chromosomal or full-proteome scale, but existing step-size formulations either forget information too aggressively or write redundant information into the fixed-size state; the Kaczmarz normalization provides a principled residual-update rule that maximally reduces state-estimation error at each position. The derivation from an interpretable online-regression objective also makes the architecture more transparent than heuristically designed gating mechanisms, aiding future biological sequence modeling at megabase context.
CODE: Not released

---

---
TITLE: Using Deep Learning Models of Gene Regulation to Guide Drug Prioritization
AUTHORS: (bioRxiv 2026.05.11.724354 authors)
SOURCE: bioRxiv | 2026.05.11.724354 | [**Link**](https://www.biorxiv.org/content/10.64898/2026.05.11.724354v1)
TOPIC TAG: Clinical ML / Genomics
TLDR: An integrative pipeline links allele-specific deep learning enhancer prediction models directly to a therapeutic drug prioritization workflow, identifying candidate drugs that modulate disease-associated regulatory variants identified by the regulatory model rather than only protein-coding mutations.
WHY IT MATTERS: The overwhelming majority of GWAS variants and rare disease mutations fall in non-coding regulatory regions that are invisible to structure-based or protein-coding drug discovery pipelines; this work directly operationalizes deep learning cis-regulatory models (trained to predict allele-specific enhancer activity) as functional filters for identifying druggable regulatory nodes. The coupling to a drug prioritization engine closes the loop between regulatory genomics ML and actionable therapeutic hypotheses, providing a blueprint for transcription-factor-targeting strategies in diseases driven by enhancer dysregulation.
CODE: Not released

---

---
TITLE: Deep Learning for Cross-Domain Spatial Transcriptomic Modeling of Tissue Repair
AUTHORS: Tuan D. Pham
SOURCE: bioRxiv | 2026.05.13.724803 | [**Link**](https://www.biorxiv.org/content/10.64898/2026.05.13.724803v1)
TOPIC TAG: Genomics / Clinical ML
TLDR: A cross-domain deep learning framework aligns spatial transcriptomic profiles from injured and healthy tissue sections without paired training data, learning domain-invariant representations of cell-state transitions during tissue repair and enabling transfer of gene expression programs across repair contexts.
WHY IT MATTERS: Spatial transcriptomics of tissue repair generates distinct domain distributions (acute injury, chronic wound, post-repair) that standard models treat in isolation; cross-domain alignment allows a single model trained on one injury context to predict molecular programs in a distinct tissue repair scenario, dramatically reducing the data collection burden for rare pathologies. The learned domain-invariant representations provide an interpretable view of conserved repair gene programs across tissue types, directly informing regenerative medicine therapeutic design.
CODE: Not released

---

---
TITLE: Semi-Parametric Bayesian Additive Regression Trees for Risk Prediction with High-Dimensional Epigenetic Signatures and Low-Dimensional Covariates
AUTHORS: Saurabh Bhandari, Brian C.-H. Chiu, Parveen Bhatti, Yuan Ji
SOURCE: arXiv | 2605.20143 | [**Link**](https://arxiv.org/abs/2605.20143)
TOPIC TAG: Clinical ML / General ML
TLDR: A semi-parametric BART model handles the mixed setting where a high-dimensional methylation array or histone modification profile is the primary predictor while clinical covariates (age, sex, exposure) enter through a parametric linear component, achieving calibrated risk prediction for lymphoma incidence that outperforms lasso, elastic net, and standard BART on held-out GWAS cohorts.
WHY IT MATTERS: Epigenome-wide association studies generate tens of thousands of CpG sites as predictors for disease risk, but standard ML models designed for genomic data ignore the rich clinical covariate structure that partially explains outcome variance; the semi-parametric formulation explicitly isolates the non-linear epigenetic contribution from the linear covariate contribution, enabling principled inference about which epigenetic features add risk information beyond demographics. This is directly applicable to multi-omics clinical cohorts where chromatin accessibility, histone modification, or DNA methylation data are jointly collected with structured clinical records.
CODE: Not released

---

---
TITLE: Crossing the 12,000-Atom Barrier with Heterogeneous Quantum-Classical Supercomputing: Quantum Chemistry of Protein-Ligand Complexes
AUTHORS: Arjun Shajan, Dmitry Kaliakin, Stephan Schindler, Takehito Nakano et al.
SOURCE: arXiv | 2605.01138 | [**Link**](https://arxiv.org/abs/2605.01138)
TOPIC TAG: General ML / Architecture
TLDR: A quantum-embedding workflow combined with a heterogeneous quantum-classical compute pipeline (two 156-qubit IBM processors + Fugaku and Miyabi-G supercomputers) computes ab initio wavefunction-quality interaction energies for protein-ligand complexes of 11,608 and 12,635 atoms — by far the largest quantum chemistry calculations on biomolecular systems to date.
WHY IT MATTERS: Scoring functions used in ML-guided drug discovery (deep learning docking, binding affinity predictors) are trained against MM-level force field energies or crude quantum data, introducing systematic errors that hurt lead optimization; wavefunction-quality energies at the scale of real protein active sites provide the ground-truth data needed to train and validate next-generation ML scoring functions free of MM approximation artifacts. This work establishes that hybrid quantum-classical computation can now produce training data of unprecedented physical accuracy for biomolecular ML, marking a new epoch for physics-informed drug discovery.
CODE: Not released

---

---
TITLE: Variational Linear Attention: Stable Associative Memory for Long-Context Transformers
AUTHORS: (arXiv 2605.11196 authors)
SOURCE: arXiv | 2605.11196 | [**Link**](https://arxiv.org/abs/2605.11196)
TOPIC TAG: Architecture / SSM
TLDR: Variational Linear Attention (VLA) reframes the linear attention state as a probabilistic latent variable and derives an ELBO training objective that improves state stability over long sequences, addressing the well-known degradation of linear attention models at long context without reverting to softmax attention.
WHY IT MATTERS: Genomic and protein language models need sub-quadratic attention to scale to chromosomal (100k+ bp) or full-proteome contexts, but existing linear attention variants suffer from state compression artifacts that cause information loss in critical long-range regulatory signals; the variational formulation provides a theoretically grounded stability mechanism and a Bayesian uncertainty estimate over the hidden state that could be used to detect low-confidence sequence regions. The ELBO objective also introduces a principled regularization that prevents the state collapse failure mode observed in GLA and Mamba-style models on very long biological sequences.
CODE: Not released

---

---
TITLE: MP2D: Constrained Monte Carlo Tree-Guided Diffusion — Gene Regulation Catch-up: TPCAV Concept Attribution for Genomic Deep Learning
AUTHORS: Yuxuan Chen et al.
SOURCE: bioRxiv | 2026.01.20.700723 | [**Link**](https://www.biorxiv.org/content/10.64898/2026.01.20.700723v2)
TOPIC TAG: Genomics / General ML
TLDR: TPCAV (Testing with PCA-projected Concept Activation Vectors) adapts the TCAV interpretability framework to deep learning genomics models by projecting concept directions into a PCA subspace, handling the high correlational structure of genomic features and recovering biologically meaningful transcription factor motif attributions.
WHY IT MATTERS: Standard TCAV assumes independent feature directions, but genomic deep learning models learn highly correlated representations driven by co-occurring TF binding motifs and chromatin states; PCA projection decorrelates these directions before concept testing, yielding concept attributions that correctly isolate individual regulatory elements rather than confounding them with correlated co-factors. This directly addresses the interpretability bottleneck for regulatory genomics models like Enformer and Borzoi, where understanding which specific enhancer syntax drives predictions is essential for variant effect interpretation.
CODE: Not released

---

==============================================================
HIGHLIGHTS OF THE DAY
==============================================================

### 1. MP2D: Constrained Monte Carlo Tree-Guided Diffusion for Multi-Objective Protein Sequence Design
*arXiv 2605.05829*

MP2D is the first protein sequence design framework to combine Monte Carlo Tree Search with conditional discrete diffusion, treating each denoising step as a node in a planning tree and guiding trajectory selection with Pareto-based multi-property rewards. This architecture break is significant: where existing methods either optimize one property at a time or use gradient guidance that collapses to a single solution, MP2D recovers a full Pareto front of diverse, high-quality protein sequences simultaneously satisfying conflicting properties. The test-time compute scaling potential — deeper tree search = better designs — means MP2D can leverage inference-time compute scaling in the same way LLM reasoning models do, establishing a new paradigm for constrained biological sequence design.
Code / weights: Not yet released (arXiv: https://arxiv.org/abs/2605.05829)

---

### 2. Expanding Functional Protein Sequence Space Using High-Entropy Generative Models
*arXiv 2605.03578*

By identifying the maximum-entropy sparse Boltzmann Machine model (meDCA) along the edge-decimation trajectory of evolutionary DCA training, Netti, Hinds, Ranganathan et al. show that standard DCA models dramatically over-constrain protein sequence space — and that relaxing to the maximum-entropy point expands the sampled viable sequence space by over 15 orders of magnitude. This is a fundamental insight about how existing generative protein models fail to capture the full neutral network that makes evolutionary exploration possible, with immediate practical consequences: meDCA-guided libraries should dramatically improve hit rates in ML-assisted directed evolution campaigns where biological diversity is the bottleneck. The Ranganathan lab's involvement lends credibility to the entropy-neutrality connection from a protein biophysics perspective.
Code / weights: Not released (arXiv: https://arxiv.org/abs/2605.03578)

---

### 3. Drift Flow Matching
*arXiv 2605.17244*

Drift Flow Matching provides the first principled unification of one-step generative models (consistency models, flow distillation) with multi-step flow matching, training a single model that can be evaluated at any desired compute budget during inference. For computational biology this resolves a long-standing practical tension: high-throughput virtual screening needs fast one-step generation while lead optimization needs quality; DFM's adaptive-budget parameterization enables both from one trained model. The theoretical connection to drift models also opens a path to re-interpreting existing flow-matching models for proteins (FrameFlow, RFdiffusion2) as DFM instances, potentially enabling post-hoc efficiency gains on already-trained models.
Code / weights: Not yet released (arXiv: https://arxiv.org/abs/2605.17244)

==============================================================
DAILY STATS
==============================================================
- Total papers found today: 11
- By topic: Protein LM: 2 | Diffusion: 2 | Flow Matching: 1 | Genomics: 3 | Architecture: 3 | General ML: 2 | Clinical ML: 3
- Sources: arXiv: 8 | bioRxiv: 2 | medRxiv: 0 | PubMed: 0 | HF Papers: 0 | PWC: 0
- Papers with code released: 0

> **Note on coverage:** Today's arXiv q-bio.BM new-submissions window (IDs ≥ 2605.19000) returned limited bio-specific content; the digest includes the freshest papers identified (2605.17244, 2605.20143) plus five papers from IDs 2605.01138–2605.08587 that fell through the gaps of prior digests due to their cross-listing between cs.LG and q-bio categories. Full weekday coverage resumes tomorrow.
