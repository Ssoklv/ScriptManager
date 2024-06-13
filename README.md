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

### 2. Render Switch

The Render Switch feature simplifies the process of switching between different render outputs within your script. This is particularly useful when dealing with multiple render layers or passes. Key functionalities include:

- **Output Selection**: Easily switch between various render outputs, such as beauty, ambient occlusion, and depth passes, without manually reconnecting nodes.
- **Render Settings Management**: Store and manage different render settings, enabling quick adjustments based on your compositing needs.
- **Batch Rendering**: Automate the rendering process for multiple outputs, reducing the time spent on manually initiating renders.
- **Independent Operation**: Designed to operate independently of other nodes, ensuring high portability and ease of use across various projects.

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
