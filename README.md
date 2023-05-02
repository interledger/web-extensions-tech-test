# Interledger Technical Test for Web Extension Developers

## Logistics
This challenge is intended to be done at home. You should write the code to work in all major browsers. You are encouraged to use any libraries that you find helpful.

We will schedule a review session afterwards with one or two of the engineers working at the Interledger Foundation, via video call. We will ask you to discuss your solution, explain your design choices and pair-program a feature live.

_Please do not share this challenge or your solution to it._

## Challenge
Write a web extension that once installed, detects all `<link>` elements on the active tab, and fires a custom "ping" event on each one. The custom event should contain a `status` property, which corresponds to the HTTP status that results from fetching the link source.

### Constraints

- the web extension project should compile and package for all major browser marketplaces
- the extension icon should have a visual indicator for when the extension has started and finished processing the page 
- when the link source on a page changes, the custom event should fire again
- adding a new link on an active page should trigger the custom event for the newly added link
