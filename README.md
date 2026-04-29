# minecraft-plugins-configs

Ready-to-use configurations and PT-BR translations for Minecraft server plugins.

Tested on Purpur 1.21.8. Most configs should work on any Spigot/Paper fork running 1.20+.
Player data has been removed. All configs are clean and ready to drop into a new server.

---

## Plugins

| Plugin | Version | Description |
|---|---|---|
| BreweryX | 3.6.0 | Fermentation and brewing system with custom drink recipes |
| CommandPanels | - | GUI panels triggered by commands |
| DailyRewardsPlus | 1.4.8 | Daily reward system with streak tracking |
| DeluxeMenus | 1.14.1 | Custom GUI menus |
| ExcellentCrates | 6.4.1 | Crate and key system |
| GriefPrevention | - | Land claiming and grief protection |
| InteractiveChat | 4.3.4.0 | Interactive chat elements (item display, inventory preview, etc.) |
| Jobs | 5.2.6.4 | Player jobs with money and XP rewards |
| MarriageMaster | - | Marriage system between players |
| PvPManager | - | PvP toggle, combat tag and newbie protection |
| TAB | 5.3.2 | Tab list and nametag formatting |
| VentureChat | 3.8.0 | Chat channels (global, local, staff) |
| Vulcan | 2.9.7.6 | Anticheat |

---

## Repository Structure

```
minecraft-plugins-configs/
|
|- BreweryX/
|   |- addons/              # Recipe addons
|   |- languages/           # Language files (en, pt, es, de, fr...)
|   |- config.yml           # Main config
|   |- recipes.yml          # Custom drink recipes (cachaça, café, cerveja, etc.)
|   |- cauldron.yml         # Cauldron behavior
|   `- custom-items.yml     # Custom item definitions
|
|- CommandPanels/
|   |- panels/              # Individual panel definitions
|   |- config.yml
|   `- inventories.yml
|
|- DailyRewardsPlus/
|   |- Data/                # Plugin data (no player data included)
|   |- Config.yml
|   |- Messages.yml         # PT-BR
|   `- Rewards.yml          # Reward definitions by day
|
|- DeluxeMenus/
|   |- gui_menus/           # Individual menu files
|   `- config.yml
|
|- ExcellentCrates/
|   |- crates/              # Crate definitions
|   |- keys/                # Key definitions
|   |- lang/                # Language files (en, pt_BR, es, fr...)
|   |- openings/            # Opening animation configs
|   |- previews/            # Preview GUI configs
|   |- ui/                  # UI definitions
|   |- config.yml
|   `- engine.yml           # Core settings (language set to pt_BR)
|
|- GriefPrevention_config.yml
|
|- InteractiveChat/
|   |- lang/                # Language files (language set to pt_br in config)
|   |- config.yml
|   `- storage.yml
|
|- Jobs/
|   |- jobs/                # Individual job definitions
|   |- locale/              # Language files (pt-BR included)
|   |- TranslatableWords/   # Translatable word lists
|   `- generalConfig.yml    # Main config (locale set to pt_BR)
|
|- MarriageMaster/
|   |- lang/
|   |   |- pt.yml           # PT-BR translation
|   |   `- items_pt.yml     # PT-BR item names
|   `- config.yml
|
|- PvPManager/
|   `- config.yml           # PT-BR messages in combat log and kill abuse sections
|
|- TAB/
|   |- config.yml           # Main config with groups, animations and formatting
|   |- groups.yml           # Group-based tab formatting
|   |- animations.yml       # Text animations
|   `- messages.yml
|
|- VentureChat/
|   |- config.yml           # Chat channels config
|   `- Messages.yml
|
`- Vulcan/
    |- config.yml           # Anticheat config with PT-BR alert messages
    `- stats.yml
```

---

## PT-BR Translation Status

| Plugin | Status |
|---|---|
| BreweryX | translated (`language: pt`) |
| DailyRewardsPlus | translated (Messages.yml) |
| ExcellentCrates | translated (lang/lang_pt_BR.yml) |
| InteractiveChat | set to pt_br (file downloaded automatically by plugin) |
| Jobs | translated (messages_pt-BR.yml) |
| MarriageMaster | translated (lang/pt.yml and lang/items_pt.yml) |
| PvPManager | partially translated (hardcoded messages in config) |
| TAB | config in PT-BR |
| VentureChat | config in PT-BR |
| Vulcan | translated (alert and punishment messages in config) |
| CommandPanels | panels in PT-BR |
| DeluxeMenus | menus in PT-BR |

---

## Usage

Drop the plugin folder into your server's `plugins/` directory alongside the plugin JAR.
Most plugins load config on first start if no config is found, so make sure to place the files before starting.

For ExcellentCrates, the language is already set to `pt_BR` in `engine.yml`.
For InteractiveChat, the language is set to `pt_br` in `config.yml` — the plugin downloads the Minecraft language file automatically on first start.

---

## Requirements

- Spigot / Paper / Purpur 1.20+
- Vault (for economy-dependent plugins: Jobs, ExcellentCrates, DailyRewardsPlus)
- PlaceholderAPI (for TAB, VentureChat, PvPManager, InteractiveChat)
