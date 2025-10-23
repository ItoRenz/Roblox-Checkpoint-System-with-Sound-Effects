# Multiple Checkpoints System with Sound

A Roblox Luau script that adds sound effects and visual feedback to multiple checkpoint parts in your game.

## Author

**ItoRenz00**

## Features

- 🔊 Play sound effects when players touch checkpoints
- 🎨 Visual feedback with color change
- ⏱️ Debounce system to prevent spam
- 🔄 Automatic setup for all checkpoints in folder
- ➕ Dynamic support for newly added checkpoints
- ⚙️ Easy configuration

## Installation

1. Create a **Folder** in your Roblox Studio workspace
2. Name the folder appropriately (e.g., "Checkpoints")
3. Add all your checkpoint **Parts** inside this folder
4. Create a **Script** inside the folder
5. Copy and paste the checkpoint system code into the script
6. Customize the configuration if needed

## Configuration

You can modify these variables at the top of the script:

```lua
local SOUND_ID = "rbxassetid://91374794193192"  -- Change to your sound ID
local SOUND_VOLUME = 0.5                         -- Volume (0-1)
local DEBOUNCE_TIME = 2                          -- Cooldown in seconds
local CHECKPOINT_COLOR = BrickColor.new("Bright green")  -- Visual feedback color
```

## How It Works

1. When a player touches a checkpoint part, the script detects it
2. A sound effect plays from the checkpoint
3. The checkpoint briefly changes color for visual feedback
4. A debounce prevents the same player from triggering it again for 2 seconds
5. After the debounce time, the checkpoint returns to its original color

## Requirements

- Roblox Studio
- Basic understanding of Roblox hierarchy
- Valid sound asset ID

## Structure

```
Workspace/
└── CheckpointsFolder/
    ├── Script (this script)
    ├── Checkpoint1 (Part)
    ├── Checkpoint2 (Part)
    └── Checkpoint3 (Part)
```

## Customization

### Change Sound

Replace the `SOUND_ID` with your own sound asset:

```lua
local SOUND_ID = "rbxassetid://YOUR_SOUND_ID_HERE"
```

### Adjust Volume

Change the volume (0 = silent, 1 = full volume):

```lua
local SOUND_VOLUME = 0.7  -- 70% volume
```

### Modify Debounce Time

Change how long before a player can trigger the same checkpoint again:

```lua
local DEBOUNCE_TIME = 5  -- 5 seconds cooldown
```

### Change Visual Effect

Customize the color that appears when checkpoint is touched:

```lua
local CHECKPOINT_COLOR = BrickColor.new("Bright red")
```

## Troubleshooting

### Sound Not Playing

- Verify your sound asset ID is correct
- Make sure the sound is not moderated by Roblox
- Check if the sound volume is not set to 0

### Script Not Working

- Ensure the script is inside the folder with checkpoints
- Verify all checkpoints are **BasePart** objects (Part, WedgePart, etc.)
- Check the Output window for error messages

### Checkpoints Triggering Too Often

- Increase the `DEBOUNCE_TIME` value
- Check if multiple parts in the player's character are touching simultaneously

## Contributing

Feel free to fork this project and submit pull requests for improvements!

## License

This project is open source and available for use in your Roblox games.

## Credits

Created by **ItoRenz00**

## Support

If you encounter any issues or have questions, please open an issue in the repository.

---

**Note:** Make sure you have the proper permissions to use any sound assets in your game.
