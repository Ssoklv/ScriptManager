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

To start working with Render Switch system, press `Create first switch`. Copy the created node and paste it throughout your script.
Each switch has `Stop tracking` & `Resume tracking` buttons. If you stop tracking a certain switch, it's current state will no longer be altered by the main "Render Switch" tab 

### 3. Backdrops System

The Backdrops system in ScriptManager provides an efficient way to visually organize and group nodes within your script. This feature includes:

- **Color-Coded Backdrops**: Assign different colors to backdrops for instant visual cues, making it easier to identify sections of your script.
- **Labels and Annotations**: Add labels and annotations to backdrops to provide additional context and information about the grouped nodes.
- **Dynamic Resizing**: Automatically resize backdrops based on the nodes contained within them, ensuring a clean and organized layout.
- **No Dependencies**: Free from dependencies on other nodes, enhancing the portability and flexibility of your script.

## Benefits

- **Improved Workflow**: Streamline your compositing workflow with centralized script management, reducing the time spent on organizational tasks.
- **Enhanced Collaboration**: Facilitate collaboration with team members through version control and clearly organized scripts.
- **Increased Efficiency**: Quickly switch between render outputs and manage render settings, allowing you to focus on the creative aspects of your work.
- **Organized Layout**: Maintain a clean and organized script layout with color-coded backdrops and annotations, making complex projects easier to manage.
- **High Portability**: The design free from expressions and node links ensures that ScriptManager can be easily integrated into various projects without compatibility issues.
