# Docusaurus MDX Previewer

A VSCode extension to preview Docusaurus MDX files with real-time rendering, including support for PlantUML and Mermaid diagrams.

![](./assets/mdx_preview.gif)

## Features

- **Live Preview**: Preview your Docusaurus MDX files in a single, reusable Webview panel.
- **Theme Support**: Automatically follows VS Code's color theme (light/dark) with manual override option.
- **Diagram Support**: Render PlantUML and Mermaid diagrams using an external server (default: `https://kroki.io`).
- **Docusaurus Styling**: Applies Docusaurus styling consistent with your theme preference.
- **Real-time Updates**: Automatically updates the preview when switching between MDX files, editing content, or changing themes.
- **Code Highlighting**: Syntax highlighting for code blocks using `rehype-highlight`.

## Future works

- Support `import` syntax.

## Installation

1. **Install from VSIX**:
   - Download the `.vsix` file from the release section or shared source.
   - In VSCode, go to Extensions view (`Ctrl+Shift+X` or `Cmd+Shift+X` on Mac), click the `...` menu, and select "Install from VSIX".
   - Choose the downloaded `.vsix` file.

2. **Install from Marketplace**:
   - Search for "Docusaurus MDX Previewer" in the VSCode Marketplace and click "Install".

## Usage

1. Open an MDX or Markdown file in VSCode.
2. Run the command `Show Docusaurus MDX Preview`:
   - Press `ctrl+alt+p` (or `cmd+alt+p` on Mac) to open the Command Palette.
   - Type and select `Show Docusaurus MDX Preview`.
3. The preview will appear in a panel beside your editor, updating automatically as you edit or switch files.

## Configuration

You can customize the extension behavior in VSCode settings:

### Theme Mode
- Open Settings (`Ctrl+,` or `Cmd+,`).
- Search for `docusaurusMdxPreview.theme`.
- Choose from three options:
  - `auto` (default): Automatically follows VS Code's color theme
  - `light`: Always use light theme
  - `dark`: Always use dark theme

### Diagram Server
- Search for `docusaurusMdxPreview.plantumlServer`.
- Set a custom URL (default is `https://kroki.io`).

### Refresh Interval
- Search for `docusaurusMdxPreview.refreshInterval`.
- Set the preview refresh interval in milliseconds (default is `500`).

Example configuration:
```json
{
  "docusaurusMdxPreview.theme": "auto",
  "docusaurusMdxPreview.plantumlServer": "https://kroki.io",
  "docusaurusMdxPreview.refreshInterval": 500
}
