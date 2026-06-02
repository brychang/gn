# gn

Investigate **graph neural network (GNN)** approaches to **graph matching** on connectomes.

Primary use case: cross-sex neuron correspondence on FAFB+BANC brain connectomes (male/female adjacency graphs plus a benchmark warm-start matching).

## Data (local only)

Connectome CSVs live under `data/` and are **not** tracked in git. Place the dataset locally:

```
data/fafb_banc_brain_min_syns_5/
├── male_connectome_graph.csv   # From Node ID, To Node ID, Weight
├── female_connectome_graph.csv
└── benchmark.csv                 # Male Node ID ↔ Female Node ID
```

Node IDs use `m` / `f` prefixes (e.g. `m1024`, `f8`). Graphs retain edges with at least 5 synapses.

Related non-GNN pipelines: [`gm`](../gm/) (band-merge, ACDC scoring).
