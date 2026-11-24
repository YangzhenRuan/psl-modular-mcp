# PSL Modular MCP server

**Answers on US and Canadian prefab modular housing: permit costs, ADU and tiny house laws, container homes, delivery, site prep and import duties.**

A free, public [MCP](https://modelcontextprotocol.io) server from [PSL Modular](https://modularpsl.com?utm_source=github&utm_medium=readme&utm_campaign=mcp): **PSL Modular Prefab Modular Housing Reference**. Connect it to ChatGPT, Claude or another AI assistant and it answers from PSL Modular's published guides and articles, citing the page each answer comes from.

```
https://modularpsl.com/mcp
```

No sign-in, no API key, nothing to install. Listed in the [official MCP Registry](https://registry.modelcontextprotocol.io/v0.1/servers?search=com.modularpsl%2Fsite) as `com.modularpsl/site`.

## What you can ask

- "How much does a modular home permit cost in Travis County, Texas, and what do I need to apply?"
- "Can I put a 400 sq ft ADU in my backyard in Oregon, and what does state law allow for tiny houses there?"
- "What does a 20 ft vs 40 ft expandable container home cost, and how long does setup take once it arrives?"
- "Should I ship 12 prefab units flat-pack or volumetric to a remote site in Colorado, and how does site prep differ?"
- "What's a realistic budget for housing a 50-person remote work crew in modular units in Canada?"
- "What import duties and customs steps apply when bringing prefab modular units into the US from overseas?"

## Tools

| Tool | What it does |
|---|---|
| `about_site` | Start here: what prefab modular, capsule and expandable container housing in the US and Canada database covers (State and county modular permit costs and requirements, ADU and tiny house laws by state, Prefab cabin rules and delivery by state, Expandable container homes: costs, sizes and setup, Flat-pack vs volumetric delivery and site prep, Glamping, lodge and remote-crew housing planning, Customs, import duties and factory-to-site shipping, Foundations, quotes and financing for prefab units), who it is for (US and Canadian developers, public agencies, architects and distributors sourcing prefab modular housing), and its free calculators. |
| `search_site` | Search prefab modular, capsule and expandable container housing in the US and Canada library: State and county modular permit costs and requirements, ADU and tiny house laws by state, Prefab cabin rules and delivery by state, Expandable container homes: costs, sizes and setup, Flat-pack vs volumetric delivery and site prep, Glamping, lodge and remote-crew housing planning, Customs, import duties and factory-to-site shipping, Foundations, quotes and financing for prefab units. |
| `read_page` | The full text of one PSL Modular page: an article, guide, FAQ page or calculator page. |
| `ask_expert` | A question still open? With your OK, your name and email, the assistant sends it to PSL Modular's specialists, and a person replies by email. |

Every tool only reads PSL Modular's published pages, except `ask_expert`, which sends only what you approve.

## Connect it

**Claude** (claude.ai and desktop, every plan; Free allows one custom connector): Customize > Connectors > **+ Add** > **Add custom connector**. Name it, paste `https://modularpsl.com/mcp`, choose **No sign in**, then **Add**. In a chat: **+** > Connectors, switch it on. ([Claude help](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp))

**ChatGPT** (Pro, Business, Enterprise, Edu; web): **Plugins** > **+** > **Add custom MCP server**. Name it, paste the URL under Connection, accept the notice, **Create as a plugin**. In a new chat type **@** and pick it. ([OpenAI help](https://help.openai.com/en/articles/12584461))

**Claude Code**:
```bash
claude mcp add --transport http psl-modular https://modularpsl.com/mcp
```
Or clone this repo: its `.mcp.json` connects it for the project.

**Cursor** (`~/.cursor/mcp.json`):
```json
{ "mcpServers": { "psl-modular": { "url": "https://modularpsl.com/mcp" } } }
```

**VS Code (GitHub Copilot)**: Command Palette > **MCP: Add Server** > HTTP > paste the URL.

**Gemini CLI**:
```bash
gemini mcp add --transport http psl-modular https://modularpsl.com/mcp
```

## Try it without an AI

```bash
curl -s https://modularpsl.com/mcp -H 'content-type: application/json' \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/call","params":{"name":"search_site","arguments":{"query":"expandable container home cost"}}}'
```

## More from PSL Modular

- Website: [modularpsl.com](https://modularpsl.com?utm_source=github&utm_medium=readme&utm_campaign=mcp)
- Questions: [modularpsl.com/contact](https://modularpsl.com/contact?utm_source=github&utm_medium=readme&utm_campaign=mcp)

Answers are general information from PSL Modular's published pages.

## License

This repository (README and config) is MIT licensed. The server is operated by PSL Modular.
