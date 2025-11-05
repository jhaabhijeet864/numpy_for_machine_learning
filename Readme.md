# NumPy Adventure — Learning NumPy with Hands-on Notebooks

A compact, task-driven collection of Jupyter notebooks that teach NumPy fundamentals through short examples and challenges. Ideal for learners who want a practical path from basics to intermediate topics used in ML/data-science workflows.

## Quick links (open these files)

- Phase notebooks
  - [phase_1.ipynb](phase_1.ipynb) — basics: array creation, properties, reshaping, views (`arr`, `arr_1d`, `reshaped`)
  - [phase_2.ipynb](phase_2.ipynb) — indexing, slicing, filtering (`numbers`, `mask`, `np.where`)
- Core topics
  - [Ufuncs.ipynb](Ufuncs.ipynb) — elementwise ops, broadcasting, `np.exp`, `np.sin`, etc.
  - [broadcasting.ipynb](broadcasting.ipynb) — broadcasting rules and examples
  - [Aggregation.ipynb](Aggregation.ipynb) — reductions (`np.sum`, `np.mean`, `np.argmax`, axis usage)
  - [Adv_indexing.ipynb](Adv_indexing.ipynb) — fancy & boolean indexing
  - [Linear_Algebra.ipynb](Linear_Algebra.ipynb) — matrix ops, `np.linalg` examples
  - [view.ipynb](view.ipynb) — copy vs view semantics
- File handling
  - [file_handling/file_io.ipynb](file_handling/file_io.ipynb) — Python file read/write basics
  - [file_handling/numpy_file_io.ipynb](file_handling/numpy_file_io.ipynb) — `np.save`, `np.load`, `np.savetxt`, `np.loadtxt` (`data_from_csv`)
  - [file_handling/bonus_pythonic_iteration.ipynb](file_handling/bonus_pythonic_iteration.ipynb) — idiomatic file iteration
  - Data files: [file_handling/sample_data.csv](file_handling/sample_data.csv), [file_handling/processed_output.txt](file_handling/processed_output.txt), [file_handling/my_data_file.npy](file_handling/my_data_file.npy), [file_handling/multiple_array.npz](file_handling/multiple_array.npz)

## What you'll learn (high level)

- Creating and inspecting arrays, shapes, dtypes, and basic sequences ([phase_1.ipynb](phase_1.ipynb))
- Indexing: basic, fancy, boolean masks and `np.where` ([phase_2.ipynb](phase_2.ipynb), [Adv_indexing.ipynb](Adv_indexing.ipynb))
- Elementwise ops / ufuncs and broadcasting ([Ufuncs.ipynb](Ufuncs.ipynb), [broadcasting.ipynb](broadcasting.ipynb))
- Aggregations and axis semantics ([Aggregation.ipynb](Aggregation.ipynb))
- Linear algebra primitives and verification ([Linear_Algebra.ipynb](Linear_Algebra.ipynb))
- Views vs copies and memory implications ([view.ipynb](view.ipynb))
- Saving/loading data with NumPy and text I/O examples (`np.save`, `np.load`, `np.savetxt`) — see [file_handling/numpy_file_io.ipynb](file_handling/numpy_file_io.ipynb) (`data_from_csv` example)

## Quick start

1. Clone the repo and create/activate a virtualenv.
2. Install minimal deps:
   ```sh
   pip install numpy jupyter
   ```
