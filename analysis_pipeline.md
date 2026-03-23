# Complete Analysis Pipeline

## Sample Information
- Total Samples: 5 Staphylococcus aureus isolates
- Sample IDs: G20253359, G20253360, G20253361, G20253517, G20253518
- Origin: Indian hospitals
- Focus: ST22-MRSA clones with PVL gene characterization
---

## Tool Versions Used
| Tool | Version | Purpose |
|------|---------|---------|
| GHRU Assembly Pipeline | Latest (Nextflow DSL2) | Assembly |
| Bakta | v1.9.3 | Genome annotation |
| mlst | v2.23.0 | MLST typing |
| spaTyper | v1.0 | Spa typing |
| sccmec | Latest (GitHub) | SCCmec typing |
| AMRFinderPlus | v3.11.18 | AMR gene detection |
| ABRicate | v1.0.1 | Virulence gene detection |
| PHASTEST | Docker version | Prophage analysis |
| Snippy | v4.6.0 | SNP detection |
| IQ-TREE | v2.2.2.6 | Phylogenetic tree building |
| Microreact | Web-based | Tree visualization |

---

## Step 1: Assembly

### Tool: GHRU Assembly Pipeline
Purpose: Assemble short-read FASTQ files from Illumina sequencing

```bash
nextflow run main.nf \
  --input_dir /data/internship_data/rachana/staph_aur \
  --output_dir assembly_output \
  --fastq_pattern 'G*_{1,2}.fastq.gz' \
  --adapter_file adapters.fas \
  --qc_conditions qc_conditions_nextera_relaxed.yml
Input: Raw reads in FASTQ format

Forward reads: G*_1.fastq.gz

Reverse reads: G*_2.fastq.gz

Output: Assembled contigs in FASTA format (all 5 samples passed QC)
