# MelScriptCollection
utility script on Autodesk Maya

# How to use
 - copy script and run in script editor
 - add script to shelf and run by click on shelf https://knowledge.autodesk.com/support/maya/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/Maya-Customizing/files/GUID-58C25080-5864-4709-BE3A-0543E9D1FCF2-htm.html
 - add script to runtine command and run by keyboard shortcut https://knowledge.autodesk.com/support/maya/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/Maya-KeyboardShortcuts/files/GUID-36D24C0F-19E4-411E-8CA9-DB7B64C3E6EA-htm.html

## scale all staff to x plane
useful for modeling mirror on x-plane  
my shortcut: PolyModeling Shelf
```
scale -r -p 0 0 0 0 1 1 ;
```

## Viewport script
### Toggle X-Ray
toggle x-ray in current viewport  
my shortcut: alt + 1
```
if (`getPanel -to (eval("getPanel -withFocus"))` == "modelPanel") { 
	$currentPanel = `getPanel -withFocus`;
	if (`modelEditor -q -xray $currentPanel`) { 
		modelEditor -edit -xray 0 $currentPanel; 
	} else { 
		modelEditor -edit -xray 1 $currentPanel;
	}
}
```

### Toggle Wireframe on shade
toggle wireframe on shade in current viewport  
my shortcut: alt + 2
```
if (`getPanel -to (eval("getPanel -withFocus"))` == "modelPanel") { 
	$currentPanel = `getPanel -withFocus`;
	if (`modelEditor -q -wos $currentPanel`) { 
		modelEditor -edit -wos 0 $currentPanel; 
	} else { 
		modelEditor -edit -wos 1 $currentPanel;
	}
}
```
