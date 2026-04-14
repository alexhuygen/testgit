# Notes - Interactive 3D Markdown Note Manager

A modern, web-based note management system with an interactive 3D spherical mindmap visualization. Organize, tag, and visualize your markdown notes in an intuitive and visually engaging way.

## Features

### 📝 Markdown Editor
- Full-featured markdown editor with live preview
- Support for syntax highlighting and formatting
- Split view mode for simultaneous editing and preview
- Auto-save functionality with dirty state tracking
- Image insertion with automatic IMG folder management

### 🌐 3D Spherical Mindmap
- Interactive 3D visualization of your note structure
- Spherical distribution of nodes for optimal space usage
- Real-time filtering and camera focus
- Smooth camera animations and transitions
- Keyboard controls for navigation (W/A/S/D for rotation, +/- for zoom)
- Mouse drag for orbital camera movement

### 🏷️ Tag System
- Frontmatter-based tag management in markdown files
- Tag cloud visualization with frequency-based sizing
- Multi-tag filtering with visual feedback
- Tag-based camera focus on the mindmap

### 📁 Folder Organization
- Hierarchical folder structure support
- Drag-and-drop file movement between folders
- Automatic IMG folder creation for image assets
- Right-click folder selection for focused viewing

### 🖼️ Image Management
- Embed images directly in markdown files
- Automatic IMG folder creation per markdown file
- Support for PNG, JPG, JPEG, GIF, WebP, and SVG formats
- Markdown syntax: `![alt text](IMG_filename/image.png)`

### 🎨 User Interface
- Light and dark mode themes
- Responsive design with resizable panels
- Intuitive sidebar with file tree and tag cloud
- Real-time status updates and notifications
- Keyboard shortcuts (Ctrl+S for save)

## Interaction Guide

### Mindmap Navigation
- **Left-click file**: Open markdown file
- **Double-click file**: Filter mindmap by file's tags
- **Right-click folder**: Select folder and focus camera
- **Drag**: Orbit the camera around the center
- **Scroll**: Zoom in/out
- **W/A/S/D**: Rotate and tilt the view
- **+/-**: Adjust zoom level

### Tag Filtering
- Click tags in the tag cloud to filter files
- Multiple tags can be selected simultaneously
- Camera automatically focuses on filtered content
- "Clear" button resets all filters

### File Management
- Create new markdown files
- Rename files with inline modal
- Move files between folders via drag-and-drop or menu
- Delete files with confirmation
- Insert images with automatic folder management

## Getting Started

### Prerequisites
- Modern web browser with File System Access API support (Chrome, Edge, Opera)
- Local folder with markdown files

### Usage
1. Open `notes.html` in your web browser
2. Click the 📂 button to select a folder containing markdown files
3. Files and folders will be automatically scanned and displayed
4. Start exploring your notes with the 3D mindmap!

### Folder Structure
```
your-notes-folder/
├── notes.md
├── another-file.md
├── IMG/
│   ├── image1.png
│   ├── image2.jpg
│   └── diagram.png
└── subfolder/
    ├── document.md
    ├── research.md
    └── IMG/
        ├── chart.png
        └── screenshot.jpg
```

## Markdown Image Syntax

Images are stored in an `IMG` folder within each directory. Reference them using:

```markdown
![alt text](IMG/image.png)
![diagram](IMG/diagram.jpg)
![screenshot](IMG/screenshot.png)
```

All images in the same folder share the same `IMG` directory, making it easy to organize and manage assets.

## Markdown Frontmatter

Add tags to your markdown files using frontmatter:

```markdown
---
tags: [project, important, review]
---

# My Note Title

Your content here...
```

## Features in Detail

### 3D Mindmap Visualization
- **Root Node**: Transparent center point (invisible)
- **Folder Nodes**: Green spheres representing directories
- **File Nodes**: Purple spheres representing markdown files
- **Active File**: Pink highlight for currently open file
- **Connection Lines**: Subtle gray lines showing relationships

### Camera Focus
- Automatically centers on filtered content
- Adjusts zoom based on extent of visible nodes
- Smooth transitions between focus points
- Maintains viewing angle during focus changes

### Image Support
- Insert images via the 🖼️ button in toolbar
- Images stored in `IMG` folder within each directory
- Automatic markdown syntax generation
- Preview images in split/preview modes

### Tag Management
- Add tags via the tag input field (press Enter)
- Remove tags by clicking the ✕ on tag pills
- Tags persist in markdown frontmatter
- Refresh tags with 🔄 button to reload from files

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| Ctrl+S | Save current file |
| W/S | Tilt mindmap view |
| A/D | Rotate mindmap view |
| +/- | Zoom in/out |
| Double-click | Filter by file tags |
| Right-click | Select folder |

## Browser Compatibility

- ✅ Chrome/Chromium 86+
- ✅ Edge 86+
- ✅ Opera 72+
- ❌ Firefox (File System Access API not supported)
- ❌ Safari (File System Access API not supported)

## Technical Stack

- **Frontend**: Vanilla JavaScript (ES6+)
- **3D Graphics**: Three.js
- **Markdown Parsing**: Marked.js
- **File System**: File System Access API
- **Styling**: CSS3 with CSS Variables

## Color Scheme

### Dark Mode
- Background: `#1e1e2e`
- Text: `#cdd6f4`
- Accent: `#89b4fa` (Blue)
- Folders: `#a6e3a1` (Green)
- Files: `#cba6f7` (Purple)

### Light Mode
- Background: `#eff1f5`
- Text: `#4c4f69`
- Accent: `#1e66f5` (Blue)
- Folders: `#40a02b` (Green)
- Files: `#8839ef` (Purple)

## Tips & Tricks

1. **Organize by Tags**: Use consistent tag naming for better filtering
2. **Use Folders**: Group related notes in folders for cleaner structure
3. **Image Management**: Keep images in the auto-generated IMG folders
4. **Camera Focus**: Double-click files to quickly focus on related content
5. **Keyboard Navigation**: Use W/A/S/D for hands-free mindmap exploration

## Limitations

- Requires modern browser with File System Access API
- Works with local folders only (no cloud sync)
- Single-user application (no collaboration features)
- Maximum practical file count depends on browser performance

## Future Enhancements

- [ ] Cloud storage integration (Google Drive, Dropbox)
- [ ] Collaborative editing
- [ ] Search functionality
- [ ] Export to PDF/HTML
- [ ] Custom color themes
- [ ] Plugin system
- [ ] Mobile app version

## License

MIT License - Feel free to use and modify for your needs.

## Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for bugs and feature requests.

## Author

Created with ❤️ for better note organization and visualization.

---

**Version**: 1.0.0  
**Last Updated**: 2026  
**Status**: Active Development
