# CSS Specificity Gotcha: Cascade Order and Specificity Tie

This repository demonstrates a subtle but important issue related to CSS specificity and the cascade.  The problem arises when selectors of equal specificity are applied to the same element; the order in which those rules appear in the stylesheet determines which rule takes precedence.

## The Bug

The `bug.css` file contains CSS rules that, when applied to a `<div>` element with the classes `special` and an ID of `specific`, result in an unexpected color. Although `#specific .special div` has high specificity, the final color might not be purple due to the cascade's behavior.

## The Solution

The `bugSolution.css` file offers a solution by either rearranging the CSS rules to prioritize the most specific and desired style or by using the `!important` flag (though this is generally discouraged).  The solution clarifies how the cascade operates to determine the resulting color.

## How to Reproduce

1. Clone this repository.
2. Open `index.html` (you'll need to create a simple `index.html` file to test the CSS) in a web browser.
3. Observe the color of the `<div>` element.  The color will highlight the cascade's interaction with specificity and the order of rules.

## Lesson Learned

Understanding CSS specificity and the cascade is crucial for writing predictable and maintainable stylesheets. Be mindful of rule order when dealing with selectors of equal specificity.