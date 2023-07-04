# Artikel 3

Introduction to progressive enchantment  
============================================================

In today's digital landscape, web design and development have become increasingly challenging. From the early days when the web was relatively small, with screen sizes like 640p x 480px, to the present, where a multitude of screen sizes exist, adapting to these changes is essential. This article explores the significance of responsive design and the need to consider various user experiences in a rapidly evolving web environment.

The Evolution of Web Design & The Rise of Responsive Design
-----------------------------------------------------------

Today, countless screen sizes exist, making it virtually impossible to keep up with every variation. As users interact with web pages in different ways, whether at home, on mobile devices, or during travel, their experiences can significantly differ. Designers must understand and cater to these variations to ensure optimal user experiences across devices.

In the beginning, web design was relatively manageable due to the limited size of the web itself. However, as screen sizes progressed to 800px and beyond, developers faced the challenge of accommodating larger websites. They initially experimented with percentage-based layouts to create responsive web pages since media queries were not yet available. Screen sizes like 1024x768 became a common standard, providing a comfortable browsing experience for many users.

So in the early days of web design, before the widespread use of responsive frameworks and modern CSS techniques, developers had to rely on different approaches to achieve responsive design. One popular method was using HTML tables for layout, as they provided a way to structure content in a grid-like format.

Developers would often divide their web page into rows and columns using nested tables. Each cell within the table would contain content or additional nested tables, creating a structured layout. While this approach allowed for some level of responsiveness, it had its limitations and wasn't ideal for complex designs.

Another approach involved using HTML framesets. Framesets allowed developers to divide a web page into separate frames, each with its own content. These frames could be sized independently, providing some level of control over the layout. However, framesets presented challenges for search engine optimization and bookmarking, making them less favorable in the long run.

As web design progressed, the introduction of CSS (Cascading Style Sheets) revolutionized the way developers approached layout and design. CSS provided more flexibility and control over the visual presentation of web pages.

One technique used before the advent of CSS frameworks involved the creative use of HTML elements such as <div> and <span>. Developers would assign classes or IDs to these elements and define styles in CSS to control their positioning, sizing, and appearance. These <div> and <span> elements acted as building blocks for constructing the layout and structure of web pages.

For example, to create a responsive two-column layout, developers would use <div> elements with CSS properties such as float, width, and margin to position the columns side by side. By specifying percentages for the column widths, the layout could adapt to different screen sizes. However, this approach often required manual adjustment and testing to ensure consistent behaviour across various devices.

Additionally, media queries were introduced to CSS, enabling developers to apply different styles based on specific screen sizes or device characteristics. Media queries allowed for conditional styling, making it possible to adjust elements, such as font sizes or column widths, based on the user's device or viewport size.

Overall, while the early approaches to responsive design using HTML tables, framesets, and creative use of <div> elements were effective to some extent, they lacked the flexibility and ease of implementation that modern CSS frameworks and techniques provide. Today, responsive design has evolved significantly, with frameworks like Bootstrap and Foundation offering a wide range of pre-built responsive components and grids that simplify the process of creating responsive layouts.


```html
<table>
 <tr>
<td>Content in cell 1</td>
<td>Content in cell 2</td>
 </tr>
 <tr>
<td>Content in cell 3</td>
<td>Content in cell 4</td>
 </tr>
</table>
```

This example showcases a basic HTML table structure with four cells. By adjusting the table's width and applying CSS styles, developers could control the layout and responsiveness of the content within each cell.
```html
<div  class="container">\
  <div  class="column">Content in column 1</div>\
  <div  class="column">Content in column 2</div>\
</div>
```

In the early days, the <div> element, known as a "division," was often used as a generic container to group and style content. By assigning specific classes or IDs to the <div> elements and defining CSS styles, developers could position them and create responsive layouts.

```css
.container {\
 width: 100%;\
}

.column {\
 float: left;\
 width: 50%;\
}

@media screen and (max-width: 768px) {\
 .column {\
width: 100%;\
  }

}
```

In this CSS example, the .container class represents the container <div> element, and the .column class represents the column <div> elements. Initially, the columns are floated side by side with a width of 50% each. However, when the screen size is below 768 pixels, the media query adjusts the column width to 100%, making the layout stack vertically on smaller screens.

These code examples illustrate how developers used HTML tables and creatively styled <div> elements to achieve responsive layouts in the early days of web design. Over time, the introduction of CSS frameworks and modern techniques, along with the standardisation of the <div> element, have simplified the process of creating responsive designs.

In the past, the <div> element was sometimes referred to as a "division" or a "block-level element."

Expanding Web Accessibility
---------------------------

With the advent of larger screens and the increasing accessibility of the web, designers began to recognize the importance of accommodating diverse devices. While laptops surpassed the previously established norms, mobile devices remained unconsidered due to their limited availability to the general population. 

![](https://lh6.googleusercontent.com/2mlqw92EkMqP9NjkcYoZymEfT8VM5I5hjTSYHQU5pZsgeFEMkiBTTIA9bdrmJrbHgsg4Ha57WU7Oyy3jTzkgASyFnl9-B6K06PViNBolXvooS_vpHh6-IDysn1qoMUXw9X9hZQfbRlC7715R-EI2BpU)

However, as smartphones gained popularity, the web expanded further, becoming accessible to an even larger audience.

Considering User Diversity
--------------------------

![](https://lh6.googleusercontent.com/bJ2tMRpUP1qiXofetheuXJWsIEdmmgqLzLsjHp9H5t7LPGrQpkDoiPRh7kwSGaE-1TMFqfLsAqISkYOmITEh5IaRHITuQgwE1gMEUM5K2yrqQe4ZXxFEi5rWERG3dt2RQ7ksX-Y72ZLuWntqVaZpu2E)

Every user is unique, with different preferences and circumstances that influence their browsing habits. Designers often fall into the trap of designing primarily for their own perspectives, neglecting the needs of other users. It is crucial to recognize the contrast between first-world and third-world countries regarding smartphone usage and adapt designs accordingly. Users with older or less powerful devices may encounter 52% more errors during app usage, underscoring the need for inclusive design.

Situational Development and Progressive Enhancement
---------------------------------------------------

Sometimes, it is beneficial to develop situation-specific solutions, taking into account constraints that can even aid in the design process. Progressive enhancement is a key concept that focuses on improving the user experience while ensuring that the core functionality remains intact. By prioritising what matters most, clearly communicating information, and considering different ways users may interact, designers can create experiences that gracefully adapt to various devices and browsing scenarios.

Conclusion
----------

In an ever-evolving web landscape, responsive design is vital to cater to the diverse needs of users across an array of devices. The accessibility of the web has increased significantly, allowing content to be accessed and consumed from anywhere. Designers must embrace progressive enhancement and consider various user experiences to create inclusive and enjoyable browsing experiences. By continuously adapting and improving, we can ensure that our web pages reach and engage users effectively, regardless of their device or location.


Used to google docs -> markdown https://euangoddard.github.io/clipboard2markdown/
----------
Reference: Aaron Gustafson Weekly nerd
