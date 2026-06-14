# Chat navigation and scroll controls

## Summary

- Added first/last page controls and a page-number jump input to the chat conversation sidebar pagination.
- Added always-visible chat scroll controls for top and bottom navigation.
- Updated chat scrolling so top/bottom buttons also scroll nested process-detail panes, including long tool result blocks inside expanded timelines.
- Added Chinese and English i18n labels for the new pagination and scroll controls.

## Validation

- `node --check web/static/js/chat.js`
- `node --check web/static/js/chat-scroll.js`
- Parsed `web/static/i18n/zh-CN.json` and `web/static/i18n/en-US.json` with Node.
- Synced the frontend changes to WSL Kali at `/home/kali/CyberStrikeAI`, restarted the service, logged in through the web UI, and created chat tasks from the frontend.
- Verified a 900-line tool-output task created real nested scroll areas:
  - `.progress-timeline.expanded`
  - `pre.tool-result`
- Verified the always-visible top/bottom buttons scroll both the outer chat message pane and the nested process-detail/tool-output scroll panes.
