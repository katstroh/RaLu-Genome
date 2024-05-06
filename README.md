# RaLu-Genome

This is the Rana luteiventris genome project for BZ 562. My goal with this project is to take ddRADseq reads from the Columbia spotted frog, Rana luteiventris, which was sequenced using Stacks in this publication:  [Forester et al. 2022](https://onlinelibrary.wiley.com/doi/10.1111/mec.16660), and align them to a recently published reference genome for a species in the same clade, the mountain yellow legged frog (Rana muscosa). This will enable me to compare de novo sequencing with reference genome alignment and inform our understanding of the genetics of R. luteiventris.

## Progress:

Rana muscosa genome accessed from NCBI and moved to Unix using conda package ncbi-datasets

Create conda environment:
```conda create -n ncbi_datasets```

Activate environment:
```conda activate ncbi_datasets```

Install the datasets conda package:
```conda install -c conda-forge ncbi-datasets-cli```

Access Rana muscosa genome and place it in a zipped file:
```datasets download genome taxon "Rana muscosa" --filename RaMu.zip```

Access ddRADseq reads for individual of Rana luteiventris through Globus and transfer to remote directory as a fastq file named "SRR21072383.fastq.gz"

To unzip the reference genome:
```unzip RaMu.zip```

Install BWA from https://github.com/lh3/bwa?tab=readme-ov-file

Add BWA to .bashrc so that it can be accessed from anywhere:
```export PATH=/projects/c836820202@colostate.edu/bwa:$PATH```




