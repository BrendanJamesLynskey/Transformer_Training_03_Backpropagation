# Transformer Training 03 — Backpropagation Through a Transformer

The chain rule, one operation at a time, from the loss back to the embedding: linear layers, GELU, softmax and the causal mask, LayerNorm, and the residual highway. What each step must save from the forward pass, and how a hand-written backward pass is checked.

**Live site:** https://brendanjameslynskey.github.io/Transformer_Training_03_Backpropagation/

What a gradient is; the backward order; linear, GELU, softmax/attention and LayerNorm backward passes; the residual highway; what must be saved (activation memory); checking against autograd and finite differences.

## Live, animated companion

This deck is the slide companion to Part 2 (Training) of [Transformer Decoder Explained](https://transformer-training-explained.vercel.app/training), where the same model trains in your browser:

- [Chapter 4: Backprop through the model](https://transformer-training-explained.vercel.app/training/04-backprop)

## Where the numbers come from

Every measured number on these slides comes from the site's [results.md](https://github.com/BrendanJamesLynskey/transformer-explainer/blob/main/results.md) (seeded NumPy reference runs; CI recomputes them), filled in at build time from its `results.json`. Numbers from papers are cited on the slide with a link. The model is tiny (5,376 parameters, one book, a CPU): its runs show mechanisms, not what happens at scale, and the slides say so where it matters. GPU runs of the site's Colab notebooks are pending; no GPU number appears here.

Part of the [Transformer Training sub-hub](https://github.com/BrendanJamesLynskey/LLM_Hub_Transformer_Training) &middot; [LLMs hub](https://github.com/BrendanJamesLynskey/LLMs)
