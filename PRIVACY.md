# Privacy Policy: Live Element for OBS

_Last updated: October 27, 2026_

Live Element for OBS ("the extension") is a Chrome extension that shows parts of web pages, and optionally a tab's audio, in OBS Studio on your own computer. This policy explains what the extension handles and where it goes.

**In short:** what you capture stays on your computer and goes only to your own OBS. We don't run servers that receive your browsing data, and the extension has no analytics, ads or tracking. Payments and the free trial are handled by ExtensionPay and Stripe.

## What the extension handles, and where it goes

### Web page content you choose to capture
- **When:** only when you pick an element (Pick element, right-click → Capture this element, or the keyboard shortcut).
- **What:** that element's HTML and styles, the page's address and title (to label the element), and, for live elements, updates to that element while its tab is open.
- **Where:** stored in the extension's local storage in your Chrome profile, and sent only to **OBS on your computer** through OBS's WebSocket server (by default `127.0.0.1`, your own machine). It is never sent to the developer or any other server.
- **Deleting it:** remove the element in the extension (✕ or Clear all), or uninstall the extension.

### Tab audio
- **When:** only when you tick "Send tab audio to OBS" for an element.
- **What and where:** that tab's audio is streamed to OBS on your computer through the same local WebSocket connection. It is not recorded or stored, and it is never sent anywhere else. You can stop it at any time; closing the tab stops it too.

### Color picking ("Pick from page")
When you use it, the extension takes a screenshot of the visible part of that tab, reads the color of the single pixel you clicked, and discards the screenshot. Only the chosen color (for example `#1f1f23`) is saved.

### OBS connection settings
Your OBS WebSocket address and password are stored locally in the extension. The password is also included in the overlay links the extension creates, so OBS can connect. These links only work on your computer; don't share them.

### The overlay file
To let OBS display your elements, the extension saves a small file, `obs-overlay.html`, to your Downloads folder (`Downloads/Live Element for OBS/`). It contains the overlay's code only, not your captured content.

## Payments and the free trial (ExtensionPay)
Pro purchases and the 7-day free trial are handled by **ExtensionPay** (extensionpay.com), with payments processed by **Stripe**.
- **Free trial:** you give ExtensionPay your email address. No payment information is collected for the trial.
- **Purchase:** you pay on ExtensionPay/Stripe's pages; the extension never sees your card details.
- **Stored in the extension:** whether you have paid, when your trial started, and an ExtensionPay account key. Some of this is kept in Chrome's synced storage, so it follows your Chrome profile.

ExtensionPay's and Stripe's handling of your email and payment details is described by them: ExtensionPay in the FAQ on <https://extensionpay.com>, and Stripe at <https://stripe.com/privacy>.

## Feedback
Pro and trial users can open "Report a problem" or "Request a feature", which opens a GitHub issue form. Issues on GitHub are **public**. Only what you type there is posted, plus the extension version and plan, which are filled in for you. Don't include passwords, OBS links or private information.

## What we don't do
- No analytics, telemetry, advertising or tracking.
- No selling, renting or sharing of your data.
- No reading of pages you haven't chosen to capture. The extension's content script stays idle until you start the picker or capture something. The one exception is reopening a site you captured a live element from: it then looks for that element again to resume live updates.
- No use of your data for anything other than showing your elements and audio in OBS.

## Permissions
- **Access to all websites:** so you can pick an element on whatever page you choose, and keep it updated live.
- **Tab capture and offscreen document:** to send a tab's audio to OBS when you turn that on.
- **Downloads:** to save the overlay file OBS loads.
- **Storage and unlimited storage:** to keep your captured elements and settings on your computer.
- **Scripting and active tab:** to start the element picker on the page you're on.
- **Context menus:** for the right-click "Capture this element" option.
- **Clipboard write:** to copy OBS links when you ask.

## Children
The extension isn't directed at children under 13 and doesn't knowingly collect their information.

## Changes
If this policy changes, the updated version will be posted here with a new date.

## Contact
Questions: open an issue in this repository, or email **kashworksstudio@gmail.com**.
