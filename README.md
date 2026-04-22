# PR 6404 Public Evidence Package

PR: https://github.com/jleechanorg/worldarchitect.ai/pull/6404
WorldArchitect head under review: `4bb5cbe2d026900dc1019dac7fc62ac6be921664`

This public package exists because the main repository is private. It republishes the media and key textual artifacts needed to review these two claims:

1. `level_up_signal` reaches the actual MCP and user response path.
2. A pending level-up state materialized into a persisted story entry renders atomically in the real browser as paired rewards and planning UI on the latest entry.

## Clean-computer reproduction outline

Prerequisites:
- Access to `https://github.com/jleechanorg/worldarchitect.ai`
- Python 3.11+
- Real Firebase credentials and real LLM credentials configured per the repo README
- `WORLDAI_DEV_MODE=true`
- `TESTING_AUTH_BYPASS=true` for the browser run

Commands used for the reviewed evidence:

```bash
git clone https://github.com/jleechanorg/worldarchitect.ai.git
cd worldarchitect.ai
git checkout 4bb5cbe2d026900dc1019dac7fc62ac6be921664

WORLDAI_DEV_MODE=true python3 testing_mcp/test_level_up_signal_evidence_real_api.py --full
WORLDAI_DEV_MODE=true TESTING_AUTH_BYPASS=true python3 testing_ui/run_layer4_level_up_evidence.py
```

Expected outputs:
- Real API harness summary ends with `Passed: 2`, `Failed: 0`, and an evidence directory under `/tmp/worldarchitect.ai/feat_zfc-level-up-model-computes/level_up_signal_real_api/iteration_002`
- Browser harness summary ends with `TEST PASSED` and an evidence directory under `/tmp/worldarchitect.ai/level-up-integrated/iteration_007`

## Browser media

- `browser/pr_6404_level_up_atomicity.gif`
- `browser/pr_6404_level_up_atomicity.mp4`
- `browser/pr_6404_level_up_atomicity.webm`
- `browser/pr_6404_level_up_atomicity.vtt`

## Terminal media

- `terminal/pr_6404_level_up_signal.gif`
- `terminal/pr_6404_level_up_signal.mp4`
- `terminal/pr_6404_level_up_signal.cast`

## Key textual artifacts

- `real_api_run.json`
- `real_api_raw_signal_propagation.txt`
- `browser_run.json`
- `browser_trace.json`
- `pending_level_up_projection_response.json`

## Dirty worktree note

The evidence was captured in a dirty worktree because unrelated local `.beads/`, roadmap/wiki, and test-file changes were intentionally preserved rather than reverted.
