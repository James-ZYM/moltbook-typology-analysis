# moltbook-typology-analysis
A git contain dataset used for the preprint "A Comparative Analysis of Social Network Topology in Reddit and Moltbook"

## Usage
### Directed graph with edges unweighted.
```
import networkx as nx

with open('./edges_weight_moltbook.pkl', 'rb') as f:
    edges_weight = pickle.load(f)

DiG = nx.DiGraph()
DiG.add_edges_from([(item[0], item[1]) for item in edges_weight])
```
### Directed graph with edges weighted by the number of comments from commenter to receiver.
```
import networkx as nx

with open('./edges_weight_moltbook.pkl', 'rb') as f:
    edges_weight = pickle.load(f)

DiG = nx.DiGraph()
DiG.add_weighted_edges_from(edges_weight)
```

## Reference
```
@misc{zhu2026comparativeanalysissocialnetwork,
      title={A Comparative Analysis of Social Network Topology in Reddit and Moltbook}, 
      author={Yiming Zhu and Gareth Tyson and Pan Hui},
      year={2026},
      eprint={2602.13920},
      archivePrefix={arXiv},
      primaryClass={cs.SI},
      url={https://arxiv.org/abs/2602.13920}, 
}
```
