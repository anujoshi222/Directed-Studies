# D3.js- Data-Driven Documents
### This repository is dedicated to learn about the d3.js library for beginners.
![Data visualisation](https://images.unsplash.com/photo-1527474305487-b87b222841cc?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=fb7509475b0802f0f2f35515fae1195e&auto=format&fit=crop&w=967&q=80)

## Sources
1. [Lynda video Tutorials](https://www.lynda.com/D3js-tutorials/Data-Visualization-D3js/162449-2.html)
2. [Tutorial teacher site](http://www.tutorialsteacher.com/d3js)
3. [Dashing D3 site](https://www.dashingd3js.com/table-of-contents)
4. [D3.js Official website](https://d3js.org/)
5. [Tutorial Point](https://www.tutorialspoint.com/d3js/)
6. [Slideshare](https://www.slideshare.net/flatironschool/d3-729-3?from_action=save)


## Framework Overview
D3 stands for Data-Driven Documents. It is an open-source JavaScript library developed by Mike Bostock to create custom interactive data visualizations in the web browser using SVG, HTML and CSS.
Data - Provided by you
Driven - d3 connects data to documents
Documents - web-based documents

![Prerequisites](https://image.slidesharecdn.com/d37-140731100120-phpapp01/95/intro-to-d3-datadriven-documents-7-638.jpg?cb=1406811316)

### Features

- **Data Driven Visualisations**: D3 is a framework that is also a visualization library for building-data driven graphics. 
It lets you build graphics that use common web standards
      
- **Using Open Web Standards**: It makes the graphics easily accessible through any web browser.
 And that means that one can use JavaScript and generate regular HTML and CSS visualizations and the slightly 
 and more flexible, scalable vector graphics known as SVG.
         
- **Works With Modern Broswers**: D3 library is very lightweight and works well across all the browsers.
 It is capable of handling large data sets.

- **Web Standards**: 
      - *HTML* = HyperText Markup Language
      HTML is used to structure the content of the web page. The current version is HTML 5. 
      It is stored in a text file with the extension ".html".

                        Example: Use D3 library from CDN
                        <!DOCTYPE html>
                        <html lang="en">
                        <head>
                            <meta charset="UTF-8">
                            <title></title>
                        </head>
                        <body>

                        </body>
                        </html>

     - *DOM* = Document Object Model
     When you write html code for your page, it gets converted to a hierarchical structure on the browser. 
     Every tag in html gets converted to an element in the DOM with a parent-child hierarchy. 
     It makes your html more logically structured. Once the DOM is formed, it makes it easier to manipulate
     (add/modify/remove) the elements on the page. 

     - *CSS* = Cascading Style Sheets
     HTML gives a structure to the web page, while CSS styles your web page making it more pleasant to look at. 
     It is a stylesheet language used to describe the presentation of a document written in HTML or XML
     (including XML dialects like SVG or XHTML). CSS describes how elements should be rendered on a web page.

     - *SVG* = Scalable Vector Graphics
     SVG is a way to render images on the web page. SVG is not a direct image but is just a way to create 
     images using text. As it's name suggests, it is scalable vector. It scales itself according to the 
     size of the browser, so resizing your browser will not distort the image. All browsers support 
     SVG except IE 8 and below.

     Since data visualizations are visual representations, it is convenient to use SVG to render visualizations using D3.

     Think of SVG as a canvas on which you can paint different shapes.
     The default measurement for SVG is pixels, so you don't need to specify if your unit is pixel.

     Now if you would like to draw a rectangle inside this SVG, draw it using <rect> :

                  Example: Square in SVG
                  <svg width="500" height="500">
                      <rect x="0" y="0" width="300" height="200"></rect>
                  </svg>

    Just like styling html elements, styling SVG elements is simple. Let's color the above rectangle in yellow. All you need to add is       an attribute "fill" and specify the color.

                  Example: Colored Rectangle
                  <svg width="500" height="500">
                      <rect x="0" y="0" width="300" height="200" fill="yellow"></rect>
                  </svg>

    - *JavaScript*
    JavaScript is a loosely-typed client side scripting language that executes in the user's browser. 
    JavaScript interact with html elements (DOM elements) in order to make the web user interface interactive.
    JavaScript implements ECMAScript standards, which includes core features based on ECMA-262 specification as 
    well as other features which are not based on ECMAScript standards.
      
- **Dynamic Properties**: D3 gives the flexibility to provide dynamic properties to most of its functions. 
 Properties can be specified as functions of data. That means your data can drive your styles and attributes.
      
- **Types of visualization**: With D3, there are no standard visualization formats. But it enables you to create
anything from an HTML table to a Pie chart, from graphs and bar charts to geospatial maps.
     
- **Custom Visualizations**: Since D3 works with web standards, it gives you complete control over
your visualization features.
     
- **Transitions**: D3 provides the transition() function. This is quite powerful because internally,
D3 works out the logic to interpolate between your values and find the intermittent states.
     
- **Interaction and animation**: D3 provides great support for animation with functions like duration(), 
delay() and ease(). Animations from one state to another are fast and responsive to user interactions.


## Prototype Idea
