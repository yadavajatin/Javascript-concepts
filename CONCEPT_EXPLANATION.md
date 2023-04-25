# Javascript-concepts
---------------WHAT IS INTERSECTION OBSERVER-----------------------------------------------------------------------
It's a way for your website or app to ask the browser to tell you when a certain element (like an image or a video) 
is visible on the screen. Instead of checking all the time if the element is visible, Intersection Observer
tells you when it enters or exits the screen.
---------------------------------------------------------------------------------------------------------------------

---------------HOW TO CREATE INTERSECTION OBSERVER-----------------------------------------------------------------------
-STEP 1-
First, you need to create a new instance of the Intersection Observer by passing in a callback function and some options:
-code-
const observer = new IntersectionObserver((entries) => {
  // Callback function
}, {
  // Options object
  root: null,
  rootMargin: '0px',
  threshold: 0.5
});

Note-The instance have two parameters 1.callback 2.Options Object

-STEP 2-
Next, you need to select the element that you want to observe and call the observe method on the observer:
-code-
const element = document.querySelector('.my-element');
observer.observe(element);

---------------OPTIONS OBJECT------------------------------------------------------------------------------------------
In the options object, you can set the ROOT element (the element that is used as the viewport for checking visibility), 
the ROOTMARGIN (the margin around the root element), 
and the THRESHOLD (the percentage of the target element's visibility needed to trigger the callback function)
------------------------------------------------------------------------------------------------------------------------

---------------WHAT ARE ENTERIES {IntersectionObserver((entries)} ------------------------------------------------------------------------------------------

1. In the context of Intersection Observer, an entry is an object that represents the intersection between the observed element and the viewport 
   (or the root element, if one is specified in the options).

2.When you observe an element using the observe method of the Intersection Observer instance, the observer starts watching that element and 
  sends a stream of entry objects to the callback function you provided. Each entry object contains information about the intersection between 
  the observed element and the viewport, such as:
  
-isIntersecting: a boolean that indicates whether the observed element is currently intersecting with the viewport or not.
____________________________________________________________________________________________________________________________________________________
-intersectionRatio: the ratio of the intersection area to the total area of the observed element.
____________________________________________________________________________________________________________________________________________________
-boundingClientRect: the position and size of the observed element relative to the viewport.
____________________________________________________________________________________________________________________________________________________
-rootBounds: the position and size of the root element relative to the viewport (if one was specified in the options).
____________________________________________________________________________________________________________________________________________________
-target: a reference to the observed element itself.You can use these properties to determine the visibility and position of the observed element, 
and take action accordingly in the callback function.



