# graphics

v.0.0.1

A collection of scripts for making diagrams and graphics. Most scripts produce
SVG output which can then be opened in software like Adobe Illustrator for
further editing.

## beer_flavor_wheel

Plot out a beer flavor wheel for further editing. This kind of diagram was first 
developed by M.C. Meilgaard in the 1970's to standardize the descriptive terms
brewers use for beer.

### Usage

```console
$ beer_flavor_wheel > wheel.svg
```

## two_by_two

A script to make attractive 2x2 diagrams. Accepts CSV data as input and
produces a SVG as output.

### Parameters

--x int
  place records horizontally using this field.
--xmin float
  records with this x value will be plotted at the left edge of the diagram.
--xmax float
  records with this x value will be plotted at the right edge of the diagram.
--y int
  place records vertically using this field.
--ymin float
  records with this x value will be plotted at the bottom edge of the diagram.
--ymax float
  records with this x value will be plotted at the top edge of the diagram.

### Example

```console
$ cat nutrition_information.csv | two_by_two --x=24 --y=25 - > two_by_two.svg
```

## venn

Produce proportionate venn diagrams, where the size of each circle and the
amount of overlap between circles accurately represents the amounts in each 
group.
