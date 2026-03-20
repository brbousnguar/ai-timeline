---
description: How to add a new event to the AI History Timeline
---

When asked to add a new event to the timeline, follow this procedure:

1. **Research Details:** Find the specific Event Title, Date (e.g. "October 2025"), Company, Description, Impact, and Link.
2. **Determine Event Type:** 
   - If the event is monumental, set `eventType: "major"`.
   - If the event is in the future, set `eventType: "planned"`.
   - Otherwise, omit the `eventType` field.
3. **Format & Insert:** Use `multi_replace_file_content` to accurately append the newly formatted JSON object inside the `timelineEvents` array in `script.js`.
4. **Logos:** Ensure that the company name used matches an existing PNG image in `assets/logos/` (the application will convert the company name to lowercase and append `.png`). If it is a new company, notify the user.
5. **Preview:** Use the `browser_subagent` to visualize the successful addition in the UI.
