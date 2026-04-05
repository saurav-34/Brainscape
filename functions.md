# Brain Map Code Map

This file maps key parts of `index.html` to line numbers for quick navigation.

## Top-Level Sections

| Section | Starts At |
|---|---:|
| CONSTANTS | 372 |
| IMAGE STORE | 397 |
| STATE | 459 |
| COORDINATE UTILS | 499 |
| NODE ANCHORS | 554 |
| EDGE ENDPOINTS | 605 |
| SVG HELPERS | 622 |
| HISTORY | 662 |
| MULTI-MAP | 700 |
| PERSISTENCE | 840 |
| RENDERER | 899 |
| CRUD HELPERS | 1152 |
| TEXT EDITOR | 1240 |
| CONTEXT MENU | 1382 |
| TOOL MANAGEMENT | 1402 |
| MOUSE EVENTS | 1426 |
| KEYBOARD | 1866 |
| CLIPBOARD PASTE | 1976 |
| TOOLBAR BUILDER | 2018 |
| INIT | 2233 |

## Image Store (IndexedDB)

| Item / Function | Line |
|---|---:|
| `imageCache` Map | 398 |
| `_openImageDB()` | 401 |
| `_loadAllImages()` | 410 |
| `storeImage(imageId, dataUrl)` | 419 |
| `deleteImage(imageId)` | 425 |
| `generateImageId()` | 431 |
| `migrateImageNodes()` | 436 |

## State And Core IDs

| Item | Line |
|---|---:|
| `uid()` | 472 |
| `mapUid()` | 478 |
| `currentMap()` | 479 |
| `_nodeRenderCache` Map | 470 |
| `_edgeRenderCache` Map | 471 |
| `canvas` ref | 500 |
| `layerNodesEl` ref | 501 |
| `layerEdgesEl` ref | 502 |
| `layerOverlayEl` ref | 503 |
| `vpEl` ref | 504 |
| `dotPatternEl` ref | 505 |
| `dotPatternCircleEl` ref | 506 |
| `sbToolEl` ref | 507 |
| `sbZoomEl` ref | 508 |
| `sbSelEl` ref | 509 |

## Utility Functions

| Function | Line |
|---|---:|
| `deepClone(value)` | 511 |
| `getBackgroundThemeById(themeId)` | 515 |
| `applyBackgroundTheme(themeId, skipSave=false)` | 519 |
| `svgRect()` | 529 |
| `screenToWorld(sx, sy)` | 531 |
| `worldToScreen(wx, wy)` | 534 |
| `eventToScreen(e)` | 537 |
| `eventToWorld(e)` | 541 |
| `viewCenter()` | 547 |
| `nodeAnchors(node)` | 555 |
| `anchorPos(nodeId, anchor)` | 569 |
| `nearestAnchor(node, wx, wy)` | 575 |
| `findSnapAnchor(sx, sy, excludeNodeId)` | 586 |
| `resolveEdge(edge)` | 606 |
| `defaultCurveCP(x1, y1, x2, y2)` | 613 |
| `el(tag, attrs={})` | 623 |
| `setAttrs(e, attrs)` | 629 |
| `isLightHexColor(color)` | 633 |
| `labelColorForNode(node)` | 646 |
| `hintColorForNode(node)` | 651 |
| `borderColorForNode(node)` | 656 |

## History And Persistence

| Function | Line |
|---|---:|
| `snapshot()` | 663 |
| `pushHistory()` | 667 |
| `applySnapshot(s)` | 673 |
| `undo()` | 686 |
| `redo()` | 692 |
| `scheduleSave()` | 842 |
| `loadFromStorage()` | 850 |

## Multi-Map Management

| Function | Line |
|---|---:|
| `saveCurrentMap()` | 701 |
| `loadMapData(m)` | 709 |
| `switchMap(id)` | 734 |
| `addMap(name)` | 745 |
| `deleteMap(id)` | 762 |
| `renameMap(id, name)` | 777 |
| `renderTabs()` | 782 |
| `startRenameTab(mapId, nameSpan)` | 821 |

## Rendering And Data Mutation

| Function | Line |
|---|---:|
| `renderNode(node)` | 901 |
| `renderEdge(edge)` | 1019 |
| `updateViewport()` | 1070 |
| `updateStatusBar()` | 1083 |
| `render()` | 1091 |
| `buildSelectionDragSnapshot()` | 1133 |
| `addNode(type, x, y, w, h, extra={})` | 1153 |
| `addEdge(type, x1, y1, x2, y2, fromId, fromAnchor, toId, toAnchor)` | 1163 |
| `deleteSelected()` | 1171 |
| `duplicateSelected()` | 1202 |
| `bringToFront()` | 1222 |
| `sendToBack()` | 1230 |

## Text Editing

| Function / Item | Line |
|---|---:|
| `textEditor` ref | 1241 |
| `textWrap` ref | 1242 |
| `openTextEditor(node)` | 1245 |
| `closeTextEditor(commit=true)` | 1273 |
| Text editor keydown/paste/input handlers | 1358 |

## Context Menu And Tooling

| Function / Item | Line |
|---|---:|
| `ctxMenu` ref | 1383 |
| `showCtxMenu(cx, cy)` | 1385 |
| `hideCtxMenu()` | 1393 |
| `setTool(t)` | 1403 |
| `setFill(color)` | 1412 |

## Interaction Event Handlers

| Handler / Function | Line |
|---|---:|
| `canvas.pointerdown` (main interaction router) | 1427 |
| `_startEdgePreview(x1, y1, x2, y2)` | 1571 |
| `canvas.pointermove` | 1578 |
| `canvas.pointerup` | 1716 |
| `canvas.dblclick` | 1803 |
| `canvas.contextmenu` | 1824 |
| `zoomAtScreenPoint(sx, sy, factor)` | 1847 |
| `canvas.wheel` | 1858 |
| `document.keydown` | 1867 |
| `fitView()` | 1928 |
| `scaleImageToCanvasBounds(width, height, maxW, maxH)` | 1944 |
| `placeImageNodeFromDataUrl(dataUrl, center, options={})` | 1952 |
| `document.paste` | 1977 |
| `document.mousedown` (close context menu) | 2013 |
| `buildPalette()` | 2019 |
| `buildBackgroundPalette()` | 2035 |
| `tool-export` click handler | 2057 |
| `tool-import` click handler | 2096 |
| `canvas.pointerdown` (image tool loader, capture=true) | 2193 |

## Startup Flow

| Step | Line |
|---|---:|
| `async` IIFE start | 2234 |
| `_openImageDB()` + `_loadAllImages()` | 2237 |
| `buildPalette()` call | 2243 |
| `buildBackgroundPalette()` call | 2244 |
| `setTool('select')` call | 2245 |
| `loadFromStorage()` + welcome bootstrap fallback | 2247 |
| `migrateImageNodes()` call | 2276 |
| `renderTabs()` | 2278 |
| `pushHistory()` | 2279 |
| `render()` | 2280 |
| `canvas.focus()` | 2281 |
