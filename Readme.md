# NumPy Adventure: Level Up Your ML Skills 🕹️🚀

<p align="center">
  <!-- Hero GIF: add `assets/hero.gif` to your repo and this will show it -->
  <img src="assets/hero.gif" alt="NumPy Adventure Hero" width="800" />
</p>

<p align="center">
  <a href="#how-to-play">▶️ Play</a> •
  <a href="#levels--quests">🎯 Levels & Quests</a> •
  <a href="#badges--achievements">🏅 Badges</a> •
  <a href="#quickstart">⚡ Quickstart</a> •
  <a href="#contributing">🤝 Contribute</a>
</p>

---

<!-- Badges row -->
<p align="center">
  <img src="https://img.shields.io/github/stars/jhaabhijeet864/numpy_for_machine_learning?style=social" alt="GitHub stars" />
  <img src="https://img.shields.io/github/forks/jhaabhijeet864/numpy_for_machine_learning?style=social" alt="GitHub forks" />
  <img src="https://img.shields.io/github/issues/jhaabhijeet864/numpy_for_machine_learning" alt="Issues" />
  <img src="https://img.shields.io/badge/Phase-Gamefied-blue" alt="Phase" />
  <!-- Example CI badge (add the workflow later to make this valid) -->
  <!-- Binder / Launch badge (configure binder if wanted) -->
  <a href="https://mybinder.org/v2/gh/jhaabhijeet864/numpy_for_machine_learning/HEAD">
    <img src="https://mybinder.org/badge_logo.svg" alt="Launch in Binder" />
  </a>
</p>

---

## ✨ What is this?

NumPy Adventure converts learning NumPy into a playful questline. Each notebook is a quest: complete it to earn XP and badges. The repo is structured in phases (levels), and every challenge has a small, focused objective so learning stays fun and hands-on.

---

## 🎮 How to Play

<details>
<summary>How to start (click to expand)</summary>

1. Clone the repo:
   ```bash
   git clone https://github.com/jhaabhijeet864/numpy_for_machine_learning.git
   cd numpy_for_machine_learning
   ```

2. (Optional) Create a virtual environment:
   ```bash
   python -m venv .venv
   source .venv/bin/activate   # macOS / Linux
   .venv\Scripts\activate      # Windows
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt   # if available
   # or:
   pip install numpy jupyter
   ```

4. Start Jupyter (or JupyterLab) and open a quest (notebook):
   ```bash
   jupyter notebook
   # or
   jupyter lab
   ```

Play tip: Open one notebook at a time, complete the "Challenge" cells, and commit your solution with a short note for maintainers to review your badge claim.

</details>

---

## 🗺️ Levels & Quests

Level 1 — Phase-1: Initiate (NumPy Basics) — 150 XP total  
- Quest: Array Creation — np.array, arange, linspace (10 XP)  
- Quest: Types & Properties — shape, ndim, dtype, size (15 XP)  
- Quest: Creation helpers — zeros, ones, full, random (20 XP)  
- Quest: Reshaping & Views — reshape, transpose, flatten, views vs copies (25 XP)  
Badge: 🥉 Novice Array Wrangler

Level 2 — Phase-2: Pathfinder (Array Operations) — 200 XP total  
- Indexing & Slicing — 1D & 2D (20 XP)  
- Boolean Masking — filters & masks (25 XP)  
- Fancy Indexing & np.where (25 XP)  
- Sorting and argsort — mini-boss (30 XP)  
Badge: 🥈 Indexing Ranger

Level 3 — Phase-3: Tactician (Intermediate / ML-focused) — 300 XP total  
- Broadcasting & Vectorization (30 XP)  
- Aggregations & Reductions (30 XP)  
- Linear Algebra — dot, matmul, inverse, eig (40 XP)  
- Boss: Linear Regression step in pure NumPy (50 XP)  
Badge: 🥇 NumPy Tactician

Extra Quests:
- Performance Tuning (views vs copies, memory layout) — 40 XP  
- File I/O (np.save / np.load / savetxt) — 20 XP  
- Add an example script in /examples — 30 XP

---

## 🏆 Badges & Achievements

Earn badges when a maintainer verifies your completed quest. To claim a badge, open an issue titled:
`Badge Claim — <Badge Name> — <Your GitHub>` and include:
- Notebook you completed
- Short explanation (1–3 bullet points)
- Optional: link to a gist with your solution

Suggested Achievements:
- 🔥 Speedrun — Finish Phase-1 within 1 hour
- 🛡️ Memory-Safe — Use views efficiently in 5 examples
- 💾 Persistence — Add an example that uses np.save/load

---

## 🎨 Make it shine — GIFs, icons & hero images

Add an animated hero GIF:
- Create or record a short demo (LICEcap, OBS, or QuickTime).
- Use ezgif.com to crop/optimize (aim for < 1MB if possible).
- Save as `assets/hero.gif` in the repo root (or `docs/assets/hero.gif`) and the hero at top will render automatically.

Badge ideas (add anywhere):
```md
![Badge Example](https://img.shields.io/badge/Level-1-25XP-brightgreen)
```

Animated progress GIF example (host locally):
```md
<img src="assets/progress.gif" alt="Progress" width="350" />
```

Where to get animated icons:
- Create your own with LICEcap or screen recording → convert to GIF
- Use free animated SVGs/GIFs from sites like https://lottiefiles.com/ (Lottie needs small JS renderer—prefer GIF export)
- GIPHY for inspiration (avoid copyrighted assets in repo)

---

## 🧪 Auto-run notebooks (CI) — optional (GitHub Actions)

You can add a workflow that runs/executes notebooks and reports success. Place this file: `.github/workflows/ci.yml`

```yaml
name: CI
on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  run-notebooks:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Set up Python
        uses: actions/setup-python@v4
        with:
          python-version: 3.10
      - name: Install dependencies
        run: |
          python -m pip install --upgrade pip
          pip install -r requirements.txt || pip install numpy jupyter nbconvert
      - name: Execute notebooks
        run: |
          # Execute all notebooks in Phase-* directories (fails workflow on error)
          find . -name "*.ipynb" -not -path "./.ipynb_checkpoints/*" | while read nb; do
            jupyter nbconvert --ExecutePreprocessor.timeout=300 --to notebook --execute "$nb" --output /tmp/$(basename "$nb")
          done
```

After adding the workflow, the CI badge at the top will display build status.

---

## 📁 Repository structure (map)

- Phase-1/ — Level-1 quests (notebooks)
- Phase-2/ — Level-2 quests (notebooks)
- Phase-3/ — Level-3 quests (notebooks)
- notebooks/ — side quests & experiments
- examples/ — small reusable scripts
- assets/ — images, hero GIFs, badges
- .github/workflows/ — CI configs
- README.md — this file

---

## ✅ Quick examples (copy into a notebook)

```python
import numpy as np

# Create, reshape, dot product
a = np.arange(12).reshape(3,4)
b = np.random.randn(4,3)
res = a.dot(b)
res.mean(axis=0)
```

Challenge: Vectorize pairwise L2 distance computation for 1k vectors (try not to use explicit Python loops).

---

## 🤝 Contributing (Guild Rules)

- Claim a quest by opening an Issue: `Claim: Phase-2 Quest 3 — Fancy Indexing`
- Submit a focused PR with notebook changes, cleared outputs (or a note if outputs intentionally included)
- Add new assets under `/assets` and reference them in README
- Use the PR template (add `.github/PULL_REQUEST_TEMPLATE.md`) and include a checklist

Suggested PR checklist:
- [ ] Notebook runs end-to-end without errors
- [ ] Clear outputs or include a note if outputs preserved
- [ ] Add/update quest entry in README (if new content)
- [ ] Add tests or example scripts in /examples if applicable

---

## 📜 License & Acknowledgments

This campaign is open-source — MIT recommended. Add a LICENSE file if you like.

Thanks to coach @chaicode and the NumPy community for inspiration.

---

## 🧾 Changelog

- v0.1 — Initial learning-focused collection (Phase-1 & Phase-2 quests)
- v0.2 — Gamified README with badges, GIF support, CI example

---

If you'd like, I can:
- generate a minimal `assets/hero.gif` sample animation and a `progress.gif` (you'll need to approve and I can provide guidance on size/format), or
- create the `.github/workflows/ci.yml` file in the repo for you so the CI badge becomes active.

Happy questing! 🧭
