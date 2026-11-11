# Punchneedle.ai MCP app

Make a punch needle pattern from your own image, or pick one from the library.

Give an image address, a finished width and a colour limit and get a stitch-grid pattern with the yarn each colour needs. Ask for patterns by theme, estimate yarn, resize a design or check that your needle, fabric and yarn work together. Answers come from the same pattern converter, calculators and guides as punchneedle.ai.

- Website: https://punchneedle.ai
- Documentation: https://punchneedle.ai/app
- Privacy: https://punchneedle.ai/privacy
- Terms: https://punchneedle.ai/terms

This repository documents the hosted connector. It does not contain the
website or its code.

## Connect

- Endpoint: `https://punchneedle.ai/api/mcp`
- Transport: Streamable HTTP
- Authentication: none (no account, sign-in or API key)

```json
{ "mcpServers": { "punchneedle-ai": { "url": "https://punchneedle.ai/api/mcp" } } }
```

In ChatGPT, add it as a custom MCP server with no authentication. In
Claude, open Customize, then Connectors, choose Add custom connector and enter the URL.

## Tools

All tools are read-only.

| Tool | What it does |
|---|---|
| `make_pattern_from_image` | Converts a public PNG, JPEG or WebP image into a punch needle pattern with the website's pattern converter. |
| `find_patterns` | Lists the original punch needle patterns in the Punchneedle.ai library, filtered by theme and level. |
| `get_pattern` | Returns one library pattern with its size, colours, making steps, materials and the yarn each colour needs in a fine-wool kit and a rug-wool kit. |
| `calculate_yarn` | Estimates the yarn for a punch needle design from its size, the share of each colour and the needle and loop height, or from a measured swatch. |
| `resize_pattern` | Rescales a library pattern, or a design of a given size, to a new width or height with the proportions kept. |
| `match_materials` | Checks whether a punch needle, a fabric and a yarn work together, using the website's material guidance. |
| `get_material_guide` | Returns the website's guide to one punch needle material: needles, needle sizes, fabric, monk's cloth, yarn, floss, hoops or glue. |

## Try asking

- "Show me punch needle flower patterns."
- "How much yarn do I need for a 30 by 20 cm punch needle piece that is 55% cream, 30% green and 15% gold?"
- "Will an Oxford regular punch needle work with rug yarn on monk's cloth?"

## Report an issue

Open an issue in this repository or use the About page at https://punchneedle.ai/about.

## License

The documentation files in this repository are MIT licensed (see
[LICENSE](LICENSE)). The Punchneedle.ai website, its content, data and brand are
not covered by this license.
