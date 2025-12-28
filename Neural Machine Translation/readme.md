# Neural Machine Translation (English → German)

A sequence-to-sequence neural machine translation system using LSTM encoder-decoder architecture with attention mechanism for translating English text to German.

## Overview

This project implements a neural machine translation (NMT) model that learns to translate English sentences to German using a parallel corpus. The architecture uses:

- **Encoder**: LSTM-based encoder that processes the source (English) sentence
- **Decoder**: LSTM-based decoder that generates the target (German) translation
- **Decoding Strategies**: Both greedy decoding and beam search with length normalization

## Features

- Custom vocabulary builder with configurable size limits
- Reverse input sequences for improved translation quality
- Teacher forcing during training
- Greedy decoding for fast inference
- Beam search decoding with length normalization for better quality
- Training visualization with loss curves

## Requirements

```
torch
matplotlib
```

## Dataset Format

The model expects a parallel corpus in TSV format with 4 columns:
```
id    english_text    id    german_text
```

Example:
```
1    Let's try something.    1    Lass uns etwas ausprobieren.
```

