# Windows-Sidebar
A Windows sidebar that can be used independently. It is recommended to use it with [SegumiOS](https://github.com/sedoruee/SegumiOS).
# Plugin Creation Guide
**Goal:** Embed a Tkinter application within the sidebar.
Place plugin files in the `plugins` folder.
**Plugin Code Example** (`plugins/your_plugin_name.py`):
```python
import tkinter as tk
def run(sidebar, frame):
    app = tk.Frame(frame)
    app.pack(fill=tk.BOTH, expand=True)
    # Build your Tkinter application within 'app'
    # ...
```
**Key Function:**
*   `run(sidebar, frame)`: The plugin's entry point. `sidebar` is the `Sidebar` object, and `frame` is the `tk.Frame` container.
*   Create a `tk.Frame` (e.g., `app`) inside `frame` to serve as the root of your application.
*   `app.pack(fill=tk.BOTH, expand=True)` ensures the application fills the available space.
*   All widgets should be added to `app`.
