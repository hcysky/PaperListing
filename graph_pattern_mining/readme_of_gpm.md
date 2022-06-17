Papers & slides of graph pattern mining systems.

# Peregrine: A Pattern-Aware Graph Mining System

EuroSys'20

**Abstract**
Graph mining workloads aim to extract structural properties  of a graph by exploring its subgraph structures. General  purpose graph mining systems provide a generic runtime to  explore subgraph structures of interest with the help of userdefined  functions that guide the overall exploration process.  However, the state-of-the-art graph mining systems remain  largely oblivious to the shape (or pattern) of the subgraphs that  they mine. This causes them to: (a) explore unnecessary subgraphs;  (b) perform expensive computations on the explored  subgraphs; and, (c) hold intermediate partial subgraphs in  memory; all of which affect their overall performance. Furthermore,  their programming models are often tied to their  underlying exploration strategies, which makes it difficult for  domain users to express complex mining tasks.  

In this paper, we develop PEREGRINE, a pattern-aware  graph mining system that directly explores the subgraphs  of interest while avoiding exploration of unnecessary subgraphs,  and simultaneously bypassing expensive computations  throughout the mining process. We design a patternbased  programming model that treats graph patterns as first  class constructs and enables PEREGRINE to extract the semantics  of patterns, which it uses to guide its exploration.  Our evaluation shows that PEREGRINE outperforms state-ofthe-  art distributed and single machine graph mining systems,  and scales to complex mining tasks on larger graphs, while  retaining simplicity and expressivity with its ‘pattern-first’  programming approach.


- [ ] [Eurosys2020 (accepted paper, video(short, long) and slides)](https://www.eurosys2020.org/program/)
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





