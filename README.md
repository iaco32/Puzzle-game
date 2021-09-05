
# WAGAWIN Puzzle Game

A javascript jigsaw puzzle game utilizing HTML5 Drag and Drop API.


## Javascript Avaialbe Options

| Property 	| Description 	| Default 	|
| --------- | ------------- | --------- |
| **el**	| Container element which will hold the puzzle. _This option **MUST** be passed a valid HTML element_ | null |
| **image**	| URL for the image to be used. Must be a valid src value for the <[img](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img#Supported_image_formats)> tag | :) |
| **numcolumns** | Number of columns in the puzzle grid | 4 |
| **numrows** | Number of rows in the puzzle grid | 3 |


## Methods

### Init
_Usage:_
```
init()
```

Initialize puzzle instance and attach to container element.

**returns** puzzle instance.

### setOpts
_Usage:_
```
setOpts( Object[ {options} ] )
```

Redeclare options on current puzzle.

**returns** puzzle instance.

### setGridSize
_Usage:_
```
setGridSize( Object[ { [numrows, numcolumns] } ])
```

Update the number of rows or columns for a puzzle.

**returns** puzzle instance.

### setImage
_Usage:_
```
setImage( String[ image_url ] )
```

Update the puzzle image (_Must be a valid src value for the <[img](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img#Supported_image_formats)> tag_).

**returns** puzzle instance.

### isSorted
_Usage:_
```
isSorted()
```

Check to see if the puzzle is completed.

**returns** true or false.

### getTiles
_Usage:_
```
getTiles()
```

Grabs the current order of tiles in the puzzle.

**returns** multi-dimensional array of tiles, the first item is the original position of the tile and the second is the tile itself.

### correctTiles
_Usage:_
```
correctTiles()
```

Counts the number of tiles in order and returns that number.

**returns** number value of correct tiles.

## Callbacks

These events are exposed through the settings and accept callback functions:

* __dragstart__ - Fires when a tile is first dragged.
* __dragenter__ - Fires when a tile enters a dropzone.
* __drag__ - Fires while a tile is currently being dragged.
* __dragover__ - Fires while a tile is dragged over a dropzone.
* __dragleave__ - Fires when a tile is exits a dropzone.
* __dragend__ - Fires when a tile is no longer being dragged.
* __drop__ - Fires when a tile is dropped.
* __touchstart__ - Fires when a tile is touched.
* __touchmove__ - Fires while a tile is dragged over the document.
* __touchhover__ - Fires while a tile is dragged over a dropzone.
* __touchend__ - Fires when a tile is no longer being dragged.
* __correct__ - Fires when a tile is dropped into the correct slot.
* __finished__ - Fires when the entire puzzle is completed.