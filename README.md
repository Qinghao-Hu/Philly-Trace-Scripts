## Introduction

This repository contains Jupyter Notebook scripts for analyzing Microsoft's Philly trace, which described in ["Analysis of Large-Scale Multi-Tenant GPU Clusters for DNN Training Workloads"](https://www.usenix.org/system/files/atc19-jeon.pdf) (ATC’19). 

The official public data can be download from [philly-traces](https://github.com/msr-fiddle/philly-traces). 

We provide the elaborate scripts to analyze the trace, however, some results are conflict to Microsoft provided. You can refer to [issue](https://github.com/msr-fiddle/philly-traces/issues/8) for more detailed information.

## Scripts Details

### `philly_analyse.ipynb`

**Description**: Code for generating time sequence trace data. 

**Input**: `cluster_job_log`, `revised_machine_list.csv`

**Output**: `timeseq.csv`


### `gpu_util_analyse.ipynb`

**Description**: Analyze the correct machine list in Philly cluster through GPU utils file.

**Input**: `cluster_gpu_util`

**Output**: `revised_machine_list.csv`


### `dataplot.ipynb`

**Description**: Plot the cluster machine distribution and time sequence cluster GPU utilization.

**Input**: `revised_machine_list.csv`, `timeseq.csv`

**Output**: figures in `imgs` folder