
Go through - https://flexiple.com/css/css-position-properties-cheat-sheet

Youtube Resource - WebDevSimplified,  Learn CSS Position In 9 Minutes


Understanding Z-Index in CSS - 

Z-Index is a CSS property used to specify the stacking order of elements that overlap. It determines which element appears on top of others when they are positioned on top of each other.

How it works:

- Elements with a higher z-index value will appear on top of elements with a lower z-index value.
- Elements with the same z-index value are stacked in the order they appear in the HTML document.
- The default z-index value is 0.

Example - 

<!DOCTYPE html>
<html>
<head>
  <title>Z-Index Example</title>
  <style>
    .container {
      position: relative;
      width: 300px;
      height: 300px;
      border: 1px solid black;
    }

    .box {
      position: absolute;
      width: 100px;
      height: 100px;
      background-color: blue;
    }

    .box1 {
      z-index: 1;
    }

    .box2 {
      z-index: 2;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="box box1">Box 1</div>
    <div class="box box2">Box 2</div>
  </div>
</body>
</html>


Explanation: -

1 .container: This element sets up the relative positioning for the boxes.
2.box: Both .box1 and .box2 are absolutely positioned within the container.
3.box1: This box has a z-index of 1.
4.box2: This box has a z-index of 2.

Result: -

In this example, .box2 will appear on top of .box1 because it has a higher z-index value. If both boxes had the same z-index value, they would be stacked in the order they appear in the HTML (.box1 on top of .box2 in this case).

Key points to remember: -

- Z-index only affects elements that overlap.
- Z-index is not inherited. Each element has its own z-index value.
- Negative z-index values can be used to position elements behind other elements.