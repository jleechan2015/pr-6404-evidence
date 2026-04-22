# PR 6404 Public Evidence Package

PR: https://github.com/jleechanorg/worldarchitect.ai/pull/6404
WorldArchitect head under review: `2de6d400ea13fb7377c50a73be57f013a1e44bf0`

This public package republishes review artifacts for a private repository.
All canonical green artifacts in this package were regenerated from a clean detached worktree on the current PR head, with `working_tree_dirty: false` in both substantive bundles.

## Claims

1. `level_up_signal` reaches the actual MCP and user response path.
2. A pending level-up state materializes into a persisted story entry that renders atomically in the real browser as paired rewards and planning UI on the latest entry.

## Current-head evidence roots

- Real API green bundle: `/tmp/worldarchitect.ai/unknown/level_up_signal_real_api/iteration_002`
- Browser green bundle: `/tmp/worldarchitect.ai/level-up-integrated/iteration_010/ui_level_up_rewards_planning_atomicity_browser/iteration_001`
- Browser red attempt on same SHA: `/tmp/worldarchitect.ai/level-up-integrated/iteration_009/ui_level_up_rewards_planning_atomicity_browser/iteration_001`
- Current-head clean rerun workspace: `/tmp/pr6404_clean_evidence_2de6`

## Current-head verification

- `python3 -m pytest /tmp/pr6404_clean_evidence_2de6/mvp_site/tests/test_rewards_engine.py /tmp/pr6404_clean_evidence_2de6/mvp_site/tests/test_llm_response_validation.py /tmp/pr6404_clean_evidence_2de6/mvp_site/tests/test_structured_fields_utils.py -q`
  - `76 passed, 2 skipped in 1.94s`
- `WORLDAI_DEV_MODE=true python3 /tmp/pr6404_clean_evidence_2de6/testing_mcp/test_level_up_signal_evidence_real_api.py --full`
  - `Passed: 2`, `Failed: 0`
- `WORLDAI_DEV_MODE=true TESTING_AUTH_BYPASS=true python3 /tmp/pr6404_clean_evidence_2de6/testing_ui/run_layer4_level_up_evidence.py`
  - first same-head attempt (`iteration_009`): failed because the live model emitted `level_up_signal.level_up=false`
  - second same-head attempt (`iteration_010`): passed

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
