# Execution and preservation record

Verified on October 28, 2026.

## Preservation

- The notebook in `original/` is byte-identical to the supplied file.
- SHA-256: `7e63f7ef422a5c9c90cbda865efa4746b9d6bec9ce1593bb1665c09ec8990cc5`.
- Every original cell, including code, Markdown, execution count, metadata, and saved outputs, is unchanged in the presentation notebook. One introductory Markdown cell and title metadata were added.
- Both embedded PNG figures were extracted from the original outputs without redrawing them.

## Fresh execution

The presentation notebook ran from top to bottom in a new Python Jupyter kernel. All nonempty code cells completed without error outputs. The measurement table, equilibrium table, and eigenvalue table matched the original plain-text table outputs exactly at their displayed precision.

A temporary diagnostic cell, not included in the presentation notebook, exported the full-precision tables and checked the stored trajectories and equilibrium residuals. All four comparison simulations reported solver success and finite state arrays, with gate values within [0, 1]. Their calcium minima were at baseline within floating-point precision. Each comparison trajectory had seven states and 25,001 saved times. The zero-current equilibrium derivative residuals had maximum absolute entries below `3e-11` in the implemented state derivative units; these entries mix units and are not a dimensionless error norm.

The numerical diagnostics are in [numerical_checks.json](results/numerical_checks.json). Environment details and table comparisons are in [verification.json](results/verification.json).

## What was not verified

The saved figure image bytes were preserved, but were not required to match rerendered image bytes. Numerical agreement was checked through the displayed tables and basic trajectory checks. No solver-tolerance convergence study, independent implementation, fresh package installation, cross-platform test, or experimental validation was performed. The exact dependency versions describe the working execution environment, not a guarantee across all platforms.

The published notebook retains the uploaded outputs. Rerun outputs were used for verification and CSV export rather than replacing those originals.
