# Pantanal ProtoSSM: BirdCLEF+ 2026 Bioacoustic Detection

This project contains a BirdCLEF+ 2026 soundscape classification pipeline built
around teacher embeddings, temporal sequence modeling, and leakage-safe
validation.

## Highlights

- Uses Google Perch embeddings and logits as teacher features.
- Splits 60-second soundscapes into 12 five-second windows.
- Predicts multi-label outputs across 234 taxa.
- Trains a ProtoSSM temporal model with cross-attention, prototype learning,
  mixup/CutMix, focal BCE, SWA, and cosine restarts.
- Adds fold-safe site/hour metadata priors and OOF stacking.
- Applies temporal-shift TTA, rank-aware scaling, delta smoothing, per-taxon
  temperature, and per-class thresholding.

## Artifact

- `pantanal_protossm_birdclef2026.ipynb`

## Reported Signals

- OOF baseline AUC logged in notebook: `0.8032`
- Challenge submission shape logged in notebook: `240 x 235`
