# IEEEBadgeWriter

> A Windows desktop application that **automates badge generation** by writing names (or any text) onto a template image — built for IEEE events and similar use cases.

> 🍴 This is a fork of the original project by [XTigerHyperX](https://github.com/XTigerHyperX/IEEEBadgeWriter-Public).

---

## ✨ Features

- Load any image as a badge template (PNG, JPG, etc.)
- Batch-process a `.txt` file of names — one badge per line
- Drag-and-drop text placement on the template preview
- Custom font support via `.ttf` files
- Font size adjustment (increase / decrease) with live preview
- Black or White text color selection
- Outputs individual badge images to a chosen folder

---

## 🖥️ Requirements

| Requirement | Details |
|---|---|
| OS | Windows 10 / 11 |
| Runtime | [.NET 8 Desktop Runtime (x64)](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-desktop-8.0.4-windows-x64-installer) |

> ⚠️ You **must** install the .NET 8 runtime before launching the application.

---

## 📦 Installation

1. Download the latest release from the [Releases](../../releases) page.
2. Install the [.NET 8 Desktop Runtime](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-desktop-8.0.4-windows-x64-installer) if not already installed.
3. Extract the ZIP archive.
4. Run `IEEEBadgeWriter.exe`.

---

## 📖 Manual — How to Use

### Step 1 — Load a Template Image

Click **"Load Template"** and select your badge background image (`.png`, `.jpg`, etc.).  
The image will be displayed in the preview panel on the right.

### Step 2 — Load a Names File

Click **"Load Text"** and select a `.txt` file containing the names to print.  
Each name must be on its own line:

```
Alice Johnson
Bob Smith
Carol White
```

The button label will update to confirm how many names were loaded (e.g. `Loaded 3 Names`).

### Step 3 — Select an Output Folder

Click **"Output"** and choose the folder where the generated badge images will be saved.

### Step 4 — Load a Custom Font *(optional)*

Click the font button and select a `.ttf` font file.  
The preview label will immediately update to display your chosen font.

### Step 5 — Position the Text

- Type a **sample name** in the sample text box to preview how text will look.
- **Drag** the label directly on the preview image to position it exactly where you want the name to appear on the badge.

### Step 6 — Adjust Font Size & Color

- Use the **`+`** and **`-`** buttons to increase or decrease the font size.
- Select **Black** or **White** for the text color using the color buttons.

### Step 7 — Generate Badges

Click **"Generate"** to start the batch process.  
The application will create one output image per name from your `.txt` file, saved in your chosen output folder. Each file will be named after the corresponding line entry.

---

## 📁 Project Structure

```
IEEEBadgeWriter/
├── IEEEBadgeWriter.sln        # Visual Studio solution
└── IEEEBadgeWriter/
    ├── Program.cs             # Application entry point
    ├── Form1.cs               # Splash / main entry form
    ├── Form2.cs               # Core badge editor UI logic
    ├── Form2.Designer.cs      # Auto-generated UI layout
    ├── Designer.cs            # Image drawing & name loading logic
    ├── Resources/             # Embedded resources (icons, assets)
    └── Properties/            # Assembly metadata
```

---

## 🛠️ Building from Source

1. Clone the repository:
   ```bash
   git clone https://github.com/Bechir-afk/IEEEBadgeWriter.git
   ```
2. Open `IEEEBadgeWriter.sln` in **Visual Studio 2022+**.
3. Restore NuGet packages (if any).
4. Build and run with `F5`.

---

## ⚠️ Known Issues

- This is a **first release** — expect some bugs.
- Very large `.txt` files (thousands of names) may cause slowdowns as each badge is processed on a separate thread.
- Text positioning is calibrated to the preview scale; minor pixel offsets may occur at extreme template resolutions.

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

---

## 👤 Credits

**Original Author:** [XTigerHyperX](https://github.com/XTigerHyperX) — [Original Repository](https://github.com/XTigerHyperX/IEEEBadgeWriter-Public)  
**Fork Maintainer:** [Bechir Ben Rabia](https://github.com/Bechir-afk)

---

## 📄 License

This project is open source. See [LICENSE](LICENSE) for details.
