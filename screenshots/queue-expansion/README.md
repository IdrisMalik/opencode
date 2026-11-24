# Queued-message expansion evidence

These images are review evidence for PR #66006, hosted on a separate fork branch so they do not land in the
implementation diff. They were rendered from the real `SessionQueuePanel` and `SessionComposerRegion` components
through the story harness with production styles and deterministic fixtures. Device scale is 2x.

`00-before-*` are captures from `origin/dev` in a separate worktree at the same story IDs. The rest are from the PR
branch after review.

Desktop states use 1280 x 900. `18-long-narrow-expanded-dark.png` uses 390 x 844.

| File                                      | State                                                                   |
| ----------------------------------------- | ----------------------------------------------------------------------- |
| `00-before-multiple-collapsed-light.png`  | Before: three queued messages, no expansion or bulk visibility controls. |
| `00-before-large-queue-light.png`         | Before: six queued messages, no queue-level visibility control.          |
| `01-empty-light.png`                      | Empty queue: the composer only.                                         |
| `02-single-collapsed-light.png`           | One long queued message, collapsed to its single-line summary.          |
| `03-single-expanded-light.png`            | One queued message expanded to its full text.                           |
| `04-multiple-collapsed-light.png`         | Three queued messages, each collapsed, with the Hide queue control.     |
| `05-multiple-expanded-light.png`          | Every queued message expanded independently.                            |
| `06-mixed-light.png`                      | Mixed states: first and third expanded, middle collapsed.               |
| `07-row-hover-actions-light.png`          | Row hover: the original labelled Steer, Undo and Remove controls.       |
| `08-row-expand-focus-light.png`           | Keyboard focus on a message's expand control.                           |
| `09-header-focus-hover-light.png`         | Keyboard focus on Hide queue, with a second row hovered.                |
| `10-parked-actions-light.png`             | Parked queue: the original labelled Send action is visible.             |
| `11-large-queue-light.png`                | Six messages: the queue scrolls under its edge fade.                    |
| `12-in-app-queue-light.png`               | The queue in the composer region, light theme.                          |
| `13-in-app-summary-light.png`             | The whole queue hidden behind its compact summary, light theme.         |
| `14-in-app-queue-dark.png`                | The queue in the composer region, dark theme.                           |
| `15-in-app-summary-dark.png`              | The whole queue hidden behind its compact summary, dark theme.          |
| `16-multiple-expanded-dark.png`           | Independently expanded messages, dark theme.                            |
| `17-mixed-dark.png`                       | Mixed per-message expansion, dark theme.                                |
| `18-long-narrow-expanded-dark.png`        | Long expanded messages at 390 px, dark theme, scrolling under the fade. |

Hide queue hides every queued row and leaves the compact summary pill. Opening the pill restores each message's
previous per-message expansion state. Row actions keep their existing labelled Steer/Send and tooltip behavior.
