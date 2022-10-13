



```python
# Preferred Renderer
cmds.preferredRenderer('vray')

# Disable colorManagement
cmds.colorManagementPrefs(e=True, cme=False)

# depth peeling
cmds.setAttr('hardwareRenderingGlobals.transparencyAlgorithm', 3)
```


```python
vPanels = cmds.getPanel(visiblePanels=1)
if not vPanels:
    return 
    
for vPanel in vPanels:
    if vPanel.find('modelPanel') == -1:
        continue
            
    cmds.modelEditor(vPanel, e=True, rendererName='vp2Renderer')
    cmds.modelEditor(vPanel, edit=1, displayAppearance='wireframe')
```

```python
cmds.editRenderLayerGlobals( currentRenderLayer = 'defaultRenderLayer' )
```

```Batchfile

set PYTHONDONTWRITEBYTECODE=1
set OCIO=*****.ocio

set MAYA_VERSION=2020
set MAYA_UI_LANGUAGE=en_US

set MAYA_DISABLE_CIP=1
set MAYA_DISABLE_CLIC_IPM=1
set MAYA_DISABLE_CER=1
set MAYA_FORCE_PANEL_FOCUS=1

set MAYA_ENABLE_LEGACY_RENDER_LAYERS=1
set MAYA_ENABLE_LEGACY_VIEWPORT=1

set MAYA_PROJECT=*****

set MAYA_SCRIPT_PATH=
set PYTHONPATH=
set MAYA_PLUG_IN_PATH=
set MAYA_MODULE_PATH=
set XBMLANGPATH=
```