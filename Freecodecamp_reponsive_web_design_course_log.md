



**Applied Accessbility:**

learnt about following topics
- Giving alternative texts for images
- Giving meaningful names for Hyperlinks
- using tags like main,header,article, section, footer to arrange the data in better and more accessible format.
- Importance of choosing high-contrast colors to make pages accessible to color blind users as well.
- Using tabindex and accesskey to make UI elements accessible by keyboard.
- using date picker for letting users to select dates.
- providing accessibily controls for audio.






**Responsive Web Design Principles:**

learnt about following topics
- applying different CSS styles for different device sizes in order to create best experience for all customers.
- Making image responsive.(by uisng max-width: 100% and heigh: auto for images)
- Setting text sizes based on the device size

**CSS Flexbox**

[10/22] learnt about following topics
 - Adding `display:flex` property to an element makes that element as a flexi container. Once the element is flexi container then it becomes easy for us design responsive UI pages.
 - Usage of `flex-direction:row`. Setting up this property to an element helps us to arrange all its child elements in horizontal manner. 
 - Usage of `flex-direction:column`. Setting up this property to an element helps us to arrange all its child elements in vertical manner.
 - Usage of `flex-direction:reverse-row`. Setting up this property to an element helps us to arrange all its child elements in horizontal manner but in a reverse(top-bottom of the child html elements). 
 - Usage of `flex-direction:reverse-column`. Setting up this property to an element helps us to arrange all its child elements in vertical manner but in a reverse(top-bottom of the child html elements). 
 - Inorder to give spacing to flex elements we use `justify-content` property. This property takes 6 values. they are `center`,`flex-start`,`flex-end`,`space-between`,`space-around` and `space-even`. `justify-content:center` arranges all the elements in center and fills up the edges with spaces.  [More info](https://www.freecodecamp.org/learn/responsive-web-design/css-flexbox/align-elements-using-the-justify-content-property)
 - `align-items` property allows us to control on how to arrange elements in cross axis(opposite to the flex-direction) format. Ex: if element has `flex-direction:row` then all the items are arranged as a row ,defining `align-items:center` arranges elements in vertically center. 
 - `flex-wrap`  property helps us to define whether flex items should be arranged within the container or not if flex elements size is higher than flex container. [More Info](https://www.freecodecamp.org/learn/responsive-web-design/css-flexbox/use-the-flex-wrap-property-to-wrap-a-row-or-column)
 - `flex-shrink` it allows an item to shrink if the flex container is too small. Items shrink when the width of the parent container is smaller than the combined widths of all the flex items within it. Higher the value higher shrinkness.
 - `flex-grow`  property controls the size of items when the parent container expands.Higher the value higher growness.
 - The `flex-basis` property specifies the initial size of the item
 - `order` property controls the sequence of the flex items. Lower the value first the elements gets arranged.
 - `align-self`. This property allows us to adjust each item's alignment individually, instead of setting them all at once using `align-items`
 
  
