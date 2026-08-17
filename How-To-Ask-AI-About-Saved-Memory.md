# How to Ask AI About Saved Memory

## View Saved Memory

You can ask:

* "What do you remember about me?"
* "Show me the memories you have saved about me."
* "What information about me are you currently using to personalize your answers?"
* "What preferences, goals, or personal information do you currently remember about me?"

## Add a New Memory

Use phrases like:

* "Remember that I prefer concise answers."
* "Save this as a memory: I’m learning Python."
* "Please remember that I prefer detailed explanations."
* "Add this to your memory: I prefer responses in Markdown format."

## Update an Existing Memory

Be explicit about the change:

* "Update your memory: I now prefer detailed explanations instead of short answers."
* "Change my saved preference from X to Y."
* "Update what you remember about me: I no longer prefer X."
* "Replace the old memory about X with this new information: Y."

## Delete / Forget a Memory

You can say:

* "Forget that I prefer X."
* "Delete the memory about X."
* "Remove this from your saved memories: X."
* "Forget everything you remember about X."

## Review and Clean Up Memory

A useful prompt:

> "Review what you remember about me. Show me the saved memories, identify anything that may be outdated or incorrect, and let me decide what to add, update, or forget."

## Recommended General Prompt

```text
Review your saved memory about me.

1. Tell me what you currently remember.
2. Separate stable preferences from temporary information.
3. Identify anything that might be outdated.
4. Do not change or delete anything yet.
5. Wait for me to tell you what I want to add, update, or forget.
```

## Important

When you want the AI to **change memory**, make the instruction explicit:

* **Remember this:** → add
* **Update this:** → modify
* **Replace this:** → change old information
* **Forget this:** → remove
* **Don't remember this:** → remove/avoid retaining it
* **Do not change anything yet:** → review only
