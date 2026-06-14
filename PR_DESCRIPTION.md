# Chat navigation and scroll controls

## Summary

- Add first/last page buttons and direct page-number input to the chat conversation sidebar pagination.
- Add always-visible chat scroll buttons for jumping to the top and bottom of the conversation.
- Make the scroll buttons handle nested process-detail scroll areas, including expanded timelines and long tool result blocks.
- Add Chinese and English labels for the new controls.

## Validation

- `node --check web/static/js/chat.js`
- `node --check web/static/js/chat-scroll.js`
- Parsed `web/static/i18n/zh-CN.json` and `web/static/i18n/en-US.json` with Node.
- Synced the changes to WSL Kali, restarted the service, logged in through the frontend, and created chat tasks from the UI.
- Verified a 900-line tool-output task created nested scroll areas and that the top/bottom buttons scroll both the outer chat pane and inner process-detail/tool-result panes.
