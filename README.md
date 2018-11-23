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
7. [Github Repository](https://github.com/d3/d3/wiki)
8. [Block code](http://bl.ocks.org/bobmonteverde/2070069)

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

- **Web Standards**: d3.js puts together the idea of the following web standards.

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


## 75% Prototype Idea

* Let's draw a line graph using the d3.js library.
* Using transitions and animations in the graph
* Making the line chart interactive for user interaction

Here is how I have started working on the project so far:

Pull d3.js library from [here](https://d3js.org/#introduction)

                  <script src="https://d3js.org/d3.v5.min.js"></script>
            
            
Create one html file and pull the d3.js library as shown below:

                   <!DOCTYPE html>
                  <html lang="en">
                  <head>
                    <meta charset="UTF-8">
                    <meta name="viewport" content="width=device-width, initial-scale=1.0">
                    <meta http-equiv="X-UA-Compatible" content="ie=edge">
                    <title>d3.js</title>
                  </head>
                  <body>
                    <h1>Bar Chart using D3.js</h1>
                    <!-- Creating blank svg tag -->
                    <svg class="chart"></svg>

                  </body>
                  </html>
                  <!--Pulling d3.js library  -->
                  <script src="https://d3js.org/d3.v4.min.js"></script>
                  <script src="index.js"></script>


Using d3 library as follows:

                  // Create data to be used
                  let data_array = [80, 100, 56, 120, 180, 30, 40, 120, 160];

                  let svg_width = 500, svg_height = 200, padding = 2;
                  let bar_width = svg_width / data_array.length;

                  //Selection of svg tag using d3 selector
                  let svg = d3.select('svg')
                  //assigning values to attributes
                  .attr("width", svg_width) 
                  .attr("height", svg_height);

Inserting data and appending the rectangles in the blank svg tag:

                  let chart = svg.selectAll("rect")
                  .data(data_array) //inserting values from data_array
                     .enter()
                     .append("rect") //appending rectangles
                     .attr("y", function(data) {
                          return svg_height - data
                     })
                     .attr("height", function(data) {
                         return data;
                     })
                     .attr("width", bar_width - padding)
                     .attr("class", "bar")
                     //To avoid overlapping of bars modify the x position of bars
                     .attr("transform", function (data, x) {
                         let translate = [bar_width * x, 0];
                         return "translate("+ translate +")";
                     });
                     
Inserting labels at the top of each bar:

                        let text = svg.selectAll("text")
                           .data(data_array)
                           .enter()
                           .append("text")
                           .text(function(data) {
                               return data;
                           })
                           .attr("y", function(data, y) {
                               return svg_height - data - 2;
                           })
                           .attr("x", function(data, i) {
                               return bar_width * i;
                           })
                           .attr("fill", "Black")
                           
  Output: After applying styling to bar and chart classes we get the following output
  ![Screenshot](https://firebasestorage.googleapis.com/v0/b/anu-first.appspot.com/o/Capture.JPG?alt=media&token=a4ad16c6-8d3b-46a9-9fb6-6b9299793e15)
  
  Using such bar graphs and line charts would be an interesting idea to use in the projects.
  
  
  ## User Stories
  
  1. As a Mother, I want to know what are the disease outbreaks happening around me, so that I can take care of myself and my family.
  
  2. As a travel enthusiast, I want to see how many people are being impacted from the disease outbreaks in particular areas, so that I can take immunization before travelling to that country.
 
  3. As a Doctor, I want to view the historical diseases data for past 1 month in the particular area, so that I can estimate vaccines/medical needs in advance.
  
  
  ## Progress Report
  
  * **Executive Summary:** As per the final project our team is building web app that enables the users to check the prevalent diseases and allergies in any of the countries on the globe. Following that, I am working on a interactive line chart using d3.js library that will show the diseases and the number of people getting infected from those diseases in a span of 1 month. My aim for making this prototype is to visualize the data in easy readable and interactive way. Also, Managing the wealth of available healthcare data allows health systems to create holistic views of patients, personalize treatments, improve communication, and enhance health outcomes. Via my prototype I am targeting all the travel enthusiast and the healthcare personnels who need to refer to the health data one or the other time. This app is apt for everybody who anytime wants to see the impact of diseases around them or in different countries.
  The major thing about my prototype is the data will not be static user will be able to interact with the data in the line chart. Visualization of any sort of data is critical in terms of validation. For this project I am using dummy data to make my prototype work. In the future, I can make use of charts.js, topo.js and react to enhance the functionlaities of the prototype.
  
  
  Source: [https://www.evariant.com/faq/why-is-healthcare-data-management-important] (https://www.evariant.com/faq/why-is-healthcare-data-management-important)
  
  * **Retrospective:** For this week, I worked on using transitions and projections in the line chart from a number of websites:
  like [D3.js Official website](https://d3js.org/) and [Lynda video Tutorials](https://www.lynda.com/D3js-tutorials/Data-Visualization-D3js/162449-2.html). I was able to use the projections and transitions for the line chart, But I faced difficulty using the datasets of different kinds. I tried pulling data from array and csv files first. Then, I started working on the json object, because I did not know how to access the json objects I was not able to work with it. I referred to online tutorial on accessing json object in Javascript [Video Tutorial](https://www.mkyong.com/javascript/how-to-access-json-object-in-javascript/). For the next time, I will focus on revising the prerequisites for learning the new technology. In this case, learning d3 requires good knowledge of Javascript,CSS, HTML and SVG elements. Revising these four before going for d3.js could be better idea as going back and forth for reference in between the project is frustrating.
  
  
  * **Plan for next week**: 
      * I will be working on the dataset of my prototype. I am using dummy data from [Mockaroo.com](https://www.mockaroo.com/)
      * I will be working on user-data interaction. How user is going to interact with the data available.
            
            
            
            
  * **Product Backlog**
  
  ![Backlog](https://firebasestorage.googleapis.com/v0/b/anu-first.appspot.com/o/backklog.JPG?alt=media&token=daaff4fe-4223-4807-ad8d-440e8efb0677)
 
 
 
 ## Prototype implementation
  
   ### Data creation for the line chart
        function generateData() {
          let Malaria = [],
              Measles = [],
              Pollen = [],
              diarrhoea = [],
              n1 = Math.round(Math.random()),
              n2 = Math.round(Math.random()),
              n3 = Math.round(Math.random()),
              n4 = Math.round(Math.random());

                for (let i = 0; i < 100; i=i+5) {
                  Malaria.push([ i*100, Math.random()+100]);
                  Measles.push([ i*100, n2 +Math.random()+100]);
                  Pollen.push([ i*100, n3 +Math.random()+100]);
                  diarrhoea.push([ i*100, n4 +Math.random()+100]);
                }

                return [
                  {
                    data: Malaria,
                    label: "Malaria"
                  },
                  {
                    data: Measles,
                    label: "Measles"
                  },
                  {
                    data: Pollen,
                    label: "Pollen Allergy"
                  },
                  {
                    data: diarrhoea,
                    label: "Skin rashes"
                  }
                ];
              
   ### Create Chart
   
         function graph(selection) {
          selection.each(function(data) {

            let container = d3.select(this).selectAll('g.point').data([data]);
            let gEnter = container.enter().append('g').attr('class', 'point').append('g');


            let g = container.select('g')
                .attr('transform', 'translate(' + margin.left + ',' + margin.top + ')');


            let range= g.selectAll('.range')
                .data(function(d) { return d });
            let rangeEnter = range.enter().append('g').attr('class', 'range')
                .on('click', function(d, i) {
                  dispatch.pointClick(d, i);
                })
                .on('mouseover', function(d, i) {
                  dispatch.pointMouseover(d, i);
                })
                .on('mouseout', function(d, i) {
                  dispatch.pointMouseout(d, i);
                });
            rangeEnter.append('circle')
                .style('fill', function(d, i){ return d.color || color[i % 10] })
                .style('stroke', function(d, i){ return d.color || color[i % 10] })
                .attr('r', 5);
            rangeEnter.append('text')
                .text(function(d) { return d.label })
                .attr('text-anchor', 'start')
                .attr('dy', '.32em')
                .attr('dx', '8');
            range.classed('disabled', function(d) { return d.disabled });
            range.exit().remove();


            let ypos = 1,
                newxpos = 5,
                maxwidth = 0,
                xpos;
            range
                .attr('transform', function(d, i) {
                   let length = d3.select(this).select('text').node().getComputedTextLength() + 28;
                   xpos = newxpos;


                   if (width < margin.left + margin.right + xpos + length) {
                     newxpos = xpos = 5;
                     ypos += 20;
                   }

                   newxpos += length;
                   if (newxpos > maxwidth) maxwidth = newxpos;

                   return 'translate(' + xpos + ',' + ypos + ')';
                });

            //position point as far right as possible within the total width
            g.attr('transform', 'translate(' + (width - margin.right - maxwidth) + ',' + margin.top + ')');

            height = margin.top + margin.bottom + ypos + 15;
          });

          return graph;
   
   
  ## Prototype Demo
  
Please follow the link to see the prototype demo: [Prototype](http://mylinux.langara.bc.ca/~a33/Directed_Studies/index)


## Retrospective Report
### What went well!

* Completed 75% of the prototype
* Collaboration with Project 2
* On track in terms of learnng goals
* Adaptability to work in real world
* Able to create charts with animation and transitions

### What did not go well

* Initially fixing issues bu yourself was difficult. I was following a tutorial where the version used for the d3 library was older one. The syntax for few functions was changed, it was really difficult to figure out what was wrong. So I refrerred to Stack overflow forum to fix the issue finally.
* Too many channels for learning was creating confusion.
* I did not freeze the features I need for the prototype

### Roadblocks

* Work stress from other courses slowed down my learning process
* I had few exams this week too, So I had less time to focus on my prototype.


### What will be done differently next time

* I will filter the resouces before starting a feature from scratch.
* I am bit week in corporating visual aids, I will sharpen my CSS skills too.
* I will prepare a plan and wireframes for the features to be executed.

## Project Plan
![Project_Plan](https://firebasestorage.googleapis.com/v0/b/anu-first.appspot.com/o/Untitled.jpg?alt=media&token=c800046c-eefd-45a0-98f3-dce496312169)

## Project User Stories

  1. As a single parent, I want to see the air quality and weather forecast around me, so that I can take care of my children and family.
  
  2. As a travel enthusiast, I want to see the disease outbreaks in particular areas, so that I can take immunization before travelling to that country.
 
  3. As a health instructor, I want to see the seasonal allergies prevalent in that area, so that I can instruct people to work on their health.
  4. As a doctor, I want to see the suggested vaccines for development of immunization against the diseases, so that I can suggest some more via the app.


## 20% Progress Report

 * **Executive Summary:** As per the final project our team is building web app that enables the users to check the prevalent diseases and allergies in any of the countries on the globe. Following that, I am working on a interactive line chart using d3.js library that will show the diseases and the number of people getting infected from those diseases in a span of 1 month. 
 I am working on the visualisation and front-end development. I am using tablaeu, d3.js, charts.js for development of the front-end charts and maps.
 
  * **Retrospective:** So far in terms of the project:
       * **Technology Research:** Initially, It was challenging to decide which technology to go for. But
then after some research, I realized for data visualization there is a bunch of libraries that can be used like React, Vue or D3.js. I chose the d3.js library because it has very cool graphs, sunburst charts, and maps as output. I will use d3.js, HTML, CSS, JQuery, Javascript, PHP as my development tools. See the links below:
[https://www.forbes.com/sites/bernardmarr/2017/07/20/the-7-best-data-visualization-tools-in-2017/#2e94de3e6c30](https://www.forbes.com/sites/bernardmarr/2017/07/20/the-7-best-data-visualization-tools-in-2017/#2e94de3e6c30)[https://bigdata-madesimple.com/review-of-20-best-big-data-visualization-tools-2/](https://bigdata-madesimple.com/review-of-20-best-big-data-visualization-tools-2/).
      * **Plan with Technology:** Map - I will use d3.js/React to create the map.Data- I will use WHO API's to fetch data for the diseases and allergies.I am responsible for implementing this API.
      * **API Research & Prototyping:**: I implemented the insect API for fetching the health-threatening insects in a specific area. Please see the link here:
            [http://mylinux.langara.bc.ca/~a33/inaturall/1.html](http://mylinux.langara.bc.ca/~a33/inaturall/1.html)
            I also used the d3.js library to implement the line chart as part of the directed studies course which is also part of project 2: [http://mylinux.langara.bc.ca/~a33/Directed_Studies/index](http://mylinux.langara.bc.ca/~a33/Directed_Studies/index)
  
  
  * **Plan for next week**: 
      * I will be working on implementing "Air Quality" weather API from the accuweather site and display the result in the front end.
                 
  * **Product Backlog**
  
  ![Backlog](https://firebasestorage.googleapis.com/v0/b/anu-first.appspot.com/o/20%25.jpg?alt=media&token=33c35119-eda3-4373-953f-59f09bba69d3)
 
 
 
 ## 40% Progress Report

 * **Executive Summary:** As per the final project our team is building web app that enables the users to check the prevalent diseases and allergies in any of the countries on the globe. Following that, I am working on a interactive line chart using d3.js library that will show the diseases and the number of people getting infected from those diseases in a span of 1 month. 
 I am working on the visualisation and front-end development. I am using tablaeu, d3.js, charts.js for development of the front-end charts and maps.
 
  * **Retrospective:** So far in terms of the project:
      
      * **Openweather API implementation using d3.js :** We have another feature where the user has to enter the location and based on that the data of weather, pressure, wind speed etc is fetched from the API. I implemeted the openweather api to achieve that.
      Please see the demo here: [file:///C:/Users/User/Desktop/map/prototype_map.html](file:///C:/Users/User/Desktop/map/prototype_map.html)
      
        
  * **Plan for next week**: 
      * I will be working on implementing the Google map API with data visualization in Jquery .
      * I also need to convert the d3.js script to react component because our app is based on react solely.
                 
  * **Product Backlog**
  
  ![Backlog](https://firebasestorage.googleapis.com/v0/b/anu-first.appspot.com/o/40%25.jpg?alt=media&token=e335bf63-7f1c-4766-b825-780e55ebb73d)
 
 
  ## 60% Progress Report

 * **Executive Summary:** As per the final project our team is building web app that enables the users to check the prevalent diseases and allergies in any of the countries on the globe. Following that, I am working on a interactive line chart using d3.js library that will show the diseases and the number of people getting infected from those diseases in a span of 1 month. 
 I am working on the visualisation and front-end development. I am using tablaeu, d3.js, charts.js for development of the front-end charts and maps.
 
  * **Retrospective:** So far in terms of the project:
       * **Map Google API implemented:** Our guest page have a map depicting the disease data on it. I implemented Google Map Api using html and Jquery. The overall requirement of our project is to get the map as a react component.
       Please see the demo file here: [http://mylinux.langara.bc.ca/~a33/googlemap](http://mylinux.langara.bc.ca/~a33/googlemap)
            
      * **Converted D3.js to a react app**: We are planning to make our app based on the react.js. I had to convert both the map and weather scripts to react components. I implemented both the API implementations to the react components.
  ![bbb](https://cdn.filestackcontent.com/61xyKf5Qpiq97IUvLvGf)
  
  * **Plan for next week**: 
      * I will be working on integrating both the components and customize the weather app search bar for the map component as well.
                 
  * **Product Backlog**
  
  ![Backlog](https://firebasestorage.googleapis.com/v0/b/anu-first.appspot.com/o/60%25.jpg?alt=media&token=38c215c9-f09d-4ec4-9402-a97929d2d688)
 
  ## 80% Progress Report

 * **Executive Summary:** As per the final project our team is building web app that enables the users to check the prevalent diseases and allergies in any of the countries on the globe. Following that, I am working on a interactive line chart using d3.js library that will show the diseases and the number of people getting infected from those diseases in a span of 1 month. 
 I am working on the visualisation and front-end development. I am using tablaeu, d3.js, charts.js for development of the front-end charts and maps.
 
  * **Retrospective:** So far in terms of the project:
       * **Imntegration of components:** I integrated the google map API component and the Accuweather API.
            
      * **Customized the Google API map:** According to the mockups and wireframes given by the designer I modified the Google map display For ex. Hiding the default controls, Changing the color for the map label and content area.
  
  * **Plan for next week**: 
      * I will be assisting my team in converting a php component to react using restful API for json object modification.
                 
  * **Product Backlog**
  
  ![Backlog](https://firebasestorage.googleapis.com/v0/b/anu-first.appspot.com/o/80%25.jpg?alt=media&token=23ae026d-3cf6-43a4-ab13-65c6ddaa4016)
 
 ## 90% Progress Report

 * **Executive Summary:** I have completed the styling and implementation of Google map component and open-weather component. The integration of both these react components was done this week. After hosting the app on heroku, the open-weather was not working. I worked on fixing this bug. In order to solve the issue, I removed the function that I was using for fetching weather information. Instead, I directly used the link to access json data from the openweather API. I also worked on enhancing the loading speed of the app on heroku.
 
  * **Retrospective:** I have completed the integration of Google app API and Openweather API as a single react app. The following tasks were performed this week.
  
       * **Bug fixing of Openweather API on heroku:** The openweather API was working fine locally butonce I host the app onheroku, it was giving 400 error. After analysing the code I realised it has some port limitation when we hit the API using the function. But once I directly fetched the data from the link. It worked fine.
![weather](https://firebasestorage.googleapis.com/v0/b/anu-first.appspot.com/o/air.JPG?alt=media&token=95ffba76-3639-4843-abce-d3254f5f4c1b)
      * **Enhanced loading speed of heroku app:** Simplified the map configuration and cleaned the code for easy readability.
     
  
  * **Plan for next week**: 
      * I will be working on some of the css stuff for the openweather component.
                 
  * **Product Backlog**
  
  ![Backlog](https://firebasestorage.googleapis.com/v0/b/anu-first.appspot.com/o/90%25.jpg?alt=media&token=ab3a652e-a611-4ee3-8544-be1a1671bdd9)
  
  ## 95% Progress Report

 * **Executive Summary:** As per the final project our team is building web app that enables the users to check the prevalent diseases and allergies in any of the countries on the globe. Following that, I am working on a interactive line chart using d3.js library that will show the diseases and the number of people getting infected from those diseases in a span of 1 month. 
 I am working on the visualisation and front-end development. I am using tablaeu, d3.js, charts.js for development of the front-end charts and maps.
 
  * **Retrospective:** 
  
  
  * **Plan for next week**: 
      * I will still be working on enhancing the visual aida and testing of integrated components.
                 
  * **Product Backlog**
  
  ![Backlog](https://firebasestorage.googleapis.com/v0/b/anu-first.appspot.com/o/95%25.jpg?alt=media&token=07d9ab4f-1b76-4790-b6e3-5bba58e12a1d)
