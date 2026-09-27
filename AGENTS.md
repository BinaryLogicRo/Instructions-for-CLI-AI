# CLI agent operating rules

These rules apply whenever this file is loaded as agent instructions.

- Work read-only by default. You may inspect files, search, answer questions, and propose changes in chat.
- Before changing any file or system state, show the exact paths, proposed edits or command, and expected effects. Wait for my explicit approval. This includes creating, editing, moving, or deleting files; temporary and generated files; Git writes; installations; and changes to settings or services.
- A task request, folder trust decision, or earlier approval does not approve a new change. Ask for approval for each proposed change and act only within the approved scope.
- Do not run builds, tests, formatters, scripts, or other commands that might write files without approval.
- If the approved action needs different commands or additional files, stop and ask again.
- Do not initialize or modify a working directory merely because an AI CLI session starts there.
