**NOTICE:** This repository is no longer maintained. Please refer to [trajminer](https://github.com/trajminer/trajminer) for new trajectory mining methods.

# Towards Semantic-Aware Multiple-Aspect Trajectory Similarity Measuring

Source code of the paper **Towards Semantic-Aware Multiple-Aspect Trajectory Similarity Measuring**, published in Transactions in GIS.

[ [publication](https://onlinelibrary.wiley.com/doi/full/10.1111/tgis.12542) ] [ [preprint](./preprint.pdf) ] [ [bibtex](./citation.bib) ]


Trajectory similarity measures included in the library:
* Edit Distance on Real sequence (EDR)
  * Chen, L., Özsu, M. T., & Oria, V. (2005, June). [**Robust and fast similarity search for moving object trajectories.**](https://dl.acm.org/citation.cfm?id=1066213) In Proceedings of the 2005 ACM SIGMOD international conference on Management of data (pp. 491-502). ACM.
* Longest Common Subsequence (LCSS)
  * Vlachos, M., Kollios, G., & Gunopulos, D. (2002). [**Discovering similar multidimensional trajectories.**](http://people.cs.aau.dk/~simas/teaching/trajectories/00994784.pdf) In Data Engineering, 2002. Proceedings. 18th International Conference on (pp. 673-684). IEEE.
* Multidimensional Similarity Measure (MSM)
  * Furtado, A. S., Kopanaki, D., Alvares, L. O., & Bogorny, V. (2016). [**Multidimensional similarity measuring for semantic trajectories.**](https://onlinelibrary.wiley.com/doi/full/10.1111/tgis.12156) Transactions in GIS, 20(2), 280-298.
* Multiple-Aspect Trajectory Similarity Measure (MUITAS)
  * Petry, L. M., Ferrero, C. A., Alvares, L. O., Renso, C., & Bogorny, V. (2019). [**Towards Semantic-Aware Multiple-Aspect Trajectory Similarity Measuring.**](https://onlinelibrary.wiley.com/doi/full/10.1111/tgis.12542) Transactions in GIS, 23(5), 960– 975.


### Usage
```
usage: Trajectory Similarity [-h] [-s {LCSS,EDR,MSM,MUITAS}] [-d {true,false}] [-t THREADS] input output config

Compute distances/similarities of trajectories.

positional arguments:
  input                  trajectory file to compute distances/similarities
  output                 output file with the distance/similarity scores
  config                 configuration file

named arguments:
  -h, --help             show this help message and exit
  -s {LCSS,EDR,MSM,MUITAS}, --similarity {LCSS,EDR,MSM,MUITAS}
                         specify the similarity measure to use
  -d {true,false}, --compute-distances {true,false}
                         specify whether to compute distances (true) or similarities (false) (default: false)
  -t THREADS, --threads THREADS
                         the number of threads to be created for running the experiment (default: 1)
```

Here's a sample [config file](sample_config.json) and [data file](sample_data.csv).
