# CCAH Developer Screen

## Questions:

### Question 1:
You are attempting to make several visual/layout changes to a web page. If you only have one chance to place your code, how do you ensure/test that it’s correct?

### Answer 1:
I would start by making a new branch for all of the new code.  First, on the new branch I would make tests with Jest, Chai, or Mocha.  This way I will know right away if my code is going to pass the tests.  I would also check my code with CSS and/or a HTML validator. Another strategy is checking that it works with different screen sizes including mobile by adjusting the screen size on the computer or in inspect elements changing the view to different devices.  In addition there are sites you can use like [mobiRead](https://ready.mobi/) to make sure the site is responsive.  It’s also great to have another person take a look at your code.  Once everything looks good and is working correctly I would check that it meets all the requirements and find out if it is approved.  Once it's approved I would merge it with the master branch.   

### Question 2:
Imagine you have a web page with a form for users to fill out and submit. Can you think of a way that the page can save the user's progress if they leave (close web page or navigate away) and come back later using front end code only?

### Answer 2:
One option would be to use local storage to keep the information for the user.  Local storage will store a limited amount of data, about 5MB. Sessions storage is another option but it only works if the user keeps that page open and is active.  The problem with session storage is that once you close the page the information will be gone.  Cookies would also be an option but that limits how much you can store too.  
 
### Question 3:
This Page (http://ccahproduction.com/assessment/frontEnd/01.html) is the page for this question.
 
You want this text: “This is the copy you must edit” to change if someone visits this page: https://ccahproduction.com/assessment/frontEnd/01.html?content=firsttime 
VS this page: https://ccahproduction.com/assessment/frontEnd/01.html?content=returning 

### Answer 3:

```

if(window.location.search.includes("returning")) {
    
    document.querySelector("p").innerHTML = "Thanks for coming back to the website!"
}

```

### Question 4:
 
You can place JavaScript code in a script tag on the page, what front end code would change the text on that page depending on the URL visited? 
Provide a code snippet – This snippet must change the text when tested. Placeholders showing that you would change the text here or what you could do to accomplish this are disqualifying.
Provide a single HTML file that demonstrates an understanding of:
Boilerplate HTML structure
Internal CSS, External CSS, and inline styles
HTML tables
HTML forms

- Your file must include:

    - Styles in a single style tag. You must also reference an external stylesheet (it does not need to be a real stylesheet, just reference one with a relative path). 
    - An external reference to a JavaScript file, either to a CDN or local file with a relative path.
    - One table with a single row and two table cells. Make the table 600px wide, centered, and 200px from the top of the screen. Achieve this however you like.
    - In the first cell, include a block of lorem ipsum text. Use inline styling to modify some or part of it.
    - Also in the first cell, include a placeholder image.
    - In the second cell, create a form with one text input that makes a "GET" request to your file.
    - Additional styling and design is not necessary, but feel free to add in additional markup that makes the document more accessible, and shows consideration for HTML best practices, including best practices for HTML used in email. What is normally included in a form? What is included in a table in an HTML email?

### Extra credit with Answers:

- Make the table cells stack on smaller screen widths. If you have trouble with this, alternatively you can make two divs below your table that stack on smaller screen widths.
    - I used a media query to stack the two cells on top of each other.  
- Include a script tag to do some sort of DOM manipulation.
    - I changed the background when you start to enter text into the form. 
- Add another field to your form with radio buttons.
    - I added 4 radio buttons for the seasons.
