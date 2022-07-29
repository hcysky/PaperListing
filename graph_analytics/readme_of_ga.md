Papers & slides of graph analytics.

# Low-Latency Graph Streaming using Compressed Purely-Functional Trees∗

PLDI'19

**Abstract**
There has been a growing interest in the graph-streaming setting where a continuous stream of graph updates is mixed with graph queries. In principle, purely-functional trees are an ideal fit for this setting as they enable safe parallelism, lightweight snapshots, and strict serializability for queries. However, directly using them for graph processing leads to significant space overhead and poor cache locality.

This paper presents C-trees, a compressed purely-functional search tree data structure that significantly improves on the space usage and locality of purely-functional trees. We design theoretically-efficient and practical algorithms for performing batch updates to C-trees, and also show that we can store massive dynamic real-world graphs using only a few bytes per edge, thereby achieving space usage close to that of the best static graph processing frameworks.

To study the applicability of our data structure, we designed Aspen, a graph-streaming framework that extends the interface of Ligra with operations for updating graphs.
We show that Aspen is faster than two state-of-the-art graphstreaming systems, Stinger and LLAMA, while requiring less memory, and is competitive in performance with the state-of-the-art static graph frameworks, Galois, GAP, and Ligra+. With Aspen, we are able to efficiently process the largest publicly-available graph with over two hundred billion edges in the graph-streaming setting using a single commodity multicore server with 1TB of memory.

**Keywords** 
streaming graph processing, purely-functional data structures, parallel graph algorithms

- [ ] paper: [Low-Latency Graph Streaming using Compressed Purely-Functional Trees (mit.edu)](https://people.csail.mit.edu/jshun/aspen.pdf); [arXiv (full version)[1904.08380\] Low-Latency Graph Streaming Using Compressed Purely-Functional Trees (arxiv.org)](https://arxiv.org/abs/1904.08380)
- [ ] code: [ldhulipala/aspen: Aspen is a Low-Latency Graph Streaming System built using Compressed Purely-Functional Trees (github.com)](https://github.com/ldhulipala/aspen)
- [ ] video: [Low-Latency Graph Streaming using Compressed Purely-Functional Trees - YouTube](https://www.youtube.com/watch?v=xOyvDwGrk_M)
- [ ] author main page: [Julian Shun (mit.edu)](https://people.csail.mit.edu/jshun/index.shtml)


# Ligra: A Lightweight Graph Processing Framework for Shared Memory

- [ ] code: [jshun/ligra: Ligra: A Lightweight Graph Processing Framework for Shared Memory (github.com)](https://github.com/jshun/ligra)

