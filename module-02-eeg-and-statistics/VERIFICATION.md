# Execution and preservation record

Checked on November 11, 2026.

## What changed in the portfolio copies

- Seven presentation notebooks add a short introduction and select the default Python 3 kernel.
- Both EEG notebooks use a relative path to the bundled workbook.
- The exploratory EEG notebook originally defined the list of frequency bands as `bandas`, then referred to it as `power_vars` in later lines. The presentation copy uses `power_vars` consistently.
- The original cells and saved outputs are preserved apart from the code changes above. Figures used in the README were extracted from the saved outputs.
- The eight notebooks in [original/](original/) are byte-for-byte copies, including the earlier temperature draft. The workbook, written answers, and slides are also unchanged. Jupyter's automatic checkpoint copies were omitted.

## Fresh execution

All seven presentation notebooks ran from the first code cell to the last in separate IPython processes with Matplotlib inline. The checked environment was Python 3.14.6 on macOS with Apple silicon. [Package versions](requirements.txt) and [execution details and original file hashes](verification.json) are included.

Every notebook regenerated the same number of plots as in the saved copy. The temperature notebook reproduced its saved text output, including the regression comparison and the strongest FFT period. The EEG reruns reproduced the centroparietal ranking, the 55.9% total variance explained by the first two components, and the classification metrics (0.938 accuracy and 0.984 ROC AUC). The exact printed text varied in the initial data check and standardization cell of both EEG notebooks. The random-sequence notebook draws new random samples on every run, so its outputs can vary.

## Scope of the checks

This checks that the code runs in the listed environment and reproduces the reported results at the displayed precision. It does not compare image bytes or test a separate Python installation or operating system. The classification retains the original evaluation procedure, including standardization before splitting and a row-level split. The score describes this course exercise.
