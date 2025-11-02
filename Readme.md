# NumPy for Machine Learning 🚀

A concise, hands-on collection of Jupyter Notebooks and examples to build a solid NumPy foundation for machine learning, data science, and scientific computing.

---

Table of Contents

- Overview
- Quickstart
- Repository structure
- What you'll learn    
- Examples
- Installation
- Run the notebooks
- Contributing
- License & Acknowledgments
- Changelog

---

Overview

This repository contains step-by-step, well-documented Jupyter Notebooks that teach NumPy from the basics up to intermediate topics commonly used in machine learning workflows. The notebooks are organized into phases so you can follow a progressive, hands-on learning path.

Why this repo?
- Focused on practical NumPy usage for ML practitioners.
- Clear, runnable notebooks with explanations and exercises.
- Small, focused examples that you can reuse in projects.

Repository structure

Notebooks and examples are grouped into phases to reflect the learning progression. Example layout:

- Phase-1/                  # Fundamentals: arrays, properties, reshaping
- Phase-2/                  # Array operations: slicing, indexing, sorting, filtering
- Phase-3/                  # Linear algebra, broadcasting, performance tips
- notebooks/                # Misc notebooks and experiments
- examples/                 # Small reusable example scripts
- README.md                 # This file

Note: I wasn't able to read the repository contents from here, so if you prefer I can update this section with the exact filenames (e.g., `Phase-1/01-array-basics.ipynb`) once you provide the list or allow access.

What you'll learn

Phase 1 - NumPy Basics
- Creating arrays from Python lists and iterables
- Array types: vectors, matrices, tensors
- Array properties: shape, ndim, size, dtype
- Creating arrays: zeros, ones, full, arange, linspace, random
- Reshaping and transposing arrays
- Views vs copies (basic intro)

Phase 2 - Array Operations
- Indexing and slicing (1D & 2D)
- Boolean masking and filtering
- Fancy indexing and np.where
- Conditional selection and np.take
- Sorting and argsort

Phase 3 - Intermediate / ML-focused
- Broadcasting rules and vectorized operations
- Aggregations: sum, mean, std, min, max
- Linear algebra: dot, matmul, inverse, eig
- Reading/writing arrays (np.save, np.load, np.savetxt)
- Performance tips (views vs copies, memory layout, dtype choices)

Quickstart

1. Clone the repository

   git clone https://github.com/jhaabhijeet864/numpy_for_machine_learning.git
   cd numpy_for_machine_learning

2. Create a virtual environment (optional but recommended)

   python -m venv .venv
   source .venv/bin/activate   # macOS / Linux
   .venv\Scripts\activate      # Windows (PowerShell or CMD)

3. Install dependencies

If there's a requirements.txt in the repo:

   pip install -r requirements.txt

If not, install the essentials:

   pip install numpy jupyter

Run the notebooks

Start Jupyter in the repo root and open the notebooks from your browser:

   jupyter notebook

Or use JupyterLab:

   pip install jupyterlab
   jupyter lab

Examples (what to try)

- Quick array creation and operations
  - Create arrays with np.array, np.arange, np.linspace
  - Reshape with .reshape and .T
  - Elementwise arithmetic and reductions

- Small ML-like examples
  - Implement a simple linear regression update step using dot products and broadcasting
  - Compute pairwise distances between vectors using vectorized NumPy

Best practices & tips

- Prefer vectorized operations over Python loops for performance.
- Watch for unintended copies; prefer views when you need efficient memory use.
- Use appropriate dtypes (float32 vs float64) for a good trade-off between speed and precision.
- Keep notebooks small and focused: one concept per notebook + exercises.

Contributing

Contributions are very welcome. Ways you can help:
- Open issues for bugs, typos, or suggestions for new notebooks.
- Submit pull requests with improved content, additional examples, or corrected notebooks.
- Add exercise solutions or small tests for notebooks.

When opening a PR, please:
- Use a descriptive title and reference any related issue.
- Keep changes focused to a single topic per PR.
- Run the notebooks and ensure outputs are consistent (clear outputs if needed).

If you'd like contribution templates (ISSUE_TEMPLATE, PULL_REQUEST_TEMPLATE), I can provide examples.

License & Acknowledgments

This project is open source — MIT recommended. Add or modify a LICENSE file as needed.

Special thanks to my coach @chaicode and the NumPy community for inspiration and guidance.

Changelog

- v0.1 - Initial learning-focused notebook collection (Phases 1 & 2)

---

If you'd like this README tuned further (shorter, more tutorial-style, or with a list of actual notebook filenames), tell me how you'd like it adjusted and I will adapt it.
