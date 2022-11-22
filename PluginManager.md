## Plug-in Manager

![Plug-in Manager](./images/PluginManager.png)

```python
# load
cmds.loadPlugin('fbxmaya.mll', qt=True)

# unload
cmds.unloadPlugin('fbxmaya.mll', f=True)

# auto load
cmds.pluginInfo('fbxmaya.mll', e=True, autoload=True)
```

## command references
* [loadPlugin](https://help.autodesk.com/cloudhelp/2023/ENU/Maya-Tech-Docs/CommandsPython/loadPlugin.html)
* [unloadPlugin](https://help.autodesk.com/cloudhelp/2023/ENU/Maya-Tech-Docs/CommandsPython/unloadPlugin.html)
* [pluginInfo](https://help.autodesk.com/cloudhelp/2023/ENU/Maya-Tech-Docs/CommandsPython/pluginInfo.html)