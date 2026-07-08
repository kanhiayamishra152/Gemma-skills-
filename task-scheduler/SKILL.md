---
name: current-time-provider
description: Retrieves the exact current system time, date, and day. Use this ONLY when the user or system needs to know the present clock data.
---

# Current Time and Date Provider

## Instructions
Use this skill ONLY when the user asks "what time is it?", "what is today's date?", "which day is it today?", or when you explicitly need to know the current exact time context to answer a direct query.

CRITICAL WARNING FOR LLM: Do NOT use this skill to schedule tasks, create timetables, or set reminders. The system already has a built-in skill named `schedule-notification` for all scheduling actions. This skill is strictly a read-only clock.

Call the `run_js` tool with the following exact parameters:
- script name: index.html
- data: A JSON string with the following field:
  - action: String. Pass "get_current_time".
