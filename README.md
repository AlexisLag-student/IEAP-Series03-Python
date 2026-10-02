# IEAP – Python series 03 – Group Lagarde|LONG | DEEMUA

Find and plot the remarkable points of a signal (zero crossings, local maxima and
minima), estimate its frequency, and redo the analysis on a noisy and on a low-pass
filtered version of the signal.

Everything is in **one notebook: `Series03-Python.ipynb`**.

## Who does what

| Part  | Student                            | Sections of the notebook                                                                                                                                                             | Branch   |
| ----- | ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------- |
| **A** | **LAGARDE Alexis** (Student A)     | §2 – functions to find and plot remarkable points: 2.1 zero crossings + plots, 2.2 docstrings / comments / unit tests, 2.3 local maxima and minima. Also: repo setup and this README | `part-a` |
| **B** | **LONG Jiangbin** (Student B)      | §3 – analyze a known signal: 3.1 create and plot the signal, 3.2 remarkable points, 3.3 `compute_frequency_from_zero_crossings`                                                      | `part-b` |
| **C** | **DEEMUA Charles Sam** (Student C) | §4 – noisy signal: 4.1 white noise, 4.2 remarkable points of the noisy signal, 4.3 Butterworth low-pass filter                                                                       | `part-c` |

## Git workflow

The parts depend on each other (B uses A's functions, C uses A's and B's), so the
work is merged **in order A → B → C**.

1. **A** creates the public repo, adds B and C as collaborators, pushes `README.md`, `LICENSE`, `.gitignore`, `requirements.txt` and the notebook
   skeleton (headers and the three START/END banners) on `main`, and protects `main`
   (no direct push, changes only through pull requests).
2. **A** works on `part-a`, commits step by step, opens a pull request. B&C reviews it,
   then it is merged.
3. **B** starts `part-b` from the updated `main`
   A&C reviews the pull request, then it is merged.
4. **C** does the same on `part-c` from the updated `main`; A&B reviews and merges.
5. Before every commit: **Kernel → Restart & Clear All Outputs**, so the diff only
   contains code and text (outputs and execution counts cause most notebook
   conflicts). After the last merge, A runs the whole notebook once and commits the
   executed version (`Final run of the notebook`).

## License

This project is released under the [MIT License](LICENSE) – © 2026 Alexis LAGARDE, Jiangbin LONG, Charles Sam DEEMU.
