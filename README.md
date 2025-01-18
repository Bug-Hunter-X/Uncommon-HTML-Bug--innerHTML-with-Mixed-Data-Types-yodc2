# Uncommon HTML Bug: innerHTML with Mixed Data Types

This repository demonstrates an uncommon bug related to using `innerHTML` in HTML. The bug occurs when attempting to append both text and HTML elements using `innerHTML` along with a number.  The resulting output may be unexpected and can cause issues when parsing or processing the element's content.

## Bug Description

The primary issue lies in using `innerHTML` to concatenate a string, HTML element, and a number. The number (123) is treated as a string when appended via `innerHTML`, but this can lead to errors if the content is processed as numbers later.

## Solution

A more robust approach would involve separating concerns and using DOM manipulation methods to add content. Instead of concatenating strings and HTML directly, we create an element dynamically using `document.createElement()` and then append it to the target element.

## How to Reproduce the Bug

1. Clone this repository.
2. Open `bug.html` in your browser.
3. Observe the unexpected result.