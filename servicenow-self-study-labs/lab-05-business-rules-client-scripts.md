# Lab 05 – Introductory Business Rules and Client Scripts

## Objective

Understand the difference between server-side and client-side scripting in ServiceNow.

## Concepts

- JavaScript
- Business Rule
- Client Script
- Server-side logic
- Client-side logic
- GlideRecord basics
- Jelly basics

## Business Rule Example – Pseudocode

```javascript
// If an incident has high priority, add a work note
if (current.priority == "1") {
    current.work_notes = "High priority incident detected. Please review immediately.";
}
```

## Client Script Example – Pseudocode

```javascript
// Show a message when category changes
function onChange(control, oldValue, newValue, isLoading) {
    if (isLoading) {
        return;
    }

    if (newValue == "hardware") {
        g_form.showFieldMsg("category", "Please check hardware assignment group.", "info");
    }
}
```

## Reflection

Business Rules run on the server and are useful for backend logic. Client Scripts run in the browser and can improve the user experience on forms.
