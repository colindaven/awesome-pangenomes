# Awesome-pangenomes

> [!Note]
> A curated list of software for pangenome analysis, primarily focused on **eukaryotic genomes**.
> A new section for microbial genomes has also been added. These tools may not scale well to large genomes.

_Last updated: March 2026_

🚀 : widely used or popular repository

🆕✨ : new tool

💤: unmaintained

⚠️: outdated

---

## Contents
- [Important blog posts](#important-blog-posts)
- [Toolkits](#toolkits)
- [Pangenome construction](#pangenome-construction)
- [Pangenome construction with De Bruijn graphs](#pangenome-construction-with-de-bruijn-graphs)
- [Pangenome pipelines](#pangenome-pipelines)
- [Annotating pangenomes](#annotating-pangenomes)
- [Short-read alignment to a pangenome graph](#short-read-alignment-to-a-pangenome-graph)
- [Long-read alignment to a pangenome graph](#long-read-alignment-to-a-pangenome-graph)
- [SNP and structural variant callers and genotypers](#snp-and-structural-variant-callers-and-genotypers)
- [Transcriptome analysis](#transcriptome-analysis)
- [Methylation analysis](#methylation-analysis)
- [Repeat analysis](#repeat-analysis)
- [Metagenome analysis](#metagenome-analysis)
- [Pangenome viewers – interactive](#pangenome-viewers--interactive)
- [Pangenome viewers – static](#pangenome-viewers--static)
- [Graph analysis and quality assessment](#graph-analysis-and-quality-assessment)
- [Graph validation tools](#graph-validation-tools)
- [Pangenome comparison](#pangenome-comparison)
- [Pangenome tools for microbes](#pangenome-tools-for-microbes)
- [File formats](#file-formats)
- [Miscellaneous tools](#miscellaneous-tools)
- [Libraries to explore pangenomes](#libraries-to-explore-pangenomes)
- [Tutorials and reviews](#tutorials-and-reviews)
- [Other lists of pangenome tools](#other-lists-of-pangenome-tools)

---

# Important blog posts

- [Untangling graphical pangenomics](https://ekg.github.io/2019/07/09/Untangling-graphical-pangenomics) — explains differences between rGFA and GFA formats (*important and frequently overlooked*).
- [On the definition of pangenome](https://lh3.github.io/2024/03/29/what-is-a-pangenome) — Overview of how the definition and usage of the pangenome concept have changed across fields and over time. 🆕✨

---

# Toolkits

- [odgi](https://github.com/pangenome/odgi) — fast toolkit for variation graphs (ODGI format) :rocket:
- [vg](https://github.com/vgteam/vg) — comprehensive toolkit for graph construction, mapping, and variant calling :rocket:
- [gaftools](https://github.com/marschall-lab/gaftools) — GAF (Graph Alignment Format) manipulation
- [gfakluge](https://github.com/edawson/gfakluge) — GFA toolkit and C++ API
- [gfatools](https://github.com/lh3/gfatools) — GFA parsing and conversion
- [gretl](https://github.com/MoinSebi/gretl) — statistics and analysis for GFA (Rust)
- [pgr-tk](https://github.com/GeneDx/pgr-tk) — pangenomic toolkit (non-GFA output)
- [GraSuite](https://forge.ird.fr/diade/GraSuite) — GFA manipulation and pangenome analysis
- [gratools](https://forge.ird.fr/diade/gratools) — efficient GFA graph processing and subgraph extraction

---

# Pangenome construction

- [Minigraph](https://github.com/lh3/minigraph) ([paper](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-020-02168-z)) — fast construction; outputs rGFA (GFA extension) :rocket:
- [minigraph-cactus](https://github.com/ComparativeGenomicsToolkit/cactus) ([docs](https://github.com/ComparativeGenomicsToolkit/cactus/blob/master/doc/pangenome.md)) ([paper](https://www.nature.com/articles/s41587-023-01793-w)) — scalable builder; outputs GFA/ODGI :rocket:
- [PGGB](https://github.com/pangenome/pggb) ([paper](https://www.nature.com/articles/s41592-024-02430-3)) — graph builder with integrated SNP detection :rocket:
- [pangene](https://github.com/lh3/pangene) ([paper](https://academic.oup.com/bioinformatics/article/40/7/btae456/7718494)) — gene-based pangenome graph construction and visualization :rocket:
- [Pantools](https://git.wur.nl/bioinformatics/pantools) ([paper](https://academic.oup.com/bioinformatics/article-abstract/38/18/4403/6647839)) — full-featured pangenome construction framework
- [PSVCP](https://github.com/wjian8/psvcp_v1.01) ([paper](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-023-02861-9)) — integrates PAV into linear genomes
- [PHG](https://bitbucket.org/bucklerlab/practicalhaplotypegraph/wiki/Home) — haplotype graph framework for genotyping
- [PATO](https://github.com/irycisBioinfo/PATO) ([paper](https://academic.oup.com/bioinformatics/article/37/23/4564/6384566)) — R-based pangenome analysis
- [Chrom_mini_graph](https://github.com/gaojunxuan/chrom_mini_graph) — colored minimizer graph construction and mapping
- [GET_PANGENES](https://github.com/Ensembl/plant-scripts/tree/master/pangenes) ([paper](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-023-03071-z)) — Ensembl pipelines for pan-gene sets
- [impg](https://github.com/ekg/impg) — implicit pangenome graph construction for homologous regions
- [MGRgraph](https://github.com/LeilyR/Multi-genome-Reference) ([preprint](https://www.biorxiv.org/content/10.1101/2020.04.11.036871)) — multi-genome reference construction (inactive)
- [MEMO](https://github.com/StephenHwang/MEMO) ([preprint](https://www.biorxiv.org/content/10.1101/2024.05.20.595044)) — k-mer-based conservation analysis and visualization
- [poasta](https://github.com/broadinstitute/poasta) — sequence-to-graph alignment and MSA (gap-affine)
- [SEQWISH](https://github.com/ekg/seqwish) ([paper](https://academic.oup.com/bioinformatics/article/39/1/btac743/6854971)) — unbiased graph construction
- [seqrush](https://github.com/pangenome/seqrush) — parallel seqwish-like construction
- [pannagram](https://github.com/iganna/pannagram) ([preprint](https://www.biorxiv.org/content/10.1101/2025.02.07.637071)) — SV detection using BLAST/MAFFT/R
- [pandagma](https://github.com/legumeinfo/pandagma) — pan-gene set construction from annotations
- [Panscan](https://github.com/CATG-Github/panscan) — SV/repeat discovery (human-focused)
- [CoreDetector](https://github.com/mfruzan/CoreDetector) ([paper](https://academic.oup.com/bioinformatics/article/39/11/btad628/7329718)) — core genome alignment
- [PanKmer](https://gitlab.com/salk-tm/pankmer) ([paper](https://academic.oup.com/bioinformatics/article/39/10/btad621/7319363)) — reference-free k-mer pangenomics
- [Panaln](https://github.com/Lilu-guo/Panaln) — construction and read alignment
- [AlfaPang](https://github.com/AdamCicherski/AlfaPang) ([paper](https://almob.biomedcentral.com/articles/10.1186/s13015-025-00277-7)) — alignment-free graph construction

---

# Pangenome construction with De Bruijn graphs

- [Bifrost](https://github.com/pmelsted/bifrost) — colored and compacted De Bruijn graphs
- [TwoPaCo](https://github.com/medvedevgroup/TwoPaCo) — compacted De Bruijn graph construction
- [Nexus](https://github.com/biointec/nexus) — bidirectional FM-index-based graph construction
- [Graphite](https://github.com/MGXlab/Graphite) — genome painting using colored De Bruijn graphs
- [BCALM 2](https://github.com/GATB/bcalm) — ultra-low-memory De Bruijn graph construction

---

# Pangenome pipelines

- [nf-core/pangenome](https://github.com/nf-core/pangenome) — scalable Nextflow pipeline (PGGB + ODGI) :rocket:
- [pangepop](https://forgemia.inra.fr/pangepop/pangepop) — Snakemake pipeline (minigraph-cactus + vg)

---

# Annotating pangenomes

- [GrAnnoT](https://forge.ird.fr/diade/dynadiv/grannot) — annotation transfer across graphs
- [Annotation scripts](https://github.com/jmonlong/manu-vggafannot/tree/main/analysis) — annotation of minigraph-cactus graphs

---

# Short-read alignment to a pangenome graph

- [vg giraffe](https://github.com/vgteam/vg) — fast graph mapper :rocket:
- [vg map](https://github.com/vgteam/vg) — legacy mapper
- [HISAT2](https://github.com/DaehwanKimLab/hisat2) — graph FM-index aligner
- [Minigraph](https://github.com/lh3/minigraph) — graph alignment (short/long reads)
- [Chrom_mini_graph](https://github.com/gaojunxuan/chrom_mini_graph) — minimizer graph mapping
- [Panaln](https://github.com/Lilu-guo/Panaln) — integrated construction and alignment
- [theseus](https://github.com/albertjimenezbl/theseus-lib) ([preprint](https://www.biorxiv.org/content/10.64898/2026.02.12.705572v1)) — sequence-to-graph alignment library

---

# Long-read alignment to a pangenome graph

- [GraphAligner](https://github.com/maickrau/GraphAligner) — long-read graph aligner :rocket:
- [vg giraffe](https://github.com/vgteam/vg) — experimental long-read support :rocket:
- [Minigraph](https://github.com/lh3/minigraph) — graph alignment
- [GraphChainer](https://github.com/algbio/GraphChainer) — built on GraphAligner
- [SPAdes PathRacer](https://github.com/eodus/pathracer#sec4.3) — path finding in graphs
- [Minichain](https://github.com/at-cg/minichain) — long-read alignment to GFA/rGFA
- [PanAligner](https://github.com/at-cg/PanAligner) — long-read graph alignment
- [poasta](https://github.com/broadinstitute/poasta) — sequence-to-graph alignment
- [PALSS](https://github.com/ldenti/palss) — graph augmentation from long reads

---

# SNP and structural variant callers and genotypers

- [vg call](https://github.com/vgteam/vg) — graph-based variant calling :rocket:
- [vg surject](https://github.com/vgteam/vg) — projection to linear reference :rocket:
- [Paragraph](https://github.com/Illumina/paragraph) — graph genotyping (short reads)
- [PanGenie](https://github.com/eblerjana/pangenie) — k-mer-based SV genotyping
- [DeepVariant](https://github.com/google/deepvariant) — deep learning variant calling
- [Varigraph](https://github.com/JiaoLab2021/varigraph) — graph genotyper (diploid/polyploid)
- [GraphTyper](https://github.com/DecodeGenetics/graphtyper) — SV genotyping (no discovery)
- [SVarp](https://github.com/asylvz/SVarp) — SV detection from graph alignments
- [bubblegun](https://github.com/fawaz-dabbaghieh/bubble_gun) — bubble/superbubble detection
- [PHI](https://github.com/at-cg/PHI) — haplotype inference on graphs
- [Ctyper](https://github.com/ChaissonLab/Ctyper) — copy-number-aware genotyping
- [rs-gfa-utils](https://github.com/chfi/rs-gfa-utils) — GFA utilities and SV extraction
- [BayesTyper](https://github.com/bioinformatics-centre/BayesTyper) — graph-based genotyping
- [Swave](https://github.com/songbowang125/Swave) — SV detection from pangenome graphs 🆕✨
- [APAV](https://github.com/SJTU-CGM/APAV) — PAV detection and visualization
- [PangenomeX](https://github.com/Nevermore233/PangenomeX) — shallow CNV detection
- [SVPG](https://github.com/coopsor/SVPG) — SV detection and graph augmentation
- [Floco](https://github.com/hugocarmaga/floco) — node copy number inference
- [DipGenie](https://github.com/gsc74/DipGenie) — phased diploid inference
- [Cosigt](https://github.com/davidebolo1993/cosigt) — haplotype-based SV genotyping

---

# Repeat analysis

- [Pantera](https://github.com/piosierra/pantera) — transposable element family identification
- [GraffeTE](https://github.com/cgroza/GraffiTE) — TE insertion polymorphism analysis

---

# Metagenome analysis

- [PanTax](https://github.com/LuoGroup2023/PanTax) — strain-level metagenomic classification

---

# Pangenome viewers – interactive

- [Bandage](https://github.com/rrwick/Bandage) — GFA graph viewer :rocket:
- [BandageNG](https://github.com/asl/BandageNG) — extended Bandage
- [SeqTubeMap](https://github.com/vgteam/sequenceTubeMap) — path visualization :rocket:
- [MoMI-G](https://github.com/MoMI-G/MoMI-G/) — SV visualization :rocket:
- [PanGraphViewer](https://github.com/TF-Chan-Lab/panGraphViewer) — desktop/web viewer
- [JBrowse 2](https://jbrowse.org) — genome browser with graph plugins
- [gfaestus](https://github.com/chfi/gfaestus) — GPU-accelerated GFA viewer

---

# Pangenome viewers – static

- [vg view](https://github.com/vgteam/vg) — static graph rendering
- [odgi](https://github.com/pangenome/odgi) — genome-scale visualization :rocket:
- [plotsr](https://github.com/schneebergerlab/plotsr) — synteny visualization

---

# Graph analysis and quality assessment

- [PG-SCUnK](https://github.com/cumtr/PG-SCUnK/) — graph quality via unique k-mers
- [Panacus](https://github.com/marschall-lab/panacus) — core size and growth estimation
- [Pansel](https://github.com/mzytnicki/pansel) — detection of over-/under-diverse regions

---

# Graph validation tools

- [vg validate](https://github.com/vgteam/vg) — graph validation
- [odgi validate](https://github.com/pangenome/odgi) — graph validation

---

# Pangenome comparison

- [junctions](https://github.com/urbanslug/junctions) — elastic-degenerate comparison
- [rs-pancat-compare](https://github.com/dubssieg/rs-pancat-compare) — segmentation edit distance

---

# Pangenome tools for microbes

- [anvi'o](https://merenlab.org/2016/11/08/pangenomics-v2/) — microbial pangenomics platform (limited eukaryotic support)
- [Roary](https://github.com/sanger-pathogens/Roary) — microbial pan-genome analysis from GFF

---

# File formats

- [GFA](http://gfa-spec.github.io/GFA-spec/GFA1.html) — assembly graph format :rocket:
- [ODGI](https://github.com/pangenome/odgi) — graph format and toolkit :rocket:
- [rGFA](https://github.com/lh3/gfatools/blob/master/doc/rGFA.md) — GFA extension with reference paths
- [vg formats](https://github.com/vgteam/vg/wiki/File-Formats) — vg-specific formats
- [PanSN-spec](https://github.com/pangenome/PanSN-spec) — haplotype naming scheme
- [GAF](https://github.com/lh3/gfatools/blob/master/doc/rGFA.md#the-graph-alignment-format-gaf) — graph alignment format
- [GAM](https://github.com/vgteam/vg/wiki/File-Formats#gam-graph-alignment--map-vgs-bam) — vg alignment format

---

# Miscellaneous tools

- [gfainject](https://github.com/chfi/gfainject) — convert BAM alignments to GFA/GAF
- [GRAFIMO](https://github.com/pinellolab/GRAFIMO) — motif scanning on graphs
- [rs-gfa](https://github.com/chfi/rs-gfa) — GFA parser (Rust)
- [ropebwt3](https://github.com/lh3/ropebwt3) — large-scale indexing and alignment
- [pollen](https://github.com/cucapra/pollen) — experimental pangenome toolkit
- [mumemto](https://github.com/vikshiv/mumemto) — MUM-based analysis and visualization
- [gfa2bin](https://github.com/MoinSebi/gfa2bin) — convert graphs to PLINK format
- [vizitig](https://gitlab.inria.fr/vizisoft/vizitig) — graph construction with annotation and visualization
- [gafpack](https://github.com/pangenome/gafpack) — node coverage from GAF
- [TeraTools](https://github.com/ucfcbb/TeraTools) — terabase-scale pangenome analysis

---

# Libraries to explore pangenomes

- [gfapy](https://github.com/ggonnella/gfapy) — GFA parsing (Python)
- [gfagraphs](https://github.com/Tharos-ux/gfagraphs) — GFA/rGFA manipulation (Python)
- [graphanalyzer](https://github.com/sablokgaurav/graphanalyzer) — GFA/PAF analysis
- [theseus](https://github.com/albertjimenezbl/theseus-lib) — sequence-to-graph alignment library

---

# Tutorials and reviews

- [INRA pangenome tutorial](https://pangenome-hackathon-genotoul-bioinfo-11d6d4f47ac33734abfa2a1377.pages.mia.inra.fr/pages/tutorial_pangenome_graph/)
- [Bao 2025 review](https://www.cambridge.org/core/journals/quantitative-plant-biology/article/complexity-welcome-pangenome-graphs-for-comprehensive-population-genomics/B2DD25F2FD0B4CB91D238DFD2257E7FA)

---

# Other lists of pangenome tools

- [Practical Pangenome Graphs](https://pangenome.github.io/)
- [awesome-genome-visualization](https://cmdcolin.github.io/awesome-genome-visualization/)

---

# Contributions

Contributions are welcome. Submit pull requests to the main branch or open an issue with relevant resources.
