# Windows-Sidebar
一个windows侧边栏,可以独立使用,推荐搭配[SegumiOS](https://github.com/sedoruee/SegumiOS)使用.
# 插件创建说明书
目标: 将 Tkinter 应用嵌入侧边栏。
插件文件放置于 `plugins` 文件夹。
插件代码示例 ( `plugins/你的插件.py`):
```python
import tkinter as tk
def run(sidebar, frame):
    app = tk.Frame(frame)
    app.pack(fill=tk.BOTH, expand=True)
    # 在 app 中构建你的 Tkinter 应用
    # ...
```
关键函数:
   `run(sidebar, frame)`: 插件入口,`sidebar` 为 `Sidebar` 对象, `frame` 为 `tk.Frame` 容器。
   在 `frame` 内创建 `tk.Frame` (例如 `app`) 作为你应用的根。
   `app.pack(fill=tk.BOTH, expand=True)` 确保应用填充可用空间。
   所有控件应添加到 `app` 中。
`sidebar` 对象:**
避免使用 `tk.Toplevel`。
注意焦点的处理
