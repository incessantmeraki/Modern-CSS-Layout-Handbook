## Flexbox

- There is container and children(direct child)
- There are two axes: main axis and cross axis which depends on the direction.


To use flex system, display property of parent container must be set to **flex**

``` css
  .parent-container {
    display: flex;
  }
```

Children can be laid out either in row or column determined by the property flex-direction which can bet set to **row**, **column**, **row-reverse**, or **column-reverse**


``` css
  .parent-container {
    display: flex;
    flex-direction: row;
  }
```

The child can be wrapped into next row or column using flex-wrap property which can be set to : **wrap**, **wrap-reverse**, or **nowrap** 


``` css
  .parent-container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
  }
```

Instead of setting flex-direction and flex-wrap separately, one can use flex-flow to set both things at once

``` css
  .parent-container {
    display: flex;
    flex-flow: row wrap;
  }
```

The alignment of items in the main-axis(flex-direction) is determined by the property justify-content which can be set to **space-between**, **space-around**, **flex-start**, **flex-end**, or **center**

``` css
  .parent-container {
    display: flex;
    flex-flow: row wrap;
    justify-content: space-around;
  }
```

The alignment of items in cross axis(not flex-direction) is determed by the property align-items which can be set to **flex-start**, **flex-end**, **center**, **stretch**, or **baseline**

``` css
  .parent-container {
    display: flex;
    flex-flow: row wrap;
    justify-content: space-around;
    align-items: center;
  }
```

The order of children in flex container can be altered individually with order property which takes an integer

``` css
  .child {
    order : -1;
  }
```

Also, individual child can be aligned using align-self property which takes same values as align-items

``` css
  .child {
    order : -1;
    align-self: flex-end;
  }
```
Instead of setting the width of child element, we set property called flex-basis in flex system. 

``` css
  .child {
    order : -1;
    align-self: flex-end;
    flex-basis: 50%;
  }
```
