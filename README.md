# gn

FAFB+BANC brain connectome data for cross-sex neuron matching (VNC-style challenge).

## Dataset: `fafb_banc_brain_min_syns_5`

| File | Description |
|------|-------------|
| `male_connectome_graph.csv` | Male adjacency: `From Node ID`, `To Node ID`, `Weight` |
| `female_connectome_graph.csv` | Female adjacency: same schema |
| `benchmark.csv` | Warm-start matching: `Male Node ID` ↔ `Female Node ID` |

Node IDs use `m` / `f` prefixes (e.g. `m1024`, `f8`). Graphs are filtered to edges with at least 5 synapses.

## Layout

```
data/fafb_banc_brain_min_syns_5/
├── male_connectome_graph.csv
├── female_connectome_graph.csv
└── benchmark.csv
```

Used by graph-matching pipelines (e.g. [`gm`](../gm/) band-merge and ACDC scoring).
