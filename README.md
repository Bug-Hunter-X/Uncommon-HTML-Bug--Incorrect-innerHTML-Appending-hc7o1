# Uncommon HTML Bug: Incorrect innerHTML Appending

This repository demonstrates an uncommon bug related to the usage of `innerHTML` in HTML.

## Bug Description
Incorrectly using `innerHTML +=` to append content to an element can lead to unexpected results.
The issue arises from directly manipulating the innerHTML with a concatenation operation which might not always correctly parse the newly added content.  This is especially noticeable when dealing with more complex HTML structures within the target element.

## How to Reproduce
1. Clone the repository.
2. Open `bug.html` in a web browser.
3. Observe that only the initial text is displayed. The appended text doesn't appear because the innerHTML is not correctly updated. 

## Solution
The solution involves using DOM manipulation functions like `insertAdjacentHTML` for better and more predictable results.  This approach will avoid unexpected behavior when parsing content into an existing HTML structure.

## Files
* `bug.html`: Demonstrates the buggy code.
* `bugSolution.html`: Provides the corrected code using `insertAdjacentHTML`.