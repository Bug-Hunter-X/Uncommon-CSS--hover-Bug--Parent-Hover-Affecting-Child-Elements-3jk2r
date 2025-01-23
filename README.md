# Uncommon CSS :hover Bug

This repository demonstrates an uncommon CSS bug related to the unexpected behavior of the `:hover` pseudo-class when interacting with parent-child relationships and certain display properties. The hover effect on a parent element unexpectedly affects its child elements even without explicit styling for child hover states.

The bug is demonstrated in `bug.css`.  A solution is provided in `bugSolution.css`.

## Bug Description
The primary issue lies in the interaction between the `:hover` pseudo-class applied to a parent element, and the display property of that parent.  When using `display: inline-block`, `display: flex`, or `display: grid`, hovering over the parent will trigger the hover effect even on child elements (specifically affecting background color here), even though there's no `:hover` rule defined for the children themselves. This can lead to unexpected visual changes that are hard to debug without understanding the subtlety.

## Solution
The solution involves understanding the cause and choosing an approach that makes the desired behavior explicit.  The `bugSolution.css` file demonstrates one approach, using more specific styling to avoid unintended consequences.