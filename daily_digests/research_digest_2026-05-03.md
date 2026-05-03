# Research Digest — 2026-05-03

> **Scope:** Papers posted or published in the last ~24–72 hours across arXiv (cs.LG, cs.AI, q-bio.BM, q-bio.QM, q-bio.GN, stat.ML, cs.NE), bioRxiv, medRxiv, PubMed, Hugging Face Papers, Semantic Scholar, and Papers With Code.  
> **Focus areas:** Protein & Molecular ML · Generative Models in Biology · Sequence & Genome Models · Architecture Innovations · General Cutting-Edge ML · Clinical & Translational ML

---

## PAPERS

---

TITLE: STORM: A Multimodal Foundation Model of Spatial Transcriptomics and Histology for Biological Discovery and Clinical Prediction
AUTHORS: Xiang, J. et al.
SOURCE: arXiv | 2604.03630 | [**Link**](https://arxiv.org/abs/2604.03630)
TOPIC TAG: Genomics / Clinical ML
TLDR: STORM is a hierarchical foundation model trained on 1.2 million spatially-resolved transcriptomic profiles matched to H&E histology across 18 organs, outperforming existing methods at predicting spatial gene expression from histology images across 11 tumor types and enhancing spatial domain discovery.
WHY IT MATTERS: Spatial transcriptomics is cost-prohibitive at scale while routine H&E staining is ubiquitous; STORM bridges the two modalities so that molecular-resolution insights can be derived from standard pathology slides without additional sequencing. Training jointly across 18 organs yields transferable morpho-molecular representations that generalize across cancer types—making spatially-resolved tumor profiling accessible far beyond the labs that can afford ST libraries.
CODE: Not released

---

TITLE: RosettaSearch: Multi-Objective Inference-Time Search for Protein Sequence Design
AUTHORS: (arXiv 2604.17175 team) et al.
SOURCE: arXiv | 2604.17175 | [**Link**](https://arxiv.org/abs/2604.17175)
TOPIC TAG: Protein LM / General ML
TLDR: Uses frontier LLMs (o4-mini, Gemini-3) as generative optimizers within a multi-objective search loop scored by RosettaFold3, achieving 18–68% improvements in structural fidelity metrics and a 2.5× design success rate over LigandMPNN without any model retraining.
WHY IT MATTERS: Inference-time scaling has transformed text reasoning tasks; RosettaSearch demonstrates that the same paradigm transfers to backbone-conditioned protein sequence design, and that gains scale with the underlying LLM's reasoning capability. This is the first large-scale validation that general reasoning LLMs can act as effective generative optimizers for a hard combinatorial biology problem.
CODE: Not released

---

TITLE: ProtoCycle: Reflective Tool-Augmented Planning for Text-Guided Protein Design
AUTHORS: (arXiv 2604.16896 team) et al.
SOURCE: arXiv | 2604.16896 | [**Link**](https://arxiv.org/abs/2604.16896)
TOPIC TAG: Protein LM / General ML
TLDR: ProtoCycle is an agentic LLM framework trained with supervised trajectories and online reinforcement learning that drives a multi-round feedback cycle of planning, tool use, and LLM-guided reflection to produce sequences satisfying free-text functional requirements with competitive foldability.
WHY IT MATTERS: Fine-tuning large generative sequence models for text-to-protein mapping is data-hungry; ProtoCycle circumvents this by composing off-the-shelf tools and embedding LLM reflection as the learning signal, showing ablations that reflection is the dominant contributor to sequence quality. The result is a data-efficient agentic blueprint for any domain where formal specification of design intent is more accessible than paired training examples.
CODE: Not released

---

TITLE: Mamba-3: Improved Sequence Modeling using State Space Principles
AUTHORS: (arXiv 2603.15569 team) et al.
SOURCE: arXiv | 2603.15569 | [**Link**](https://arxiv.org/abs/2603.15569)
TOPIC TAG: SSM / Architecture
TLDR: Mamba-3 unifies a more expressive recurrence derived from SSM discretization, complex-valued state updates for richer state tracking, and a multi-input multi-output (MIMO) formulation, yielding significant gains on retrieval, state-tracking, and language modeling benchmarks without increasing decode latency.
WHY IT MATTERS: State space models are the dominant choice for genomic and long-context protein sequence modeling due to their sub-quadratic complexity; the expressivity improvements in Mamba-3—especially complex-valued states that capture oscillatory motifs—directly benefit long-range regulatory element modeling and protein evolutionary signal detection. Zero-latency gains make this a drop-in replacement for production bio-sequence pipelines.
CODE: Not released

---

TITLE: CrossLLM-Mamba: Multimodal State Space Fusion of LLMs for RNA Interaction Prediction
AUTHORS: (arXiv 2602.22236 team) et al.
SOURCE: arXiv | 2602.22236 | [**Link**](https://arxiv.org/abs/2602.22236)
TOPIC TAG: SSM / Genomics
TLDR: Reformulates RNA interaction prediction as a state-space alignment problem, using bidirectional Mamba encoders to enable deep cross-modal communication between modality-specific LLM embeddings, achieving state-of-the-art performance across RNA–protein, RNA–small-molecule, and RNA–RNA interaction categories in a single unified model.
WHY IT MATTERS: RNA is an emerging drug target class yet RNA interaction prediction has remained fragmented across three separate sub-problems with incompatible architectures; CrossLLM-Mamba unifies them and avoids the quadratic cost of transformer attention for long RNA strands by leveraging SSM hidden-state propagation for cross-modal alignment. The framework sets a new benchmark on all three categories simultaneously, enabling end-to-end rational RNA-targeting drug design pipelines.
CODE: Not released

---

TITLE: CellScape: Uncovering Spatial Tissue Domains and Cell Types in Spatial Omics through Cross-Scale Profiling of Cellular and Genomic Interactions
AUTHORS: Yan, R. et al.
SOURCE: arXiv | 2602.12651 | [**Link**](https://arxiv.org/abs/2602.12651)
TOPIC TAG: Genomics
TLDR: CellScape is a dual-branch deep learning framework that jointly models cellular spatial interactions in tissue space and genomic regulatory relationships among cells, producing integrated representations that improve spatial domain segmentation and cell-type annotation across diverse spatial transcriptomics datasets.
WHY IT MATTERS: Spatial omics methods typically treat spatial context and gene regulation as independent signals, discarding biologically meaningful interactions between cell neighborhoods and their underlying regulatory states; CellScape's joint modeling recovers domain boundaries that are invisible to either branch alone. The cross-scale design is applicable to emerging multi-resolution spatial platforms that simultaneously capture sub-cellular and tissue-level organization.
CODE: Not released

---

TITLE: Predicting RNA 3D Structure and Conformers Using a Pre-trained Secondary Structure Model and Structure-Aware Attention
AUTHORS: (Nat. Mach. Intell. team) et al.
SOURCE: Nature Machine Intelligence | 10.1038/s42256-026-01223-x | [**Link**](https://www.nature.com/articles/s42256-026-01223-x)
TOPIC TAG: Genomics
TLDR: Couples a pre-trained RNA secondary structure model with a structure-aware attention module to predict diverse 3D conformational ensembles for single-chain RNAs, outperforming existing methods on the RNA-Puzzles and casp-RNA benchmarks.
WHY IT MATTERS: RNA function depends on its ability to adopt multiple structures, yet nearly all computational methods output a single static conformation; the ensemble-generating capability here is directly relevant to understanding riboswitch mechanisms, aptamer design, and RNA-targeting drug selectivity. Using secondary structure predictions as a pre-training inductive bias dramatically reduces the data requirements compared to learning from 3D structures alone.
CODE: Not released

---

TITLE: Flow Matching for Generative Modelling in Bioinformatics and Computational Biology
AUTHORS: (Nat. Mach. Intell. team) et al.
SOURCE: Nature Machine Intelligence | 10.1038/s42256-026-01220-0 | [**Link**](https://www.nature.com/articles/s42256-026-01220-0)
TOPIC TAG: Flow Matching
TLDR: A comprehensive review and unified theoretical framework describes how flow matching enables simulation-free training of Continuous Normalizing Flows for protein backbone generation, DNA/RNA sequence design, and small-molecule docking, and introduces new guidance strategies for discrete biological alphabets.
WHY IT MATTERS: Flow matching has rapidly become the default training objective for structure-based generative models in biology yet lacks a unified treatment; this Nature Machine Intelligence paper provides the canonical reference covering all biological modalities, including the first systematic treatment of Dirichlet flow for discrete sequences. The novel discrete-guidance extensions are practically important for controlled generation of sequences with specified functional properties.
CODE: Not released

---

TITLE: De Novo Design of Epitope-Specific Antibodies via a Structure-Driven Computational Workflow
AUTHORS: (Nature Communications 2026 team) et al.
SOURCE: Nature Communications | 10.1038/s41467-025-67361-9 | [**Link**](https://www.nature.com/articles/s41467-025-67361-9)
TOPIC TAG: Protein LM
TLDR: A fully computational pipeline combining RFdiffusion backbone hallucination with epitope-constraint scoring generates scFvs targeting user-specified antigen epitopes, with cryo-EM confirming atomically accurate conformations for all six CDR loops on multiple therapeutic targets.
WHY IT MATTERS: Epitope-specific antibody generation has historically required months of animal immunization and library screening; this in-silico-only workflow reduces the discovery phase to hours and has atomic-level cryo-EM validation, setting a new standard for computational antibody design. The compatibility with any user-defined epitope—not just flat protein surfaces—enables targeting of allosteric sites and cryptic epitopes inaccessible to conventional campaigns.
CODE: Not released

---

TITLE: Scaling and Quantization of Large-Scale Foundation Model Enables Resource-Efficient Predictions in Network Biology
AUTHORS: (Nature Computational Science 2026 team) et al.
SOURCE: Nature Computational Science | 10.1038/s43588-026-00972-4 | [**Link**](https://www.nature.com/articles/s43588-026-00972-4)
TOPIC TAG: General ML
TLDR: Larger foundation models pretrained on more diverse biological network data yield monotonically better predictions across network biology tasks, and post-training quantization preserves almost all of this performance at a fraction of inference cost, demonstrating resource-efficient deployment is feasible.
WHY IT MATTERS: Scaling laws had been established for language and vision but not for biological network reasoning tasks; this work is one of the first to document them in the omics domain, providing a quantitative roadmap for bio-FM development. The lossless quantization result opens deployment of large network biology models in resource-constrained clinical or laboratory settings without sacrificing predictive accuracy.
CODE: Not released

---

TITLE: CMGL: Confidence-Guided Multi-Omics Graph Learning for Cancer Subtype Classification
AUTHORS: (arXiv 2604.24201 team) et al.
SOURCE: arXiv | 2604.24201 | [**Link**](https://arxiv.org/abs/2604.24201)
TOPIC TAG: Clinical ML / Genomics
TLDR: Estimates per-sample modality reliability via evidential deep learning and uses the resulting confidence scores to dynamically guide cross-omics fusion and graph construction, surpassing the strongest multi-omics baseline by 4.03% in average accuracy across four single-cancer subtyping benchmarks.
WHY IT MATTERS: Multi-omics integration is complicated by varying data quality and informativeness across modalities and patients, which static fusion methods ignore; explicit per-sample uncertainty modeling is a meaningful step toward trustworthy clinical multi-omics AI. The confidence-guided graph construction also provides interpretable modality importance scores that could flag ambiguous cases in clinical deployment.
CODE: Not released

---

TITLE: SimpleTES: Evaluation-Driven Scaling for Scientific Discovery
AUTHORS: Ye, H., Ermon, S., Zou, J. et al.
SOURCE: arXiv | 2604.19341 | [**Link**](https://arxiv.org/abs/2604.19341)
TOPIC TAG: General ML
TLDR: SimpleTES is a general framework combining parallel exploration, feedback-driven refinement, and local selection to scale LLM-powered scientific discovery loops, showing that scaling along the evaluation-compute axis—rather than model parameters—drives the largest gains in hypothesis quality and experimental design.
WHY IT MATTERS: As LLMs are applied to hypothesis generation and experimental design in drug discovery and genomics, knowing what to scale is critical; SimpleTES establishes that investment in verifiers and simulators (evaluation compute) yields greater returns than model-size scaling. The framework provides a concrete blueprint for designing AI-driven discovery loops that can be adopted immediately in lead optimization and regulatory genomics workflows.
CODE: Not released

---

TITLE: Multi-Objective Reinforcement Learning for Generating Covalent Inhibitor Candidates
AUTHORS: (arXiv 2604.20019 team) et al.
SOURCE: arXiv | 2604.20019 | [**Link**](https://arxiv.org/abs/2604.20019)
TOPIC TAG: Clinical ML
TLDR: A SMILES-based LSTM optimized with Pareto crowding distance RL simultaneously maximizes binding affinity, synthetic accessibility, and covalent warhead reactivity for EGFR and ACHE targets, rediscovering known inhibitors and spontaneously generating novel warhead chemotypes—including allenes, 3-oxo-β-sultams, and α-methylene-β-lactones—absent from training data.
WHY IT MATTERS: Covalent drugs offer irreversible target engagement with sub-nanomolar potency but designing warheads with appropriate selectivity is notoriously difficult to specify as a single-objective problem; the multi-objective Pareto approach naturally balances reactivity, selectivity, and synthesizability. Emergence of warhead scaffolds beyond the training distribution demonstrates that the RL policy generalizes covalent chemical space rather than interpolating, making this a practical tool for covalent medicinal chemistry programs.
CODE: Not released

---

TITLE: A Systematic Survey and Benchmark of Deep Learning for Molecular Property Prediction in the Foundation Model Era
AUTHORS: Li, Z., Chen, X., Wen, H., Zhang, R., Li, M., Zhang, X., Yin, H., Yang, Q., Lam, K.-Y., Lio, P., Yiu, S.-M.
SOURCE: arXiv | 2604.16586 | [**Link**](https://arxiv.org/abs/2604.16586)
TOPIC TAG: General ML
TLDR: Traces four paradigms—Quantum, Descriptor-ML, Geometric Deep Learning, Foundation Models—through a unified taxonomy of molecular representations, architectures, and tasks, benchmarking each across physicochemical, ADMET, and bioactivity endpoints to identify when each paradigm is preferred.
WHY IT MATTERS: Foundation model adoption in molecular property prediction has outpaced systematic benchmarking, leading to widespread misapplication of models to unsuitable tasks; this survey provides the most comprehensive task-model alignment guide to date. The taxonomy of when geometric inductive biases versus scale are the limiting factor is directly actionable for practitioners choosing models for drug discovery campaigns.
CODE: Not released

---

TITLE: Learning Structure, Energy, and Dynamics: A Survey of Artificial Intelligence for Protein Dynamics
AUTHORS: (arXiv 2604.25244 team) et al.
SOURCE: arXiv | 2604.25244 | [**Link**](https://arxiv.org/abs/2604.25244)
TOPIC TAG: Protein LM / General ML
TLDR: Comprehensive survey covering AI methods for protein conformational ensemble generation, molecular dynamics trajectory prediction, Boltzmann generators, machine learning potentials, collective variable discovery, and coarse-grained modeling, with critical analysis of where current approaches fail on disordered proteins and large complexes.
WHY IT MATTERS: Protein function is intrinsically dynamic yet most ML protein tools target static structures; this survey systematically maps the landscape of dynamics-aware ML models including flow matching ensembles, diffusion-based trajectory generators, and score-based approaches to free energy surfaces. The failure-mode analysis for disordered proteins and large assemblies provides a clear research agenda for the field.
CODE: Not released

---

TITLE: Graph Neural Networks for Protein–Ligand Interaction Prediction: Current Methods and Future Directions
AUTHORS: (bioRxiv April 2026 team) et al.
SOURCE: bioRxiv | 10.64898/2026.04.23.720519 | [**Link**](https://www.biorxiv.org/content/10.64898/2026.04.23.720519v1)
TOPIC TAG: Protein LM / Clinical ML
TLDR: Benchmarks hybrid GNN architectures integrating protein language model embeddings for protein–ligand binding affinity prediction, identifying explainability and distributional shift as the primary barriers to clinical translation and motivating scientifically grounded inductive biases.
WHY IT MATTERS: Protein–ligand affinity prediction is the central computational task in structure-based drug design, yet the field has fragmented into dozens of incomparable GNN variants; this systematic benchmark clarifies which architectural choices matter and under what data regimes. The explainability gap analysis motivates an important research thread—interpretable binding site attribution—that is underrepresented relative to the accuracy-focused literature.
CODE: Not released

---

==============================================================
HIGHLIGHTS OF THE DAY
==============================================================

**1. STORM: A Multimodal Foundation Model of Spatial Transcriptomics and Histology**
*(arXiv 2604.03630)*

STORM is the most architecturally ambitious paper of today's digest: a single foundation model trained jointly on 1.2 million spatially-resolved transcriptomic profiles matched to H&E histology images across 18 different human organs. Its hierarchical design integrates morphological features, gene expression, and spatial context into a shared molecular–morphological representation that is then used for two high-value tasks: discovering biologically coherent spatial tissue domains and predicting spatially-resolved gene expression directly from H&E images across 11 cancer types. The clinical significance is substantial—spatial transcriptomics costs hundreds of dollars per sample and is out of reach for most clinical settings, while H&E is universally available; STORM effectively unlocks molecular profiling of existing pathology archives at zero additional sequencing cost, and its multi-organ generalization suggests it will transfer to new tumor types with minimal fine-tuning.
Code / weights: Not released

---

**2. CrossLLM-Mamba: Multimodal State Space Fusion of LLMs for RNA Interaction Prediction**
*(arXiv 2602.22236)*

CrossLLM-Mamba introduces a genuinely novel idea: reformulating interaction prediction between RNA and three distinct molecular partners (proteins, small molecules, other RNAs) as a state-space alignment problem, where bidirectional Mamba encoders communicate across modalities through hidden state propagation rather than through attention cross-attention heads. This avoids the quadratic complexity that has constrained transformer-based RNA interaction models to short sequences and enables deep "crosstalk" between the LLM embeddings of each modality. The fact that a single unified architecture achieves state-of-the-art on all three interaction categories simultaneously—while remaining computationally tractable for full-length RNA transcripts—makes CrossLLM-Mamba a step-change for computational RNA drug discovery, where the ability to simultaneously predict a lead molecule's RNA–protein and RNA–small-molecule binding landscape is critical for off-target risk assessment.
Code / weights: Not released

---

**3. RosettaSearch: Multi-Objective Inference-Time Search for Protein Sequence Design**
*(arXiv 2604.17175)*

RosettaSearch makes a striking empirical claim: off-the-shelf reasoning-capable LLMs (o4-mini, Gemini-3) can serve as effective generative optimizers for the hard combinatorial problem of backbone-conditioned protein sequence design, without any model retraining, simply by operating as proposal generators inside a multi-objective search loop that scores candidates with RosettaFold3. Across 400 protein targets, RosettaSearch recovers high-fidelity designs that LigandMPNN's single-pass decoding fails to produce, with structural fidelity improvements of 18–68% and a 2.5× increase in design success rate. Performance scales predictably with the LLM's reasoning capability, establishing a direct link between progress on general AI reasoning and practical protein engineering throughput—every future LLM generation will automatically improve protein design without task-specific training.
Code / weights: Not released

---

==============================================================
DAILY STATS
==============================================================
- Total papers found today: 16
- By topic: Protein LM: 5 | Flow Matching: 1 | Genomics: 5 | SSM/Architecture: 2 | General ML: 4 | Clinical ML: 3
- Sources: arXiv: 10 | bioRxiv: 1 | Nature Machine Intelligence: 2 | Nature Computational Science: 1 | Nature Communications: 1 | PubMed: 0 | HF Papers: 0 | PWC: 0
- Papers with code released: 0
