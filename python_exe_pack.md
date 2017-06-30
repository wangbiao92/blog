## exe打包工具
1. **Py2exe**（不再更新）
2. **pyinstaller**（推荐）
---

- 安装pyinstaller(pip的话目前只试用3.5及以前版本)
```
pip install pyinstaller
```

- 打包exe文件<br>
1、打开cmd，指定到要打包的文件路径<br>
2、
```
pyinstaller -F xx.py
```
3、完成→ 报错（python版本问题报错）
```
IndexError: tuple index out of range
```
解决：
1.安装3.5级以下版本
或
2.https://github.com/pyinstaller/pyinstaller 把PyInstaller提出来。删掉python/Lib/site-packages/PyInstaller 文件夹，把解压得到的PyInstaller放进去应该就OK了