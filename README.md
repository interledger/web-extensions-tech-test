# Interledger Technical Test for Web Extension Developers

## Logistics
This challenge is intended to be done at home. You should write the code to work in all major browsers. You are encouraged to use any libraries that you find helpful.

We will schedule a review session afterwards with one or two of the engineers working at the Interledger Foundation, via video call. We will ask you to discuss your solution, explain your design choices and pair-program a feature live.

_Please do not share this challenge or your solution to it._

## Challenge
Write a web extension that once installed, detects all [`<link>` elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/link) on the active tab, and dispatches an custom [event](https://developer.mozilla.org/en-US/docs/Web/API/Event/Event) called "ping" on each of these<link> elements. The custom event should contain a `status` property, which corresponds to the HTTP status that results from fetching the link source. There is no pop-up UI required for completing this challenge. 

### Constraints

- the web extension project should compile and package for all major browser marketplaces
- the extension icon should have a visual indicator for when the extension has started and finished processing the page 
- when the link source on a page changes, the custom event should be dispatched again
- adding a new link on an active page should trigger the custom event for the newly added link
