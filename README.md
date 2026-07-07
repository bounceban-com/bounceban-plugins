# BounceBan Plugins — Claude Code Plugin Marketplace

A [Claude Code plugin marketplace](https://code.claude.com/docs/en/plugin-marketplaces) for BounceBan tools.

## Installation

Add the marketplace:

```shell
/plugin marketplace add bounceban-com/bounceban-plugins
```

Then install a plugin:

```shell
/plugin install bounceban@bounceban-plugins
```

## Using in the Claude Code desktop app

The desktop app (Mac/Windows) supports the same `/plugin` commands as the CLI — type them directly into the chat input:

1. Open the Claude Code desktop app and start a session in any project.
2. Add this marketplace:

   ```shell
   /plugin marketplace add bounceban-com/bounceban-plugins
   ```

3. Install the plugin:

   ```shell
   /plugin install bounceban@bounceban-plugins
   ```

   You can also type `/plugin` on its own to browse and manage marketplaces and installed plugins interactively.

4. Set your BounceBan API key (get one at <https://bounceban.com/app/api/settings>). The desktop app doesn't always inherit variables from your shell profile, so the most reliable option is to put it in `~/.claude/settings.json`:

   ```json
   {
     "env": {
       "BOUNCEBAN_API_KEY": "your-api-key"
     }
   }
   ```

   Alternatively, `export BOUNCEBAN_API_KEY="your-api-key"` in your shell profile works when the app inherits your login environment.

5. Restart the session, then just ask naturally — e.g. *"verify jane@acme.com"*, *"clean this email list"*, or *"how many BounceBan credits do I have left?"*.

## Available plugins

| Plugin | Description |
| :----- | :---------- |
| [bounceban](https://github.com/bounceban-com/claudecode-plugin-email-verification) | Verify email addresses with the BounceBan API: single and bulk verification specializing in catch-all (accept-all) and SEG-protected emails, quick free/disposable/role/syntax checks, credits and rate-limit management, and webhooks. |

## License

Each plugin is licensed under its own repository's license. The `bounceban` plugin is MIT licensed.
