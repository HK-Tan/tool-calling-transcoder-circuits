# Tool-Calling Circuit Analysis with Qwen3-4B

This notebook investigates the circuits underlying tool-calling behavior in Qwen3-4B using attribution graphs and causal interventions.

## Experiments

1. **Known Answer vs Tool Use** - Compare circuits when the model knows an answer directly vs. when it delegates to a tool
2. **Tool Selection Circuits** - Analyze what circuits determine which tool to call when multiple tools are available
3. **Intervention Studies** - Validate understanding by ablating or amplifying specific supernodes to change model behavior

## Requirements

- GPU with ~24GB+ VRAM (A40, A100, RTX 4090)
- 100-200GB disk space for model weights and transcoders
- Python 3.10+

## Setup

```bash
pip install -r requirements.txt
```

You'll also need a HuggingFace token to download model weights:
```bash
export HF_TOKEN=your_token_here
# or run: huggingface-cli login
```

## Usage

Open `tool_calling_circuit_analysis.ipynb` in Jupyter and run the cells.

## Attribution

The `circuit_tracer/` folder contains code from [circuit-tracer](https://github.com/safety-research/circuit-tracer) by Michael Hanna and Mateusz Piotrowski (MIT License). See `circuit_tracer/LICENSE` for details.

The `graph_visualization.py` file is also from the circuit-tracer demos.

## Citation

If you use the circuit-tracer library, please cite:

```bibtex
@misc{circuit-tracer,
  author = {Hanna, Michael and Piotrowski, Mateusz and Lindsey, Jack and Ameisen, Emmanuel},
  title = {circuit-tracer},
  howpublished = {\url{https://github.com/safety-research/circuit-tracer}},
  note = {The first two authors contributed equally and are listed alphabetically.},
  year = {2025}
}
```
