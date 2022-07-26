Papers & slides of graph pattern mining systems.

# Peregrine: A Pattern-Aware Graph Mining System

EuroSys'20

**Abstract**
Graph mining workloads aim to extract structural properties  of a graph by exploring its subgraph structures. General  purpose graph mining systems provide a generic runtime to  explore subgraph structures of interest with the help of userdefined  functions that guide the overall exploration process.  However, the state-of-the-art graph mining systems remain  largely oblivious to the shape (or pattern) of the subgraphs that  they mine. This causes them to: (a) explore unnecessary subgraphs;  (b) perform expensive computations on the explored  subgraphs; and, (c) hold intermediate partial subgraphs in  memory; all of which affect their overall performance. Furthermore,  their programming models are often tied to their  underlying exploration strategies, which makes it difficult for  domain users to express complex mining tasks.  

In this paper, we develop PEREGRINE, a pattern-aware  graph mining system that directly explores the subgraphs  of interest while avoiding exploration of unnecessary subgraphs,  and simultaneously bypassing expensive computations  throughout the mining process. We design a patternbased  programming model that treats graph patterns as first  class constructs and enables PEREGRINE to extract the semantics  of patterns, which it uses to guide its exploration.  Our evaluation shows that PEREGRINE outperforms state-ofthe-  art distributed and single machine graph mining systems,  and scales to complex mining tasks on larger graphs, while  retaining simplicity and expressivity with its ‘pattern-first’  programming approach.


- [x] Eurosys'20: [Eurosys2020 (accepted paper, video(short, long) and slides)](https://www.eurosys2020.org/program/)
- [ ] paper: [Peregrine: A Pattern-Aware Graph Mining System](https://dl.acm.org/doi/abs/10.1145/3342195.3387548)
- [ ] slides: [PowerPoint Presentation (eurosys2020.org)](https://www.eurosys2020.org/wp-content/uploads/2020/04/slides/431_jamshidi_slides.pdf)
- [ ] video: ([short](https://www.youtube.com/watch?v=MChTp0rDl_I),[long](https://www.youtube.com/watch?v=o3BaYgeR0nQ)) 
- [ ] codes: [pdclab/peregrine: Peregrine: A Pattern-Aware Graph Mining System (github.com)](https://github.com/pdclab/peregrine)

# Arabesque: A System for Distributed Graph Mining

SOSP'15

**Abstract**
Distributed data processing platforms such as MapReduce and Pregel have substantially simplified the design and deployment of certain classes of distributed graph analytics algorithms. However, these platforms do not represent a good match for distributed graph mining problems, as for example finding frequent subgraphs in a graph. Given an input graph, these problems require exploring a very large number of subgraphs and finding patterns that match some “interestingness” criteria desired by the user. These algorithms are very important for areas such as social networks, semantic web, and bioinformatics. 

In this paper, we present Arabesque, the first distributed data processing platform for implementing graph mining algorithms. Arabesque automates the process of exploring a very large number of subgraphs. It defines a high-level filter-process computational model that simplifies the development of scalable graph mining algorithms: Arabesque explores subgraphs and passes them to the application, which must simply compute outputs and decide whether the subgraph should be further extended. We use Arabesque’s API to produce distributed solutions to three fundamental graph mining problems: frequent subgraph mining, counting motifs, and finding cliques. Our implementations require a handful of lines of code, scale to trillions of subgraphs, and represent in some cases the first available distributed solutions.


- [ ] paper: [Arabesque | Proceedings of the 25th Symposium on Operating Systems Principles (acm.org)](https://dl.acm.org/doi/10.1145/2815400.2815410)
- [ ] slides: [Arabesque: sosp15-slides.pptx (live.com)](https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fhomepages.dcc.ufmg.br%2F~carlos%2Fpapers%2Fsosp%2Fsosp15-slides.pptx&wdOrigin=BROWSELINK) 
- [ ] video: [Arabesque: a system for distributed graph mining - YouTube](https://www.youtube.com/watch?v=exwS71jpUAw) 
- [ ] [The morning paper (acolyer.org)](https://blog.acolyer.org/2016/01/26/arabesque/) 
- [ ] [Project page](http://arabesque.qcri.org/) 
- [ ] [Code (github.com)](https://github.com/qcri/Arabesque) 


# Tesseract: Distributed, General Graph Pattern Mining on Evolving Graphs

EuroSys'21

**Abstract**
Tesseract is the first distributed system for executing general graph mining algorithms on evolving graphs. Tesseract scales out by decomposing a stream of graph updates into per-update mining tasks and dynamically assigning these tasks to a set of distributed workers. We present a novel approach to change detection that efficiently determines the exact modifications to the algorithm’s output for each update to the input graph. We use a disaggregated, multiversioned graph store to allow workers to process updates independently, without producing duplicates. Moreover, Tesseract provides interactive mining insights for complex applications using an incremental aggregation API. Finally, we implement and evaluate Tesseract and demonstrate that it achieves orders-of-magnitude improvements over state-of-the-art systems.

- [ ] paper: [Tesseract: Distributed, General Graph Pattern Mining on Evolving Graphs (binds.ch)](https://binds.ch/wp-content/uploads/2021/04/tesseract2021.pdf)
- [ ] slides: [tesseract2021_slides.pdf (binds.ch)](https://binds.ch/wp-content/uploads/2021/05/tesseract2021_slides.pdf); [Tesseract: Distributed, General Graph Pattern Mining on Evolving Graphs - Authors: : Laurent Bindschaedler, Jasmina Malicevic, et al (mit.edu)](https://people.csail.mit.edu/jshun/6827-s22/lectures/lecture17-1.pdf)  
- [ ] video: [[EuroSys'21\] Tesseract: Distributed, General Graph Pattern Mining on Evolving Graphs (Long) - YouTube](https://www.youtube.com/watch?v=C8XdmSTvXHM); [[EuroSys'21\] Tesseract: Distributed, General Graph Pattern Mining on Evolving Graphs (Short) - YouTube](https://www.youtube.com/watch?v=1_N0NHe1fTI)


# MaNIACS: Approximate Mining of Frequent Subgraph Patterns through Sampling

KDD'21

"And we're zany to the max!" — Animaniacs theme song

**Abstract**
We present MaNIACS, a sampling-based randomized algorithm for computing high-quality approximations of the collection of the subgraph patterns that are frequent in a single, large, vertexlabeled graph, according to the Minimum Node Image-based (MNI) frequency measure. The output of MaNIACS comes with strong probabilistic guarantees, obtained by using the empirical Vapnik-Chervonenkis (VC) dimension, a key concept from statistical learning theory, together with strong probabilistic tail bounds on the difference between the frequency of a pattern in the sample and its exact frequency. MaNIACS leverages properties of the MNIfrequency to aggressively prune the pattern search space, and thus to reduce the time spent in exploring subspaces containing no frequent patterns. In turn, this pruning leads to better bounds to the maximum frequency estimation error, which leads to increased pruning, resulting in a beneficial feedback effect. The results of our experimental evaluation of MaNIACS on real graphs show that it returns high-quality collections of frequent patterns in large graphs up to two orders of magnitude faster than the exact algorithm.

- [ ] paper: [MaNIACS : Approximate Mining of Frequent Subgraph Patterns through Sampling (acm.org)](https://dl.acm.org/doi/pdf/10.1145/3447548.3467344)
- [ ] video: [MaNIACS | Proceedings of the 27th ACM SIGKDD Conference on Knowledge Discovery & Data Mining](https://dl.acm.org/doi/abs/10.1145/3447548.3467344)


# FINGERS: Exploiting Fine-Grained Parallelism in Graph Mining Accelerators

ASPLOS'22

**Abstract**
Graph mining is an emerging application of high importance and
also with high complexity, thus requiring efficient hardware acceleration. Current accelerator designs only utilize coarse-grained parallelism, leaving large room for further optimizations. Our key insight is to fully exploit fine-grained parallelism to overcome the existing issues of hardware underutilization, inefficient resource provision, and limited single-thread performance under imbalanced loads. Targeting pattern-aware graph mining algorithms, we first comprehensively identify and analyze the abundant fine-grained parallelism at the branch, set, and segment levels during search tree exploration and set operations.We then propose a novel graph mining accelerator, FINGERS, which effectively exploits these multiple levels of fine-grained parallelism to achieve significant performance improvements. FINGERS mainly enhances the design of each single processing element with parallel compute units for set operations, and efficient techniques for task scheduling, load balancing, and data aggregation. FINGERS outperforms the state-of-the-art design by 2.8× on average and up to 8.9× with the same chip area. We also demonstrate that different patterns and different graphs exhibit drastically different parallelism opportunities, justifying the necessity of exploiting all levels of fine-grained parallelism in FINGERS.

- [x] ASPLOS'22: [ASPLOS 2022 – Proceedings (conference-publishing.com)](https://www.conference-publishing.com/list.php?Event=ASPLOS22&Full=noabs) 
- [ ] paper: [FINGERS: Exploiting Fine-Grained Parallelism in Graph Mining Accelerators (acm.org)](https://dl.acm.org/doi/pdf/10.1145/3503222.3507730) 
- [ ] video: [ASPLOS'22 - Session 1A - FINGERS: Exploiting Fine-Grained Parallelism in Graph Mining Accelerators - YouTube](https://www.youtube.com/watch?v=_2WeQuFpMFE) 

# FlexMiner: A Pattern-Aware Accelerator for Graph Pattern Mining

ISCA'21

**Abstract**
Graph pattern mining (GPM) is a class of algorithms widely used in many real-world applications in bio-medicine, ecommerce, security, social sciences, etc. GPM is a computationally intensive problem with an enormous amount of coarse-grain parallelism and therefore, attractive for hardware acceleration. Unfortunately, existing GPM accelerators have not used the best known algorithms and optimizations, and thus offer questionable benefits over software implementations.

We present FlexMiner, a software/hardware co-designed GPM accelerator that improves the efficiency without compromising the generality or productivity of state-of-the-art software GPM frameworks. FlexMiner exploits massive amount of coarse-grain parallelism in GPM by deploying a large number of specialized processing elements. For efficient searches, the FlexMiner hardware accepts pattern-specific execution plans, which are generated automatically by the FlexMiner compiler from the given pattern(s). To avoid repetitive computation on neighborhood connectivity, we provide dedicated on-chip storage to memoize reusable connectivity information in a connectivity map (c-map) which is implemented with low-cost yet high-throughput hardware. The on-chip memories in FlexMiner are managed dynamically using heuristics derived by the compiler, and thus are fully utilized. We have evaluated FlexMiner with 4 GPM applications on a wide range of real-world graphs. Our cycle-accurate simulation shows that FlexMiner with 64 PEs achieves 10.6× speedup on average over the state-of-the-art software system executing 20 threads on a 10-core Intel CPU.

**Index Terms**—accelerator, software/hardware co-design, graph pattern mining, pattern aware

- [x] author resume: [[Xuhao Chen @ MIT\] (chenxuhao.github.io)](https://chenxuhao.github.io/) 
- [x] author publications: [Xuhao Chen's Homepage (chenxuhao.github.io)](https://chenxuhao.github.io/pubs.html)
- [ ] paper: [people.csail.mit.edu/xchen/docs/isca-2021.pdf](http://people.csail.mit.edu/xchen/docs/isca-2021.pdf); [FlexMiner: A Pattern-Aware Accelerator for Graph Pattern Mining (acm.org)](https://dl.acm.org/doi/pdf/10.1109/ISCA52012.2021.00052)
- [ ] video: [MIT-CSAIL-FastCodeSeminar-XuhaoChen-4-28-2021.mp4 (dropbox.com)](https://www.dropbox.com/s/263c0otvtl3w9wc/MIT-CSAIL-FastCodeSeminar-XuhaoChen-4-28-2021.mp4?dl=0)
- [ ] GraphMinerBench: [chenxuhao/GraphMiner: Graph Pattern Mining (github.com)](https://github.com/chenxuhao/GraphMiner) 


# Pangolin: An Efficient and Flexible Graph Pattern Mining System on CPU and GPU

VLDB'20

**Abstract**
There is growing interest in graph pattern mining (GPM) problems such as motif counting. GPM systems have been developed to provide unified interfaces for programming algorithms for these problems and for running them on parallel systems. However, existing systems may take hours to mine even simple patterns in moderate-sized graphs, which significantly limits their real-world usability.

We present Pangolin, an efficient and flexible in-memory GPM framework targeting shared-memory CPUs and GPUs. Pangolin is the first GPM system that provides high-level abstractions for GPU processing. It provides a simple programming interface based on the extend-reduce-filter model, which allows users to specify application specific knowledge for search space pruning and isomorphism test elimination. We describe novel optimizations that exploit locality, reduce memory consumption, and mitigate the overheads of dynamic memory allocation and synchronization.

Evaluation on a 28-core CPU demonstrates that Pangolin outperforms existing GPM frameworks Arabesque, RStream, and Fractal by 49×, 88×, and 80× on average, respectively. Acceleration on a V100 GPU further improves performance of Pangolin by 15× on average. Compared to state-of-the-art hand-optimized GPM applications, Pangolin provides competitive performance with less programming effort.

- [ ] paper: [Pangolin: An Efficient and Flexible Graph Pattern Mining System on CPU and GPU (acm.org)](https://dl.acm.org/doi/pdf/10.14778/3389133.3389137)
- [ ] slides: https://chenxuhao.github.io/docs/vldb-2020.pptx
- [ ] code: [Galois/lonestar/mining at master · IntelligentSoftwareSystems/Galois (github.com)](https://github.com/IntelligentSoftwareSystems/Galois/tree/master/lonestar/mining)
- [ ] News: [Pangolin: An Efficient and Flexible Graph Pattern Mining System (utexas.edu)](https://cns.utexas.edu/news/pangolin-an-efficient-and-flexible-graph-mining-system-on-cpu-and-gpu) 


# Sandslash: A Two-Level Framework for Efficient Graph Pattern Mining


ICS'21

**Abstract**
Graph pattern mining (GPM) is a key building block in diverse applications, including bioinformatics, chemical engineering, social network analysis, recommender systems and security. Existing GPM frameworks either provide high-level interfaces for productivity at the cost of expressiveness or provide expressive low-level interfaces at the cost of increased programming complexity. They also lack the flexibility to explore combinations of optimizations to achieve performance competitive with hand-optimized applications.

We present Sandslash, an in-memory graph pattern mining framework that uses a novel programming interface to support productive, expressive, and efficient GPM on large graphs. Sandslash provides a high-level API that only needs a specification of the GPM problem from the user, and the system implements fast subgraph enumeration, provides efficient data structures, and applies high-level optimizations automatically. To achieve performance competitive with expert-optimized implementations, Sandslash also provides a low-level API that allows users to express algorithm-specific optimizations. This enables Sandslash to support both high-productivity and high-efficiency without losing expressiveness. We evaluate Sandslash using five GPM applications and a wide range of real-world graphs. Experimental results demonstrate that applications written using Sandslash’s high-level or low-level API outperform those in state-of-the-art GPM systems Au- toMine, Pangolin, and Peregrine on average by 13.8×, 7.9×, and 5.4×, respectively. We also show that these Sandslash applications outperform expert-optimized GPM implementations by 2.3× on average with less programming effort.

- [ ] paper: [Sandslash: A Two-Level Framework for Efficient Graph Pattern Mining (mit.edu)](http://people.csail.mit.edu/xchen/docs/ics-2021.pdf); [Sandslash | Proceedings of the ACM International Conference on Supercomputing](https://dl.acm.org/doi/10.1145/3447818.3460359)
- [ ] code: [chenxuhao/GraphMiner: Graph Pattern Mining (github.com)](https://github.com/chenxuhao/GraphMiner)



# Fractal: A General-Purpose Graph Pattern Mining System

SIGMOD'19

**Abstract**
In this paper we propose Fractal, a high performance and high productivity system for supporting distributed graph pattern mining (GPM) applications. Fractal employs a dynamic (auto-tuned) load-balancing based on a hierarchical and locality-aware work stealing mechanism, allowing the system to adapt to diferent workload characteristics. Additionally, Fractal enumerates subgraphs by combining a depth-irst strategy with a from scratch processing paradigm to avoid storing large amounts of intermediate state and, thus, improves memory eiciency. Regarding programmer productivity, Fractal presents an intuitive, expressive and modular API, allowing for rapid compositional expression of many GPM algorithms. Fractal-based implementations outperform both existing systemic solutions and specialized distributed solutions on many problems - from frequent graph mining to subgraph querying, over a range of datasets.

**Key Words**
graph pattern mining; distributed systems

- [ ] paper: [Fractal: A General-Purpose Graph Pattern Mining System (viniciusvdias.github.io)](https://viniciusvdias.github.io/publication/dias-2019-fractal/dias-2019-fractal.pdf)
- [ ] code: [dccspeed/fractal (github.com)](https://github.com/dccspeed/fractal)

# RStream: Marrying Relational Algebra with Streaming for Efficient Graph Mining on A Single Machine

OSDI'18

**Abstract**
Graph mining is an important category of graph algorithms that aim to discover structural patterns such as cliques and motifs in a graph. While a great deal of work has been done recently on graph computation such as PageRank, systems support for scalable graph mining is
still limited. Existing mining systems such as Arabesque focus on distributed computing and need large amounts of compute and memory resources.

We built RStream, the first single-machine, out-of-core mining system that leverages disk support to store intermediate data. At its core are two innovations: (1) a rich programming model that exposes relational algebra for developers to express a wide variety of mining tasks; and (2) a runtime engine that implements relational algebra efficiently with tuple streaming. A comparison between RStream and four state-of-the-art distributed mining/Datalog systems — Arabesque, ScaleMine, DistGraph, and BigDatalog — demonstrates that RStream outperforms
all of them, running on a 10-node cluster, e.g., by at least a factor of 1.7×, and can process large graphs on an inexpensive machine.

- [ ] paper: [osdi18-wang.pdf (usenix.org)](https://www.usenix.org/system/files/osdi18-wang.pdf)
- [ ] code: [rstream-system/RStream (github.com)](https://github.com/rstream-system/RStream)

# GMiner: An Efficient Task-Oriented Graph Mining System

EuroSys'18

**Abstract**

Graph mining is one of the most important areas in data mining. However, scalable solutions for graph mining are still lacking as existing studies focus on sequential algorithms. While many distributed graph processing systems have been proposed in recent years, most of them were designed to parallelize computations such as PageRank and Breadth-First Search that keep states on individual vertices and propagate updates along edges. Graph mining, on the other hand, may generate many subgraphs whose number can far exceed the number of vertices. This inevitably leads to much higher computational and space complexity rendering existing graph systems inefficient. We propose G-Miner, a distributed system with a new architecture designed for general graph mining. G-Miner adopts a unified programming framework for implementing a wide range of graph mining algorithms. We model subgraph processing
as independent tasks, and design a novel task pipeline to streamline task processing for better CPU, network and I/O utilization. Our extensive experiments validate the efficiency of G-Miner for a range of graph mining tasks.

**Key Words**
Distributed System, Large-Scale Graph Mining

- [ ] author: [Hongzhi Chen's Homepage [陈宏智\] (yaobaiwei.github.io)](https://yaobaiwei.github.io/)
- [ ] paper: [G-Miner: An Efficient Task-Oriented Graph Mining System (acm.org)](https://dl.acm.org/doi/pdf/10.1145/3190508.3190545)
- [ ] code: [yaobaiwei/GMiner: An efficient large-scale graph mining framework. (github.com)](https://github.com/yaobaiwei/GMiner)
- [ ] slides: [GMiner slides](https://yaobaiwei.github.io/papers/G-Miner_EuroSys.pptx)

# Large Scale Graph Mining with G-Miner

SIGMOD'19  DEMO

**Abstract**
This Demo presents G-Miner, a distributed system for graph mining. The take-aways for Demo attendees are: (1) a good understanding of the challenges of various graph mining workloads; (2) useful insights on how to design a good system for graph mining by comparing G-Miner with existing systems on performance, expressiveness and user-friendliness; and (3) how to use G-Miner for interactive graph analytics.

- [ ] paper: [Large Scale Graph Mining with G-Miner (acm.org)](https://dl.acm.org/doi/pdf/10.1145/3299869.3320219)
- [ ] code: [yaobaiwei/GMiner: An efficient large-scale graph mining framework. (github.com)](https://github.com/yaobaiwei/GMiner)


# AutoMine: Harmonizing High-level Abstraction and High Performance for Graph Mining

SOSP'19

**Abstract**
Graph mining algorithms that aim at identifying structural patterns of graphs are typically more complex than graph computation algorithms such as breadth first search. Researchers have implemented several systems with high-level and flexible interfaces customized for tackling graph mining problems. However, we find that for triangle counting, one of the simplest graph mining problems, such systems can be several times slower than a single-threaded implementation of a straightforward algorithm.

In this paper, we reveal the root causes of the severe inefficiencies of state-of-the-art graph mining systems and the challenges to address the performance problems. We build AutoMine, a single-machine system to provide both high-level interfaces and high performance for large-scale graph mining applications. The novelty of AutoMine comes from 1) a new representation of subgraph patterns and 2) compilation techniques that automatically generate efficient mining code with minimized memory consumption from a high-level abstraction. We have extensively evaluated AutoMine against 3 graph mining systems on 8 real-world graphs of different scales. Our experimental results show that AutoMine often produces several orders of magnitude better performance and can process very large graphs existing systems cannot handle.

- [ ] paper: [AutoMine: Harmonizing High-Level Abstraction and High Performance for Graph Mining (acm.org)](https://dl.acm.org/doi/pdf/10.1145/3341301.3359633)
- [ ] slide: [AutoMine: Harmonizing High-Level Abstraction and High Performance for Graph Mining (mit.edu)](https://people.csail.mit.edu/jshun/6886-s20/lectures/lecture15-2.pdf)
- [ ] video: [AutoMine: Harmonizing High-Level Abstraction and High Performance for Graph Mining - YouTube](https://www.youtube.com/watch?v=1q1YNUFSo9s)

# GraphPi: High Performance Graph Pattern Matching through Effective Redundancy Elimination

SC'20

**Abstract**
Graph pattern matching, which aims to discover structural patterns in graphs, is considered one of the most fundamental graph mining problems in many real applications. Despite previous efforts, existing systems face two main challenges. First, inherent symmetry existing in patterns can introduce a large amount of redundant computation. Second, different matching orders for a pattern have significant performance differences and are quite hard to predict. When these factors are mixed, this problem becomes extremely complicated. High efficient pattern matching remains an open problem currently. 

To address these challenges, we propose GraphPi, a high performance distributed pattern matching system. GraphPi utilizes a new algorithm based on 2-cycles in group theory to generate multiple sets of asymmetric restrictions, where each set can eliminate redundant computation completely. We further design an accurate performance model to determine the optimal matching order and asymmetric restriction set for efficient pattern matching. We evaluate GraphPi on Tianhe-2A supercomputer. Results show that GraphPi outperforms the state-ofthe-art system, by up to 105× for 6 real-world graph datasets on a single node. We also scale GraphPi to 1,024 computing nodes (24,576 cores).

**Key Words**
Graph mining, pattern matching, automorphisms elimination

- [ ] paper: [GraphPi.pdf (acm.org)](https://dl.acm.org/doi/pdf/10.5555/3433701.3433834)
- [ ] slide: [清华翟季冬-GraphPi-High-Performance-Graph-Pattern-Matching](https://www.ccita.net/wp-content/uploads/dlm_uploads/2021/01/4.2.1-清华翟季冬-GraphPi-High-Performance-Graph-Pattern-Matching.pdf)
- [ ] code: [thu-pacman/GraphPi (github.com)](https://github.com/thu-pacman/GraphPi)





