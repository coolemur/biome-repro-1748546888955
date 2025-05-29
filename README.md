The issue occurs not with local configurations file, but when we run it with env variable:

BIOME_CONFIG_PATH=/Users/Mantas/.config/biome.json biome lint

To test, move biome-config to your user .config directory, rename it to biome.json
and run `BIOME_CONFIG_PATH=/user_path/.config/biome.json biome lint src/index.ts`

Remove local configuration file from project directory.

Expectation:

As this global configuration file has `"noForEach": "off"` lint should skip that rule.