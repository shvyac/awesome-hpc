<!--lint ignore-->
# Awesome HPC [![Awesome](https://awesome.re/badge-flat.svg)](https://awesome.re)

[日本語版はこちら / Japanese](README.ja.md)

High Performance Computing tools and resources for engineers and administrators. ⭐ badges show live GitHub star counts (via shields.io).

High Performance Computing (HPC) most generally refers to the practice of aggregating computing power in a way that delivers much higher performance than one could get out of a typical desktop computer or workstation in order to solve large problems in science, engineering, or business.

> Forked from [dstdev/awesome-hpc](https://github.com/dstdev/awesome-hpc) ![GitHub stars](https://img.shields.io/github/stars/dstdev/awesome-hpc?style=flat&label=%E2%AD%90) and refreshed (2026-10): moved / renamed / archived projects updated, plus newer schedulers, workflow engines, performance-portability layers, and storage.

## Contents
<details>
  <summary><b>(click to expand)</b></summary>

- [Provisioning](#provisioning)
- [Workload Managers](#workload-managers)
- [Pipelines](#pipelines)
- [Applications](#applications)
- [Compilers](#compilers)
- [MPI](#mpi)
- [Parallel Computing](#parallel-computing)
- [Benchmarking](#benchmarking)
- [Miscellaneous](#miscellaneous)
- [Performance](#performance)
- [Parallel Shells](#parallel-shells)
- [Containers](#containers)
- [Environment Management](#environment-management)
- [Visualization](#visualization)
- [Parallel Filesystems](#parallel-filesystems)
- [Programming Languages](#programming-languages)
- [Monitoring](#monitoring)
- [Journals](#journals)
- [Podcasts](#podcasts)
- [Blogs](#blogs)
- [Conferences](#conferences)
- [Websites](#websites)
- [User Groups](#user-groups)
- [Contributing](#contributing)
- [shvyac's awesome lists](#shvyacs-awesome-lists)

</details>

## Provisioning
- [Grendel](https://grendel.readthedocs.io/) ![GitHub stars](https://img.shields.io/github/stars/ubccr/grendel?style=flat&label=%E2%AD%90) - Bare Metal Provisioning system for HPC Linux clusters ([Source Code](https://github.com/ubccr/grendel)) `GPL-3`.
- [xCAT](https://xcat.org/) ![GitHub stars](https://img.shields.io/github/stars/xcat2/xcat-core?style=flat&label=%E2%AD%90) - xCAT is a toolkit for deployment and administration of clusters of all sizes; the 2023 sunset was reversed and development continues under the xCAT Consortium ([Source Code](https://github.com/xcat2/xcat-core)) `EPL-1.0`.
- [Confluent](https://xcat2.github.io/confluent-docs/) ![GitHub stars](https://img.shields.io/github/stars/xcat2/confluent?style=flat&label=%E2%AD%90) - Bootstrap, deployment and operation of scale-out server configurations; recommended by the xCAT project as its long-term successor ([Source Code](https://github.com/xcat2/confluent)) `Apache-2.0`.
- [Warewulf](https://warewulf.org/) ![GitHub stars](https://img.shields.io/github/stars/warewulf/warewulf?style=flat&label=%E2%AD%90) - Warewulf is a stateless and diskless container operating system provisioning system for large clusters of bare metal and/or virtual systems ([Source Code](https://github.com/warewulf/warewulf)) `BSD-3`.
- [Rocks](http://www.rocksclusters.org/) - A Linux distribution for developing Linux clusters; no longer actively developed (last release 7.0, 2017) `other`.
- [Cobbler](https://cobbler.github.io/) ![GitHub stars](https://img.shields.io/github/stars/cobbler/cobbler?style=flat&label=%E2%AD%90) - Cobbler is a Linux installation server that allows for rapid setup of network installation environments ([Source Code](https://github.com/cobbler/cobbler)) `GPL-2.0`.
- [Base Command Manager](https://docs.nvidia.com/base-command-manager/index.html) - NVIDIA Base Command Manager (formerly Bright Cluster Manager) allows administrators to quickly build and manage heterogeneous clusters `Proprietary`.
- [Scyld](https://www.penguinsolutions.com/computing/products/software/scyld-clusterware/) - Scyld ClusterWare is developed based on the continuing evolution of Beowulf clusters first developed at NASA in the 1990s `Proprietary`.
- [BlueBanquise](https://bluebanquise.com) ![GitHub stars](https://img.shields.io/github/stars/bluebanquise/bluebanquise?style=flat&label=%E2%AD%90) - BlueBanquise is an open source cluster deployment and management stack built on Python and Ansible ([Source Code](https://github.com/bluebanquise/bluebanquise)) `MIT`.

## Workload Managers
- [Slurm](https://slurm.schedmd.com/documentation.html) ![GitHub stars](https://img.shields.io/github/stars/SchedMD/slurm?style=flat&label=%E2%AD%90) - A free and open source, highly scalable workload manager and job scheduler; SchedMD was acquired by NVIDIA in December 2025 ([Source Code](https://github.com/SchedMD/slurm)) `GPL-2.0`.
- [OpenPBS](https://www.openpbs.org/) ![GitHub stars](https://img.shields.io/github/stars/openpbs/openpbs?style=flat&label=%E2%AD%90) - OpenPBS® software optimizes job scheduling and workload management in high-performance computing (HPC) environments ([Source Code](https://github.com/openpbs/openpbs)) `AGPL-3.0`.
- [Flux](https://flux-framework.org/) ![GitHub stars](https://img.shields.io/github/stars/flux-framework/flux-core?style=flat&label=%E2%AD%90) - Next-generation hierarchical resource manager and scheduler from LLNL, usable standalone or nested inside other schedulers ([Source Code](https://github.com/flux-framework/flux-core)) `LGPL-3.0`.
- [HTCondor](https://htcondor.org/) ![GitHub stars](https://img.shields.io/github/stars/htcondor/htcondor?style=flat&label=%E2%AD%90) - High-throughput computing workload manager for large numbers of independent jobs ([Source Code](https://github.com/htcondor/htcondor)) `Apache-2.0`.
- [LSF](https://www.ibm.com/products/hpc-workload-management) - A job scheduler and workload management software developed by IBM `Proprietary`.
- [Grid Engine](https://www.siemens.com/en-us/products/hpcworks/grid-engine/) - HPCWorks Grid Engine (formerly Univa / Altair Grid Engine), now part of Siemens after its acquisition of Altair `Proprietary`.
- [Moab](https://adaptivecomputing.com/moab-hpc-suite/) - Moab is a workload management and job scheduler `other`.
- [Torque](https://github.com/adaptivecomputing/torque) ![GitHub stars](https://img.shields.io/github/stars/adaptivecomputing/torque?style=flat&label=%E2%AD%90) - Torque is a workload management and job scheduler from Adaptive Computing `other`.
- [Volcano](https://volcano.sh/) ![GitHub stars](https://img.shields.io/github/stars/volcano-sh/volcano?style=flat&label=%E2%AD%90) - Volcano is a CNCF batch system built on Kubernetes for AI/ML, big data, and HPC ([Source Code](https://github.com/volcano-sh/volcano)) `Apache-2.0`.
- [Kueue](https://kueue.sigs.k8s.io/) ![GitHub stars](https://img.shields.io/github/stars/kubernetes-sigs/kueue?style=flat&label=%E2%AD%90) - Kubernetes-native job queueing and quota management (SIG Scheduling) ([Source Code](https://github.com/kubernetes-sigs/kueue)) `Apache-2.0`.
- [Slinky](https://slinky.schedmd.com/) ![GitHub stars](https://img.shields.io/github/stars/SlinkyProject/slurm-operator?style=flat&label=%E2%AD%90) - SchedMD / NVIDIA toolkit for running Slurm on Kubernetes (slurm-operator, slurm-bridge, and container images) ([Source Code](https://github.com/SlinkyProject/slurm-operator)) `Apache-2.0`.
- [Kube Batch](https://github.com/kubernetes-retired/kube-batch) ![GitHub stars](https://img.shields.io/github/stars/kubernetes-retired/kube-batch?style=flat&label=%E2%AD%90) - A batch scheduler of Kubernetes for high performance workloads; archived (retired), see Volcano and Kueue `Apache-2.0`.

## Pipelines
- [Nextflow](https://nextflow.io) ![GitHub stars](https://img.shields.io/github/stars/nextflow-io/nextflow?style=flat&label=%E2%AD%90) - Data-driven computational pipelines ([Source Code](https://github.com/nextflow-io/nextflow)) `Apache-2.0`.
- [Snakemake](https://snakemake.github.io/) ![GitHub stars](https://img.shields.io/github/stars/snakemake/snakemake?style=flat&label=%E2%AD%90) - Python-based workflow management system with Slurm and other cluster executors ([Source Code](https://github.com/snakemake/snakemake)) `MIT`.
- [Parsl](https://parsl-project.org/) ![GitHub stars](https://img.shields.io/github/stars/Parsl/parsl?style=flat&label=%E2%AD%90) - Python parallel scripting library for running tasks across laptops, clusters, and supercomputers ([Source Code](https://github.com/Parsl/parsl)) `Apache-2.0`.
- [Cromwell](https://cromwell.readthedocs.io/en/stable/) ![GitHub stars](https://img.shields.io/github/stars/broadinstitute/cromwell?style=flat&label=%E2%AD%90) - Scientific workflow engine designed for simplicity & scalability ([Source Code](https://github.com/broadinstitute/cromwell)) `BSD-3`.
- [Pegasus](https://pegasus.isi.edu/) ![GitHub stars](https://img.shields.io/github/stars/pegasus-isi/pegasus?style=flat&label=%E2%AD%90) - A configurable system for mapping and executing scientific workflows over a wide range of computational infrastructure ([Source Code](https://github.com/pegasus-isi/pegasus)) `Apache-2.0`.

## Applications
- [Spack](https://spack.io) ![GitHub stars](https://img.shields.io/github/stars/spack/spack?style=flat&label=%E2%AD%90) - A flexible package manager that supports multiple versions, configurations, platforms, and compilers ([Source Code](https://github.com/spack/spack)) `other`.
- [EasyBuild](https://easybuild.io/) ![GitHub stars](https://img.shields.io/github/stars/easybuilders/easybuild?style=flat&label=%E2%AD%90) - EasyBuild - building software with ease ([Source Code](https://github.com/easybuilders/easybuild)) `GPL-2`.

## Compilers
- [Nvidia](https://developer.nvidia.com/hpc-compilers) - NVIDIA HPC SDK compilers for Fortran, C/C++ with OpenACC, OpenMP, and CUDA `Proprietary`.
- [Portland Group](https://developer.nvidia.com/hpc-sdk) - The former PGI Fortran, C/C++ compilers, now integrated into the NVIDIA HPC SDK `Proprietary`.
- [Intel](https://www.intel.com/content/www/us/en/developer/tools/oneapi/hpc-toolkit.html) - Intel oneAPI HPC Toolkit with the LLVM-based Intel C/C++ (icx) and Fortran (ifx) compilers `Proprietary`.
- [Cray](https://cpe.ext.hpe.com/docs/) - HPE Cray Compiling Environment (CCE), part of the HPE Cray Programming Environment `Proprietary`.
- [GNU](https://gcc.gnu.org/) - The GNU Compiler Collection is a suite of compilers targeting many languages ([Source Code](https://gcc.gnu.org/git.html)) `GPL-3`.
- [LLVM](https://llvm.org/) ![GitHub stars](https://img.shields.io/github/stars/llvm/llvm-project?style=flat&label=%E2%AD%90) - The LLVM project is a collection of modular compilers and toolchains, including the Flang Fortran compiler ([Source Code](https://github.com/llvm/llvm-project)) `Apache-2.0`.

## MPI
- [OpenMPI](https://www.open-mpi.org/) ![GitHub stars](https://img.shields.io/github/stars/open-mpi/ompi?style=flat&label=%E2%AD%90) - Open source MPI implementation (v5.x: full MPI-3.1 conformance with many MPI-4.0 features) ([Source Code](https://github.com/open-mpi/ompi)) `BSD`.
- [MPICH](https://www.mpich.org/) ![GitHub stars](https://img.shields.io/github/stars/pmodels/mpich?style=flat&label=%E2%AD%90) - MPICH is a high-performance and widely portable implementation of the MPI standard ([Source Code](https://github.com/pmodels/mpich)) `other`.
- [MVAPICH](https://mvapich.cse.ohio-state.edu/) - MVAPICH is an open source MPI implementation for InfiniBand, RoCE, and other high-performance networks developed by Ohio State University `BSD`.
- [Intel-MPI](https://www.intel.com/content/www/us/en/developer/tools/oneapi/mpi-library.html) - Intel MPI Library, Intel's MPICH-based implementation of the MPI standard `other`.

## Parallel Computing
- [ArrayFire](https://arrayfire.org/docs/index.htm) ![GitHub stars](https://img.shields.io/github/stars/arrayfire/arrayfire?style=flat&label=%E2%AD%90) - A general purpose tensor library that simplifies the process of software development for parallel architectures ([Source Code](https://github.com/arrayfire/arrayfire)) `BSD-3`.
- [OpenMP](https://www.openmp.org/) - OpenMP is an application programming interface that supports multi-platform shared-memory multiprocessing programming `other`.
- [Kokkos](https://kokkos.org/) ![GitHub stars](https://img.shields.io/github/stars/kokkos/kokkos?style=flat&label=%E2%AD%90) - C++ performance portability programming ecosystem for CPUs and GPUs ([Source Code](https://github.com/kokkos/kokkos)) `Apache-2.0 WITH LLVM-exception`.
- [RAJA](https://raja.readthedocs.io/) ![GitHub stars](https://img.shields.io/github/stars/llnl/RAJA?style=flat&label=%E2%AD%90) - LLNL C++ performance portability layer for loop-level parallelism ([Source Code](https://github.com/llnl/RAJA)) `BSD-3`.

## Benchmarking
- [OSU Benchmarks](https://mvapich.cse.ohio-state.edu/benchmarks/) - A collection of benchmarking tools for MPI developed by Ohio State University `other`.
- [Intel MPI Benchmarks](https://github.com/intel/mpi-benchmarks) ![GitHub stars](https://img.shields.io/github/stars/intel/mpi-benchmarks?style=flat&label=%E2%AD%90) - A set of MPI performance benchmarks developed by Intel `other`.
- [HPCC Systems](https://hpccsystems.com/) ![GitHub stars](https://img.shields.io/github/stars/hpcc-systems/HPCC-Platform?style=flat&label=%E2%AD%90) - HPCC Systems (High Performance Computing Cluster) is an open source, massive parallel-processing computing platform for big data processing and analytics ([Source Code](https://github.com/hpcc-systems/HPCC-Platform)) `other`.
- [LINPACK](https://www.netlib.org/linpack/) - LINPACK is a set of efficient fortran subroutines for solving linear systems which benchmarks are useful for HPC `other`.
- [IOzone](https://www.iozone.org/) - IOzone is a filesystem benchmark tool `OSS`.
- [IOR](https://ior.readthedocs.io/) ![GitHub stars](https://img.shields.io/github/stars/hpc/ior?style=flat&label=%E2%AD%90) - Interleaved or Random is a useful benchmarking tool for testing parallel filesystems ([Source Code](https://github.com/hpc/ior)) `GPL-2`.
- [MDtest](https://ior.readthedocs.io/) ![GitHub stars](https://img.shields.io/github/stars/hpc/ior?style=flat&label=%E2%AD%90) - MDtest is an MPI-based application for evaluating the metadata performance of a file system, shipped with IOR ([Source Code](https://github.com/hpc/ior)) `GPL-2`.
- [FIO](https://fio.readthedocs.io/en/latest/fio_doc.html) ![GitHub stars](https://img.shields.io/github/stars/axboe/fio?style=flat&label=%E2%AD%90) - Flexible I/O is an advanced disk benchmark that depends upon the kernel's AIO access library ([Source Code](https://github.com/axboe/fio)) `GPL-2`.
- [elbencho](https://github.com/breuner/elbencho) ![GitHub stars](https://img.shields.io/github/stars/breuner/elbencho?style=flat&label=%E2%AD%90) - A distributed storage benchmark for files, objects & blocks with support for GPUs `GPL-3`.

## Miscellaneous
- [OpenOnDemand](https://openondemand.org/) ![GitHub stars](https://img.shields.io/github/stars/OSC/ondemand?style=flat&label=%E2%AD%90) - Open OnDemand helps computational researchers and students efficiently utilize remote computing resources by making them easy to access from any device ([Source Code](https://github.com/OSC/ondemand)) `MIT`.
- [Open XDMod](https://open.xdmod.org) ![GitHub stars](https://img.shields.io/github/stars/ubccr/xdmod?style=flat&label=%E2%AD%90) - Open XDMoD is an open source tool to facilitate the management of high performance computing resources ([Source Code](https://github.com/ubccr/xdmod/)) `LGPL-3`.
- [Coldfront](https://coldfront.readthedocs.io/en/latest/) ![GitHub stars](https://img.shields.io/github/stars/coldfront/coldfront?style=flat&label=%E2%AD%90) - ColdFront is an open source resource allocation system designed to provide a central portal for administration, reporting, and measuring scientific impact of HPC resources ([Source Code](https://github.com/coldfront/coldfront)) `GPL-3`.
- [Pavilion2](https://pavilion2.readthedocs.io/) ![GitHub stars](https://img.shields.io/github/stars/hpc/pavilion2?style=flat&label=%E2%AD%90) - Pavilion is a Python 3 (3.6+) based framework for running and analyzing tests targeting HPC systems ([Source Code](https://github.com/hpc/pavilion2)) `other`.
- [Reframe](https://reframe-hpc.readthedocs.io/en/stable/) ![GitHub stars](https://img.shields.io/github/stars/reframe-hpc/reframe?style=flat&label=%E2%AD%90) - A powerful Python framework for writing and running portable regression tests and benchmarks for HPC systems ([Source Code](https://github.com/reframe-hpc/reframe)) `BSD-3`.
- [OLCF Test Harness](https://olcf.github.io/olcf-test-harness/) ![GitHub stars](https://img.shields.io/github/stars/olcf/olcf-test-harness?style=flat&label=%E2%AD%90) - The OLCF Test Harness (OTH) helps automate the testing of applications, tools, and other system software ([Source Code](https://github.com/olcf/olcf-test-harness)) `other`.
- [GoSlmailer](https://github.com/CLIP-HPC/goslmailer) ![GitHub stars](https://img.shields.io/github/stars/CLIP-HPC/goslmailer?style=flat&label=%E2%AD%90) - Goslmailer is a drop-in notification delivery solution for slurm that can do slack, mattermost, teams, and more.

## Performance
- [TotalView](https://totalview.io/products/totalview) - TotalView is a debugging tool for HPC applications `Proprietary`.
- [Tau](https://www.cs.uoregon.edu/research/tau/home.php) - TAU Performance System® is a portable profiling and tracing toolkit for performance analysis of parallel programs written in Fortran, C, C++, UPC, Java, Python `other`.
- [Valgrind](https://www.valgrind.org/) - Valgrind is a tool designed to profile programs to determine memory leaks ([Source Code](https://sourceware.org/git/?p=valgrind.git)) `GPL-2`.
- [Paraver](https://tools.bsc.es/paraver) - Paraver is a very flexible data browser that is part of the CEPBA-Tools toolkit `other`.
- [PAPI](https://icl.utk.edu/papi/) - Performance Application Programming Interface (PAPI) is a performance analysis tool `other`.
- [HPCToolkit](https://hpctoolkit.org/) - Sampling-based performance measurement and analysis for CPU and GPU applications on supercomputers; development moved from GitHub to GitLab ([Source Code](https://gitlab.com/hpctoolkit/hpctoolkit)) `BSD-3`.
- [Caliper](https://github.com/llnl/Caliper) ![GitHub stars](https://img.shields.io/github/stars/llnl/Caliper?style=flat&label=%E2%AD%90) - LLNL instrumentation and performance profiling library with annotation APIs for C, C++, Fortran and Python `BSD-3`.
- [Darshan](https://wordpress.cels.anl.gov/darshan/) ![GitHub stars](https://img.shields.io/github/stars/darshan-hpc/darshan?style=flat&label=%E2%AD%90) - Lightweight, scalable I/O characterization tool for capturing application I/O behavior on HPC systems ([Source Code](https://github.com/darshan-hpc/darshan)) `other`.

## Parallel Shells
- [pdsh](https://linux.die.net/man/1/pdsh) ![GitHub stars](https://img.shields.io/github/stars/chaos/pdsh?style=flat&label=%E2%AD%90) - pdsh runs terminal commands across multiple hosts in parallel ([Source Code](https://github.com/chaos/pdsh)) `GPL-2`.
- [ClusterShell](https://clustershell.readthedocs.io/en/latest/intro.html) ![GitHub stars](https://img.shields.io/github/stars/clustershell/clustershell?style=flat&label=%E2%AD%90) - Scalable cluster administration Python framework ([Source Code](https://github.com/clustershell/clustershell)) `LGPL-2.1`.

## Containers
- [Apptainer](https://apptainer.org) ![GitHub stars](https://img.shields.io/github/stars/apptainer/apptainer?style=flat&label=%E2%AD%90) - Apptainer (formerly Singularity) is an open source container system ([Source Code](https://github.com/apptainer/apptainer)) `BSD`.
- [SingularityCE](https://sylabs.io/docs/) ![GitHub stars](https://img.shields.io/github/stars/sylabs/singularity?style=flat&label=%E2%AD%90) - Community Edition of Singularity maintained by Sylabs ([Source Code](https://github.com/sylabs/singularity)) `other`.
- [Charliecloud](https://charliecloud.io/) - Charliecloud provides user-defined software stacks (UDSS) for high-performance computing (HPC) centers; development moved to GitLab ([Source Code](https://gitlab.com/charliecloud/charliecloud)) `Apache-2.0`.
- [Docker](https://www.docker.com/) - Docker is a set of platform as a service products that use OS-level virtualization to deliver software in packages called containers `other`.
- [uDocker](https://indigo-dc.github.io/udocker/) ![GitHub stars](https://img.shields.io/github/stars/indigo-dc/udocker?style=flat&label=%E2%AD%90) - A basic user tool to execute simple docker containers in batch or interactive systems without root privileges ([Source Code](https://github.com/indigo-dc/udocker)) `Apache-2.0`.
- [Shifter](https://www.nersc.gov/research-and-development/user-defined-images/) ![GitHub stars](https://img.shields.io/github/stars/NERSC/shifter?style=flat&label=%E2%AD%90) - Shifter is Linux containers for HPC ([Source Code](https://github.com/NERSC/shifter)) `other`.
- [HPC Container Maker](https://github.com/NVIDIA/hpc-container-maker) ![GitHub stars](https://img.shields.io/github/stars/NVIDIA/hpc-container-maker?style=flat&label=%E2%AD%90) - HPC Container Maker is an open source tool to make it easier to generate container specification files `Apache-2.0`.
- [Sarus](https://github.com/eth-cscs/sarus) ![GitHub stars](https://img.shields.io/github/stars/eth-cscs/sarus?style=flat&label=%E2%AD%90) - An OCI-compatible container engine for HPC `BSD`.
- [Singularity HPC](https://singularity-hpc.readthedocs.io) ![GitHub stars](https://img.shields.io/github/stars/singularityhub/singularity-hpc?style=flat&label=%E2%AD%90) - Singularity Registry HPC (shpc) allows you to install containers as modules ([Source Code](https://github.com/singularityhub/singularity-hpc)) `MPL 2.0`.

## Environment Management
- [Lmod](https://lmod.readthedocs.io/en/latest/) ![GitHub stars](https://img.shields.io/github/stars/TACC/Lmod?style=flat&label=%E2%AD%90) - Lmod: An Environment Module System based on Lua, Reads TCL Modules, Supports a Software Hierarchy ([Source Code](https://github.com/TACC/Lmod)) `other`.
- [Environment Modules](https://modules.readthedocs.io/en/latest/) ![GitHub stars](https://img.shields.io/github/stars/envmodules/modules?style=flat&label=%E2%AD%90) - Environment Modules: provides dynamic modification of a user's environment ([Source Code](https://github.com/envmodules/modules)) `GPL-2`.
- [Anaconda](https://www.anaconda.com/) - Anaconda is a Python and R distribution for use in computational science `other`.
- [Miniforge](https://conda-forge.org/download/) ![GitHub stars](https://img.shields.io/github/stars/conda-forge/miniforge?style=flat&label=%E2%AD%90) - Minimal conda / mamba installer that defaults to the community conda-forge channel ([Source Code](https://github.com/conda-forge/miniforge)) `other`.
- [Mamba](https://mamba.readthedocs.io/en/latest/) ![GitHub stars](https://img.shields.io/github/stars/mamba-org/mamba?style=flat&label=%E2%AD%90) - Mamba is a reimplementation of the conda package manager in C++ ([Source Code](https://github.com/mamba-org/mamba)) `BSD`.
- [Pixi](https://pixi.sh/) ![GitHub stars](https://img.shields.io/github/stars/prefix-dev/pixi?style=flat&label=%E2%AD%90) - Fast, reproducible project and environment manager built on the conda ecosystem (Rust) ([Source Code](https://github.com/prefix-dev/pixi)) `BSD-3`.

## Visualization
- [Visit](https://visit-dav.github.io/visit-website/) ![GitHub stars](https://img.shields.io/github/stars/visit-dav/visit?style=flat&label=%E2%AD%90) - VisIt - Visualization and Data Analysis for Mesh-based Scientific Data ([Source Code](https://github.com/visit-dav/visit)) `BSD-3`.
- [Paraview](https://www.paraview.org/) ![GitHub stars](https://img.shields.io/github/stars/Kitware/ParaView?style=flat&label=%E2%AD%90) - ParaView is an open-source, multi-platform data analysis and visualization application based on Visualization Toolkit (VTK) ([Source Code](https://github.com/Kitware/ParaView)) `BSD-3`.

## Parallel Filesystems
- [IBM Storage Scale (GPFS)](https://www.ibm.com/products/storage-scale) - High-performance clustered file system from IBM, formerly GPFS / Spectrum Scale `Proprietary`.
- [Quobyte](https://www.quobyte.com/) - A high performance filesystem `Proprietary`.
- [Ceph](https://ceph.io/en/) ![GitHub stars](https://img.shields.io/github/stars/ceph/ceph?style=flat&label=%E2%AD%90) - Ceph is a distributed object, block, and file storage platform ([Source Code](https://github.com/ceph/ceph)) `other`.
- [Weka](https://www.weka.io/) - A file system designed for HPC `Proprietary`.
- [Lustre/Exascaler](https://www.lustre.org/) - Lustre is an open-source, distributed parallel file system software platform designed for scalability, high-performance, and high-availability ([Source Code](https://git.whamcloud.com/fs/lustre-release.git)) `other`.
- [BeeGFS](https://www.beegfs.io/) ![GitHub stars](https://img.shields.io/github/stars/ThinkParQ/beegfs?style=flat&label=%E2%AD%90) - BeeGFS is a hardware-independent POSIX parallel file system developed with a strong focus on performance and designed for ease of use, simple installation, and management ([Source Code](https://github.com/ThinkParQ/beegfs)) `other`.
- [DAOS](https://daos.io/) ![GitHub stars](https://img.shields.io/github/stars/daos-stack/daos?style=flat&label=%E2%AD%90) - Distributed Asynchronous Object Storage: open source, NVMe-native storage stack for HPC and AI ([Source Code](https://github.com/daos-stack/daos)) `BSD-2-Clause-Patent`.
- [OrangeFS](http://www.orangefs.org/) ![GitHub stars](https://img.shields.io/github/stars/waltligon/orangefs?style=flat&label=%E2%AD%90) - OrangeFS is a next generation parallel file system for Linux clusters ([Source Code](https://github.com/waltligon/orangefs)) `other`.
- [MooseFS](https://moosefs.com/) ![GitHub stars](https://img.shields.io/github/stars/moosefs/moosefs?style=flat&label=%E2%AD%90) - Moose File System is an Open-source, POSIX-compliant distributed file system developed by Core Technology ([Source Code](https://github.com/moosefs/moosefs)) `GPL-2.0`.

## Programming Languages
- [Julia](https://julialang.org/) ![GitHub stars](https://img.shields.io/github/stars/JuliaLang/julia?style=flat&label=%E2%AD%90) - Julia is a high-level, high-performance dynamic language for technical computing ([Source Code](https://github.com/JuliaLang/julia)) `MIT`.
- [Futhark](https://futhark-lang.org/) ![GitHub stars](https://img.shields.io/github/stars/diku-dk/futhark?style=flat&label=%E2%AD%90) - Futhark is a purely functional data-parallel programming language in the ML family ([Source Code](https://github.com/diku-dk/futhark)) `isc`.
- [Chapel](https://chapel-lang.org/) ![GitHub stars](https://img.shields.io/github/stars/chapel-lang/chapel?style=flat&label=%E2%AD%90) - Chapel is a programming language designed for productive parallel computing at scale ([Source Code](https://github.com/chapel-lang/chapel)) `Apache-2.0`.

## Monitoring
### Prometheus Based
- [Slurm Exporter](https://github.com/vpenso/prometheus-slurm-exporter) ![GitHub stars](https://img.shields.io/github/stars/vpenso/prometheus-slurm-exporter?style=flat&label=%E2%AD%90) - Prometheus exporter for performance metrics from Slurm `GPL-3.0`.
- [Slurm Exporter (Rivos)](https://github.com/rivosinc/prometheus-slurm-exporter) ![GitHub stars](https://img.shields.io/github/stars/rivosinc/prometheus-slurm-exporter?style=flat&label=%E2%AD%90) - Actively maintained Slurm exporter exposing select scheduler metrics to Prometheus `Apache-2.0`.
- [Slurm Exporter](https://github.com/ubccr/slurm-exporter) ![GitHub stars](https://img.shields.io/github/stars/ubccr/slurm-exporter?style=flat&label=%E2%AD%90) - Slurm Exporter for Prometheus using Rest API `GPL-3.0`.
- [Infiniband Exporter](https://github.com/treydock/infiniband_exporter) ![GitHub stars](https://img.shields.io/github/stars/treydock/infiniband_exporter?style=flat&label=%E2%AD%90) - The InfiniBand exporter collects counters from InfiniBand switches and HCAs `Apache-2.0`.
- [Cgroup Exporter](https://github.com/treydock/cgroup_exporter) ![GitHub stars](https://img.shields.io/github/stars/treydock/cgroup_exporter?style=flat&label=%E2%AD%90) - Produces metrics from cgroups `Apache-2.0`.
- [Cgroup Exporter](https://github.com/phpHavok/cgroups_exporter) ![GitHub stars](https://img.shields.io/github/stars/phpHavok/cgroups_exporter?style=flat&label=%E2%AD%90) - A Prometheus exporter for cgroup-level metrics `unknown`.
- [GPFS Exporter](https://github.com/treydock/gpfs_exporter) ![GitHub stars](https://img.shields.io/github/stars/treydock/gpfs_exporter?style=flat&label=%E2%AD%90) - The GPFS exporter collects metrics from the GPFS filesystem `Apache-2.0`.
- [Lustre Exporter](https://github.com/GSI-HPC/lustre_exporter) ![GitHub stars](https://img.shields.io/github/stars/GSI-HPC/lustre_exporter?style=flat&label=%E2%AD%90) - Prometheus exporter for use with the Lustre parallel filesystem `GPL-3.0`.
- [DCGM Exporter](https://github.com/NVIDIA/dcgm-exporter) ![GitHub stars](https://img.shields.io/github/stars/NVIDIA/dcgm-exporter?style=flat&label=%E2%AD%90) - NVIDIA GPU metrics exporter for Prometheus leveraging DCGM `Apache-2.0`.

## Journals
- [Journal of Super Computing](https://www.springer.com/journal/11227) - An International Journal of High-Performance Computer Design, Analysis, and Use.

## Podcasts
- [This week in HPC](https://www.intersect360.com/media/podcasts/) - Each week, Intersect360 Research CEO Addison Snell and HPCwire editor Tiffany Trader dissect the week's top HPC stories.
- [Exascale Project](https://www.exascaleproject.org/podcast/) - ECP's Let's Talk Exascale podcast; the Exascale Computing Project concluded in 2024 and the episodes remain as an archive.
- [@HPCpodcast](https://insidehpc.com/category/resources/hpc-podcast/) - Join Shahin Khan and Doug Black as they discuss Supercomputing technologies and the applications, markets, and policies that shape them.

## Blogs
- [HPCWire](https://www.hpcwire.com/) - Since 1987 covering the fastest computers in the world and the people who run them.
- [InsideHPC](https://insidehpc.com/) - insideHPC is a global publication recognized for its comprehensive and insightful coverage of the HPC-AI community, linking vendors, end-users and HPC strategists.
- [The Next Platform](https://www.nextplatform.com/category/hpc/) - Offers in-depth coverage of high-end computing at large enterprises, supercomputing centers, hyperscale data centers, and public clouds.
- [The Register HPC](https://www.theregister.com/hpc) - The Register is a leading and trusted global online enterprise technology news publication, reaching roughly 40 million readers worldwide.
- [HPC at Dell](http://hpcatdell.com) - High-Performance Computing knowledge base articles from Dell.

## Conferences

- [Pearc](https://pearc.acm.org/) - Practice & Experience in Advanced Research Computing.
- [Supercomputing (SC)](https://supercomputing.org/) - The International Conference for High Performance Computing, Networking, Storage, and Analysis.
- [Supercomputing International (ISC)](https://www.isc-hpc.com/) - The International Conference for High Performance Computing, Networking, Storage, and Analysis.
- [CCGrid](https://dl.acm.org/conference/ccgrid) - IEEE/ACM International Symposium on Cluster, Cloud and Internet Computing.
- [IEEE-HPEC](https://ieee-hpec.org/) - IEEE High Performance Embedded Computing.
- [Hot Chips](https://hotchips.org) - Semiconductor industry's leading conference on high-performance microprocessors and related circuits.
- [Hot Interconnects](https://hoti.org) - IEEE conference on software architectures and implementations for interconnection networks of all scales.
- [ESSA](https://sites.google.com/view/essa-2024/) - Workshop on Extreme-Scale Storage and Analysis (2024 edition site).
- [IEEE-IPDPS](https://www.ipdps.org/) - IEEE International Parallel & Distributed Processing Symposium.
- [ESPM2 Workshop](http://nowlab.cse.ohio-state.edu/espm2/) - International Workshop on Extreme Scale Programming Models and Middleware (page for the 2023 edition, held with SC23).
- [LCI Workshops](https://linuxclustersinstitute.org/workshops/) - The Linux Clusters Institute (LCI) is providing education and advanced technical training for the deployment and use of computing clusters to the high performance computing community worldwide.
- [HPC Carpentry](https://www.hpc-carpentry.org/) - Teaching basic skills for high-performance computing.

## Websites

- [Top500](https://top500.org) - The TOP500 project ranks and details the 500 most powerful non-distributed computer systems in the world.
- [LLNL HPC Tutorials](https://hpc-tutorials.llnl.gov/) ![GitHub stars](https://img.shields.io/github/stars/llnl/HPC-Tutorials?style=flat&label=%E2%AD%90) - Free tutorials on parallel computing, MPI, OpenMP, POSIX threads, and Slurm from Lawrence Livermore National Laboratory ([Source Code](https://github.com/llnl/HPC-Tutorials)).

## User Groups
- [MVAPICH](https://mug.mvapich.cse.ohio-state.edu/) - The MUG conference provides an open forum for all attendees (users, system administrators, researchers, engineers, and students) to discuss and share their knowledge on using MVAPICH libraries.
- [Slurm](https://slurm.schedmd.com/slurm_ug_agenda.html) - The annual Slurm user group meeting.

## Contributing

Contributing guidelines can be found in [contributing.md](contributing.md). Update both `README.md` and `README.ja.md` when you can.

## shvyac's awesome lists

All curated lists maintained by [shvyac](https://github.com/shvyac):

- [awesome-AI-Powered-Executive-Dashboards](https://github.com/shvyac/awesome-AI-Powered-Executive-Dashboards) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-AI-Powered-Executive-Dashboards?style=flat&label=%E2%AD%90)
- [awesome-ai-tool-for-mechanical-engineering](https://github.com/shvyac/awesome-ai-tool-for-mechanical-engineering) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ai-tool-for-mechanical-engineering?style=flat&label=%E2%AD%90)
- [awesome-audio-softwares](https://github.com/shvyac/awesome-audio-softwares) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-audio-softwares?style=flat&label=%E2%AD%90)
- [awesome-azure-ai-dynamics365-security](https://github.com/shvyac/awesome-azure-ai-dynamics365-security) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-azure-ai-dynamics365-security?style=flat&label=%E2%AD%90)
- [awesome-ballroom-dance](https://github.com/shvyac/awesome-ballroom-dance) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ballroom-dance?style=flat&label=%E2%AD%90)
- [awesome-cad-cae](https://github.com/shvyac/awesome-cad-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cad-cae?style=flat&label=%E2%AD%90)
- [awesome-cms-ai](https://github.com/shvyac/awesome-cms-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cms-ai?style=flat&label=%E2%AD%90)
- [awesome-dashboards-visualization](https://github.com/shvyac/awesome-dashboards-visualization) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-dashboards-visualization?style=flat&label=%E2%AD%90)
- [awesome-ghost-artists](https://github.com/shvyac/awesome-ghost-artists) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ghost-artists?style=flat&label=%E2%AD%90)
- [awesome-hamradio](https://github.com/shvyac/awesome-hamradio) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-hamradio?style=flat&label=%E2%AD%90)
- [awesome-hpc](https://github.com/shvyac/awesome-hpc) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-hpc?style=flat&label=%E2%AD%90)
- [awesome-iso27001-isms-tools](https://github.com/shvyac/awesome-iso27001-isms-tools) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-iso27001-isms-tools?style=flat&label=%E2%AD%90)
- [awesome-local-llm](https://github.com/shvyac/awesome-local-llm) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-local-llm?style=flat&label=%E2%AD%90)
- [awesome-m5stack-arduino](https://github.com/shvyac/awesome-m5stack-arduino) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-m5stack-arduino?style=flat&label=%E2%AD%90)
- [awesome-map-gis](https://github.com/shvyac/awesome-map-gis) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-map-gis?style=flat&label=%E2%AD%90)
- [awesome-meshless-cae](https://github.com/shvyac/awesome-meshless-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-meshless-cae?style=flat&label=%E2%AD%90)
- [awesome-online-services](https://github.com/shvyac/awesome-online-services) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-online-services?style=flat&label=%E2%AD%90)
- [awesome-open-source-solvers](https://github.com/shvyac/awesome-open-source-solvers) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-open-source-solvers?style=flat&label=%E2%AD%90)
- [awesome-osint-ai](https://github.com/shvyac/awesome-osint-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-osint-ai?style=flat&label=%E2%AD%90)
- [awesome-redmine-ai](https://github.com/shvyac/awesome-redmine-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-redmine-ai?style=flat&label=%E2%AD%90)
- [awesome-requirements-system-ai](https://github.com/shvyac/awesome-requirements-system-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-requirements-system-ai?style=flat&label=%E2%AD%90)
- [awesome-trading-stock](https://github.com/shvyac/awesome-trading-stock) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-trading-stock?style=flat&label=%E2%AD%90)
