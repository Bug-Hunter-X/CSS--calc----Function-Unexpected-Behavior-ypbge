# CSS `calc()` Function Unexpected Behavior

This repository demonstrates an unexpected behavior of the CSS `calc()` function when used without explicitly defining the parent element's width. The issue occurs when `calc()` is used to calculate a width that depends on the parent's width, but the parent's width is not explicitly set.

## Bug
The `bug.css` file contains the following CSS code:
```css
div {
  width: calc(100% - 10px);
}
```
When applied to a div whose parent's width is not explicitly set, this code may not work as expected.

## Solution
The `bugSolution.css` file contains the solution, which involves setting an explicit width for the parent element, which solves the unexpected layout issue.
```css
.parent {
  width: 300px;
}
div {
  width: calc(100% - 10px);
  background-color: lightblue;
  padding: 10px; 
}
```