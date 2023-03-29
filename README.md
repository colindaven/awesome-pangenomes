# awesome-pangenomes
## A list of software capable of analyzing eukaryotic genomes for pangenomics 


# Toolkits

* vg https://github.com/vgteam/vg Full featured construction, mapping and SNP calling toolkit based on multiple formats.
* odgi https://github.com/pangenome/odgi Fast toolkit based on odgi format
* gfatools https://github.com/lh3/gfatools Toolkit for GFA parsing and conversion



# Pangenome construction

* Minigraph https://github.com/lh3/minigraph Fast method intended for 50+ bp SVs by Heng Li
* Cactus/minigraph https://github.com/ComparativeGenomicsToolkit/cactus 
* PGGB https://github.com/pangenome/pggb Pangenome Graph Builder, calculates SNPs as part of the pipeline.
* Pantools v3+ https://git.wur.nl/bioinformatics/pantools Fully featured construction and 
* PSVCP https://github.com/wjian8/psvcp_v1.01
* PHG Practical Haplotype Graph https://bitbucket.org/bucklerlab/practicalhaplotypegraph/wiki/Home


# Short read alignment to a pangenome graph

* vg map https://github.com/vgteam/vg Original vg mapper
* vg giraffe https://github.com/vgteam/vg Faster and more modern alternative to vg map
* Hisat2 https://github.com/DaehwanKimLab/hisat2



# Long read alignment to a pangenome graph

* GraphAligner https://github.com/maickrau/GraphAligner Fast long read aligner
* Minigraph https://github.com/lh3/minigraph Construct graphs or align long reads to graphs
* GraphChainer https://github.com/algbio/GraphChainer Built on codebase of GraphAligner



# SNP callers and genotypers

* vg call https://github.com/vgteam/vg
* Paragraph https://github.com/Illumina/paragraph
* Pangenie https://github.com/eblerjana/pangenie
* vg surject to linear reference, then use linear caller like Freebayes, Deepvariant etc



# Structural Variation (SV) callers and genotypers

* vg call https://github.com/vgteam/vg
* GraphTyper https://github.com/DecodeGenetics/graphtyper 
* Pangenie https://github.com/eblerjana/pangenie



# Pangenome viewers -interactive

* Panagram https://github.com/kjenike/panagram 
* Bandage https://github.com/rrwick/Bandage Visualize GFA files
* SeqTubemap https://github.com/vgteam/sequenceTubeMap Elegant path visualization for smaller regions of a pangenome from the vg team
* VAG https://github.com/lipingfangs/VAG Visualization of short sequence alignments in a pangenome
* Panache https://github.com/SouthGreenPlatform/panache View linearized pangenomes
* Waragraph https://github.com/chfi/waragraph

# Pangenome viewers -static

* vg - generates static images
* odgi - generates static images


# Graph validation tools

* vg validate
* odgi validate



# File formats

* GFA http://gfa-spec.github.io/GFA-spec/GFA1.html An assembly interchange format read by both vg and odgi
* rGFA https://github.com/lh3/gfatools/blob/master/doc/rGFA.md An extended GFA format, rGFA contains extra tags.
* vg https://github.com/vgteam/vg Vg has it's own mass of file formats: https://github.com/vgteam/vg/wiki/File-Formats#gam-graph-alignment--map-vgs-bam
* odgi https://github.com/pangenome/odgi
* PanSN-spec https://github.com/pangenome/PanSN-spec A naming system for haplotypes in pangenomes
* GAF - Graph Alignment Format https://github.com/lh3/gfatools/blob/master/doc/rGFA.md#the-graph-alignment-format-gaf. Created by minigraph, convertible by vg. Similar to PAF.
* GAM - Graph Alignment/Map https://github.com/vgteam/vg/wiki/File-Formats#gam-graph-alignment--map-vgs-bam. Created by vg giraffe. 



# Contributions

Is something missing? Contributions are welcome, please make PRs to main.
