# Temporal eval workflow: `NoneType` length error

This note is preserved from a support question and is unrelated to the homepage template; skip it if you only need the static site.

## English

`RETRY_STATE_MAXIMUM_ATTEMPTS_REACHED` with `object of type 'NoneType' has no len()` from `EvalWorkflowCrud.get_workflow_status` appears when the database query returns no row/`None`. In this case `len(workflow_status)` raises a TypeError. To fix this, ensure the workflow record exists or add a guard before the assertion (for example, return an empty list when no result or check for `None` first).

## 中文

当 `EvalWorkflowCrud.get_workflow_status` 查询不到记录时会得到 `None`，调用 `len(None)` 会报错；先判空或补齐对应的 workflow 记录即可。
