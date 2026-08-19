# Agentic Graph AI

Professional research portfolio for David Foutch, a computational structural biologist developing protein structure network methods, scientific software, and interpretable machine-learning workflows.

## Research represented

- Protein structure networks and conformational change
- PDB2Graph scientific software for PyMOL
- EGFR pocket random-walk and representation-learning experiments
- LRH-1 graph attention network pilot workflow
- Peer-reviewed work in computational structural biology

## Local development

Requires Node.js 22 or newer.

```bash
npm install
npm run dev
```

Create the production site with:

```bash
npm run build
```

The static output is written to `dist/` and is suitable for GitHub Pages.

## Deployment

Deployment is intentionally separated from the retired AWS S3 workflow in the archived `website-portfolio` repository. This project is designed for GitHub Pages and a custom domain managed through GoDaddy DNS.

## Scientific integrity

Project language distinguishes completed results from active validation. The LRH-1 GAT workflow is described as a pilot until its split robustness and dataset limitations have been fully audited.

## Interactive molecular artifacts

The site embeds two standalone 3Dmol.js artifacts from local project data:

- `public/interactive/lrh1-psn-comparison.html` is the validated 1YOK/4PLD
  RING-network comparison exported from `lrh1-drug-screening-project`.
- `public/interactive/lrh1-gat-1yok-ig.html` was recovered from the Stanford Demo
  `/viz/psn_net` route. It embeds `1YOK.pdb`, the `1YOK_c7_A.csv` heavy-atom
  contact graph filtered at `kmin=8`, and the top 25 scores from
  `group_c7.0/ig_delta_neg.csv`.

The GAT artifact is labeled as Integrated Gradients attribution. It must not be
described as a statistical-significance map or as raw graph-attention weights.
Both files embed their structure and network data; they load only the 3Dmol.js
renderer from a public CDN at viewing time.
