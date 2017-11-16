## Flexbox

There is container and children(direct child)

There are two axes: main axis and cross axis which depends on the direction.


To use flex system, **display** property of parent container must be set to *flex*

``` css
  .parent-container {
    display: flex;
  }
```

Children can be laid out either in row or column determined by the property **flex-direction** which can bet set to *row*, *column*, *row-reverse*, or *column-reverse*


``` css
  .parent-container {
    display: flex;
    flex-direction: row;
  }
```

The child can be wrapped into next row or column using **flex-wrap** property which can be set to : *wrap*, *wrap-reverse*, or *nowrap* 


``` css
  .parent-container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
  }
```

Instead of setting flex-direction and flex-wrap separately, one can use **flex-flow** to set both things at once

``` css
  .parent-container {
    display: flex;
    flex-flow: row wrap;
  }
```

The arrangement of items in the main-axis(flex-direction) is determined by the property **justify-content** which can be set to *space-between*, *space-around*, *flex-start*, *flex-end*, or *center*

``` css
  .parent-container {
    display: flex;
    flex-flow: row wrap;
    justify-content: space-around;
  }
```

The alignment of items in cross axis(not flex-direction) is determed by the property **align-items** which can be set to *flex-start*, *flex-end*, *center*, *stretch*, or *baseline*

``` css
  .parent-container {
    display: flex;
    flex-flow: row wrap;
    justify-content: space-around;
    align-items: center;
  }
```
The spacing of elements in cross-axis is determined by the property **align-content** which can be set to values used for justify-content.
``` css
  .parent-container {
    display: flex;
    flex-flow: row wrap;
    justify-content: space-around;
    align-items: center;
    align-content: center;
  }
```

The order of children in flex container can be altered individually with **order** property which takes an integer

``` css
  .child {
    order : -1;
  }
```

Also, individual child can be aligned using **align-self** property which takes same values as align-items

``` css
  .child {
    order : -1;
    align-self: flex-end;
  }
```
Instead of setting the width of child element, we set property called **flex-basis** in flex system. 

``` css
  .child {
    order : -1;
    align-self: flex-end;
    flex-basis: 50%;
  }
```
## Grid

Flex is a 1-D (either row or column) layout system. It is usually used in UI elements in a page. For the entire layout of the main site or complex layout within UI component , grid proves to be more powerful. Grid is a 2D layout system (rows and columns).

Similar to flex, it also have concept of parent(wrapper) and children.

To use grid system, **display** property must be set to grid.

``` css
  .parent-container {
    display: grid;
  }
```
Spacing between blocks inside grid is set using **grid-gap** property

``` css
  .parent-container {
    display: grid;
    grid-gap: 2%;
  }
```

CSS for children contains the position for row and columns specified by property **grid-row** and **grid-column** which takes value in form of *startline/endline*
  
*line numbering starts from the left of box in 1st row 1st column i.e no. of gap to the left of that box is 1*

``` css
  .r1c1 {
    grid-row: 1/2;
    grid-column: 1/2;
  }
  
  r2c2 {
    grid-row: 1/2;
    grid-column: 2/3;
  }
```

Instead of separately specifying rows and column separately, they can be specified at once using **grid-area** which takes value in the format *startrow/startcolumn/endrow/endcolumn*

``` css
  .r1c1 {
    grid-area: 1/1/2/2;
  }
  
  r2c2 {
    grid-area:: 1/2/2/3;
  }
  ```
  
Also, **order** property can be used for grid items in a similar way it was used for flexbox items.

Size (width and height) of boxes in the grid can be specified explicity or implicity using **grid-template-columns** and **grid-template-rows** properties. Excpicit units includes px, %, em, rem . Implicit value follows a format xfr where fr refers to fraction and x is number. Both explicit and explicit values can used together by separating them with space.

Also, there is something called repeat(x,y) which repeats y x times.

```css
  parent-container {
    grid-template-columns: 50px 1fr 1fr 1fr;
    grid-template-rows: repeat(5, auto);
  }
```

Above two properties can be combined into one with **grid-template** which takes value in format  *grid-template-rows / grid-template-columns*
```css
  parent-container {
    grid-template: 50px 1fr 1fr 1fr / repeat(5, auto) ;
  }
```
## Lab

To get real sense of above commands play, with these sites:

[Flexbox Froggy](https://flexboxfroggy.com/)
[Grid Garden](https://flexboxfroggy.com/)
