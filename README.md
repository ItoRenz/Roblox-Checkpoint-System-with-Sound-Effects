# Roblox Checkpoint System with Sound Effects

A simple and efficient checkpoint system for Roblox games that plays sound effects and provides visual feedback when players touch checkpoints.

## Features

- ✨ **Sound Effects**: Plays a custom sound when checkpoint is touched
- 🎨 **Visual Feedback**: Checkpoint changes color briefly when activated
- 🔄 **Auto-Detection**: Automatically detects all checkpoint parts in folder
- ⏱️ **Debounce System**: Prevents spam activation (2-second cooldown)
- 📦 **Easy Setup**: Single script manages multiple checkpoints
- 🔌 **Hot-Reload**: Automatically recognizes new checkpoints added to folder

## Installation

1. Create a **Folder** in Workspace (e.g., "Checkpoints")
2. Add all checkpoint **Parts** inside the folder
3. Insert a **Script** (not LocalScript) inside the same folder
4. Copy and paste the checkpoint script code into the script

## Folder Structure

```
Workspace
└── Checkpoints (Folder)
    ├── Script (checkpoint script)
    ├── Checkpoint1 (Part)
    ├── Checkpoint2 (Part)
    ├── Checkpoint3 (Part)
    └── ... (more checkpoint parts)
```

## Configuration

You can customize the following settings in the script:

```lua
local soundId = "rbxassetid://91374794193192"  -- Change sound asset ID
sound.Volume = 0.5                              -- Adjust volume (0-1)
task.wait(2)                                     -- Change debounce duration
checkpoint.BrickColor = BrickColor.new("Bright green")  -- Change color effect
```

## How It Works

1. When a player's character touches any checkpoint part
2. The script verifies it's a valid player
3. Plays the sound effect
4. Changes checkpoint color to green temporarily
5. Applies 2-second cooldown per player
6. Returns checkpoint to original color

## Requirements

- Roblox Studio
- Valid sound asset ID
- Parts must be BasePart type (Part, MeshPart, etc.)

## Customization

### Change Sound
Replace the `soundId` variable with your desired audio asset ID:
```lua
local soundId = "rbxassetid://YOUR_SOUND_ID"
```

### Adjust Volume
Modify the volume value (0.0 to 1.0):
```lua
sound.Volume = 0.5  -- 50% volume
```

### Change Color Effect
Edit the BrickColor during activation:
```lua
checkpoint.BrickColor = BrickColor.new("Bright blue")
```

### Modify Cooldown
Change the debounce wait time:
```lua
task.wait(3)  -- 3 second cooldown
```

## License

This project is open source and available for free use in your Roblox games.

## Support

If you encounter any issues or have questions, feel free to open an issue on GitHub.

---

Made with ❤️ for the Roblox developer community
