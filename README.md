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

## Using in the Claude desktop app

The desktop app doesn't support `/plugin` slash commands — install through the settings UI instead:

1. In the sidebar, click **Customize**.

   ![Sidebar with Customize entry](docs/images/01-sidebar-customize.png)

2. Under **Customize**, select **Plugins**.

   ![Customize section with Plugins entry](docs/images/02-customize-plugins.png)

3. In the Plugins panel, click **Add** → **Add marketplace**.

   ![Add menu with Add marketplace option](docs/images/03-add-marketplace-menu.png)

4. Choose **Add from a repository**.

   ![Add marketplace dialog with Add from a repository option](docs/images/04-add-from-repository.png)

5. Enter `bounceban-com/bounceban-plugins` as the URL and click **Sync**.

   ![Marketplace URL field with Sync button](docs/images/05-sync-marketplace.png)

6. Find **Bounceban** in the plugin list and click **+** to install it.

   ![Bounceban plugin card with install button](docs/images/06-install-plugin.png)

7. The plugin now appears in your **Plugins** list.

   ![Plugins list showing the installed Bounceban plugin](docs/images/07-plugins-list.png)

8. Set your BounceBan API key (get one at <https://bounceban.com/app/api/settings>) as the `BOUNCEBAN_API_KEY` environment variable, e.g. in `~/.claude/settings.json`:

   ```json
   {
     "env": {
       "BOUNCEBAN_API_KEY": "your-api-key"
     }
   }
   ```

9. Start a new chat and ask naturally — e.g. *"verify jane@acme.com"*, *"clean this email list"*, or *"how many BounceBan credits do I have left?"*.

## Available plugins

| Plugin | Description |
| :----- | :---------- |
| [bounceban](https://github.com/bounceban-com/claudecode-plugin-email-verification) | Verify email addresses with the BounceBan API: single and bulk verification specializing in catch-all (accept-all) and SEG-protected emails, quick free/disposable/role/syntax checks, credits and rate-limit management, and webhooks. |

## License

Each plugin is licensed under its own repository's license. The `bounceban` plugin is MIT licensed.
