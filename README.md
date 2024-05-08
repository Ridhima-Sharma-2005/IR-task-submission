# IR-task-submission
to create the webpage I used html and css and for connecting it to the backend I used google apps script to upload the files on the google drive.
starting with the structural framework of the webpage , i used css for the basic styling like defining the font, margin, padding, background colour. here I used container for layout purpose. it is styled to have a specific width, margin, background color, padding and many other things. similarly some styling is done to the tags like form, input, textarea , button i.e. it will be applied to anything that will be written between these tags. all this is done another style tag under head
then comes the body part which includes everything that will be shown on the webpage. I started with a division element with a attribute named class having value as container. this will implement the container styling on the element. then a form tag is used to create a form.
label tag is used to display text on the webpage and is connected to the input tag using for attribute. the input tag is used to specify a one line input with type defining the type of input expected(here, text or file) . each input tag is associated with a id which is unique for everyone and is same as the value of for in label tag. for file the type attribute of input tag would contain the value as file. multiple means that any format of the file is accepted  .after this there is a submit button to submit the form. the closing of the form tag closes the form. then comes the connectivity of the html with the backend.

a file named code.gs contains the script. it starts with a doGet function which is a reserved function that is called when the web app is accessed via an http get request. HtmlService.createHtmlOutputFromFile() method reads the content of an HTML file named 'index' and creates an HTML output object with that content. the next line helps to create  an I frame to help embed this web app in other websites.
another function used here is uploadFiles whose working is as follows
two variable filea and fileb is declared which stores the file uploaded by the user(file is retrieved using the name attribute of the file object in html code) . then a folder is retrieved from the google drive using its id and another subfolder is created within it with the name of the student to store the file uploaded by the student in different folders. then using filea and fileb variables two files are created in the folder just created. 
now to connect this script with the html file a script tag is created . the first line of code performs a function whenever the element with id submitBtn is clicked. the function include running  the function named uploadFiles in the google script. after the successful upload of the files a message flashes that the form is submitted successfully.

at the end the url generated of the webapp is used in a local html file using iframe tag which helps us to embed these files in any html file we want.

some anomalies in my webpage:
i stored the files uploaded in google drive but didn't store the the information typed by the student. this can be easily stored in a excel file which would be in the same folder and would be updated whenever a new student submits the form. the code for this has not been provided by me.

link of the google scripts
https://script.google.com/d/1lk-Or9VocCpUixNwW76pII-6PpM5u0cbNt2cIsBcztLnTkxcdsduHsIq/edit?usp=sharing
