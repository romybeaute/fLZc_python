# fLZc

Python wrapper package from https://github.com/lcbarnett/fLZc
Computing Lempel-Ziv complexity using optimized C implementations (LZ76, LZ78), with optional normalisation. 
Built for speed and integration with neuroscience or time series workflows.

## Features

- Fast C-based computation of LZ76 and LZ78 complexity
- Running complexity profiles
- Dictionary output
- Normalisation based on theoretical or empirical expectations
- Works with binary strings derived from numerical time series

## Installation (Development Mode)

This project uses [scikit-build-core](https://scikit-build-core.readthedocs.io/en/latest/) with `pyproject.toml` 

### Prerequisites

- Python 3.7–3.13
- `pip`, `virtualenv`, and CMake >= 3.15
- macOS, Linux (Windows support not yet tested)

### Step-by-step

Clone and install in editable mode:

```bash
git clone <your-repo-url> fLZc_python
cd fLZc_python
python -m venv .flzcvenv
source .flzcvenv/bin/activate

# Optional: Clean previous builds
rm -rf build/ dist/ _skbuild/ fLZc_python/lib*.dylib

# Install in editable mode (will compile the C code)
pip install -e .
