# Stackurity for Cursor

Ask your AI assistant what software runs across your servers, deployed applications, repositories and container images, which components have known vulnerabilities or are end of life, and which upgrades fix them.

This plugin adds the Stackurity Cloud MCP server (`https://app.stackurity.dev/mcp`, Streamable HTTP) to Cursor.

## Setup

1. Install the plugin from the Cursor Marketplace.
2. The first time Cursor uses Stackurity, it opens a Stackurity sign-in page in your browser. Sign in.
3. Choose what Cursor can see (the whole organisation, or one project) and its role. Tick **Allow changes** only if it should make changes for you; without it the connection only reads.
4. Click **Allow**.

Stackurity registers Cursor itself (OAuth dynamic client registration), so there is no client ID, secret or API key to configure. You can disconnect at any time in Stackurity under Settings, AI assistants.

## Self-hosted Stackurity

Self-hosted servers expose the same endpoint at `https://<your server>/mcp`. Add it to `~/.cursor/mcp.json` instead of installing this plugin:

```json
{ "mcpServers": { "stackurity": { "url": "https://<your server>/mcp" } } }
```

## Questions to try

- "What should we fix first on the shop project?"
- "Which servers run an end-of-life operating system?"
- "Did last night's upgrade fix it?"
- "Where is log4j installed, and at which versions?"

## Links

- Website: https://stackurity.ai
- Docs: https://stackurity.ai/docs/ai-assistants
- Source: https://github.com/stackurity/stackurity
- Support: info@stackurity.ai

## License

Apache-2.0
