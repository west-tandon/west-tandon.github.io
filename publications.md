---
title: Publication
permalink: /publication/
---


### 2020

_Supporting Interoperability Between Open-Source Search Engines with the Common Index File Format_<br>
<small><u>Abstract</u>: There exists a natural tension between encouraging a diverse ecosystem of open-source search engines and supporting fair, replicable comparisons across those systems. To balance these two goals, we examine two approaches to providing interoperability between the inverted indexes of several systems. The first takes advantage of internal abstractions around index structures and building wrappers that allow one system to directly read the indexes of another. The second involves sharing indexes across systems via a data exchange specification that we have developed, called the Common Index File Format (CIFF). We demonstrate the first approach with the Java systems Anserini and Terrier, and the second approach with Anserini, JASSv2, OldDog, PISA, and Terrier. Together, these systems provide a wide range of implementations and features, with different research goals. Overall, we recommend CIFF as a low-effort approach to support independent innovation while enabling the types of fair evaluations that are critical for driving the field forward.</small> <br>
Jimmy Lin, Joel Mackenzie, Chris Kamphuis, Craig Macdonald, Antonio Mallia, Michal Siedlaczek, Andrew Trotman, Arjen de Vries<br>
SIGIR, 2020 <br>
[PDF](https://arxiv.org/pdf/2003.08276.pdf)

### 2019

_GPU-Accelerated Decoding of Integer Lists_<br>
<small><u>Abstract</u>:
	    An inverted index is the basic data structure used in most current large-scale information retrieval systems. It can be modeled as a collection of sorted sequences of integers. Many compression techniques for inverted indexes have been studied in the past, with some of them reaching tremendous decompression speeds through the use of SIMD instructions available on modern CPUs. While there has been some work on query processing algorithms for Graphics Processing Units (GPUs), little of it has focused on how to efficiently access compressed index structures, and we see some potential for significant improvements in decompression speed.
	    In this paper, we describe and implement two encoding schemes for index decompression on GPU architectures. Their format and decoding algorithm is adapted from existing CPU-based compression methods to exploit the execution model and memory hierarchy offered by GPUs. We show that our solutions, GPU-BP and GPU-VByte, achieve significant speedups over their already carefully optimized CPU counterparts.</small> <br>
Antonio Mallia, Michal Siedlaczek, Torsten Suel and Mohamed Zahran<br>
CIKM, 2019 <br>
[PDF](https://www.antoniomallia.it/uploads/CIKM19.pdf)


_Forward Index Compression for Instance Retrieval in an Augmented Reality Application_<br>
<small><u>Abstract</u>:
Instance retrieval systems are widely used in applications such as robot navigation, medical diagnosis, and augmented reality. Blippar is a company that creates compelling augmented reality experiences or provides you with the tools to build your own. In this paper we focus on one of the company's augmented-reality applications, with which users are able to point their phone cameras at different objects in order to receive information about the objects in real time. In this paper, we provide what we believe to be the first study of forward index compression techniques for such instance retrieval systems. First, we perform an analysis of real-world data from a large-scale commercial instance retrieval system, run by Blippar focusing on augmented reality. Then we propose an entropy-based lossless compression strategy. Experiments show that our proposed Huffman-based approach outperforms a variety of other compression techniques, while also increasing overall system efficiency slightly.</small> <br>
Qi Wang, Michal Siedlaczek, Yen-Yu Chen, Michael Gormish, Torsten Suel<br>
IEEE Big Data Conference, 2019<br>
[PDF](https://engineering.nyu.edu/~suel/papers/forward-bd19.pdf)


### 2018
