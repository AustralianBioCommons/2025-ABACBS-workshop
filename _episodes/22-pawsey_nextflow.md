---
title: "Run NextFlow pipeline on Setonix"
teaching: 0
exercises: 15
questions:
objectives:
- Run NextFlow pipeline on Setonix
keypoints:
- Logging on to Pawsey systems uses SSH (secure shell)
---
### Load required modules
Pawsey has pre-installed Nextflow and Singularity which can be loaded in your user environment using

```bash
module load module load nextflow/24.10.0 #TODO: test this (prefer not conda installed)
module load singularity/4.1.0-slurm
```

### Nextflow workflow execution
During workflow execution Nextflow will pull the neccessary containers from a hosted repository.

```bash
nextflow run nf-core/hello
```

You can see the workflow code that has been pulled is available at `$HOME/.nextflow/assets/nf-core/hello`. Similarly, NextFlow will automatically pull the containers required to execute the workflow. These can be found in the default work directory.


# TODO: Any extra background here?