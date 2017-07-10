*Please email us ([Evolgenius Team](mailto:evolgenius.team@gmail.com)) if you have any questions; attach your datasets and trees if necessary.*

## Leaf label decorations

### Table of contents
* [overview](#overview)
* [modifiers](#modifiers)
* [examples](#examples)
* [add leaf label decoration to collapsed trees](#add-leaf-label-decoration-to-collapsed-trees)

{anchor:overview}
### Overview
Leaf decorations are colour objects / shapes to be shown between the leaf node labels and branches:

![](images/DatasetLeafLabelDeco_leafdeco_example.png)

The tree:

```
(A:0.1,(B:0.2,(C:0.3,D:0.4)100:0.05)100:0.1)90:0.43;
```

the dataset:

```
!defaultstrokewidth	0.7
A	triangle,red:red
B	triangle,white:red
C	triangle,white:green
D	triangle,green:green
```

A decoration shape can be written as :

```
shape,fill_color[:stroke_color](_stroke_color)
```

**_Note_**
1. a leaf label can have multiple decoration shapes, but only one decoration dataset can be shown at a time
2. leaf labels can have different numbers of colour shapes; see more examples bellow.
Here is an annotated example of the dataset:

![](images/DatasetLeafLabelDeco_leafdeco_dataset_explained.png)

**_Supported color shapes_**
1. triangle
2. circle
3. rect
4. star
5. check

{anchor:modifiers}
### Supported modifiers

```
!defaultstrokewidth	0.7
```

{anchor:examples}
### Examples

Example 1:

```
!defaultstrokewidth	0.7
A	star,red
B	rect,red	check,green
C	star,white:red	triangle,white:green
D	circle,white:green
```

![](images/DatasetLeafLabelDeco_leafdeco_example1.png)

{anchor:add leaf label decoration to collapsed trees}
### Add leaf label decoration to collapsed trees
Evolview supports collapsing at internal nodes; collapsed nodes are treated as leaf nodes. It is therefore very straightforward to add leaf label decorations to a collapsed tree. See [here](/datasets/13_collapse_at_internal_nodes/DatasetCollapseInternalNodes.md) for more information.


[<< previous section: leaf background color](/datasets/05_leaf/DatasetLeafBKColor.md)      |       [next section: strip and shape >>](/datasets/06_strip_and_shape/DatasetColorStripShape.md)
