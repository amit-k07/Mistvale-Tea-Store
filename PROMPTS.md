## Prompt 1
- Tool: Gemini (Adobe Al Extension)
- Type: code
- Prompt: 
  > I am working on a vanilla HTML/JS store. Here is the JavaScript code. Please find and fix bugs based on these rules: 
  > 1. Calculate price from PRODUCTS array, not HTML.
  > 2. Limit 5 per product or max stock.
  > 3. Coupon WELCOME10 gives 10% off (max 150) on non-gift items for subtotal > 399.
  > 4. Free shipping > 599.
  > 5. Format money to Indian format (₹) and round totals.
  > 6. Sort and search must work together. Out of stock at the bottom.
  > 7. Handle Pincode API errors gracefully.
  > Also, remove all jQuery and use Vanilla JS.
- Outcome: accepted
- Why: The AI perfectly understood the constraints and successfully refactored the legacy jQuery code into modern, bug-free Vanilla JavaScript while applying all the strict business rules.

## Prompt 2
- Tool: Gemini (Adobe Al Extension)
- Type: code
- Prompt:
  > Here is the BRAND.md file and my current CSS. Rewrite the CSS entirely to match the brand rules exactly. Use CSS custom properties for colors, clamp() for typography, CSS Grid for the layout, and ensure focus-visible states and reduced-motion media queries are included.
- Outcome: modified
- Why: The initial CSS was great but missed hiding the checkout form visually while keeping it functional. I manually adjusted the form submission logic and tweaked the quick-view modal z-index to ensure it didn't overlap the fixed header.

## Prompt 3
- Tool: Gemini (Adobe Al Extension)
- Type: code
- Prompt:
  > Now rewrite the HTML body. Remove the blink and marquee tags. Structure it semantically (header, nav, section, footer). Make the FAQ an accessible accordion using aria-expanded. Add JSON-LD schema for Organization and FAQPage at the bottom.
- Outcome: accepted
- Why: The AI generated clean, semantic HTML5. The ARIA attributes for the FAQ accordion and the JSON-LD schema were implemented perfectly according to SEO best practices.

## Prompt 4
- Tool: Gemini (Adobe Al Extension)
- Type: image
- Prompt:
  > A premium dark green tea tin canister sitting on a textured linen cloth. Next to it, a small heap of dark, malty CTC black tea leaves. Soft natural lighting, earthy cream background, high-quality product photography, minimalist.
- Outcome: modified
- Why: The first image had some text written on the tin box. I re-prompted to specify "no text on the packaging" and cropped the final result to a strict 1:1 aspect ratio.

## Prompt 5
- Tool: Gemini (Adobe Al Extension)
- Type: image
- Prompt:
  > A serene, high-quality photograph of a quiet tea garden at dawn in the Darjeeling hills. Soft, natural morning light, mist rolling over the green tea bushes. Calm, earthy, premium vibe. Warm tones, 16:9 aspect ratio, depth of field. No text, no people.
- Outcome: accepted
- Why: The image perfectly captured the "misty hills" vibe required for the brand's hero section. Compressed it using WebP to keep it under 250kb.
- 