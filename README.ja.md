<!--lint ignore-->
# Awesome HPC（日本語） [![Awesome](https://awesome.re/badge-flat.svg)](https://awesome.re)

[English README](README.md)

エンジニアと管理者のための、ハイパフォーマンスコンピューティング（HPC）のツールとリソース集です。⭐ バッジは GitHub のスター数をリアルタイム表示します(shields.io)。

[ハイパフォーマンスコンピューティング（HPC）](https://ja.wikipedia.org/wiki/スーパーコンピュータ)とは、一般的なデスクトップ PC やワークステーションをはるかに上回る性能が得られるように計算資源を束ね、科学・工学・ビジネスの大規模な問題を解くための取り組みを広く指します。

> [dstdev/awesome-hpc](https://github.com/dstdev/awesome-hpc) ![GitHub stars](https://img.shields.io/github/stars/dstdev/awesome-hpc?style=flat&label=%E2%AD%90) からフォークし、2026 年 10 月に更新しました。移転・改名・アーカイブされたプロジェクトを反映し、新しいスケジューラ、ワークフローエンジン、性能可搬性レイヤー、ストレージを追加しています。

## 目次
<details>
  <summary><b>（クリックで展開）</b></summary>

- [プロビジョニング](#プロビジョニング)
- [ワークロードマネージャ](#ワークロードマネージャ)
- [パイプライン](#パイプライン)
- [アプリケーション管理](#アプリケーション管理)
- [コンパイラ](#コンパイラ)
- [MPI](#mpi)
- [並列計算](#並列計算)
- [ベンチマーク](#ベンチマーク)
- [その他](#その他)
- [性能解析・デバッグ](#性能解析デバッグ)
- [並列シェル](#並列シェル)
- [コンテナ](#コンテナ)
- [環境管理](#環境管理)
- [可視化](#可視化)
- [並列ファイルシステム](#並列ファイルシステム)
- [プログラミング言語](#プログラミング言語)
- [監視](#監視)
- [学術誌](#学術誌)
- [ポッドキャスト](#ポッドキャスト)
- [ブログ・ニュース](#ブログニュース)
- [カンファレンス](#カンファレンス)
- [Web サイト](#web-サイト)
- [ユーザーグループ](#ユーザーグループ)
- [コントリビューション](#コントリビューション)
- [shvyac の awesome リスト](#shvyac-の-awesome-リスト)

</details>

## プロビジョニング
- [Grendel](https://grendel.readthedocs.io/) ![GitHub stars](https://img.shields.io/github/stars/ubccr/grendel?style=flat&label=%E2%AD%90) - HPC Linux クラスタ向けのベアメタル・プロビジョニングシステム（[ソースコード](https://github.com/ubccr/grendel)） `GPL-3`。
- [xCAT](https://xcat.org/) ![GitHub stars](https://img.shields.io/github/stars/xcat2/xcat-core?style=flat&label=%E2%AD%90) - あらゆる規模のクラスタの展開・管理ツールキット。2023 年に発表された開発終了は撤回され、xCAT Consortium のもとで開発が続いている（[ソースコード](https://github.com/xcat2/xcat-core)） `EPL-1.0`。
- [Confluent](https://xcat2.github.io/confluent-docs/) ![GitHub stars](https://img.shields.io/github/stars/xcat2/confluent?style=flat&label=%E2%AD%90) - スケールアウト型サーバー構成の初期構築・展開・運用ツール。xCAT プロジェクトが長期的な後継として推奨（[ソースコード](https://github.com/xcat2/confluent)） `Apache-2.0`。
- [Warewulf](https://warewulf.org/) ![GitHub stars](https://img.shields.io/github/stars/warewulf/warewulf?style=flat&label=%E2%AD%90) - ベアメタル／仮想マシンからなる大規模クラスタ向けの、ステートレス・ディスクレスなコンテナ OS プロビジョニングシステム（[ソースコード](https://github.com/warewulf/warewulf)） `BSD-3`。
- [Rocks](http://www.rocksclusters.org/) - Linux クラスタ構築用の Linux ディストリビューション。現在は開発停止（最終リリースは 2017 年の 7.0） `other`。
- [Cobbler](https://cobbler.github.io/) ![GitHub stars](https://img.shields.io/github/stars/cobbler/cobbler?style=flat&label=%E2%AD%90) - ネットワークインストール環境をすばやく構築できる Linux インストールサーバー（[ソースコード](https://github.com/cobbler/cobbler)） `GPL-2.0`。
- [Base Command Manager](https://docs.nvidia.com/base-command-manager/index.html) - NVIDIA Base Command Manager（旧 Bright Cluster Manager）。異種混在クラスタを迅速に構築・管理できる `Proprietary`。
- [Scyld](https://www.penguinsolutions.com/computing/products/software/scyld-clusterware/) - 1990 年代に NASA で生まれた Beowulf クラスタの流れをくむ Scyld ClusterWare `Proprietary`。
- [BlueBanquise](https://bluebanquise.com) ![GitHub stars](https://img.shields.io/github/stars/bluebanquise/bluebanquise?style=flat&label=%E2%AD%90) - Python と Ansible で構築されたオープンソースのクラスタ展開・管理スタック（[ソースコード](https://github.com/bluebanquise/bluebanquise)） `MIT`。

## ワークロードマネージャ
- [Slurm](https://slurm.schedmd.com/documentation.html) ![GitHub stars](https://img.shields.io/github/stars/SchedMD/slurm?style=flat&label=%E2%AD%90) - 無料・オープンソースで高いスケーラビリティを持つワークロードマネージャ／ジョブスケジューラ。開発元 SchedMD は 2025 年 12 月に NVIDIA が買収（[ソースコード](https://github.com/SchedMD/slurm)） `GPL-2.0`。
- [OpenPBS](https://www.openpbs.org/) ![GitHub stars](https://img.shields.io/github/stars/openpbs/openpbs?style=flat&label=%E2%AD%90) - HPC 環境のジョブスケジューリングとワークロード管理を最適化するソフトウェア（[ソースコード](https://github.com/openpbs/openpbs)） `AGPL-3.0`。
- [Flux](https://flux-framework.org/) ![GitHub stars](https://img.shields.io/github/stars/flux-framework/flux-core?style=flat&label=%E2%AD%90) - LLNL が開発する次世代の階層型リソースマネージャ／スケジューラ。単体でも他のスケジューラの中に入れ子でも使える（[ソースコード](https://github.com/flux-framework/flux-core)） `LGPL-3.0`。
- [HTCondor](https://htcondor.org/) ![GitHub stars](https://img.shields.io/github/stars/htcondor/htcondor?style=flat&label=%E2%AD%90) - 大量の独立ジョブを扱うハイスループット・コンピューティング向けワークロードマネージャ（[ソースコード](https://github.com/htcondor/htcondor)） `Apache-2.0`。
- [LSF](https://www.ibm.com/products/hpc-workload-management) - IBM のジョブスケジューラ／ワークロード管理ソフトウェア `Proprietary`。
- [Grid Engine](https://www.siemens.com/en-us/products/hpcworks/grid-engine/) - HPCWorks Grid Engine（旧 Univa／Altair Grid Engine）。Altair の買収により現在は Siemens の製品 `Proprietary`。
- [Moab](https://adaptivecomputing.com/moab-hpc-suite/) - ワークロード管理・ジョブスケジューラ `other`。
- [Torque](https://en.wikipedia.org/wiki/TORQUE) - ワークロード管理・ジョブスケジューラ `other`。
- [Volcano](https://volcano.sh/) ![GitHub stars](https://img.shields.io/github/stars/volcano-sh/volcano?style=flat&label=%E2%AD%90) - AI／ML、ビッグデータ、HPC 向けの Kubernetes 上のバッチシステム（CNCF プロジェクト）（[ソースコード](https://github.com/volcano-sh/volcano)） `Apache-2.0`。
- [Kueue](https://kueue.sigs.k8s.io/) ![GitHub stars](https://img.shields.io/github/stars/kubernetes-sigs/kueue?style=flat&label=%E2%AD%90) - Kubernetes ネイティブのジョブキューイングとクォータ管理（SIG Scheduling）（[ソースコード](https://github.com/kubernetes-sigs/kueue)） `Apache-2.0`。
- [Kube Batch](https://github.com/kubernetes-retired/kube-batch) ![GitHub stars](https://img.shields.io/github/stars/kubernetes-retired/kube-batch?style=flat&label=%E2%AD%90) - 高性能ワークロード向けの Kubernetes バッチスケジューラ。アーカイブ済み（後継は Volcano や Kueue） `Apache-2.0`。
- [OpenLava](https://en.wikipedia.org/wiki/OpenLava) - かつてのワークロード管理・ジョブスケジューラ。開発終了 `other`。
- [Maui](https://en.wikipedia.org/wiki/Maui_Cluster_Scheduler) - 旧来のオープンソース・ジョブスケジューラ（Moab の前身）。メンテナンス終了 `other`。

## パイプライン
- [Nextflow](https://nextflow.io) ![GitHub stars](https://img.shields.io/github/stars/nextflow-io/nextflow?style=flat&label=%E2%AD%90) - データ駆動型の計算パイプライン（[ソースコード](https://github.com/nextflow-io/nextflow)） `Apache-2.0`。
- [Snakemake](https://snakemake.github.io/) ![GitHub stars](https://img.shields.io/github/stars/snakemake/snakemake?style=flat&label=%E2%AD%90) - Python ベースのワークフロー管理システム。Slurm などのクラスタ実行に対応（[ソースコード](https://github.com/snakemake/snakemake)） `MIT`。
- [Parsl](https://parsl-project.org/) ![GitHub stars](https://img.shields.io/github/stars/Parsl/parsl?style=flat&label=%E2%AD%90) - ノート PC からクラスタ、スーパーコンピュータまでタスクを並列実行できる Python ライブラリ（[ソースコード](https://github.com/Parsl/parsl)） `Apache-2.0`。
- [Cromwell](https://cromwell.readthedocs.io/en/stable/) ![GitHub stars](https://img.shields.io/github/stars/broadinstitute/cromwell?style=flat&label=%E2%AD%90) - シンプルさとスケーラビリティを重視した科学ワークフローエンジン（[ソースコード](https://github.com/broadinstitute/cromwell)） `BSD-3`。
- [Pegasus](https://pegasus.isi.edu/) ![GitHub stars](https://img.shields.io/github/stars/pegasus-isi/pegasus?style=flat&label=%E2%AD%90) - 多様な計算基盤へ科学ワークフローを割り当てて実行する、設定可能なシステム（[ソースコード](https://github.com/pegasus-isi/pegasus)） `Apache-2.0`。

## アプリケーション管理
- [Spack](https://spack.io) ![GitHub stars](https://img.shields.io/github/stars/spack/spack?style=flat&label=%E2%AD%90) - 複数のバージョン・構成・プラットフォーム・コンパイラに対応する柔軟なパッケージマネージャ（[ソースコード](https://github.com/spack/spack)） `other`。
- [EasyBuild](https://easybuild.io/) ![GitHub stars](https://img.shields.io/github/stars/easybuilders/easybuild?style=flat&label=%E2%AD%90) - 科学技術ソフトウェアを簡単にビルドするためのフレームワーク（[ソースコード](https://github.com/easybuilders/easybuild)） `GPL-2`。

## コンパイラ
- [Nvidia](https://developer.nvidia.com/hpc-compilers) - NVIDIA HPC SDK の Fortran、C/C++ コンパイラ。OpenACC、OpenMP、CUDA に対応 `Proprietary`。
- [Portland Group](https://developer.nvidia.com/hpc-sdk) - 旧 PGI の Fortran、C/C++ コンパイラ。現在は NVIDIA HPC SDK に統合 `Proprietary`。
- [Intel](https://www.intel.com/content/www/us/en/developer/tools/oneapi/hpc-toolkit.html) - Intel oneAPI HPC Toolkit。LLVM ベースの Intel C/C++（icx）と Fortran（ifx）コンパイラを含む `Proprietary`。
- [Cray](https://cpe.ext.hpe.com/docs/) - HPE Cray Programming Environment に含まれる HPE Cray Compiling Environment（CCE） `Proprietary`。
- [GNU](https://gcc.gnu.org/) - 多数の言語に対応する GNU コンパイラコレクション（[ソースコード](https://gcc.gnu.org/git.html)） `GPL-3`。
- [LLVM](https://llvm.org/) ![GitHub stars](https://img.shields.io/github/stars/llvm/llvm-project?style=flat&label=%E2%AD%90) - モジュール化されたコンパイラとツールチェーン群。Fortran コンパイラ Flang も含む（[ソースコード](https://github.com/llvm/llvm-project)） `Apache-2.0`。

## MPI
- [OpenMPI](https://www.open-mpi.org/) ![GitHub stars](https://img.shields.io/github/stars/open-mpi/ompi?style=flat&label=%E2%AD%90) - オープンソースの MPI 実装（v5.x は MPI-3.1 に完全準拠し、MPI-4.0 の機能も多数サポート）（[ソースコード](https://github.com/open-mpi/ompi)） `BSD`。
- [MPICH](https://www.mpich.org/) ![GitHub stars](https://img.shields.io/github/stars/pmodels/mpich?style=flat&label=%E2%AD%90) - 高性能で移植性の高い MPI 標準の実装（[ソースコード](https://github.com/pmodels/mpich)） `other`。
- [MVAPICH](https://mvapich.cse.ohio-state.edu/) - InfiniBand、RoCE などの高速ネットワーク向けにオハイオ州立大学が開発するオープンソース MPI 実装 `BSD`。
- [Intel-MPI](https://www.intel.com/content/www/us/en/developer/tools/oneapi/mpi-library.html) - Intel MPI Library。MPICH ベースの Intel 製 MPI 実装 `other`。

## 並列計算
- [ArrayFire](https://arrayfire.org/docs/index.htm) ![GitHub stars](https://img.shields.io/github/stars/arrayfire/arrayfire?style=flat&label=%E2%AD%90) - 並列アーキテクチャ向けソフトウェア開発を簡単にする汎用テンソルライブラリ（[ソースコード](https://github.com/arrayfire/arrayfire)） `BSD-3`。
- [OpenMP](https://www.openmp.org/) - マルチプラットフォームの共有メモリ並列プログラミングのための API `other`。
- [Kokkos](https://kokkos.org/) ![GitHub stars](https://img.shields.io/github/stars/kokkos/kokkos?style=flat&label=%E2%AD%90) - CPU と GPU にまたがる C++ の性能可搬性プログラミング・エコシステム（[ソースコード](https://github.com/kokkos/kokkos)） `Apache-2.0 WITH LLVM-exception`。
- [RAJA](https://raja.readthedocs.io/) ![GitHub stars](https://img.shields.io/github/stars/llnl/RAJA?style=flat&label=%E2%AD%90) - ループレベルの並列化のための LLNL の C++ 性能可搬性レイヤー（[ソースコード](https://github.com/llnl/RAJA)） `BSD-3`。

## ベンチマーク
- [OSU Benchmarks](https://mvapich.cse.ohio-state.edu/benchmarks/) - オハイオ州立大学が開発した MPI ベンチマーク集 `other`。
- [Intel MPI Benchmarks](https://github.com/intel/mpi-benchmarks) ![GitHub stars](https://img.shields.io/github/stars/intel/mpi-benchmarks?style=flat&label=%E2%AD%90) - Intel が開発した MPI 性能ベンチマーク集 `other`。
- [HPCC Systems](https://hpccsystems.com/) ![GitHub stars](https://img.shields.io/github/stars/hpcc-systems/HPCC-Platform?style=flat&label=%E2%AD%90) - ビッグデータ処理・分析のためのオープンソースの超並列計算プラットフォーム（[ソースコード](https://github.com/hpcc-systems/HPCC-Platform)） `other`。
- [LINPACK](https://www.netlib.org/linpack/) - 線形方程式を解く Fortran サブルーチン群。そのベンチマークは HPC の性能指標として使われる `other`。
- [IOzone](https://www.iozone.org/) - ファイルシステムのベンチマークツール `OSS`。
- [IOR](https://ior.readthedocs.io/) ![GitHub stars](https://img.shields.io/github/stars/hpc/ior?style=flat&label=%E2%AD%90) - 並列ファイルシステムの性能評価に便利なベンチマーク（Interleaved or Random）（[ソースコード](https://github.com/hpc/ior)） `GPL-2`。
- [MDtest](https://ior.readthedocs.io/) ![GitHub stars](https://img.shields.io/github/stars/hpc/ior?style=flat&label=%E2%AD%90) - ファイルシステムのメタデータ性能を評価する MPI ベースのツール。IOR に同梱（[ソースコード](https://github.com/hpc/ior)） `GPL-2`。
- [FIO](https://fio.readthedocs.io/en/latest/fio_doc.html) ![GitHub stars](https://img.shields.io/github/stars/axboe/fio?style=flat&label=%E2%AD%90) - カーネルの AIO を利用する高機能なディスクベンチマーク（Flexible I/O）（[ソースコード](https://github.com/axboe/fio)） `GPL-2`。
- [elbencho](https://github.com/breuner/elbencho) ![GitHub stars](https://img.shields.io/github/stars/breuner/elbencho?style=flat&label=%E2%AD%90) - ファイル・オブジェクト・ブロック向けの分散ストレージベンチマーク。GPU にも対応 `GPL-3`。

## その他
- [OpenOnDemand](https://openondemand.org/) ![GitHub stars](https://img.shields.io/github/stars/OSC/ondemand?style=flat&label=%E2%AD%90) - どの端末からでもリモートの計算資源を簡単に使えるようにする Web ポータル（[ソースコード](https://github.com/OSC/ondemand)） `MIT`。
- [Open XDMod](https://open.xdmod.org) ![GitHub stars](https://img.shields.io/github/stars/ubccr/xdmod?style=flat&label=%E2%AD%90) - HPC 資源の管理を支援するオープンソースのメトリクス収集・分析ツール（[ソースコード](https://github.com/ubccr/xdmod/)） `LGPL-3`。
- [Coldfront](https://coldfront.readthedocs.io/en/latest/) ![GitHub stars](https://img.shields.io/github/stars/coldfront/coldfront?style=flat&label=%E2%AD%90) - HPC 資源の割り当て・報告・研究成果の把握を一元化するオープンソースのリソース割り当てシステム（[ソースコード](https://github.com/coldfront/coldfront)） `GPL-3`。
- [Pavilion2](https://pavilion2.readthedocs.io/) ![GitHub stars](https://img.shields.io/github/stars/hpc/pavilion2?style=flat&label=%E2%AD%90) - HPC システム向けのテストを実行・分析する Python 3 製フレームワーク（[ソースコード](https://github.com/hpc/pavilion2)） `other`。
- [Reframe](https://reframe-hpc.readthedocs.io/en/stable/) ![GitHub stars](https://img.shields.io/github/stars/reframe-hpc/reframe?style=flat&label=%E2%AD%90) - HPC システム向けの可搬な回帰テストとベンチマークを記述・実行する Python フレームワーク（[ソースコード](https://github.com/reframe-hpc/reframe)） `BSD-3`。
- [OLCF Test Harness](https://olcf.github.io/olcf-test-harness/) ![GitHub stars](https://img.shields.io/github/stars/olcf/olcf-test-harness?style=flat&label=%E2%AD%90) - アプリケーション、ツール、システムソフトウェアのテストを自動化（[ソースコード](https://github.com/olcf/olcf-test-harness)） `other`。
- [GoSlmailer](https://github.com/CLIP-HPC/goslmailer) ![GitHub stars](https://img.shields.io/github/stars/CLIP-HPC/goslmailer?style=flat&label=%E2%AD%90) - Slurm のジョブ通知を Slack、Mattermost、Teams などに届けるドロップイン置き換えツール。

## 性能解析・デバッグ
- [TotalView](https://totalview.io/products/totalview) - HPC アプリケーション向けデバッガ `Proprietary`。
- [Tau](https://www.cs.uoregon.edu/research/tau/home.php) - Fortran、C、C++、UPC、Java、Python の並列プログラムを解析する可搬なプロファイリング・トレースツール `other`。
- [Valgrind](https://www.valgrind.org/) - メモリリークなどを調べるプロファイリングツール（[ソースコード](https://sourceware.org/git/?p=valgrind.git)） `GPL-2`。
- [Paraver](https://tools.bsc.es/paraver) - CEPBA-Tools に含まれる柔軟なトレースデータブラウザ `other`。
- [PAPI](https://icl.utk.edu/papi/) - ハードウェア性能カウンタを扱う性能解析用 API（Performance Application Programming Interface） `other`。

## 並列シェル
- [pdsh](https://linux.die.net/man/1/pdsh) ![GitHub stars](https://img.shields.io/github/stars/chaos/pdsh?style=flat&label=%E2%AD%90) - 複数ホストでコマンドを並列実行する（[ソースコード](https://github.com/chaos/pdsh)） `GPL-2`。
- [ClusterShell](https://clustershell.readthedocs.io/en/latest/intro.html) ![GitHub stars](https://img.shields.io/github/stars/clustershell/clustershell?style=flat&label=%E2%AD%90) - スケーラブルなクラスタ管理用 Python フレームワーク（[ソースコード](https://github.com/clustershell/clustershell)） `LGPL-2.1`。

## コンテナ
- [Apptainer](https://apptainer.org) ![GitHub stars](https://img.shields.io/github/stars/apptainer/apptainer?style=flat&label=%E2%AD%90) - オープンソースのコンテナシステム（旧 Singularity）（[ソースコード](https://github.com/apptainer/apptainer)） `BSD`。
- [SingularityCE](https://sylabs.io/docs/) ![GitHub stars](https://img.shields.io/github/stars/sylabs/singularity?style=flat&label=%E2%AD%90) - Sylabs が開発する Singularity のコミュニティ版（[ソースコード](https://github.com/sylabs/singularity)） `other`。
- [Charliecloud](https://charliecloud.io/) - HPC センター向けにユーザー定義ソフトウェアスタック（UDSS）を提供。開発は GitLab に移行（[ソースコード](https://gitlab.com/charliecloud/charliecloud)） `Apache-2.0`。
- [Docker](https://www.docker.com/) - OS レベルの仮想化でソフトウェアをコンテナとして配布するプラットフォーム `other`。
- [uDocker](https://indigo-dc.github.io/udocker/) ![GitHub stars](https://img.shields.io/github/stars/indigo-dc/udocker?style=flat&label=%E2%AD%90) - バッチ／対話型システムで root 権限なしに Docker コンテナを実行するユーザーツール（[ソースコード](https://github.com/indigo-dc/udocker)） `Apache-2.0`。
- [Shifter](https://www.nersc.gov/research-and-development/user-defined-images/) ![GitHub stars](https://img.shields.io/github/stars/NERSC/shifter?style=flat&label=%E2%AD%90) - HPC 向け Linux コンテナ（[ソースコード](https://github.com/NERSC/shifter)） `other`。
- [HPC Container Maker](https://github.com/NVIDIA/hpc-container-maker) ![GitHub stars](https://img.shields.io/github/stars/NVIDIA/hpc-container-maker?style=flat&label=%E2%AD%90) - コンテナ定義ファイルの生成を簡単にするオープンソースツール `Apache-2.0`。
- [Sarus](https://github.com/eth-cscs/sarus) ![GitHub stars](https://img.shields.io/github/stars/eth-cscs/sarus?style=flat&label=%E2%AD%90) - HPC 向けの OCI 互換コンテナエンジン `BSD`。
- [Singularity HPC](https://singularity-hpc.readthedocs.io) ![GitHub stars](https://img.shields.io/github/stars/singularityhub/singularity-hpc?style=flat&label=%E2%AD%90) - コンテナをモジュールとしてインストールできるレジストリ（shpc）（[ソースコード](https://github.com/singularityhub/singularity-hpc)） `MPL 2.0`。

## 環境管理
- [Lmod](https://lmod.readthedocs.io/en/latest/) ![GitHub stars](https://img.shields.io/github/stars/TACC/Lmod?style=flat&label=%E2%AD%90) - Lua ベースの Environment Module システム。TCL モジュールの読み込みとソフトウェア階層に対応（[ソースコード](https://github.com/TACC/Lmod)） `other`。
- [Environment Modules](https://modules.readthedocs.io/en/latest/) ![GitHub stars](https://img.shields.io/github/stars/envmodules/modules?style=flat&label=%E2%AD%90) - ユーザー環境を動的に切り替える（[ソースコード](https://github.com/envmodules/modules)） `GPL-2`。
- [Anaconda](https://www.anaconda.com/) - 科学技術計算向けの Python／R ディストリビューション `other`。
- [Miniforge](https://conda-forge.org/download/) ![GitHub stars](https://img.shields.io/github/stars/conda-forge/miniforge?style=flat&label=%E2%AD%90) - コミュニティの conda-forge チャネルを既定とする最小構成の conda／mamba インストーラ（[ソースコード](https://github.com/conda-forge/miniforge)） `other`。
- [Mamba](https://mamba.readthedocs.io/en/latest/) ![GitHub stars](https://img.shields.io/github/stars/mamba-org/mamba?style=flat&label=%E2%AD%90) - conda パッケージマネージャの C++ による再実装（[ソースコード](https://github.com/mamba-org/mamba)） `BSD`。
- [Pixi](https://pixi.sh/) ![GitHub stars](https://img.shields.io/github/stars/prefix-dev/pixi?style=flat&label=%E2%AD%90) - conda エコシステム上に構築された、高速で再現性の高いプロジェクト・環境マネージャ（Rust 製）（[ソースコード](https://github.com/prefix-dev/pixi)） `BSD-3`。

## 可視化
- [Visit](https://visit-dav.github.io/visit-website/) ![GitHub stars](https://img.shields.io/github/stars/visit-dav/visit?style=flat&label=%E2%AD%90) - メッシュベースの科学データの可視化・解析ツール（[ソースコード](https://github.com/visit-dav/visit)） `BSD-3`。
- [Paraview](https://www.paraview.org/) ![GitHub stars](https://img.shields.io/github/stars/Kitware/ParaView?style=flat&label=%E2%AD%90) - VTK を基盤とするオープンソース・マルチプラットフォームのデータ解析・可視化アプリケーション（[ソースコード](https://github.com/Kitware/ParaView)） `BSD-3`。

## 並列ファイルシステム
- [IBM Storage Scale (GPFS)](https://www.ibm.com/products/storage-scale) - IBM の高性能クラスタファイルシステム（旧 GPFS／Spectrum Scale） `Proprietary`。
- [Quobyte](https://www.quobyte.com/) - 高性能ファイルシステム `Proprietary`。
- [Ceph](https://ceph.io/en/) ![GitHub stars](https://img.shields.io/github/stars/ceph/ceph?style=flat&label=%E2%AD%90) - 分散オブジェクト・ブロック・ファイルストレージ基盤（[ソースコード](https://github.com/ceph/ceph)） `other`。
- [Weka](https://www.weka.io/) - HPC 向けに設計されたファイルシステム `Proprietary`。
- [Lustre/Exascaler](https://www.lustre.org/) - スケーラビリティ、高性能、高可用性を重視したオープンソースの分散並列ファイルシステム（[ソースコード](https://git.whamcloud.com/fs/lustre-release.git)） `other`。
- [BeeGFS](https://www.beegfs.io/) ![GitHub stars](https://img.shields.io/github/stars/ThinkParQ/beegfs?style=flat&label=%E2%AD%90) - 性能と導入・管理のしやすさを重視した、ハードウェア非依存の POSIX 並列ファイルシステム（[ソースコード](https://github.com/ThinkParQ/beegfs)） `other`。
- [DAOS](https://daos.io/) ![GitHub stars](https://img.shields.io/github/stars/daos-stack/daos?style=flat&label=%E2%AD%90) - HPC と AI 向けの NVMe ネイティブなオープンソース・ストレージスタック（Distributed Asynchronous Object Storage）（[ソースコード](https://github.com/daos-stack/daos)） `BSD-2-Clause-Patent`。
- [OrangeFS](http://www.orangefs.org/) ![GitHub stars](https://img.shields.io/github/stars/waltligon/orangefs?style=flat&label=%E2%AD%90) - Linux クラスタ向けの次世代並列ファイルシステム（[ソースコード](https://github.com/waltligon/orangefs)） `other`。
- [MooseFS](https://moosefs.com/) ![GitHub stars](https://img.shields.io/github/stars/moosefs/moosefs?style=flat&label=%E2%AD%90) - Core Technology が開発するオープンソースの POSIX 準拠分散ファイルシステム（[ソースコード](https://github.com/moosefs/moosefs)） `GPL-2.0`。

## プログラミング言語
- [Julia](https://julialang.org/) ![GitHub stars](https://img.shields.io/github/stars/JuliaLang/julia?style=flat&label=%E2%AD%90) - 技術計算向けの高水準・高性能な動的言語（[ソースコード](https://github.com/JuliaLang/julia)） `MIT`。
- [Futhark](https://futhark-lang.org/) ![GitHub stars](https://img.shields.io/github/stars/diku-dk/futhark?style=flat&label=%E2%AD%90) - ML 系の純粋関数型データ並列プログラミング言語（[ソースコード](https://github.com/diku-dk/futhark)） `isc`。
- [Chapel](https://chapel-lang.org/) ![GitHub stars](https://img.shields.io/github/stars/chapel-lang/chapel?style=flat&label=%E2%AD%90) - 大規模並列計算を生産的に書くためのプログラミング言語（[ソースコード](https://github.com/chapel-lang/chapel)） `Apache-2.0`。

## 監視
### Prometheus ベース
- [Slurm Exporter](https://github.com/vpenso/prometheus-slurm-exporter) ![GitHub stars](https://img.shields.io/github/stars/vpenso/prometheus-slurm-exporter?style=flat&label=%E2%AD%90) - Slurm の性能メトリクスを出力する Prometheus エクスポーター `GPL-3.0`。
- [Slurm Exporter (Rivos)](https://github.com/rivosinc/prometheus-slurm-exporter) ![GitHub stars](https://img.shields.io/github/stars/rivosinc/prometheus-slurm-exporter?style=flat&label=%E2%AD%90) - スケジューラの主要メトリクスを Prometheus に出力する、活発にメンテナンスされている Slurm エクスポーター `Apache-2.0`。
- [Slurm Exporter](https://github.com/ubccr/slurm-exporter) ![GitHub stars](https://img.shields.io/github/stars/ubccr/slurm-exporter?style=flat&label=%E2%AD%90) - REST API を使う Prometheus 向け Slurm エクスポーター `GPL-3.0`。
- [Infiniband Exporter](https://github.com/treydock/infiniband_exporter) ![GitHub stars](https://img.shields.io/github/stars/treydock/infiniband_exporter?style=flat&label=%E2%AD%90) - InfiniBand スイッチと HCA のカウンタを収集 `Apache-2.0`。
- [Cgroup Exporter](https://github.com/treydock/cgroup_exporter) ![GitHub stars](https://img.shields.io/github/stars/treydock/cgroup_exporter?style=flat&label=%E2%AD%90) - cgroup のメトリクスを出力 `Apache-2.0`。
- [Cgroup Exporter](https://github.com/phpHavok/cgroups_exporter) ![GitHub stars](https://img.shields.io/github/stars/phpHavok/cgroups_exporter?style=flat&label=%E2%AD%90) - cgroup 単位のメトリクスを出力する Prometheus エクスポーター `unknown`。
- [GPFS Exporter](https://github.com/treydock/gpfs_exporter) ![GitHub stars](https://img.shields.io/github/stars/treydock/gpfs_exporter?style=flat&label=%E2%AD%90) - GPFS ファイルシステムのメトリクスを収集 `Apache-2.0`。
- [Lustre Exporter](https://github.com/GSI-HPC/lustre_exporter) ![GitHub stars](https://img.shields.io/github/stars/GSI-HPC/lustre_exporter?style=flat&label=%E2%AD%90) - Lustre 並列ファイルシステム用の Prometheus エクスポーター `GPL-3.0`。
- [DCGM Exporter](https://github.com/NVIDIA/dcgm-exporter) ![GitHub stars](https://img.shields.io/github/stars/NVIDIA/dcgm-exporter?style=flat&label=%E2%AD%90) - DCGM を利用する NVIDIA GPU メトリクスの Prometheus エクスポーター `Apache-2.0`。

## 学術誌
- [Journal of Super Computing](https://www.springer.com/journal/11227) - 高性能計算機の設計・解析・利用に関する国際学術誌。

## ポッドキャスト
- [This week in HPC](https://www.intersect360.com/media/podcasts/) - Intersect360 Research の Addison Snell と HPCwire の Tiffany Trader が毎週の HPC ニュースを解説。
- [Exascale Project](https://www.exascaleproject.org/podcast/) - ECP のポッドキャスト「Let's Talk Exascale」。Exascale Computing Project は 2024 年に終了し、エピソードはアーカイブとして公開中。
- [@HPCpodcast](https://insidehpc.com/category/resources/hpc-podcast/) - Shahin Khan と Doug Black がスーパーコンピューティング技術とその応用・市場・政策を語る。

## ブログ・ニュース
- [HPCWire](https://www.hpcwire.com/) - 1987 年から世界最速のコンピュータとそれを運用する人々を伝えるニュースサイト。
- [InsideHPC](https://insidehpc.com/) - HPC と AI のコミュニティを網羅的に報じる国際的なメディア。
- [The Next Platform](https://www.nextplatform.com/category/hpc/) - 大企業、スパコンセンター、ハイパースケールデータセンター、パブリッククラウドのハイエンド計算を深掘り。
- [The Register HPC](https://www.theregister.com/hpc) - 大手のエンタープライズ IT ニュースサイト The Register の HPC カテゴリ。
- [HPC at Dell](http://hpcatdell.com) - Dell による HPC のナレッジベース記事。

## カンファレンス

- [Pearc](https://pearc.acm.org/) - Practice & Experience in Advanced Research Computing。
- [Supercomputing (SC)](https://supercomputing.org/) - HPC、ネットワーク、ストレージ、解析の国際会議（米国）。
- [Supercomputing International (ISC)](https://www.isc-hpc.com/) - HPC の国際会議（欧州）。
- [CCGrid](https://dl.acm.org/conference/ccgrid) - クラスタ・クラウド・インターネットコンピューティングに関する IEEE／ACM 国際シンポジウム。
- [IEEE-HPEC](https://ieee-hpec.org/) - IEEE High Performance Embedded Computing。
- [Hot Chips](https://hotchips.org) - 高性能マイクロプロセッサと関連回路に関する半導体業界の主要会議。
- [Hot Interconnects](https://hoti.org) - あらゆる規模の相互接続ネットワークのソフトウェア設計と実装に関する IEEE 会議。
- [ESSA](https://sites.google.com/view/essa-2024/) - 超大規模ストレージと解析のワークショップ（2024 年版サイト）。
- [IEEE-IPDPS](https://www.ipdps.org/) - IEEE 国際並列分散処理シンポジウム。
- [ESPM2 Workshop](http://nowlab.cse.ohio-state.edu/espm2/) - 超大規模プログラミングモデルとミドルウェアの国際ワークショップ。
- [LCI Workshops](https://linuxclustersinstitute.org/workshops/) - Linux Clusters Institute による、計算クラスタの導入と利用のための教育・技術トレーニング。
- [HPC Carpentry](https://www.hpc-carpentry.org/) - HPC の基本スキルを教える講座。

## Web サイト

- [Top500](https://top500.org) - 世界で最も強力な計算機システム 500 台をランキングし詳細を紹介。
- [LLNL HPC Tutorials](https://hpc-tutorials.llnl.gov/) ![GitHub stars](https://img.shields.io/github/stars/llnl/HPC-Tutorials?style=flat&label=%E2%AD%90) - ローレンス・リバモア国立研究所による、並列計算、MPI、OpenMP、POSIX スレッド、Slurm の無料チュートリアル（[ソースコード](https://github.com/llnl/HPC-Tutorials)）。

## ユーザーグループ
- [MVAPICH](https://mug.mvapich.cse.ohio-state.edu/) - 利用者、管理者、研究者、エンジニア、学生が MVAPICH の知見を共有する MUG カンファレンス。
- [Slurm](https://slurm.schedmd.com/slurm_ug_agenda.html) - 年次の Slurm ユーザーグループ会議。

## コントリビューション

コントリビューションのガイドラインは [contributing.md](contributing.md) を参照してください。可能なら `README.md` と `README.ja.md` の両方を更新してください。

## shvyac の awesome リスト

[shvyac](https://github.com/shvyac) が管理しているキュレーションリストの一覧:

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
