CSS Questions:

- What is the difference between classes and IDs in CSS?
> They are almost the same, but ID has higher piority.

- What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
> Resetings will remove all of the styles, while normalizing is trying to create a standard view. I think in most of time, 
> we should use nornalizing, since it won't reset all styles defined by browser. BootStrap is using normalizing css.

- Describe Floats and how they work.
> Float will make content all way to left or right, eg. create a sidebar menu.

- Describe z-index and how stacking context is formed.
> z-index is used to create layer, it works combination with position setting, eg position:related.

- Describe BFC(Block Formatting Context) and how it works.
> BFC is create by overflow, it cause the margin between two element cllopse, but it could used for preventing duplicate margin.
> eg. http://codepen.io/SitePoint/pen/XbVOXp

- What are the various clearing techniques and which is appropriate for what context?
> - float: left
> - display: table
> - clear: both
> - overflow: auto
> - .clearfix
> I suggest using .clearfix or clear:both solution other solutions could lead potential layout issue.

- Explain CSS sprites, and how you would implement them on a page or site.
> CSS sprites is using one image with several graphs, usually the icons, on it, and create a placeholder to display the image with specified icon coordination. By limit the size of the placehoder, the space will display only the icon we need, and hide rest. By this way, it could reduce the request and improve the web performance. The more important thing is it could fix jump menu display issue, since the specified icon is already load in the big image file.

- What are your favourite image replacement techniques and which do you use when?
> It is usually used for logo for the page. Replace text with image.

- How would you approach fixing browser-specific styling issues?
> There is no perfect solution, normalizing css could be a shortcut. IE has `<!--[if IE]>...<[!endif]-->` comment to help.

- How do you serve your pages for feature-constrained browsers?
> Future first, and fix the older with hack.

- What techniques/processes do you use?
> - Progressive Enhancement
> - Graceful Degradation

- What are the different ways to visually hide content (and make it available only for screen readers)?
> - .sr-only (from bootstrap)
> - display: none
> - visibility: hidden

- Have you ever used a grid system, and if so, what do you prefer?
> - 960Grid, YUI Grid all 24 column solution
> - BootStrap Grid, 12 Column
> - GridPak, 99 Column
> - I use BootStrap more often, 960 is not a bad choise, since it is simple

- Have you used or implemented media queries or mobile specific layouts/CSS?
> Media Query is good solution for responsive design
> eg. @media (max-width: 600){...}

- Are you familiar with styling SVG?
> SVG is basically a XML file contains image path, it is benefit due the the vector property. Image won't lost curve when resize. It also saves space.

- How do you optimize your webpages for print?
> Create a style for Print, media query could be a solution

- What are some of the "gotchas" for writing efficient CSS?
> Remove redundant qualifiers
> Be More specified, less using global style, eg div

- What are the advantages/disadvantages of using CSS preprocessors?
> advantages: logic, light weight
> disvantage: efficent, performance, difficult to maintain due to the logic

- Describe what you like and dislike about the CSS preprocessors you have used.
> LESS: Goods, BootStrap is based on it
> SASS/SCSS
> They are quite similar, both provide logic features; I don't use them too much actually.

- How would you implement a web design comp that uses non-standard fonts?
> by creating @family-face{font-famly: customizedName; src: url('xxx')}

- Explain how a browser determines what elements match a CSS selector.
> by using class, id and element name, id has the highest piority, then class, then the element name; there are also several persudo selectors, such as [propertyname=value]

- Describe pseudo-elements and discuss what they are used for.
> use for logic matching the selector

- Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
> pading, margin, layer, box-sizing

- What does * { box-sizing: border-box; } do? What are its advantages?
> It would aply to all element, which it is bad practice usually.

- List as many values for the display property that you can remember.
> display: inherit, none, inline-block, inline-flex, inline-table, block, flex, run-in, list-item, table, table-cell, table-caption ...

- What's the difference between inline and inline-block?
> inline such as span, inline-block, would be like div with padding, margin and size.

- What's the difference between a relative, fixed, absolute and statically positioned element?
> - relative, related to current position
> - fixed, related to viewport
> - absolute, related to parent element
> - static, the default normal position

- The 'C' in CSS stands for Cascading. How is priority determined in assigning styles (a few examples)? How can you use this system to your advantage?
> eg. the selectors piority, by using !important keywords.

- What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
> BootStrap, Meterial CSS, jQuery UI

- Have you played around with the new CSS Flexbox or Grid specs?
> They are both a solution for responsive design; for flex... mostly, I used it for centering item. I found there is issue with video. The video doesn't follow the flex rule in some case.

- How is responsive design different from adaptive design?
> It is using percentage, respond to different devices.

- Have you ever worked with retina graphics? If so, when and what techniques did you use?
> Use Media Query to setup the radio for retina graphic

- Is there any reason you'd want to use translate() instead of absolute positioning, or vice-versa? And why?
> trasnlate has better performance especially for animation, but it is also cost a lot of line coding.
