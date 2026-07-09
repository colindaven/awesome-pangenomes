[![DOI](https://zenodo.org/badge/608649460.svg)](https://doi.org/10.5281/zenodo.18208384)

# awesome-pangenomes
## A list of software capable of analyzing mainly **eukaryotic** genomes for pangenomics. 

A new section for microbial genomes has also been added, these tools may not scale to large genomes. 

:rocket: indicates a popular repository

## Contents
- [Important blog posts](#important-blog-posts)
- [Pangenome construction](#pangenome-construction)
- [Pangenome construction with De Bruijn graphs](#pangenome-construction-with-de-bruijn-graphs)
- [Pangenome pipelines](#pangenome-pipelines)
- [Annotating pangenomes](#annotating-pangenomes)
- [Short read alignment to a pangenome graph](#short-read-alignment-to-a-pangenome-graph)
- [Long read alignment to a pangenome graph](#long-read-alignment-to-a-pangenome-graph)
- [SNP and Structural Variant callers and genotypers](#snp-and-structural-variant-callers-and-genotypers)
- [Transcriptome analysis](#transcriptome-analysis)
- [Methylation analysis](#methylation-analysis)
- [Repeat analysis](#repeat-analysis)
- [Metagenome analysis](#metagenome-analysis)
- [Pangenome viewers - interactive](#pangenome-viewers---interactive)
- [Pangenome viewers - static](#pangenome-viewers---static)
- [Graph analysis and quality assessment](#graph-analysis-and-quality-assessment)
- [Graph validation tools](#graph-validation-tools)
- [Pangenome comparison](#pangenome-comparison)
- [Pangenome tools for microbes](#pangenome-tools-for-microbes)
- [File formats](#file-formats)
- [Miscellaneous tools](#miscellaneous-tools)
- [Libraries to explore pangenomes](#libraries-to-explore-pangenomes)
- [Tutorials and reviews](#tutorials-and-reviews)
- [Other lists of pangenome tools](#other-lists-of-pangenome-tools) 

# Important blog posts

| Title | Author | Year | Link |
|-------|--------|------|------|
| A proposal of the Graphical Fragment Assembly format | Heng Li | 2014 | [Post](https://lh3.github.io/2014/07/19/a-proposal-of-the-grapical-fragment-assembly-format) |
| First update on GFA | Heng Li | 2014 | [Post](https://lh3.github.io/2014/07/23/first-update-on-gfa) |
| On the graphical representation of sequences | Heng Li | 2014 | [Post](https://lh3.github.io/2014/07/25/on-the-graphical-representation-of-sequences) |
| On a reference pan-genome model (Part I) | Heng Li | 2019 | [Post](https://lh3.github.io/2019/07/08/on-a-reference-pan-genome-model) |
| On a reference pan-genome model (Part II) | Heng Li | 2019 | [Post](https://lh3.github.io/2019/07/12/on-a-reference-pan-genome-model-part-ii) |
| Untangling graphical pangenomics | Erik Garrison | 2019 | [Post](https://ekg.github.io/2019/07/09/Untangling-graphical-pangenomics) |
| On the definition of pangenome | Heng Li | 2024 | [Post](https://lh3.github.io/2024/03/29/what-is-a-pangenome) |

# Toolkits

| Tool | Repository | Description | Status |
|------|-----------|-------------|--------|
| odgi | [GitHub](https://github.com/pangenome/odgi) | Fast toolkit based on odgi format | :rocket: |
| vg | [GitHub](https://github.com/vgteam/vg) | Full featured construction, mapping and SNP calling toolkit based on multiple formats | :rocket: |
| gaftools | [GitHub](https://github.com/marschall-lab/gaftools) | Toolkit for GAF (Graph Alignment Format) sorting and manipulation | |
| gfakluge | [GitHub](https://github.com/edawson/gfakluge) | Toolkit and c++ API for GFA manipulation | |
| gfatools | [GitHub](https://github.com/lh3/gfatools) | Toolkit for GFA parsing and conversion | |
| gretl | [GitHub](https://github.com/MoinSebi/gretl) | Statistics and analysis for GFA files, written in Rust | |
| pgr-tk | [GitHub](https://github.com/GeneDx/pgr-tk) | A PanGenomic Research Toolkit | |
| GraSuite | [Forge](https://forge.ird.fr/diade/GraSuite) | A suite of tools for GFA pangenomes and graph manipulation | |
| gratools | [Forge](https://forge.ird.fr/diade/gratools) | Handle GFA genomes quickly, calculate node depth and other operations | |

# Pangenome construction

| Tool | Repository | Description | Status |
|------|-----------|-------------|--------|
| Minigraph | [GitHub](https://github.com/lh3/minigraph) | Fast method by Heng Li, produces referenceGFA (rGFA) format | |
| minigraph_cactus | [GitHub](https://github.com/ComparativeGenomicsToolkit/cactus) | Cactus-based pangenome construction | |
| PGGB | [GitHub](https://github.com/pangenome/pggb) | Pangenome Graph Builder, calculates SNPs as part of pipeline | :rocket: |
| pangene | [GitHub](https://github.com/lh3/pangene) | Constructs pangenome gene graph from one protein sequence | |
| Pantools v3+ | [Git](https://git.wur.nl/bioinformatics/pantools) | Fully featured construction of pangenome graphs | |
| PSVCP | [GitHub](https://github.com/wjian8/psvcp_v1.01) | Add PAV to linear genome to construct pangenome | |
| PHG | [Bitbucket](https://bitbucket.org/bucklerlab/practicalhaplotypegraph/wiki/Home) | Practical Haplotype Graph | |
| PATO | [GitHub](https://github.com/irycisBioinfo/PATO) | R package for pangenome construction | |
| Chrom_mini_graph | [GitHub](https://github.com/gaojunxuan/chrom_mini_graph) | Generate and map reads onto colored minimizer pangenome | |
| GET_PANGENES | [GitHub](https://github.com/Ensembl/plant-scripts/tree/master/pangenes) | Perl scripts used by Ensembl for pangenome construction | |
| impg | [GitHub](https://github.com/ekg/impg) | Create implicit pangenome graph for homologous target regions | |
| MGRgraph | [GitHub](https://github.com/LeilyR/Multi-genome-Reference) | Algorithm to build Multi-genome Reference | |
| MEMO | [GitHub](https://github.com/StephenHwang/MEMO) | Constructs pangenome with kmer-based conservation analysis | |
| poasta | [GitHub](https://github.com/broadinstitute/poasta) | Gap-affine sequence-to-graph and partial order aligner | |
| SEQWISH | [GitHub](https://github.com/ekg/seqwish) | Unbiased pangenome graphs | |
| seqrush | [GitHub](https://github.com/pangenome/seqrush) | Parallel pangenome construction using simplified seqwish algorithm | |
| pannagram | [GitHub](https://github.com/iganna/pannagram) | Construct pangenomes and find SVs using blast, mafft and R tools | |
| pandagma | [GitHub](https://github.com/legumeinfo/pandagma) | Calculate pan-gene sets from genome assemblies and annotations | |
| Panscan | [GitHub](https://github.com/CATG-Github/panscan) | Construct matrix identifying novel sequences, SVs, repetitive regions | |
| CoreDetector | [GitHub](https://github.com/mfruzan/CoreDetector) | Flexible program for core-genome identification | |
| PanKmer | [GitLab](https://gitlab.com/salk-tm/pankmer) | K-mer-based and reference-free pangenome analysis | |
| Panaln | [GitHub](https://github.com/Lilu-guo/Panaln) | Pangenome construction and read alignment | |
| AlfaPang | [GitHub](https://github.com/AdamCicherski/AlfaPang) | Alignment-free algorithm for pangenome graph construction | |

# Pangenome construction with De Bruijn graphs

| Tool | Repository | Description | Status |
|------|-----------|-------------|--------|
| Bifrost | [GitHub](https://github.com/pmelsted/bifrost) | Highly parallel construction and indexing of colored de Bruijn graphs | |
| TwoPaCo | [GitHub](https://github.com/medvedevgroup/TwoPaCo) | Efficient algorithm to build compacted de Bruijn graph | |
| Nexus | [GitHub](https://github.com/biointec/nexus) | Pangenome de Bruijn graph construction using bidirectional algorithm | |
| Graphite | [GitHub](https://github.com/MGXlab/Graphite) | Painting genomes using colored de Bruijn graph | |
| BCALM 2 | [GitHub](https://github.com/GATB/bcalm) | Ultra-low memory and fast de Bruijn graph construction | |

# Pangenome pipelines

| Tool | Repository | Description | Status |
|------|-----------|-------------|--------|
| nf-core pangenome | [GitHub](https://github.com/nf-core/pangenome) | Scalable Nextflow approach to building pangenomes with PGGB | |
| pangepop | [Forgemia](https://forgemia.inra.fr/pangepop/pangepop) | Snakemake pipeline using minigraph-cactus and vg giraffe | |

# Annotating pangenomes

| Tool | Repository | Description | Status |
|------|-----------|-------------|--------|
| GrAnnoT | [Forge](https://forge.ird.fr/diade/dynadiv/grannot) | Transfer linear genomic annotations through pangenome GFA graph | |
| Annotation_scripts | [GitHub](https://github.com/jmonlong/manu-vggafannot/tree/main/analysis) | Annotate minigraph-cactus pangenomes | |

# Short read alignment to a pangenome graph

| Tool | Repository | Description | Status |
|------|-----------|-------------|--------|
| vg giraffe | [GitHub](https://github.com/vgteam/vg) | Faster and more modern alternative to vg map | :rocket: |
| vg map | [GitHub](https://github.com/vgteam/vg) | Original but obsolete vg mapper | |
| Hisat2 | [GitHub](https://github.com/DaehwanKimLab/hisat2) | Alignment tool for pangenomes | |
| Minigraph | [GitHub](https://github.com/lh3/minigraph) | Construct graphs or align short/long reads to graphs | |
| Chrom_mini_graph | [GitHub](https://github.com/gaojunxuan/chrom_mini_graph) | Map reads onto colored minimizer pangenome | |
| Panaln | [GitHub](https://github.com/Lilu-guo/Panaln) | Pangenome construction and read alignment | |
| theseus | [GitHub](https://github.com/albertjimenezbl/theseus-lib) | Fast optimal sequence to graph alignment library | |

# Long read alignment to a pangenome graph

| Tool | Repository | Description | Status |
|------|-----------|-------------|--------|
| GraphAligner | [GitHub](https://github.com/maickrau/GraphAligner) | Fast long read graph aligner | :rocket: |
| vg giraffe | [GitHub](https://github.com/vgteam/vg) | Align long reads to graphs | :rocket: |
| Minigraph | [GitHub](https://github.com/lh3/minigraph) | Construct graphs or align short/long reads | |
| GraphChainer | [GitHub](https://github.com/algbio/GraphChainer) | Built on codebase of GraphAligner | |
| Spades Pathracer | [GitHub](https://github.com/eodus/pathracer#sec4.3) | Align long reads to genomic graphs | |
| Minichain | [GitHub](https://github.com/at-cg/minichain) | Align long reads to GFA or rGFA format pangenomes | |
| PanAligner | [GitHub](https://github.com/at-cg/PanAligner) | Align long reads to pangenomes | |
| poasta | [GitHub](https://github.com/broadinstitute/poasta) | Gap-affine sequence-to-graph and partial order aligner | |
| PALSS | [GitHub](https://github.com/ldenti/palss) | Pangenome Graph Augmentation from Long-reads | |

# SNP and Structural Variant callers and genotypers

| Tool | Repository | Description | Status |
|------|-----------|-------------|--------|
| vg call | [GitHub](https://github.com/vgteam/vg) | Variant caller for pangenomes | :rocket: |
| vg surject | [GitHub](https://github.com/vgteam/vg) | Surject to linear reference for SNP calling | :rocket: |
| Paragraph | [GitHub](https://github.com/Illumina/paragraph) | Graph-based genotyping tools for short read data | |
| Pangenie | [GitHub](https://github.com/eblerjana/pangenie) | K-mer-based SV genotyping using short reads | |
| Deepvariant | [GitHub](https://github.com/google/deepvariant/blob/r1.6/docs/deepvariant-vg-case-study.md) | SNP calling on vg giraffe aligned bam files | |
| Varigraph | [GitHub](https://github.com/JiaoLab2021/varigraph) | Pangenome graph-based genotyper for diploid/polyploid genomes | |
| GraphTyper | [GitHub](https://github.com/DecodeGenetics/graphtyper) | Graph SV genotyper | |
| SVarp | [GitHub](https://github.com/asylvz/SVarp) | Detect structural variants in GFA format pangenome | |
| bubblegun | [GitHub](https://github.com/fawaz-dabbaghieh/bubble_gun) | Detect Bubbles and Superbubbles | |
| PHI | [GitHub](https://github.com/at-cg/PHI) | Pangenome-based Haplotype Inference | |
| Ctyper | [GitHub](https://github.com/ChaissonLab/Ctyper) | Allele-specific and copy number genotyping | |
| rs-gfa-utils | [GitHub](https://github.com/chfi/rs-gfa-utils) | Rust utils for GFA format operations | |
| BayesTyper | [GitHub](https://github.com/bioinformatics-centre/BayesTyper) | Genotyping using variant graphs | |
| Swave | [GitHub](https://github.com/songbowang125/Swave) | Detect SVs from pangenome graphs | |
| APAV | [GitHub](https://github.com/SJTU-CGM/APAV) | Pangenome PAV detection and visualization | |
| PangenomeX | [GitHub](https://github.com/Nevermore233/PangenomeX) | Pangenome shallow CNV caller | |
| SVPG | [GitHub](https://github.com/coopsor/SVPG) | Structural Variant detection and pangenome augmentation | |
| Floco | [GitHub](https://github.com/hugocarmaga/floco) | Call individual node copy number on pangenome | |
| DipGenie | [GitHub](https://github.com/gsc74/DipGenie) | Pangenome graph-based phased diploid inference | |
| Cosigt | [GitHub](https://github.com/davidebolo1993/cosigt) | Pangenome-based structural genotyping | |
| giggles | [GitHub](https://github.com/samarendra-pani/giggles) | Genotype Inference using genome graphs and long reads | |

# Transcriptome analysis

| Tool | Repository | Description | Status |
|------|-----------|-------------|--------|
| pantas | [GitHub](https://github.com/AlgoLab/pantas) | Haplotype-aware differential quantification of alternative splicing | |
| rpvg | [GitHub](https://github.com/jonassibbesen/rpvg) | Infer expression of haplotype-specific transcript paths | |
| PanGraphRNA | [GitHub](https://github.com/cma2015/PanGraphRNA) | Docker/Galaxy platform for graph pangenome-based RNA-seq | |

# Methylation analysis

| Tool | Repository | Description | Status |
|------|-----------|-------------|--------|
| methylGrapher | [GitHub](https://github.com/twlab/methylGrapher) | Align bisulfite reads to pangenome GFA and call methylation | |

# Repeat analysis

| Tool | Repository | Description | Status |
|------|-----------|-------------|--------|
| Pantera | [GitHub](https://github.com/piosierra/pantera) | Identify transposon element families from pangenomes | |
| GraffeTE | [GitHub](https://github.com/cgroza/GraffiTE) | Analyze transposable element insertion polymorphisms | |

# Metagenome analysis

| Tool | Repository | Description | Status |
|------|-----------|-------------|--------|
| Pantax | [GitHub](https://github.com/LuoGroup2023/PanTax) | Strain-level metagenomic attribution for short/long reads | |

# Pangenome viewers - interactive

| Tool | Repository | Description | Status |
|------|-----------|-------------|--------|
| Bandage | [GitHub](https://github.com/rrwick/Bandage) | Visualize GFA files in interactive standalone app | :rocket: |
| BandageNG | [GitHub](https://github.com/asl/BandageNG) | Fork of Bandage with path/walk selection and coloring | |
| SeqTubemap | [GitHub](https://github.com/vgteam/sequenceTubeMap) | Elegant path visualization for pangenome regions | :rocket: |
| MoMI-G | [GitHub](https://github.com/MoMI-G/MoMI-G/) | Genome graph browser for SVs visualization | :rocket: |
| pangene | [GitHub](https://github.com/lh3/pangene) | Visualize protein set mapped to genomes | :rocket: |
| Panagram | [GitHub](https://github.com/kjenike/panagram) | Alignment-free pangenome browser and analysis toolkit | |
| VAG | [GitHub](https://github.com/lipingfangs/VAG) | Visualization of short sequence alignments in pangenome | |
| Panache | [GitHub](https://github.com/SouthGreenPlatform/panache) | View linearized pangenomes | |
| Waragraph | [GitHub](https://github.com/chfi/waragraph) | Pangenome graph visualization | |
| PanGraphViewer | [GitHub](https://github.com/TF-Chan-Lab/panGraphViewer) | Desktop and web versions, VCF input support | |
| Wally | [GitHub](https://github.com/tobiasrausch/wally#subcommand-gfa-visualization-of-pan-genome-graphs-work-in-progress) | View GFA (Work in progress) | |
| VRPG | [GitHub](https://github.com/codeatcg/VRPG) | View rGFA or GFA in Python/HTML | |
| Pantograph | [Web](https://help.pantograph.computomics.com/) | Commercial pangenome graph viewer | |
| PGV | [GitHub](https://github.com/w-gao/pgv) | Web-based viewer similar to SeqTubeMap | |
| Pancat | [GitHub](https://github.com/Tharos-ux/pancat) | Filter and visualize GFA files | |
| gfaestus | [GitHub](https://github.com/chfi/gfaestus) | GPU-accelerated GFA visualizer using Vulkan | |
| gfaviz | [GitHub](https://github.com/ggonnella/gfaviz) | Interactive tool for visualization of graphs in GFA | |
| AGB | [GitHub](https://github.com/almiheenko/AGB) | Interactive assembly graph browser | |
| graphgenomeviewer | [Web](https://cmdcolin.github.io/graphgenomeviewer/) | Web-based viewer for small to medium GFA files | |
| JBrowse 2 | [GitHub/Web](https://jbrowse.org) | Web genome browser with synteny and alignment plugins | |
| strangepg | [GitHub](https://github.com/qwx9/strangepg) | Modern GFA viewer, alternative to Bandage | |
| savanache | [Forge](https://forge.ird.fr/diade/savanache/savanache/) | Browser-based viewer for minigraph GFA files | |

# Pangenome viewers - static

| Tool | Repository | Description | Status |
|------|-----------|-------------|--------|
| vg view | [GitHub](https://github.com/vgteam/vg) | Generate static images from vg compatible files | |
| odgi | [GitHub](https://github.com/pangenome/odgi) | Generate genome-wide static images from odgi/gfa | :rocket: |
| plotsr | [GitHub](https://github.com/schneebergerlab/plotsr) | High-quality synteny and structural rearrangement visualization | |
| gfalook | [GitHub](https://github.com/pangenome/gfalook) | 2026 reimplementation of odgi viz in Rust with more features | |

# Graph analysis and quality assessment

| Tool | Repository | Description | Status |
|------|-----------|-------------|--------|
| PG-SCunK | [GitHub](https://github.com/cumtr/PG-SCUnK/) | Assess graph representation quality using unique kmers | |
| Panacus | [GitHub](https://github.com/marschall-lab/panacus) | Fast pangenome growth and core size estimation | |
| Pansel | [GitHub](https://github.com/mzytnicki/pansel) | Find over/under-diverse regions in GFA pangenome | |

# Graph validation tools

| Tool | Repository | Description | Status |
|------|-----------|-------------|--------|
| vg validate | [GitHub](https://github.com/vgteam/vg) | Validate vg graphs | |
| odgi validate | [GitHub](https://github.com/pangenome/odgi) | Validate odgi graphs | |

# Pangenome comparison

| Tool | Repository | Description | Status |
|------|-----------|-------------|--------|
| junctions | [GitHub](https://github.com/urbanslug/junctions) | Pangenome comparison using elastic-degenerate strings | |
| rs-pancat-compare | [GitHub](https://github.com/dubssieg/rs-pancat-compare) | Pairwise pangenome graph comparison | |

# Pangenome tools for microbes

| Tool | Repository | Description | Status |
|------|-----------|-------------|--------|
| Panalyze | [GitHub](https://github.com/downingtim/Panalyze) | Viral pangenome variation graphs - Construction to visualization | |
| anvi'o | [Web](https://merenlab.org/2016/11/08/pangenomics-v2/) | Microbial pangenomics - Annotation, Construction, Visualization | |
| Roary | [GitHub](https://github.com/sanger-pathogens/Roary) | Tool for prokaryotic pangenomes with Prokka GFF files | |
| pandora | [GitHub](https://github.com/iqbal-lab-org/pandora) | Pan-genome graph structure and variant identification | |

# File formats

| Format | Repository/Spec | Description | Status |
|--------|-----------------|-------------|--------|
| GFA | [Spec](http://gfa-spec.github.io/GFA-spec/GFA1.html) | Assembly interchange format for vg and odgi | :rocket: |
| odgi | [GitHub](https://github.com/pangenome/odgi) | Easy interconversion to GFA | :rocket: |
| rGFA | [GitHub](https://github.com/lh3/gfatools/blob/master/doc/rGFA.md) | Extended GFA format with reference sequence | |
| vg formats | [GitHub](https://github.com/vgteam/vg/wiki/File-Formats#gam-graph-alignment--map-vgs-bam) | Multiple vg file formats (GAM, etc) | |
| PanSN-spec | [GitHub](https://github.com/pangenome/PanSN-spec) | Naming system for haplotypes in pangenomes | :rocket: |
| GAF | [GitHub](https://github.com/lh3/gfatools/blob/master/doc/rGFA.md#the-graph-alignment-format-gaf) | Graph Alignment Format, similar to PAF | |
| GAM | [GitHub](https://github.com/vgteam/vg/wiki/File-Formats#gam-graph-alignment--map-vgs-bam) | Graph Alignment/Map format | |
| pgbam | [GitHub](https://github.com/kokyriakidis/pgbam) | Bridging BAM alignments and pangenomic GAF alignments | |
| gbz-base | [GitHub](https://github.com/jltsiren/gbz-base) | GBZ and GAF formats based on SQLite | |

# Miscellaneous tools

| Tool | Repository | Description | Status |
|------|-----------|-------------|--------|
| gfainject | [GitHub](https://github.com/chfi/gfainject) | Map short alignments in BAM to GFA in GAF format | |
| GRAFIMO | [GitHub](https://github.com/pinellolab/GRAFIMO) | GRAph-based Finding of Motif Occurrences using vg | |
| rs-gfa | [GitHub](https://github.com/chfi/rs-gfa) | GFA parser in Rust | |
| rs-gfa-utils | [GitHub](https://github.com/chfi/rs-gfa-utils) | Rust utils for GFA format operations | |
| ropebwt3 | [GitHub](https://github.com/lh3/ropebwt3) | Construct and align against TB-scale references | |
| pollen | [GitHub](https://github.com/cucapra/pollen) | Nascent project for faster pangenomics tools | |
| mumemto | [GitHub](https://github.com/vikshiv/mumemto) | Use maximal unique matches for sequence analysis | |
| gfa2bin | [GitHub](https://github.com/MoinSebi/gfa2bin) | Convert pangenome formats to Plink for GWAS | |
| vizitig | [GitLab](https://gitlab.inria.fr/vizisoft/vizitig) | All-in-one genomic/transcriptomic de Bruijn graph constructor | |
| gafpack | [GitHub](https://github.com/pangenome/gafpack) | Calculate node coverage from GAF alignments | |
| TeraTools | [GitHub](https://github.com/ucfcbb/TeraTools) | Efficient terabase-scale pangenome analysis | |
| Kente | [GitHub](https://github.com/treangenlab/Kente) | Graph-based approach for HGT detection | |

# Libraries to explore pangenomes

| Library | Repository | Description | Status |
|---------|-----------|-------------|--------|
| gfapy | [GitHub](https://github.com/ggonnella/gfapy) | GFA1/GFA2 parsing and graph exploration in Python | |
| gfagraphs | [GitHub](https://github.com/Tharos-ux/gfagraphs) | rGFA and GFA1 parsing and editing in Python | |
| graphanalyzer | [GitHub](https://github.com/sablokgaurav/graphanalyzer) | Python package to read and analyze PAF and GFA | |
| theseus | [GitHub](https://github.com/albertjimenezbl/theseus-lib) | Fast sequence to graph alignment library | |

# Tutorials and reviews

| Title | Repository/Link | Year | Status |
|-------|-----------------|------|--------|
| INRA Pangenome Tutorial | [Web](https://pangenome-hackathon-genotoul-bioinfo-11d6d4f47ac33734abfa2a1377.pages.mia.inra.fr/pages/tutorial_pangenome_graph/) | 2024 | Nice glossary and tutorial |
| Complexity, Welcome Pangenome Graphs for Population Genomics | [Cambridge](https://www.cambridge.org/core/journals/quantitative-plant-biology/article/complexity-welcome-pangenome-graphs-for-comprehensive-population-genomics/B2DD25F2FD0B4CB91D238DFD2257E7FA) | 2025 | Review article |

# Other lists of pangenome tools

| Resource | Link | Description |
|----------|------|-------------|
| Practical Pangenome Graphs | [Web](https://pangenome.github.io/) | Pangenome tools and resources |
| awesome-genome-visualization | [Web](https://cmdcolin.github.io/awesome-genome-visualization/) | Genome visualization tools with graph tag |

# Contributions

Is something missing? Contributions are welcome, please make PRs to main or write an issue with a link. 

# Citations 

This is not "published" in an academic journal, but you can cite it via the DOI at the top if you like.
