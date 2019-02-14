# MelScriptCollection
utility script on Autodesk Maya

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
