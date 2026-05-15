# Research Digest — 2026-05-15

> **Scope:** Papers posted or published in the last ~24 hours across arXiv (cs.LG, cs.AI, q-bio.BM, q-bio.QM, q-bio.GN, stat.ML, cs.NE), bioRxiv, medRxiv, PubMed, Hugging Face Papers, Semantic Scholar, and Papers With Code.  
> **Focus areas:** Protein & Molecular ML · Generative Models in Biology · Sequence & Genome Models · Architecture Innovations · General Cutting-Edge ML · Clinical & Translational ML

---

## PAPERS

---

TITLE: ENSEMBITS: An Alphabet of Protein Conformational Ensembles
AUTHORS: (arXiv 2605.13789 team) et al.
SOURCE: arXiv | 2605.13789 | [**Link**](https://arxiv.org/abs/2605.13789)
TOPIC TAG: Protein LM / Architecture
TLDR: ENSEMBITS is the first tokenizer of protein conformational ensembles, trained with a Residual VQ-VAE using a frame distillation objective on a large molecular dynamics corpus, outperforming all methods on RMSF prediction while matching or exceeding static tokenizers on EC, GO, binding site, affinity, and zero-shot mutation-effect prediction.
WHY IT MATTERS: All existing protein structure tokenizers encode only local geometry of a single static conformation, discarding the correlated motions and alternative states that govern function and drive drug resistance; ENSEMBITS is the first vocabulary to capture ensemble-level dynamics in a discrete token space. Because the frame distillation objective lets ENSEMBITS predict dynamics tokens from a single predicted structure, it sidesteps the data sparsity bottleneck, providing an immediately deployable dynamic prior for protein language modeling and ensemble-generative design.
CODE: Not released

---

TITLE: DPLM-Evo: Towards A Generative Protein Evolution Machine
AUTHORS: (arXiv 2605.00182 team) et al.
SOURCE: arXiv | 2605.00182 | [**Link**](https://arxiv.org/abs/2605.00182)
TOPIC TAG: Diffusion / Protein LM
TLDR: DPLM-Evo is an evolutionary discrete diffusion protein language model that explicitly predicts substitution, insertion, and deletion operations during denoising by decoupling a variable-length latent alignment space from the observed sequence space, achieving state-of-the-art mutation effect prediction on ProteinGym and enabling length-variable in silico protein evolution for the first time. (ICML 2026)
WHY IT MATTERS: All prior masked diffusion protein LMs use a masking-based absorbing process that has no biological analogy—proteins do not emerge from masks but evolve through accumulated edits including indels; DPLM-Evo's contextualized evolutionary noising kernel produces biologically informed, context-dependent mutation patterns that respect conservation gradients. This unlocks a new class of application: explicit edit-trajectory optimization for post-editing or scaffold growth on existing proteins without full-sequence redesign.
CODE: Not released (ICML 2026 accepted; code to be released)

---

TITLE: Proteo-R1: Reasoning Foundation Models for De Novo Protein Design
AUTHORS: (arXiv 2605.02937 team) et al.
SOURCE: arXiv | 2605.02937 | [**Link**](https://arxiv.org/abs/2605.02937)
TOPIC TAG: Protein LM / General ML
TLDR: Proteo-R1 decouples protein design into a multimodal LLM understanding expert that identifies key functional residues and passes them as hard constraints to a diffusion-based generation expert, combining chain-of-thought structural reasoning with conditional geometric co-design.
WHY IT MATTERS: Existing diffusion-based design models are non-deliberative—they directly synthesize geometries without reasoning about which residues govern binding or specificity, making designs difficult to audit or steer; Proteo-R1's reasoning-geometry factorization mirrors expert human design workflows and provides interpretable checkpoints at the residue-specification stage. The dual-expert architecture sets a new precedent for integrating LLM-scale reasoning with geometric deep learning in molecular design.
CODE: [**Project page**](https://smiles724.github.io/r1/)

---

TITLE: Yeti: A Compact Protein Structure Tokenizer for Reconstruction and Multi-modal Generation
AUTHORS: Giri, N. et al.
SOURCE: arXiv | 2605.09981 | [**Link**](https://arxiv.org/abs/2605.09981)
TOPIC TAG: Protein LM / Architecture
TLDR: Yeti is a protein structure tokenizer trained end-to-end with a flow matching objective using lookup-free quantization, achieving the best codebook utilization and token diversity with 10× fewer parameters than ESM3 and enabling joint unconditional sequence-structure cogeneration competitive with models 10× larger.
WHY IT MATTERS: Existing structure tokenizers are trained with reconstruction losses that are misaligned with downstream generative modeling objectives, creating a bottleneck when those tokens are consumed by autoregressive or diffusion protein models; Yeti directly optimizes the tokenizer for generative compatibility, removing the reconstruction-generation mismatch at the source. The 10× parameter reduction makes multimodal protein generation more accessible for smaller research groups.
CODE: Not released

---

TITLE: ProteinJEPA: Latent Prediction Complements Protein Language Models
AUTHORS: Ofer, D. et al.
SOURCE: arXiv | 2605.07554 | [**Link**](https://arxiv.org/abs/2605.07554)
TOPIC TAG: Protein LM
TLDR: Masked-position MLM+JEPA — adding joint embedding prediction at masked positions on top of standard MLM in protein language models — wins 10 of 16 downstream tasks versus 3 losses against MLM-only training under matched wall-clock budgets on ESM2 at 35M and 150M scales.
WHY IT MATTERS: JEPA-style latent prediction has demonstrated strong representation learning in vision and video but had not been systematically evaluated for protein sequences; the masked-position recipe is a minimal, immediately applicable training improvement that consistently lifts downstream performance with no architectural change to existing protein LMs. The analysis reveals that latent prediction and token-level MLM provide complementary supervision signals, suggesting that combining them should become standard practice in protein foundation model training.
CODE: Not released

---

TITLE: MicroFuse: Protein-to-Genome Expert Fusion for Microbial Operon Reasoning
AUTHORS: Cho, S. et al.
SOURCE: arXiv | 2605.08815 | [**Link**](https://arxiv.org/abs/2605.08815)
TOPIC TAG: MoE / Architecture / Genomics
TLDR: MicroFuse integrates ProstT5 structure-aware protein embeddings with Bacformer genome-context embeddings via a four-expert soft MoE module (protein, genome-context, agreement, conflict experts) with cross-modal contrastive alignment, trained on OG-Operon100K, achieving SOTA AUROC and AUPRC for prokaryotic operon prediction.
WHY IT MATTERS: Operon prediction requires simultaneously reasoning about protein biochemistry and genomic co-localization signals that existing single-modality methods treat separately and incompletely; the soft MoE fusion with explicitly named agreement and conflict experts is a principled way to handle modality disagreement without forcing a single unified embedding. MicroFuse's OG-Operon100K dataset, derived from the OMG metagenomic corpus, also provides the most biologically rigorous benchmark for operon prediction to date.
CODE: Not released

---

TITLE: SCOPE: Siamese Contrastive Operon Pair Embeddings for Functional Sequence Representation and Classification
AUTHORS: Gupta, A. et al.
SOURCE: arXiv | 2605.11022 | [**Link**](https://arxiv.org/abs/2605.11022)
TOPIC TAG: Genomics
TLDR: SCOPE uses a Siamese MLP over contrastively aligned protein language model embeddings to classify prokaryotic gene pairs as co-operonic or not, achieving ROC-AUC of 0.71 competitive with state-of-the-art on the DGEB leaderboard, with cosine similarity over the learned embedding space largely sufficient for the classification task.
WHY IT MATTERS: Operon identification is critical for reconstructing gene regulatory networks and annotating unannotated microbial genes, but existing methods require organism-specific tuning; SCOPE's contrastive embedding approach transfers across organisms without labeled interaction data. The finding that learned cosine geometry encodes most operon structure without a trained head suggests protein LM embeddings already contain rich co-regulatory information accessible through simple contrastive training.
CODE: Not released

---

TITLE: ToolMol: Evolutionary Agentic Framework for Multi-objective Drug Discovery
AUTHORS: (arXiv 2605.12784 team) et al.
SOURCE: arXiv | 2605.12784 | [**Link**](https://arxiv.org/abs/2605.12784)
TOPIC TAG: General ML / Molecular ML
TLDR: ToolMol combines a multi-objective genetic algorithm with an agentic LLM operator that modifies molecules via structured tool calls rather than raw SMILES string edits, achieving SOTA multi-objective property optimization across three protein targets with predicted binding affinity gains exceeding 10% over prior methods.
WHY IT MATTERS: Direct LLM manipulation of SMILES strings produces high rates of invalid molecules because LLMs lack syntactic awareness of molecular grammar; abstracting modifications through tool-calling APIs enforces structural validity at the generation step rather than requiring post-hoc filtering. The evolutionary loop over the LLM operator integrates population-level diversity pressure with per-molecule LLM refinement, a combination that outperforms both stand-alone evolutionary algorithms and stand-alone generative models.
CODE: Not released

---

TITLE: Set-Aggregated Genome Embeddings (SAGE) for Microbiome Abundance Prediction
AUTHORS: Kim, Y. et al.
SOURCE: arXiv | 2605.12286 | [**Link**](https://arxiv.org/abs/2605.12286)
TOPIC TAG: Genomics / General ML
TLDR: SAGE exploits the few-shot learning capabilities of genomic language models to predict community-level microbiome abundance profiles directly from raw genome DNA sequences using set-level aggregation, demonstrating improved generalization to novel genomes compared to classical bioinformatics approaches.
WHY IT MATTERS: Classical microbiome abundance estimation relies on read-mapping to reference databases and fails for novel or undercharacterized organisms; SAGE's use of GLM embeddings as universal genome descriptors enables community abundance prediction without reference databases, making it directly applicable to metagenomic datasets from poorly studied environments. The set-aggregation design cleanly separates individual genome representation from community-level prediction, providing a modular framework for plugging in better foundation models as they emerge.
CODE: Not released

---

TITLE: ReCoG: Relational and Compact Context Graph Learning for Few-shot Molecular Property Prediction
AUTHORS: Wang, Z. et al.
SOURCE: arXiv | 2605.13024 | [**Link**](https://arxiv.org/abs/2605.13024)
TOPIC TAG: General ML / Molecular ML
TLDR: ReCoG constructs relational and compact context graphs over support molecules to address insufficient structural context modeling and redundant auxiliary context in few-shot molecular property prediction, submitted to ICML 2026 and achieving state-of-the-art performance on standard FSMPP benchmarks.
WHY IT MATTERS: Drug discovery and materials design routinely require predicting molecular properties from only a handful of labeled examples; existing context-aware few-shot methods struggle to distinguish genuinely task-relevant structural context from noisy auxiliary information. ReCoG's compaction step selectively retains high-signal structural relationships, directly improving data efficiency and making the approach more suitable for early-stage discovery where labeled data is scarcest.
CODE: Not released

---

TITLE: From Enhanced Sampling to Human-Readable Representations of Protein Dynamics
AUTHORS: (arXiv 2605.03394 team) et al.
SOURCE: arXiv | 2605.03394 | [**Link**](https://arxiv.org/abs/2605.03394)
TOPIC TAG: Protein LM / General ML
TLDR: A fully automated pipeline that transforms enhanced sampling MD trajectories into interpretable protein dynamics representations by applying frequency-selective anharmonic mode analysis followed by weighted dynamic cross-correlation matrix decomposition, extracting human-readable coupled-motion signatures without manual feature engineering.
WHY IT MATTERS: Enhanced sampling generates enormous volumes of MD data that researchers cannot efficiently interpret without domain-specific manual curation; automated extraction of coupled-motion signatures provides a scalable bridge between simulation and biological insight. The resulting representations encode allosteric communication pathways and conformational switching events in a format directly usable by protein language models or as features for downstream property prediction.
CODE: Not released

---

TITLE: Adaptive Memory Decay for Log-Linear Attention
AUTHORS: (arXiv 2605.06946 team) et al.
SOURCE: arXiv | 2605.06946 | [**Link**](https://arxiv.org/abs/2605.06946)
TOPIC TAG: Architecture / SSM
TLDR: Proposes log-linear attention that organizes key-value memory across a Fenwick tree hierarchy, growing the hidden state logarithmically with sequence length at log-linear compute cost, with adaptive memory decay tuned per-head to balance short- and long-range retention.
WHY IT MATTERS: Quadratic attention is the primary bottleneck for genomic and protein language models that need context windows of 100k+ base pairs or amino acids; log-linear attention's hierarchical memory achieves O(L log L) compute without the fixed-decay bias of existing linear attention variants, potentially enabling sub-quadratic genomic foundation models that retain long-range regulatory signals. The per-head adaptive decay is an important flexibility advantage over uniform-decay alternatives like Mamba or Hyena.
CODE: Not released

---

TITLE: RNA-FM: Flow-Matching Generative Model for Genome-wide RNA-Seq Prediction
AUTHORS: Song, Y. et al.
SOURCE: arXiv | 2605.11622 | [**Link**](https://arxiv.org/abs/2605.11622)
TOPIC TAG: Flow Matching / Clinical ML
TLDR: RNA-FM formulates genome-wide bulk RNA-seq prediction from histopathology whole-slide images as a continuous-time conditional transport problem via flow matching, learning a velocity field mapping a Gaussian prior to the full transcriptome distribution conditioned on tissue morphology.
WHY IT MATTERS: Sequencing-based transcriptomics is expensive and cannot be performed retrospectively on archived FFPE slides; RNA-FM's generative framing properly captures biological heterogeneity and uncertainty in the transcriptome-morphology mapping rather than collapsing to a point estimate, enabling probabilistic inference of molecular programs from standard pathology workflows. The flow matching objective avoids mode collapse seen in prior GAN-based spatial expression predictors, recovering long-tailed gene expression distributions critical for rare-cell-type characterization.
CODE: Not released

---

TITLE: D3LM: A Discrete DNA Diffusion Language Model for Bidirectional DNA Understanding and Generation
AUTHORS: Yang, Z. et al.
SOURCE: arXiv | 2603.01780 | [**Link**](https://arxiv.org/abs/2603.01780)
TOPIC TAG: Diffusion / Genomics
TLDR: D3LM reformulates the Nucleotide Transformer v2 architecture as a masked diffusion model in discrete DNA space, unifying bidirectional sequence understanding with generative DNA synthesis, achieving an SFID of 10.92 on regulatory element generation versus the previous best of 29.16 from autoregressive models.
WHY IT MATTERS: Autoregressive DNA models sacrifice bidirectionality—the fundamental strand-symmetry of DNA regulatory relationships—while BERT-style models cannot generate; D3LM is the first model to achieve both in a single unified training objective by treating generation as a masked diffusion process over nucleotides. The systematic study of tokenization schemes and sampling strategies for masked DNA diffusion provides the community with empirically validated design recipes for this new model class.
CODE: [**Code & models**](https://huggingface.co/collections/Hengchang-Liu/d3lm)

---

==============================================================
HIGHLIGHTS OF THE DAY
==============================================================

### 1. ENSEMBITS: An Alphabet of Protein Conformational Ensembles
*arXiv 2605.13789*

ENSEMBITS is the first discrete tokenizer designed for protein conformational ensembles rather than static structures, trained with a Residual VQ-VAE and a novel frame distillation objective on large-scale molecular dynamics data. By encoding correlated motions and alternative conformational states into discrete tokens, it enables protein language models to reason about protein dynamics for the first time—matching or beating static tokenizers on every standard function prediction benchmark while also capturing RMSF (flexibility) patterns that static tokenizers are blind to. As generative biology shifts from single-structure prediction toward ensemble generation, ENSEMBITS provides the crucial discrete vocabulary that is a prerequisite for training dynamics-aware protein LMs and designing proteins with specified flexibility profiles.
Code: Not released

---

### 2. DPLM-Evo: Towards A Generative Protein Evolution Machine
*arXiv 2605.00182 | ICML 2026*

DPLM-Evo addresses a foundational mismatch in discrete diffusion protein models: all prior approaches use mask-absorbing diffusion despite the fact that proteins evolve through substitutions, insertions, and deletions—not emergence from masks. By introducing a decoupled latent alignment space that separates variable-length observation sequences from fixed-length latent representations, DPLM-Evo makes indel-aware generation tractable without changing the inference-time compute budget. It sets a new state of the art on ProteinGym mutation effect prediction in the single-sequence setting and demonstrates length-variable in silico evolution—a capability with direct applications to antibody affinity maturation, enzyme active-site remodeling, and scaffold extension.
Code: To be released (ICML 2026)

---

### 3. Proteo-R1: Reasoning Foundation Models for De Novo Protein Design
*arXiv 2605.02937*

Proteo-R1 introduces a reasoning-geometry factorization to de novo protein design: a multimodal LLM first analyzes sequence, structure, and textual annotations to identify which residues govern binding or specificity via explicit chain-of-thought reasoning, then passes these residue-level decisions as hard geometric constraints to a diffusion co-design model. This mirrors how human protein engineers actually operate—first reasoning about critical interaction anchors, then optimizing backbone geometry subject to those constraints—and produces designs with greater interpretability and controllability than end-to-end diffusion alone. The dual-expert architecture establishes a new paradigm for combining LLM-scale reasoning with geometric deep learning that is likely to generalize broadly to RNA design, small-molecule optimization, and materials discovery.
Code: [**Project page**](https://smiles724.github.io/r1/)

---

==============================================================
DAILY STATS
==============================================================
- Total papers found today: 14
- By topic: Protein LM: 6 | Diffusion: 3 | Flow Matching: 1 | Genomics: 4 | Architecture: 3 | MoE: 1 | General ML: 3 | Clinical ML: 1
- Sources: arXiv: 14 | bioRxiv: 0 | medRxiv: 0 | PubMed: 0 | HF Papers: 1 | PWC: 0
- Papers with code released: 2 (Proteo-R1 project page; D3LM HuggingFace)
