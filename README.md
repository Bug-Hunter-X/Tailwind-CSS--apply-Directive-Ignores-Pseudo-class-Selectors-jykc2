# Tailwind CSS @apply Directive and Pseudo-classes

This repository demonstrates a bug where Tailwind CSS's `@apply` directive fails to apply styles defined within pseudo-class selectors (`:hover`, `:focus`, etc.) when nested within a class.  The bug is present in specific scenarios, particularly when applying styles to hover or focus states using the `@apply` directive within a parent class definition.

## Problem Description
The `@apply` directive is intended for applying pre-defined Tailwind classes to a given selector. However, when used with a pseudo-class selector inside a class, the styles associated with the pseudo-class are not applied. The base class styles apply, but the pseudo-class styles are effectively ignored by the `@apply` directive.

## How to Reproduce
The `bug.css` file illustrates the issue. The expected behavior is for the button to change background color on hover.  However, due to the bug, this does not occur.

## Solution
The `bugSolution.css` file demonstrates a workaround. Instead of using `@apply` for pseudo-classes, the solution applies the styles directly. This ensures that the styles for the pseudo-class selectors are properly applied.