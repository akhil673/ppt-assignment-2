### Q.1 What’s Box Model in CSS ? 

The CSS box model is a way of representing HTML elements in a rectangular format. It consists of four parts:

1. Content: This is the actual content of the element, such as text, images, or other media.
2. Padding: This is the space between the content and the border. It is transparent, so it does not affect the layout of the element.
3. Border: This is the line that surrounds the content and padding.
4. Margin: This is the space between the border and the rest of the page. It is also transparent, so it does not affect the layout of the element.
The box model is used to control the size and appearance of HTML elements. For example, you can use the padding property to add space around the content of an element, or the border property to add a border around an element.

Here is an example of the CSS box model:

```CSS
div {
  width: 100px;
  height: 100px;
  padding: 10px;
  border: 1px solid black;
  margin: 10px;
}
```

### Q.2 What are the Different Types of Selectors in CSS & what are the advantages of them?
There are five main types of selectors in CSS:

1. Simple selectors: These selectors select elements based on their tag name, id, or class. For example, the selector p will select all p elements on the page.
2. Combinator selectors: These selectors combine simple selectors to select elements based on their relationship to each other. For example, the selector div > p will select all p elements that are direct children of div elements.
3. Pseudo-class selectors: These selectors select elements based on their state or condition. For example, the selector :hover will select all elements that are currently being hovered over by the mouse.
4. Pseudo-element selectors: These selectors select parts of elements. For example, the selector ::before will select the content that is inserted before an element.
5. Attribute selectors: These selectors select elements based on their attributes. For example, the selector [href] will select all elements that have an href attribute.

### Q.3 What is VW/VH ?

VW/VH typically refers to the ratio between the width (VW) and height (VH) of an object or a display. It is commonly used in the context of responsive web design, where the dimensions of elements are specified relative to the viewport size.

The VW unit represents a percentage of the viewport width, while the VH unit represents a percentage of the viewport height. For example, if an element has a width of 50VW, it will occupy 50% of the viewport width. Similarly, if an element has a height of 25VH, it will occupy 25% of the viewport height.

Using VW/VH units allows for fluid and flexible designs that adapt to different screen sizes and resolutions. It helps ensure that elements on a webpage or interface are proportionally sized relative to the available screen space, providing a better user experience across various devices.

### Q.4 Whats difference between Inline, Inline Block and block ?


The main difference between inline, inline-block, and block elements in CSS is how they are displayed in the browser.

Inline elements are displayed on the same line as other inline elements. They do not take up a full line of width, and they do not have any margins or padding by default. Examples of inline elements include <span>, <a>, and <img>.
Inline-block elements are a hybrid of inline and block elements. They are displayed on the same line as other inline elements, but they can also take up a full line of width and have margins and padding. This makes them a good choice for elements that you want to be able to control the width and position of, but you still want them to be displayed inline with other elements.
Block elements are displayed on a new line, and they take up the full width of their container. They have margins and padding by default. Examples of block elements include <div>, <p>, and <ul>.


### Q.5 How is Border-box different from Content Box?

The box-sizing property in CSS defines how the width and height of an element are calculated. The two values of the box-sizing property are content-box and border-box.

1. Content-box is the default value of the box-sizing property. In content-box, the width and height of an element only include the content of the element, not the border or padding. So, if you set an element's width to 100px, that 100px will only include the content of the element, and the border and padding will be added on top of that.
2. Border-box tells the browser to account for any border and padding in the values you specify for an element's width and height. So, if you set an element's width to 100px in border-box, that 100px will include the border and padding, and the content of the element will shrink to fit within that space.

### Q.6 What’s z-index and How does it Function ?
The z-index property in CSS specifies the stack order of an element. An element with a higher z-index value is always in front of an element with a lower z-index value.

The z-index property only works on positioned elements (position: absolute, position: relative, position: fixed, or position: sticky) and flex items (elements that are direct children of display:flex elements).

If two positioned elements overlap without a z-index specified, the element positioned last in the HTML code will be shown on top.

For example, the following code will create two overlapping divs, with the second div being shown on top:
```HTML
<div id="first-div">This is the first div.</div>
<div id="second-div">This is the second div.</div>
```
```CSS
#first-div {
  position: absolute;
  top: 0;
  left: 0;
  width: 100px;
  height: 100px;
  background-color: red;
}

#second-div {
  position: absolute;
  top: 0;
  left: 0;
  width: 100px;
  height: 100px;
  background-color: green;
  z-index: 1;
}
```
### Q.7 What’s Grid & Flex and difference between them?

CSS Grid and Flexbox are two layout models that are used to arrange elements on a web page. They are both powerful tools, but they have different strengths and weaknesses.

CSS Grid is a two-dimensional layout model, which means that it can be used to create layouts that have both rows and columns. This makes it ideal for creating complex layouts, such as those with multiple columns or rows of elements. CSS Grid is also very flexible, and it can be used to create a wide variety of layouts.

Flexbox is a one-dimensional layout model, which means that it can only be used to create layouts that have either rows or columns. This makes it less flexible than CSS Grid, but it is also easier to learn and use. Flexbox is also well-suited for creating layouts with a lot of elements, as it can be used to automatically distribute the elements evenly across the layout.

### Q.8 Difference between absolute and relative and sticky and fixed position explain with example.
here are the differences between absolute, relative, sticky, and fixed positioning in CSS:

Absolute positioning removes an element from the normal flow of the document and positions it absolutely, relative to its closest positioned ancestor. This means that the element will stay in the same position on the page, even if you scroll.
Relative positioning also removes an element from the normal flow of the document, but it positions it relative to its original position. This means that the element will move with the rest of the page when you scroll, but you can still offset it by specifying a top, bottom, left, or right value.
Sticky positioning is a combination of relative and absolute positioning. It positions an element relative to its original position, but it will "stick" to the top of the viewport when you scroll past it. This is a useful technique for creating headers or navigation bars that stay visible at the top of the page as you scroll.
Fixed positioning is similar to absolute positioning, but it positions an element absolutely, relative to the viewport. This means that the element will stay in the same position on the page, even if you scroll or resize the window.