# Queued-message expansion screenshots

These are implementation screenshots, not separate mockups. They were rendered from the story harness
(`bun --cwd packages/stories dev`) with the real `SessionQueuePanel` and `SessionComposerRegion` components, deterministic
prompts from `packages/app/src/session/composer/queue-panel.stories.tsx`, and the production app styles. Device scale is 2x.

Desktop states use the 1280 x 900 viewport unless the filename says otherwise. `18-long-narrow-expanded-dark.png` uses
390 x 844.

`00-before-*` are captures from `origin/dev` before this change, made in a separate worktree with the same story harness.
The rest are after.

| File                                      | State                                                                   |
| ----------------------------------------- | ----------------------------------------------------------------------- |
| `00-before-multiple-collapsed-light.png`  | Before: three queued messages, no expansion or collapse controls.       |
| `00-before-large-queue-light.png`         | Before: six queued messages, no queue-level collapse control.            |
| `01-empty-light.png`                      | Empty queue: the composer only.                                         |
| `02-single-collapsed-light.png`           | One long queued message, collapsed to its single-line summary.          |
| `03-single-expanded-light.png`            | One queued message expanded to its full text.                           |
| `04-multiple-collapsed-light.png`         | Three queued messages, each collapsed, with the queue header.           |
| `05-multiple-expanded-light.png`          | Every queued message expanded independently.                            |
| `06-mixed-light.png`                      | Mixed states: first and third expanded, middle collapsed.               |
| `07-row-hover-actions-light.png`          | Row hover: steer, undo and remove controls.                             |
| `08-row-expand-focus-light.png`           | Keyboard focus on a message's expand control.                           |
| `09-header-focus-hover-light.png`         | Keyboard focus on Collapse all, with a second row hovered.              |
| `10-parked-actions-light.png`             | Parked queue: the first message's send action is always visible.        |
| `11-large-queue-light.png`                | Six messages: the queue scrolls under its edge fade.                    |
| `12-in-app-queue-light.png`               | The queue in the composer region, light theme.                          |
| `13-in-app-summary-light.png`             | The whole queue collapsed to its compact summary, light theme.          |
| `14-in-app-queue-dark.png`                | The queue in the composer region, dark theme.                           |
| `15-in-app-summary-dark.png`              | The whole queue collapsed to its compact summary, dark theme.           |
| `16-multiple-expanded-dark.png`           | Independently expanded messages, dark theme.                            |
| `17-mixed-dark.png`                       | Mixed per-message expansion, dark theme.                                |
| `18-long-narrow-expanded-dark.png`        | Long expanded messages at 390 px, dark theme, scrolling under the fade. |
| `19-summary-focus-light.png`              | Keyboard focus on the summary pill after Collapse all.                  |

The whole-queue Collapse all state (13 and 15) hides every queued row and leaves the compact summary pill. Expanding it
restores each message's previous per-message expansion state.
