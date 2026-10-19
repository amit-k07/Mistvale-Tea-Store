# Mistvale Tea Co. - Rescue Project Notes

## What I changed:
- **Bugs Fixed:** Rebuilt the entire cart logic. Prices are now strictly fetched from the `PRODUCTS` array. Implemented the 'WELCOME10' logic (capped at ₹150, ignored for Gifts, min subtotal ₹399). Prevented adding >5 items or out-of-stock items. Fixed the API search race condition by implementing a session ID check, and handled the Pincode API promise rejections gracefully so the UI doesn't get stuck.
- **Design:** Removed Comic Sans, neon colors, and blinking marquees. Replaced with a fully semantic, WCAG AA compliant CSS architecture using CSS variables for the strict brand palette (Tea Green, Parchment, etc.). Implemented responsive typography using `clamp()`.
- **UX:** Built a smooth, right-sliding cart drawer. Made the FAQ an accessible accordion. Added clear hover and focus-visible states for keyboard navigation. Replaced the pop-up newsletter with a clean inline form.
- **Technical:** Stripped out jQuery entirely in favor of Vanilla JS. Added JSON-LD for Organization and FAQPage. Maintained the exact `checkout-form` structure and payload as required by the backend contract.

## What the AI got wrong:
- **Made-up Data:** Initially, when generating the JSON-LD schema, the AI tried to invent an aggregate rating for the overall store. I caught this and removed it, adhering strictly to the rule of using only provided facts.
- **Form Submission:** The AI initially tried to replace the hidden checkout form with a standard fetch POST request. I had to explicitly instruct it to keep the form elements intact and trigger a DOM event submission to respect the "contract" constraint.
- **Image Text:** Image generators Gemini (Adobe AI Extension) struggled with putting gibberish text on the tea tins. I had to refine prompts to explicitly forbid text and rely on post-generation cropping.

## Images:
- Used Gemini (Adobe AI Extension) for product and hero images.
- Used SVG generation for the logo to ensure crisp scaling.
- **Post-processing:** All generated images were cropped to 1:1 (products) or 16:9 (hero), resized down (800x800 for products), and converted to `.webp` formats to strictly meet the <150KB (products) and <250KB (hero) constraints.

## How I tested it:
- **Browsers:** Chrome (Primary), Safari, Firefox.
- **Responsiveness:** Tested on Chrome DevTools using iPhone 12/SE dimensions (360px+) to ensure 2-column mobile grids worked without horizontal scrolling.
- **Accessibility:** Navigated the entire site using only the `Tab` key to verify `focus-visible` rings and tested the FAQ accordion functionality.

## Time spent:
- Approximately 3.5 hours.

## Extra features I added:
- Integrated a dynamic "Amount needed for free shipping" progress bar inside the cart.
- Added live validation for the newsletter email input.
- 