## Case Study: Genomic Insights into the Pathogenicity of E. coli O104:H4
## 1. Executive Summary
This project presents a de novo assembly and comparative genomic analysis of the Escherichia coli O104:H4 strain, responsible for the 2011 foodborne outbreak in Europe. The bacterial genome was reconstructed from high-throughput Immumina sequencing data and the molecular basis of its virulence was investigated. The analysis successfully identified pathogenicity islands carrying Shiga-toxin genes that are absent in the standard reference genome, highlighting the genomic plasticity of this pathogen.

## 2. Methodology & Workflow

### Data Acquisition: 

Raw paired-end reads were retrieved from the NCBI Sequence Read Archive (SRA accession: SRR292770).

### Preprocessing: 

Trimmomatic (v0.40) was used for adapter trimming and quality filtering (Phred33; LEADING:30, TRAILING:30, MINLEN:30).

### De Novo Assembly: 

SPAdes assembler was employed for initial contig generation, followed by scaffold refinement using RagTag.

### Annotation: 

Structural and functional annotation was performed via the RAST (Rapid Annotations using Subsystems Technology) server.

## 3. Assembly Quality Assessment

The quality of the de novo assembly was evaluated using QUAST. 

<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/7f0afd0f-03ca-44fe-aedb-51026c7bb04c" />

The assembly demonstrated high coverage, though it retained a level of fragmentation typical of short-read assembly, which was mitigated through scaffolding.

## 4. Pathogenicity Analysis

Comparative analysis using Mauve revealed significant structural variation between our de novo assembly and the reference genome.

<img width="1348" height="395" alt="image" src="https://github.com/user-attachments/assets/44369765-bc31-4c58-950e-94e90d76831b" />


Key Findings: While the overall genomic synteny is conserved, two distinct genetic loci were identified in the de novo assembly that were absent in the reference strain.

<img width="879" height="237" alt="image" src="https://github.com/user-attachments/assets/711b33de-7004-462d-bba3-782ab7efeafc" />

Virulence Factors: Functional annotation of these unique loci confirmed the presence of Shiga-toxin genes. This indicates that the studied isolate possesses a higher virulence potential than the chosen reference strain, likely acquired via horizontal gene transfer (prophage integration).

<img width="564" height="250" alt="image" src="https://github.com/user-attachments/assets/58b9838a-e1eb-4b4a-ac8d-64cd25cec63a" />    <img width="233" height="250" alt="image" src="https://github.com/user-attachments/assets/dc5dccb9-3983-4ace-a714-005d37848321" />


## 5. Conclusion
This study demonstrates the utility of de novo assembly in identifying mobile genetic elements that contribute to bacterial pathogenicity. The identification of Shiga-toxin genes exclusive to our assembly emphasizes that relying solely on standard reference genomes can lead to an underestimation of the virulence profile of a given isolate.
