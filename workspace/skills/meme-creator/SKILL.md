---
name: meme-creator
description: Create funny meme images about any topic. Use when the user asks to create a meme, make a joke image, or generate humorous content about a subject (e.g. "meme about bitcoin", "create a funny image about mondays").
---

# Meme Creator

Generate meme-style images with humorous captions about any topic.

## Steps

1. **Pick the angle.** Based on the topic, come up with a short, punchy meme concept. Think of a relatable or absurd take that would work as a meme.

2. **Write the caption.** Create a short, funny caption (1-2 lines max). Good memes are concise.

3. **Generate the image.** Call `generate_image` with a detailed prompt:

```
generate_image(
  prompt="[detailed image description including the meme text as overlay]",
  filename="meme-[topic]-[timestamp].png"
)
```

### Image prompt guidelines

- Describe the scene, characters, and expressions in detail
- Include the meme text as part of the prompt (e.g. "with bold white text at the top saying '...' and at the bottom saying '...'")
- Use a fun, exaggerated cartoon or illustration style
- Keep it clean and appropriate
- Aspect ratio is always 1:1 (square)

4. **Present the result.** Show the generated image to the user and include the caption as text.

## Examples

**User:** "meme about bitcoin"

Concept: The classic "this is fine" situation but with crypto

```
generate_image(
  prompt="Square 1024x1024 meme image. Cartoon illustration of a nervous man sitting at a computer surrounded by red stock charts and fire, smiling awkwardly while holding a coffee mug that says 'HODL'. Bold white Impact font text at the top: 'PORTFOLIO DOWN 40%' and at the bottom: 'THIS IS FINE'. Bright colors, exaggerated expressions, meme style.",
  filename="meme-bitcoin-20260227.png"
)
```

**User:** "meme about programmers"

Concept: The classic "it works on my machine" excuse

```
generate_image(
  prompt="Square 1024x1024 meme image. Split panel comic style. Top panel: confident programmer at desk pointing at screen with smug expression, text 'IT WORKS ON MY MACHINE'. Bottom panel: same programmer looking panicked at a server rack on fire, text 'THE PRODUCTION SERVER'. Bold white Impact font, cartoon style, vibrant colors.",
  filename="meme-programmers-20260227.png"
)
```

## Tips

- If the topic is vague, pick the most universally relatable angle
- Pop culture references and current trends make better memes
- The funnier the contrast or absurdity, the better
- Always generate a square image (1:1)
