# Interledger Technical Test for Web Extension Developers

## Logistics
This challenge is intended to be done at home. You should write the code to work in all major browsers. You are encouraged to use any libraries that you find helpful.

We will schedule a review session afterwards with one or two of the engineers working at the Interledger Foundation, via video call. We will ask you to discuss your solution, explain your design choices and pair-program a feature live.

_Please do not share this challenge or your solution to it._

## Challenge

Write a web extension that once installed, detects all [`<link>` elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/link) on the active tab and dispatches a [custom event](https://developer.mozilla.org/en-US/docs/Web/API/CustomEvent) called `"ping"` on each of these elements. The custom event should contain a `status` property, which corresponds to the HTTP status that results from fetching the link `href`. There is no popup or UI required for completing this challenge.

### Constraints

- The source code should use TypeScript.
- Use a build system (you may use existing tools or systems to speed up this process).
- The web extension project should run in all major browsers — bonus points for Safari support.
- The extension icon should have a visual indicator for when the extension has started and finished processing the page.
- The user should not be required to click the extension icon to trigger the link elements processing (hint: don’t use `activeTab` permission).
- When a link `href `changes in the active tab, the custom event should be dispatched again on the link tag.
- Adding a new link element to the active tab page should trigger a custom event for the newly added link element.
- When a link element is removed from the active page, console.log the removed element’s `href` (i.e. Removed link: {href})
- Changes that happen in the inactive/unfocused tabs should be ignored.
- Use manifest version 3 (MV3).
- Provide a README with instructions on how to setup, build, and install the extension.
