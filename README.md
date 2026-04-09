## Installation

This plugin requires both a CEP panel (UI) and a native plugin.  
Because the native plugin is not code-signed yet, macOS will block it by default.

---

### Step 1 — Install the UI (CEP Panel)

Copy the `AudioControls` folder to:

```
/Library/Application Support/Adobe/CEP/extensions/
```

---

### Step 2 — Install the Native Plugin

Copy `Panelator.plugin` to:

```
/Library/Application Support/Adobe/Common/Plug-ins/7.0/MediaCore/
```

---

### Step 3 — Remove macOS Quarantine

macOS will block unsigned plugins.  
Run the following command to allow After Effects to load it:

```bash
xattr -dr com.apple.quarantine /Library/Application\ Support/Adobe/Common/Plug-ins/7.0/MediaCore/Panelator.plugin
```

Alternatively:
- Right-click `Panelator.plugin`
- Open Terminal in that folder
- Run:

```bash
xattr -dr com.apple.quarantine .
```

---

### Step 4 — Launch After Effects

Open After Effects and find the panel under:

```
Window → Extensions → AudioControls
```

---

## Notes

- The plugin is currently **not code-signed**, so macOS will quarantine it automatically after download.
- Removing the quarantine flag is required for it to work.
- Both components are required:
  - `AudioControls` → UI (CEP Panel)
  - `Panelator.plugin` → Native functionality
