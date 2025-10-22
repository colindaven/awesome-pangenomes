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
- [Pangenome viewers -interactive](#Pangenome-viewers--interactive)
- [Pangenome viewers -static](#Pangenome-viewers--static)
- [Graph analysis and quality assessment](#graph-analysis-and-quality-assessment)
- [Graph validation tools](#graph-validation-tools)
- [Pangenome comparison](#pangenome-comparison)
- [Pangenome tools for microbes](#pangenome-tools-for-microbes)
- [File formats](#file-formats)
- [Miscellaneous tools](#miscellaneous-tools)
- [Libraries to explore pangenomes](#libraries-to-explore-pangenomes)
- [Tutorials](#tutorials)
- [Other lists of pangenome tools](#other-lists-of-pangenome-tools) 

# Important blog posts

* [Untangling-graphical-pangenomics](https://ekg.github.io/2019/07/09/Untangling-graphical-pangenomics) Excellent blog by Erik Garrison explaining the differences between rGFA and GFA formats and approaches - *important and frequently overlooked* 

# Toolkits

* [odgi](https://github.com/pangenome/odgi) Fast toolkit based on odgi format :rocket:
* [vg](https://github.com/vgteam/vg) Full featured construction, mapping and SNP calling toolkit based on multiple formats. :rocket:
* [gaftools](https://github.com/marschall-lab/gaftools) Toolkit for GAF (Graph Alignment Format) sorting and manipulation.
* [gfakluge](https://github.com/edawson/gfakluge) Toolkit and c++ API for GFA manipulation
* [gfatools](https://github.com/lh3/gfatools) Toolkit for GFA parsing and conversion
* [gretl](https://github.com/MoinSebi/gretl) ([paper](https://github.com/MoinSebi/gretl)) Statistics and analysis for GFA files, written in Rust
* [pgr-tk](https://github.com/GeneDx/pgr-tk) A PanGenomic Research Toolkit, output of this process is not a GFA file.
* [GraSuite](https://forge.ird.fr/diade/GraSuite) A suite of tools for GFA pangenomes and graph manipulation and pangenome.


# Pangenome construction

* [Minigraph](https://github.com/lh3/minigraph) ([paper](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-020-02168-z)) Fast method by Heng Li, produces referenceGFA (rGFA) format (not GFA or odgi) :rocket:
* [minigraph_cactus](https://github.com/ComparativeGenomicsToolkit/cactus) and [docs](https://github.com/ComparativeGenomicsToolkit/cactus/blob/master/doc/pangenome.md) ([paper](https://www.nature.com/articles/s41587-023-01793-w)) Pangenome builder which prioritizes downstream compatibility. Produces GFA and odgi. :rocket:
* [PGGB](https://github.com/pangenome/pggb) ([paper](https://www.nature.com/articles/s41592-024-02430-3)) Pangenome Graph Builder, calculates SNPs as part of the pipeline. Produces GFA and odgi. :rocket:
* [pangene](https://github.com/lh3/pangene) ([paper](https://academic.oup.com/bioinformatics/article/40/7/btae456/7718494?login=true)) Pangene constructs a pangenome gene graph from one protein set and many genomes and includes simple but effective visualization :rocket:
* [Pantools v3+](https://git.wur.nl/bioinformatics/pantools) ([paper](https://academic.oup.com/bioinformatics/article-abstract/38/18/4403/6647839)) Fully featured construction of pangenome graphs
* [PSVCP](https://github.com/wjian8/psvcp_v1.01) ([paper](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-023-02861-9)) Add PAV to the linear genome to construct a pangenome.
* [PHG Practical Haplotype Graph](https://bitbucket.org/bucklerlab/practicalhaplotypegraph/wiki/Home) ([paper](https://acsess.onlinelibrary.wiley.com/doi/10.1002/tpg2.20009))
* [PATO](https://github.com/irycisBioinfo/PATO) ([paper](https://academic.oup.com/bioinformatics/article/37/23/4564/6384566)) R package for pangenome construction
* [Chrom_mini_graph](https://github.com/gaojunxuan/chrom_mini_graph) ([poster](https://www.cs.toronto.edu/~kgao/assets/pdf/CMG-Poster.pdf)) Generate and map reads onto a coloured minimizer pangenome graph
* [GET_PANGENES](https://github.com/Ensembl/plant-scripts/tree/master/pangenes) ([paper](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-023-03071-z)) Perl scripts used by the Ensembl Plants team for pangenomics
* [impg](https://github.com/ekg/impg) Create an implicit pangenome graph for a homologous target region, then use output bed files to extract sequences for PGGB etc.
* [MGRgraph](https://github.com/LeilyR/Multi-genome-Reference) ([preprint](https://www.biorxiv.org/content/10.1101/2020.04.11.036871)) An algorithm to Build a Multi-genome Reference (warning - last updated 2018)
* [MEMO](https://github.com/StephenHwang/MEMO) ([preprint](https://www.biorxiv.org/content/10.1101/2024.05.20.595044)) MEMO constructs a pangenome and index and allows kmer based conservation analyses and visualization
* [poasta](https://github.com/broadinstitute/poasta) Fast, gap-affine sequence-to-graph and partial order aligner and MSA construction
* [SEQWISH](https://github.com/ekg/seqwish) ([paper](https://academic.oup.com/bioinformatics/article/39/1/btac743/6854971)) Unbiased pangenome graphs
* [seqrush](https://github.com/pangenome/seqrush) Parallel pangenome construction using a simplified seqwish like algorithm.
* [pannagram](https://github.com/iganna/pannagram) ([preprint](https://www.biorxiv.org/content/10.1101/2025.02.07.637071)) Construct pangenomes and find SVs using blast, mafft and R tools
* [pandagma](https://github.com/legumeinfo/pandagma) Calculate pan-gene sets from a collection of genome assemblies and their annotations
* [Panscan](https://github.com/CATG-Github/panscan) Construct a matrix and identify novel sequences, SVs, and repetitive regions. Requires Gencode GFF3s. Human orientated.
* [CoreDetector](https://github.com/mfruzan/CoreDetector) ([paper](https://academic.oup.com/bioinformatics/article/39/11/btad628/7329718)) CoreDetector: a flexible and efficient program for core-genome alignment of evolutionary diverse genomes
* [PanKmer](https://gitlab.com/salk-tm/pankmer) ([paper](https://academic.oup.com/bioinformatics/article/39/10/btad621/7319363)) PanKmer: k-mer-based and reference-free pangenome analysis
* [Panaln](https://github.com/Lilu-guo/Panaln) Pangenome construction and read alignment
* [AlfaPang](https://github.com/AdamCicherski/AlfaPang) ([paper](https://almob.biomedcentral.com/articles/10.1186/s13015-025-00277-7)) alignment free algorithm for pangenome graph construction


# Pangenome construction with De Bruijn graphs
* [Bifrost](https://github.com/pmelsted/bifrost) ([paper](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-020-02135-8)) Bifrost: highly parallel construction and indexing of colored and compacted de Bruijn graphs
* [TwoPaCo](https://github.com/medvedevgroup/TwoPaCo) ([paper](https://academic.oup.com/bioinformatics/article/33/24/4024/2725383)) TwoPaCo: an efficient algorithm to build the compacted de Bruijn graph from many complete genomes
* [Nexus](https://github.com/biointec/nexus ) ([paper](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-023-05531-6)) Pan-genome de Bruijn graph using the bidirectional FM-index
* [Graphite](https://github.com/MGXlab/Graphite) ([paper](https://academic.oup.com/nargab/article/6/4/lqae142/7832412)) Graphite: painting genomes using a colored de Bruijn graph 


# Pangenome pipelines

* [nf-core pangenome](https://github.com/nf-core/pangenome) ([paper](https://doi.org/10.1093/bioinformatics/btae609)) A scalable Nextflow approach to building pangenomes with PGGB with visualization by odgi. :rocket:
* [pangepop](https://forgemia.inra.fr/pangepop/pangepop) A snakemake pipeline to create a pangenome with minigraph-cactus and align reads against it with vg giraffe

# Annotating pangenomes
* [GrAnnoT](https://forge.ird.fr/diade/dynadiv/grannot) ([preprint](https://www.biorxiv.org/content/10.1101/2025.02.26.640337v1)) Transfer linear genomic annotations through a pangenome GFA graph
* [Annotation_scripts](https://github.com/jmonlong/manu-vggafannot/tree/main/analysis) ([preprint](https://www.biorxiv.org/content/10.1101/2024.10.12.618009v1)) Annotate a minigraph-cactus pangenome with regions or SNPs


# Short read alignment to a pangenome graph

* [vg giraffe](https://github.com/vgteam/vg) Faster and more modern alternative to vg map :rocket:
* [vg map](https://github.com/vgteam/vg) Original vg mapper (superseded by vg giraffe)
* [Hisat2](https://github.com/DaehwanKimLab/hisat2)
* [Minigraph](https://github.com/lh3/minigraph) Construct graphs or align short or long reads to graphs
* [Chrom_mini_graph](https://github.com/gaojunxuan/chrom_mini_graph) Generate and map reads onto a coloured minimizer pangenome graph
* [Panaln](https://github.com/Lilu-guo/Panaln) Pangenome construction and read alignment


# Long read alignment to a pangenome graph

* [GraphAligner](https://github.com/maickrau/GraphAligner) Fast long read graph aligner :rocket:
* [vg giraffe](https://github.com/vgteam/vg) Vg giraffe can now align long reads to graphs as well
* [Minigraph](https://github.com/lh3/minigraph) Construct graphs or align short or long reads to graphs 
* [GraphChainer](https://github.com/algbio/GraphChainer) Built on codebase of GraphAligner
* [Spades Pathracer](https://github.com/eodus/pathracer#sec4.3) Align long reads to genomic graphs
* [Minichain](https://github.com/at-cg/minichain) Align long reads to pangenomes in GFA or rGFA format
* [PanAligner](https://github.com/at-cg/PanAligner) Align long reads to pangenomes
* [poasta](https://github.com/broadinstitute/poasta) Fast, gap-affine sequence-to-graph and partial order aligner and MSA construction
* [PALSS](https://github.com/ldenti/palss) ([preprint](https://www.biorxiv.org/content/10.1101/2025.02.07.637057v1)) Pangenome Graph Augmentation from Long-reads Specific Strings

# SNP and Structural Variant callers and genotypers

* [vg call](https://github.com/vgteam/vg) Variant caller for pangenomes, with gam or GAF output :rocket:
* [vg surject](https://github.com/vgteam/vg) surject to linear reference, then use linear SNP caller like Freebayes, Deepvariant etc :rocket:
* [Paragraph](https://github.com/Illumina/paragraph) A suite of graph-based genotyping tools for short read data
* [Pangenie](https://github.com/eblerjana/pangenie) kmer-based SV genotyping using short reads. Intended for human only (in 2023).
* [Deepvariant](https://github.com/google/deepvariant/blob/r1.6/docs/deepvariant-vg-case-study.md) Case study of deep variant SNP calling on vg giraffe aligned bam files
* [Varigraph](https://github.com/JiaoLab2021/varigraph) ([preprint](https://www.biorxiv.org/content/10.1101/2025.02.17.638628v1)) A pangenome graph based genotyper for diploid and polyploid genomes
* [GraphTyper](https://github.com/DecodeGenetics/graphtyper) A graph SV genotyper (does not call SVs)  
* [SVarp](https://github.com/asylvz/SVarp) Use long reads to detect structural variants in a GFA format pangenome.
* [bubblegun](https://github.com/fawaz-dabbaghieh/bubble_gun) A tool for detecting Bubbles and Superbubbles
* [PHI Pangenome-based Haplotype Inference](https://github.com/at-cg/PHI) ([preprint](https://www.biorxiv.org/content/10.1101/2024.10.27.620212v1)) A genotyper using low coverage short or long reads for haploid pangenomes, requires Gurobi license.
* [Ctyper](https://github.com/ChaissonLab/Ctyper) Allele-specific and copy number specific genotyping using pangenomes
* [rs-gfa-utils](https://github.com/chfi/rs-gfa-utils) Rust utils for GFA format operations including ultrabubble (SV) to VCF, GAF to PAF, subgraphs etc
* [BayesTyper](https://github.com/bioinformatics-centre/BayesTyper) ([paper](https://pubmed.ncbi.nlm.nih.gov/29915429/)) Accurate genotyping across variant classes and lengths using variant graphs
* [Swave](https://github.com/songbowang125/Swave) ([preprint](https://www.biorxiv.org/content/10.1101/2025.07.06.663386v1.abstract)) Detect SVs from a (minigraph) pangenome graph (free for non-commercial use)
* [APAV](https://github.com/SJTU-CGM/APAV) ([paper](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1013288)) A pangenome PAV detection and visualization toolkit in Perl and R.
* [PangenomeX](https://github.com/Nevermore233/PangenomeX) ([paper](https://academic.oup.com/bib/article/26/5/bbaf550/8293245?login=true)) Pangenome shallow CNV caller in python. Requires building and normalization.

# Transcriptome analysis

* [pantas](https://github.com/AlgoLab/pantas) Haplotype aware differential quantification of alternative splicing events on spliced pangenome graphs
* [rpvg](https://github.com/jonassibbesen/rpvg) Infer the expression of haplotype-specific transcript paths using RNA-seq reads aligned to a spliced pangenome graph


# Methylation analysis

* [methylGrapher](https://github.com/twlab/methylGrapher?tab=readme-ov-file) Align bisulfite reads to a pangenome GFA graph and call methylation


# Repeat analysis

* [Pantera](https://github.com/piosierra/pantera) Identification of transposon element families from a set of pangenomes
* [GraffeTE](https://github.com/cgroza/GraffiTE) ([paper](https://www.nature.com/articles/s41467-024-53294-2)) A unified framework to analyze transposable element insertion polymorphisms using graph genomes


# Metagenome analysis

* [Pantax](https://github.com/LuoGroup2023/PanTax) Pantax attempts to provide strain level metagenomic attribution for short or long reads (but requires the licensed Gurobi optimizer)



# Pangenome viewers -interactive

* [Bandage](https://github.com/rrwick/Bandage) Visualize GFA files in an interactive standalone app :rocket:
    * [BandageNG](https://github.com/asl/BandageNG) Fork of Bandage that allows you to select and color paths and walks in the graph
* [SeqTubemap](https://github.com/vgteam/sequenceTubeMap) Elegant path visualization for smaller regions of a pangenome from the vg team :rocket:
* [MoMI-G](https://github.com/MoMI-G/MoMI-G/) Genome graph browser for SVs visualization. User can filter and visualize annotations and inspect SVs with read alignments over the genome graph. :rocket:
* [pangene](https://github.com/lh3/pangene) Pangene can visualize one protein set mapped to x genomes to check synteny and presence/absence of genes. :rocket:
* [Panagram](https://github.com/kjenike/panagram) Plots k-mer conservation
* [VAG](https://github.com/lipingfangs/VAG) Visualization of short sequence alignments in a pangenome
* [Panache](https://github.com/SouthGreenPlatform/panache) View linearized pangenomes
* [Waragraph](https://github.com/chfi/waragraph)
* [PanGraphViewer](https://github.com/TF-Chan-Lab/panGraphViewer) Desktop and web versions. Based on cytoscape.js. Can get to chromosome coordinates, allows VCF input.
* [Wally](https://github.com/tobiasrausch/wally#subcommand-gfa-visualization-of-pan-genome-graphs-work-in-progress) View GFA (Work in progress 2023)
* [VRPG](https://github.com/codeatcg/VRPG) View rGFA or GFA, written in python and html
* [Pantograph](https://help.pantograph.computomics.com/) is a commercial pangenome graph viewer option
* [PGV](https://github.com/w-gao/pgv) A web based viewer similar to SeqTubeMap
* [Pancat](https://github.com/Tharos-ux/pancat) Scripts to filter and visualize GFA files
* [gfaestus](https://github.com/chfi/gfaestus) GFA visualizer, GPU-accelerated using Vulkan 
* [gfaviz](https://github.com/ggonnella/gfaviz) Graphical interactive tool for the visualization of sequence graphs in GFA format
* [AGB](https://github.com/almiheenko/AGB) Interactive assembly graph browser
* [graphgenomeviewer](https://cmdcolin.github.io/graphgenomeviewer/) Web based viewer for small to medium GFA files
* [JBrowse 2](https://jbrowse.org) Web based genome browser with synteny views and plugins for multiple-alignments that can be extracted from Cactus graphs. [GitHub](https://github.com/cmdcolin/jbrowse-plugin-mafviewer)
* [strangepg](https://github.com/qwx9/strangepg) A modern GFA viewer and alternative to the Bandage tool


# Pangenome viewers -static

* [vg view](https://github.com/vgteam/vg) - generates static images
* [odgi](https://github.com/pangenome/odgi) - generates static images :rocket:
* [plotsr](https://github.com/schneebergerlab/plotsr) - generates static images


# Graph analysis and quality assessment

* [PG-SCunK](https://github.com/cumtr/PG-SCUnK/) ([preprint](https://www.biorxiv.org/content/10.1101/2025.04.03.646777v1)) - assess graph representation quality using unique kmers from source genomes
* [Panacus](https://github.com/marschall-lab/panacus) ([paper](https://academic.oup.com/bioinformatics/article/40/12/btae720/7914008)) Panacus: fast and exact pangenome growth and core size estimation
* [Pansel](https://github.com/mzytnicki/pansel)) Find overdiverse or underdiverse regions in a GFA pangenome.



# Graph validation tools

* [vg validate](https://github.com/vgteam/vg)
* [odgi validate](https://github.com/pangenome/odgi)


# Pangenome comparison

* [junctions](https://github.com/urbanslug/junctions) Pangenome comparison using elastic-degenerate strings.
* [rs-pancat-compare](https://github.com/dubssieg/rs-pancat-compare) Pairwise pangenome graph comparison by the computation of a segmentation edit distance.


# Pangenome tools for microbes

* [anvi'o](https://merenlab.org/2016/11/08/pangenomics-v2/) Microbial pangenomics - Annotation, Construction, Visualization and Manipulation (Eukaryote too excepted annotation)
* [Roary](https://github.com/sanger-pathogens/Roary) A well-documented and feature-rich tool which works on Prokka gff files and has an entertaining FAQ. 

# File formats

* [GFA](http://gfa-spec.github.io/GFA-spec/GFA1.html) An assembly interchange format read by both vg and odgi :rocket:
* [odgi](https://github.com/pangenome/odgi) Easy interconversion to main interchange format GFA. :rocket:
* [rGFA](https://github.com/lh3/gfatools/blob/master/doc/rGFA.md) An extended GFA format, rGFA contains extra tags and includes a reference sequence. See minigraph.
* [vg](https://github.com/vgteam/vg) Vg has its own mass of file formats: https://github.com/vgteam/vg/wiki/File-Formats#gam-graph-alignment--map-vgs-bam
* [PanSN-spec](https://github.com/pangenome/PanSN-spec) A naming system for haplotypes in pangenomes.
* [GAF - Graph Alignment Format](https://github.com/lh3/gfatools/blob/master/doc/rGFA.md#the-graph-alignment-format-gaf) Created by minigraph, convertible by vg. Similar to PAF.
* [GAM - Graph Alignment/Map](https://github.com/vgteam/vg/wiki/File-Formats#gam-graph-alignment--map-vgs-bam) and [here](https://github.com/vgteam/libvgio/blob/master/deps/vg.proto#L38-L54) Created by vg giraffe. May be superseded by GAF format.


# Miscellaneous tools

* [gfainject](https://github.com/chfi/gfainject) Map short alignments in BAM format to a GFA (seems it is not a real aligner but a conversion tool). Output in GAF format.
* [GRAFIMO](https://github.com/pinellolab/GRAFIMO) GRAph-based Finding of Individual Motif Occurrences using vg.
* [rs-gfa](https://github.com/chfi/rs-gfa) A GFA parser in Rust.
* [rs-gfa-utils](https://github.com/chfi/rs-gfa-utils) Rust utils for GFA format operations including ultrabubble (SV) to VCF, GAF to PAF, subgraphs etc
* [ropebwt3](https://github.com/lh3/ropebwt3) Can construct and align sequences against huge TB scale references and retrieve haplotypes.
* [pollen](https://github.com/cucapra/pollen) A nascent project to develop faster tools for pangenomics in python and Rust. Contains MyGFA, FlatGFA and slow_odgi.
* [mumemto](https://github.com/vikshiv/mumemto) Use maximal unique matches to analyze and statically visualize a set of fasta sequences.
* [gfa2bin](https://github.com/MoinSebi/gfa2bin) Convert various pangenome formats to Plink format for GWAS


# Libraries to explore pangenomes

* [gfapy](https://github.com/ggonnella/gfapy) implements GFA1 and GFA2 parsing and scalable exploration of graphs in Python.
* [gfagraphs](https://github.com/Tharos-ux/gfagraphs) implements rGFA and GFA1 parsing and editing of graphs in Python.
* [graphanalyzer](https://github.com/sablokgaurav/graphanalyzer) a python package to read and analyze the PAF and the GFA files for the graphs.

# Tutorials

* [INRA_pangenomes:tutorial](https://pangenome-hackathon-genotoul-bioinfo-11d6d4f47ac33734abfa2a1377.pages.mia.inra.fr/pages/tutorial_pangenome_graph/) 2024 - Nice pangenome glossary and tutorial


# Other lists of pangenome tools

* [Practical Pangenome Graphs](https://pangenome.github.io/)
* [awesome-genome-visualization](https://cmdcolin.github.io/awesome-genome-visualization/) - specifically tools tagged with [Graph](https://cmdcolin.github.io/awesome-genome-visualization/?latest=true&tag=Graph) and or [Pangenome](https://cmdcolin.github.io/awesome-genome-visualization/?latest=true&tag=Pangenome)


# Contributions

Is something missing? Contributions are welcome, please make PRs to main or write an issue with a link.
