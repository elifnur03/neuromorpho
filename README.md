## What this project is about

A neuron's shape is not random — it is its function, made visible. A neuron with thousands of branching dendrites can integrate input from thousands of sources simultaneously. A simple neuron with a compact dendritic tree processes far less. This project asks: how much more complex are pyramidal neurons (the brain's long-range excitatory workhorses) than granule cells (compact, local processors) — and does this difference hold across mammals, from mice to humans?

Using open reconstruction data from NeuroMorpho.org, I analyzed 88 neurons across two cell types and four species, produced four publication-quality figures, and ran statistical tests confirming the differences are significant.

---

## Research question

> Do pyramidal neurons have greater dendritic branching complexity than granule cells — and is this difference consistent across mammalian species?

**Hypothesis:** Pyramidal neurons will be significantly more complex across all metrics. The difference will be larger in primates (human, macaque) than rodents (rat, mouse).

---

## Cell types compared

| Cell type | Location | Function | Expected complexity |
|---|---|---|---|
| Pyramidal | Cortex, hippocampus CA1/CA3 | Long-range excitation, cortical computation | High |
| Granule | Dentate gyrus, cerebellum | Local processing, pattern separation | Low |

---

## Species compared

Human · Macaque · Rat · Mouse

---

## Metrics analyzed

| Metric | What it measures |
|---|---|
| Total dendritic length | Sum of all branch lengths in µm |
| Branch points | Number of bifurcations in the dendritic tree |
| Max branching order | Depth of the deepest branch from soma |
| Terminal tip count | Number of dendritic endpoints |
| Mean branch length | Average individual segment length |

---

## Key findings

- Pyramidal neurons have **4–5× more total dendritic length** than granule cells across all species (p < 0.001)
- Human pyramidal neurons average **~8,200 µm** of total dendritic length vs **~1,800 µm** for human granule cells
- The pyramidal-granule complexity ratio is **larger in primates** (4.6× in humans) than rodents (4.1× in mice)
- Sholl analysis reveals a **characteristic double-peak** in pyramidal neurons (basal ~80 µm, apical tuft ~320 µm) absent in granule cells
- Human pyramidal neurons sustain dendritic branching at distances **>400 µm** from the soma; mouse neurons drop near zero beyond **250 µm**
- All differences are statistically significant (Mann-Whitney U, p < 0.001 ***)

---

## How to run

### Google Colab (recommended)
1. Go to [colab.research.google.com](https://colab.research.google.com)
2. File → Upload notebook → `neuromorpho_project.ipynb`
3. Run all cells top to bottom
4. Cell 2 downloads real SWC files from NeuroMorpho API; Cell 4 is the pre-loaded fallback

### Local Python
```bash
git clone https://github.com/YOUR_USERNAME/neuromorpho-project
cd neuromorpho-project
pip install neurom pandas numpy matplotlib seaborn scipy
jupyter notebook neuromorpho_project.ipynb
```


## What I learned

Dendritic morphology is not just a structural curiosity — it is the physical substrate of neural computation. The double-peaked Sholl profile of pyramidal neurons reflects a real functional division: basal dendrites integrate local, bottom-up input while the apical tuft integrates long-range, top-down signals. Human pyramidal neurons sustain this apical tuft at greater distances from the soma than mouse neurons, which may contribute to greater capacity for integrating contextual and predictive signals.

Granule cells taught me the opposite lesson: simplicity is not a deficit. Their compact, precise dendritic trees are optimized for pattern separation — keeping similar memories distinct — and that function may actually require less integration, not more.

The cross-species comparison also challenged me to think carefully about what morphological differences between humans and rodents actually mean. More complex is not simply better — it is differently adapted. Evolution does not optimize for general intelligence; it optimizes for survival in specific environments.

---

## References

Ascoli, G. A., et al. (2007). NeuroMorpho.org: A central resource for neuronal morphologies. *Journal of Neuroscience*, 27(35), 9247–9251.

DeFelipe, J., et al. (2002). Microstructure of the neocortex: Comparative aspects. *Journal of Neurocytology*, 31(3–5), 299–316.

Elston, G. N. (2003). Cortex, cognition and the cell. *Cerebral Cortex*, 13(11), 1124–1138.

Sholl, D. A. (1953). Dendritic organization in neurons of the visual and motor cortices of the cat. *Journal of Anatomy*, 87(4), 387–406.

---

*This project was completed independently using open-access data from NeuroMorpho.org. All code is available above. Feedback welcome.*

