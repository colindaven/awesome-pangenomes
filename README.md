# awesome-pangenomes
## A list of software capable of analyzing **eukaryotic** genomes for pangenomics 

:rocket: indicates a popular repository

# Toolkits

* [vg](https://github.com/vgteam/vg) Full featured construction, mapping and SNP calling toolkit based on multiple formats. :rocket:
* [odgi](https://github.com/pangenome/odgi) Fast toolkit based on odgi format :rocket:
* [gfatools](https://github.com/lh3/gfatools) Toolkit for GFA parsing and conversion
* [gfakluge](https://github.com/edawson/gfakluge) Toolkit and c++ API for GFA manipulation
* [gaftools](https://github.com/marschall-lab/gaftools) Toolkit for GAF (Graph Alignment Format) sorting and manipulation.
* [gretl](https://github.com/MoinSebi/gretl) Statistics and analysis for GFA files, written in Rust
* [pgr-tk](https://github.com/GeneDx/pgr-tk) A PanGenomic Research Took Kit, the unfortunate thing is that the output of this process is not a GFA file.


# Pangenome construction

* [Minigraph](https://github.com/lh3/minigraph) Fast method by Heng Li, produces referenceGFA (rGFA) format (not GFA or odgi) :rocket:
* [Cactus/minigraph](https://github.com/ComparativeGenomicsToolkit/cactus) Pangenome builder which prioritizes downstream compatibility. Produces GFA and odgi. :rocket:
* [PGGB](https://github.com/pangenome/pggb) Pangenome Graph Builder, calculates SNPs as part of the pipeline. Produces GFA and odgi. :rocket:
* [Pantools v3+](https://git.wur.nl/bioinformatics/pantools) Fully featured construction of pangenome graphs
* [PSVCP](https://github.com/wjian8/psvcp_v1.01) Add PAV to the linear genome to construct a pangenome.
* [PHG Practical Haplotype Graph](https://bitbucket.org/bucklerlab/practicalhaplotypegraph/wiki/Home)
* [PATO](https://github.com/irycisBioinfo/PATO) R package for pangenome construction
* [Chrom_mini_graph](https://github.com/gaojunxuan/chrom_mini_graph) Generate and map reads onto a coloured minimizer pangenome graph
* [GET_PANGENES](https://github.com/Ensembl/plant-scripts/tree/master/pangenes) Perl scripts used by the Ensembl Plants team for pangenomics
* [impg](https://github.com/ekg/impg) Create an implicit pangenome graph for a homologous target region, then use output bed files to extract sequences for PGGB etc.
* [MGRgraph](https://github.com/LeilyR/Multi-genome-Reference) An Algorithm to Build a Multi-genome Reference (warning - last updated 2018)
* [pangene](https://github.com/lh3/pangene) Pangene constructs a pangenome gene graph from one protein set and many genomes and includes simple but effective visualization :rocket:
* [MEMO](https://github.com/StephenHwang/MEMO) MEMO constructs a pangenome and index and allows kmer based conservation analyses and visualization
* [poasta](https://github.com/broadinstitute/poasta) Fast, gap-affine sequence-to-graph and partial order aligner and MSA construction


# Short read alignment to a pangenome graph

* [vg map](https://github.com/vgteam/vg) Original vg mapper (superseded by vg giraffe)
* [vg giraffe](https://github.com/vgteam/vg) Faster and more modern alternative to vg map :rocket:
* [Hisat2](https://github.com/DaehwanKimLab/hisat2)
* [Minigraph](https://github.com/lh3/minigraph) Construct graphs or align short or long reads to graphs
* [Chrom_mini_graph](https://github.com/gaojunxuan/chrom_mini_graph) Generate and map reads onto a coloured minimizer pangenome graph



# Long read alignment to a pangenome graph

* [GraphAligner](https://github.com/maickrau/GraphAligner) Fast long read graph aligner :rocket:
* [Minigraph](https://github.com/lh3/minigraph) Construct graphs or align short or long reads to graphs 
* [GraphChainer](https://github.com/algbio/GraphChainer) Built on codebase of GraphAligner
* [Spades Pathracer](https://github.com/eodus/pathracer#sec4.3) Align long reads to genomic graphs
* [Minichain](https://github.com/at-cg/minichain) Align long reads to pangenomes in GFA or rGFA format
* [PanAligner](https://github.com/at-cg/PanAligner) Align long reads to pangenomes
* [poasta](https://github.com/broadinstitute/poasta) Fast, gap-affine sequence-to-graph and partial order aligner and MSA construction


# SNP callers and genotypers

* [vg call](https://github.com/vgteam/vg) SNP caller for pangenomes, with gam or GAF output :rocket:
* [Paragraph](https://github.com/Illumina/paragraph) A suite of graph-based genotyping tools for short read data
* [Pangenie](https://github.com/eblerjana/pangenie) kmer-based SV genotyping using short reads. Intended for human only (in 2023).
* [vg surject](https://github.com/vgteam/vg) surject to linear reference, then use linear SNP caller like Freebayes, Deepvariant etc :rocket:
* [Deepvariant](https://github.com/google/deepvariant/blob/r1.6/docs/deepvariant-vg-case-study.md) Case study of deep variant SNP calling on vg giraffe aligned bam files



# Structural Variation (SV) callers and genotypers

* [vg call](https://github.com/vgteam/vg) Call and genotype structural variants on a graph using long and short reads. :rocket:
* [GraphTyper](https://github.com/DecodeGenetics/graphtyper) A graph SV genotyper (does not call SVs)  
* [Pangenie](https://github.com/eblerjana/pangenie) kmer-based SV genotyping using short reads. Intended for human only (in 2023).
* [SVarp](https://github.com/asylvz/SVarp) Use long reads to detect structural variants in a GFA format pangenome.


# Bubble (SV) detection

* [bubblegun](https://github.com/fawaz-dabbaghieh/bubble_gun) A tool for detecting Bubbles and Superbubbles


# Pangenome viewers -interactive

* [Panagram](https://github.com/kjenike/panagram)
* [Bandage](https://github.com/rrwick/Bandage) Visualize GFA files in an interactive standalone app :rocket:
* [SeqTubemap](https://github.com/vgteam/sequenceTubeMap) Elegant path visualization for smaller regions of a pangenome from the vg team :rocket:
* [VAG](https://github.com/lipingfangs/VAG) Visualization of short sequence alignments in a pangenome
* [Panache](https://github.com/SouthGreenPlatform/panache) View linearized pangenomes
* [Waragraph](https://github.com/chfi/waragraph)
* [PanGraphViewer](https://github.com/TF-Chan-Lab/panGraphViewer)
* [Wally](https://github.com/tobiasrausch/wally#subcommand-gfa-visualization-of-pan-genome-graphs-work-in-progress) View GFA (Work in progress 2023)
* [VRPG](https://github.com/codeatcg/VRPG) View rGFA or GFA, written in python and html
* [Pantograph](https://help.pantograph.computomics.com/) is a commercial pangenome graph viewer option
* [PGV](https://github.com/w-gao/pgv) A web based viewer similar to SeqTubeMap
* [Pancat](https://github.com/Tharos-ux/pancat) Scripts to filter and visualize GFA files
* [gfaestus](https://github.com/chfi/gfaestus) GFA visualizer, GPU-accelerated using Vulkan 
* [gfaviz](https://github.com/ggonnella/gfaviz) Graphical interactive tool for the visualization of sequence graphs in GFA format
* [AGB](https://github.com/almiheenko/AGB) Interactive assembly graph browser
* [MoMI-G](https://github.com/MoMI-G/MoMI-G/) Genome graph browser for SVs visualization. User can filter and visualize annotations and inspect SVs with read alignments over the genome graph. :rocket:
* [pangene](https://github.com/lh3/pangene) Pangene can visualize one protein set mapped to x genomes to check synteny and presence absence. :rocket:

# Pangenome viewers -static

* [vg view](https://github.com/vgteam/vg) - generates static images
* [odgi](https://github.com/pangenome/odgi) - generates static images

# Pangenome pipelines

* [pangenome](https://github.com/nf-core/pangenome). A comprehensive nf-core Nextflow pipeline using PGGB and odgi components. Better parallelized than PGGB alone. :rocket:
* [pangepop](https://forgemia.inra.fr/pangepop/pangepop) A snakemake pipeline to create a pangenome with minigraph-cactus and align reads against it with vg giraffe


# Graph validation tools

* [vg validate](https://github.com/vgteam/vg)
* [odgi validate](https://github.com/pangenome/odgi)

# File formats

* [GFA](http://gfa-spec.github.io/GFA-spec/GFA1.html) An assembly interchange format read by both vg and odgi :rocket:
* [rGFA](https://github.com/lh3/gfatools/blob/master/doc/rGFA.md) An extended GFA format, rGFA contains extra tags and includes a reference sequence. See minigraph.
* [vg](https://github.com/vgteam/vg) Vg has it's own mass of file formats: https://github.com/vgteam/vg/wiki/File-Formats#gam-graph-alignment--map-vgs-bam
* [odgi](https://github.com/pangenome/odgi) Easy interconversion to main interchange format GFA.
* [PanSN-spec](https://github.com/pangenome/PanSN-spec) A naming system for haplotypes in pangenomes
* [GAF - Graph Alignment Format](https://github.com/lh3/gfatools/blob/master/doc/rGFA.md#the-graph-alignment-format-gaf) Created by minigraph, convertible by vg. Similar to PAF.
* [GAM - Graph Alignment/Map](https://github.com/vgteam/vg/wiki/File-Formats#gam-graph-alignment--map-vgs-bam) and [here](https://github.com/vgteam/libvgio/blob/master/deps/vg.proto#L38-L54) Created by vg giraffe. May be superseded by GAF format.


# Miscellaneous tools

* [gfainject](https://github.com/chfi/gfainject) Map short alignments in BAM format to a GFA (seems it is not a real aligner but a conversion tool). Output in GAF format.
* [GRAFIMO](https://github.com/pinellolab/GRAFIMO) GRAph-based Finding of Individual Motif Occurrences using vg
* [rs-gfa](https://github.com/chfi/rs-gfa) A GFA parser in Rust.


# kmer based approaches

* [PanKmer](https://gitlab.com/salk-tm/pankmer)


# Libraries to explore pangenomes

* [gfapy](https://github.com/ggonnella/gfapy) implements GFA1 and GFA2 parsing and scalable exploration of graphs in Python
* [gfagraphs](https://github.com/Tharos-ux/gfagraphs) implements rGFA and GFA1 parsing and editing of graphs in Python
* [graphanalyzer](https://github.com/sablokgaurav/graphanalyzer) a python package to read and analyze the PAF and the GFA files for the graphs.


# Other lists of pangenome tools

* [Practical Pangenome Graphs](https://pangenome.github.io/)

# Contributions

Is something missing? Contributions are welcome, please make PRs to main or write an issue with a link.
