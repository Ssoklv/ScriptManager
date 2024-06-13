# ScriptManager

ScriptManager is a versatile and powerful Nuke gizmo designed to streamline and enhance your script management workflow. It integrates several essential features such as global localization policy & GPU usage controls, "Render Switch" system, and "Backdrop Groups" system, all aimed at improving efficiency and organization within large Nuke scripts. The core advantage of ScriptManager is its lack of expressions and links to other nodes, which significantly increases its portability across different Nuke environments and setups.

## Installation

Since ScriptManager is simply a [NoOp](https://learn.foundry.com/nuke/content/reference_guide/other_nodes/noop.html) node containing a collection of executable Python scripts, integrating it into your Nuke workflow is very straightforward:

1. **Download**: Clone or download the ScriptManager repository from GitHub(or simply copy the contents of ScriptManager.nk file).
2. **Drag & Drop**: Copy the ScriptManager.nk into your Nuke script.

It is important to maintain the gizmo's original name - "ScriptManager". Since there are no expressions or links, changing the gizmo's name will break most of the Python scripts 
## Features

### 1. "ScriptManager" tab

This tab contains a few scripts that can improve overall script speed. It includes:

- **Localization mode**: Changes the localization policy for all Read-type nodes within your selection. Select a part of the script, choose a Localization mode, press "Update mode".
- **GPU usage**: Buttons for disabling/enabling "use GPU if available" option for nodes within your selection.

### 2. "Render Switch"

The Render Switch feature simplifies the process of switching between different streams within your script before sending it to render. This is particularly useful when dealing with compute-heavy nodes or passes. Key functionalities include:

- **Render Mode**: Easily switch which variable is used for all Render Switch nodes: `$gui` or `nuke.executing`. `$gui` is used with Render farm, while `nuke.executing` is an option for local calculations
- **Switch Color**: Select the color of all Render Switch nodes in your script. Pick a color and press `Update Switch Color`
- **Bookmarks**: Add or delete all the switches from "Bookmarks" list.

To start working with "Render Switch" system, press `Create first switch`. Copy the created node and paste it throughout your script.
Each switch has `Stop tracking` & `Resume tracking` buttons. If you stop tracking a certain switch, it's current state will no longer be altered by the main "Render Switch" tab 

### 3. "Backdrops" System

The "Backdrops" system in ScriptManager provides an efficient way to visually organize and group backdrops within your script. This feature includes:

- **Group Color**: Assign different colors to groups of backdrops for instant visual cues, making it easier to identify sections of your script.
- **Group Icon**: Add icons to backdrop groups to provide additional context and information about the grouped nodes. This parameter references icons in `.../Nuke/plugins/icons`.
- **Bookmarks**: Add or delete backdrops within your selection from "Bookmarks" list.

To start working with "Backdrops" system:
1. Add 2+ groups to the `Groups` list by pressing `Add Group`.
2. Select a backdrop and press `Convert Backdrop`.
3. Pick a color and an icon for each group.
4. Press `Update Group settings`.
