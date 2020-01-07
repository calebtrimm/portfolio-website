# Description

Create an HTML file and a CSS file that reproduces the following  
https://youtu.be/_t29BK3Tseg

# Instructions and tips to succeed

To successfully create this web page, here are a few guidelines to keep in mind:

### 1. Start by **doing what you can**

Take a moment to look at the different parts of the web page. Do you see anything that you would be comfortable doing?

- Can you create a black bar at the top of the page?
- What about creating a fullscreen background? This was one of the CSS exercises
- There are 2 big sections with some text and a background color. Perhaps you do not know how to do gradient backgrounds, but you may know how to set a blue background color.
- The images have a zoom effect and a dark background with text showing up when you hover, perhaps trying to reproduce that whole behavior seems daunting. Try displaying images and creating the layout, you can **worry about the fancy stuff later**.
- There is a styled input box and checkbox around the bottom, perhaps you're not sure how to do that. If you get stuck trying to make it look the same, **focus on doing what you can** - a simple input and checkbox - and move on. You can come back to more troublesome parts later on.

### 2. Find a balance between struggling and moving on

Following the first point, it's fine to struggle on a feature which you want to achieve, but if you're exhausting all your energy on it while you could have spent some time doing things you know how to do, you should accept that **some parts should be tackled on at a later point**.

### 3. When you have a hammer, everything looks like a nail

- Maybe not the best use of this saying, but the point is that you should keep your mind open, there are many different solutions to a problem. Maybe you see something where flexbox would be very helpful, but after trying things out it's not as easy as you thought. That doesn't necessarily mean you're on the wrong track, but perhaps you should **try looking into a different solution if something you thought would be easy is taking much more time and effort than anticipated**. Again, balance between struggle and moving on.
- Don't be afraid to redo something if you realize the current solution won't work for a new feature. Perhaps you coded something that works and looks good, but when you try adding another feature it doesn't behave the way you expected. You may need to rethink your solution to accomodate new features.

### 4. I'm tired / feel lost / nothing is working

- If you end up feeling that way, sometimes the best remedy is to just take a step out for a few minutes, walk for a bit, think about something else. Many times, I ended up finding a solution or just a new perspective allowing me to move forward by stepping out and coming back with fresh eyes.
- It's normal to run into obstacles, it is part of the learning process. **If you are not struggling, you're probably not learning much.**
- The instructor and the T.Cs are here to help

## Evaluation criterias

- Layout and general page presentation matches expectations (e.g. fixed navbar, fullscreen image with header, things are where they should be and visuals match expectations)
- Nothing is missing (all the sections are here, all the images, all the links, etc.)
- Is mobile responsive (Does the layout change to adapt to different screen sizes? How does it look on mobile, tablet, desktop?)
- Implements all the extra features (Animation on the 'cool' box, zoom effect on image, underline hover effect on navbar links)

You will have a PASS / FAIL on each grading rubric and a final PASS / FAIL grade for the module. The final grade is based on your project and the effort put into it. If some things are missing / don't look exactly right but I see you are going in the right direction and have made a real effort, you will be ok.

### Deadline

You have until the start of the next module (next Tuesday) to submit this project (push it on a new repository called **html-css-project**).

# Reference

Use the Poppins font. Use rem as unit for font-size (scales with device size).

I suggest using CSS variables for things like color (`#3a3633` is the primary color in this design, used for background color, text color) or **border-radius** (`4px`) so it's consistent across different elements.

The website has a navbar with links that scroll smoothly to different sections of the page. To achieve this, you will need to specify an id on the different sections of the page (e.g. `<div id="features"></div>`) and you can then use an anchor tag to go to that section (`<a href="#features"></a>`).
You can use this CSS to have smooth scrolling:

```css
html {
  scroll-behavior: smooth;
}
```

Here are some of the CSS properties used for the project (this is not a full list of the properties used, just the new or potentially confusing ones):

---

`background-color`  
You can use **rgba** to make transparent colors. **a** is the transparency value. e.g. `background-color: rgba(0,0,0,0.5);`

`object-fit`  
Size an <img> element like you would a background image, with properties like **cover** (automatically zoom in / out to cover the whole area), **contain**, etc.

`object-position`  
Can be used like the `background-position` property

`-webkit-appearance: none`  
Some elements (e.g. checkbox input) cannot be styled. Using this CSS property, the functionality of the element is kept but the look of the element can be created from scratch. The _webkit_ prefix is to use the chrome implementation of the `appearance` CSS property.

`background-image`  
For gradient backgrounds, use `linear-gradient(direction, color1, color2)`. Example: `background-image: linear-gradient(to right, #fff, blue);`

`border-top-right-radius`  
You can specify `border-radius` on specific corners (top-left, top-right, bottom-left, bottom-right)

`transform`  
If you want to apply multiple transform effects (e.g. translate and rotate), the syntax is: `transform: translate() rotate()`

`transform-origin`  
Use this to specify from which point a transform should happen (e.g. scale from the left, center, or right of the element)

`transition`  
If you want to apply transitions on multiple properties, the syntax is: `transition: property_name duration easing_function, property_name2 duration easing_function`

`keyframes`  
Use to make animations. **from** is like `0%` and **to** is like `100%`. You can add as many keyframes as you want (e.g. `from{} 50%{} 80%{} 90%{} to{}`). You can also add keyframes in media queries, just use the same name to override the existing keyframe.

`grid-auto-rows`  
Use this to specify the height of new grid rows (vs. `grid-template-rows` where you specify an explicit amount of rows and their size)

---

## Media queries

I suggest putting all your media queries in one place (at the bottom for example.). You can use these values:  
Tablets: `768px`  
Desktops: `1200px`

Notice there is no value for mobile, you should do mobile first design. All your CSS rules are for mobile (smaller than 768px screen width). Then you can override the CSS rules inside your media queries for larger screen sizes.

## Notes

If your CSS rules are getting too complicated (e.g. `.myclassname > .someotherclass > div > span`) you should create new classes.  
**ID**s are useful for specific sections of the web page (e.g. _features_ section) as well as specific elements which you know there will be only one of (**ID**s need to be unique)
