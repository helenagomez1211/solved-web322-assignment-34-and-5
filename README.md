Download Link: https://assignmentchef.com/product/solved-web322-assignment-34-and-5
<br>
This assignment is a continuation of Assignment 1 and 2, thus all the requirements for this assignment is to be made “on top” of your Assignment 1 and 2.




<h1>Assignment 3</h1>

<h2><strong>Application Architecture</strong></h2>




<ol>

 <li>Your application <strong>MUST</strong> be structured <strong>FULLY </strong>according to the MVC Design pattern. Thus, your views, models and controllers must be separated as per the design pattern requirements.</li>

</ol>




<ol>

 <li><strong>All</strong> sensitive credential information <strong>must</strong> be stored in <strong>environment variables</strong>.  Examples include: your sendgrid access token, MongoDB connection string, etc. Implement environment variables locally using the <a href="https://www.npmjs.com/package/dotenv">dotenv</a> 3rd party package.</li>

</ol>

<h2><strong> </strong></h2>




<h2><strong>User Registration Module </strong></h2>




You are required to implement database functionality for your registration page that was previously implemented in Assignment 1 and 2. Thus, when a user fills out the registration form and then hits the submit button, provided that all the validation criteria were not violated, your website must then create a user account in your database.




<strong>Once the user account is created, your web application must then redirect the user to a dashboard page.</strong>




Regarding your database functionality, the following rules must be followed:




<ol>

 <li>Setup and configure a MongoDB cloud service using MongoDB Atlas <a href="https://www.mongodb.com/cloud/atlas">https://www.mongodb.com/cloud/atlas</a>.</li>

 <li>Connect your web application to your MongoDB database using an ODM called <strong>Mongoose.</strong></li>

 <li>Name your database and collections appropriately.</li>

 <li>Ensure that the email field in your registration form <strong>is</strong> <strong>unique</strong>, thus your application must prohibit different users from having the same email in the database.</li>

 <li>Passwords <strong>must not</strong> be stored in plain text in the database; thus, your application must store passwords in an encrypted format. You can use a 3rd party package called <a href="https://www.npmjs.com/package/bcryptjs"><strong>bcryptjs</strong></a> to do the aforementioned.</li>

</ol>




Note:

<ul>

 <li>For MongoDB, see week 8 lecture Notes: <a href="https://web322.ca/notes/week08">https://web322.ca/notes/week08</a></li>

 <li>For bcrytptjs, see week 11 lecture Notes : <a href="https://web322.ca/notes/week11">https://web322.ca/notes/week11</a></li>

</ul>




<h2><strong>Authentication Module</strong></h2>




You are required to implement a fully functional authentication module with the following features:




<ul>

 <li>Your application must allow a Data Entry Clerk and customers who want to purchase meal packages, to <strong>log-in via the login form created in Assignment 1 and 2.</strong></li>

 <li>Upon a successful authentication (entering an email and password pair that exists in the database) <strong>a session must be created to maintain the user state until they have logged out of the application. </strong></li>

 <li>Upon an unsuccessful authentication, the application <strong>must</strong> display an appropriate message (Example:<strong> Sorry, you entered the wrong email and/or password</strong>)</li>

 <li>Also, after successfully authenticating, the application must determine if the person logging in is a data entry clerk or a regular user and will be redirected to their respective dashboard.</li>

 <li>A customer will be directed to a user dashboard and a data entry clerk will be directed to a data entry clerk dashboard.</li>

 <li>Both dashboards, must show the user’s name (first name and last name) and a logout link</li>

 <li>The logout link must destroy the session created when the user initially authenticated.</li>

 <li>Specific routes can only be accessed when users are logged-in, thus those routes must be protected.</li>

</ul>




Note:

<ul>

 <li>For implementing session and protecting routes in Express app, see week 11 lecture notes : <a href="https://web322.ca/notes/week11">https://web322.ca/notes/week11</a></li>

</ul>
















<h1>Assignment 4</h1>

<h1></h1>

<h2><strong>Data Entry Clerk Module</strong></h2>




You are required to implement a Data Entry Clerk module that allow a data entry clerk to do the following:




<ol>

 <li><strong>Create Meal Packages:</strong> The Data Entry Clerk must be able to add new meal packages to the database. See the following data that must be added when a product is created:

  <ol>

   <li>Meal Package name,</li>

   <li>Meal Package price,</li>

   <li>Meal Package description or details,</li>

   <li>Meal Package food category</li>

   <li>The number of meals inside the package</li>

   <li>Set Meal package as a top package to be shown on the home page (or not).</li>

   <li>Upload a photo of the meal package (to keep the project simple, only upload one image per meal package).</li>

  </ol></li>

</ol>




<ol>

 <li>Ensure that all created meal packages that were entered into the database are populated on the front-end of the web application, specifically on the meal package listing page that was created in Assignment 1 and 2. Additionally, only meal packages that were set as “Top Meal Packages” should be populated in the “Top Meal Package” section of the home page. <strong>Please note, a visitor to the web application does not need to be logged in to view the meal packages that were created by the data entry clerk.</strong></li>

</ol>

<strong> </strong>

<ol>

 <li>Ensure that a user can only upload an image, i.e. jpgs, gifs, or pngs, for the meal package photo.</li>

</ol>

<strong> </strong>

<ol>

 <li>View a list of all created meal packages.</li>

</ol>




<ol>

 <li>Edit and change meal package details for a selected meal package. Example: price, title etc</li>

</ol>




Please note, a Data Entry Clerk must be logged-in to the web application to be able to do the aforementioned (create meal packages, view all created meal packages, edit and change meal package details). To facilitate the logging in of the Data Entry clerk, create a regular user in the Front-End and then long into your MongoDB Atlas account and manually change a field in the document to make allow the application to able to make the distinction between customer vs data entry clerk – <strong>I will further expound on this in class.</strong>










<h1>Assignment 5</h1>

<h2></h2>

<h2><strong>Meal Package Description Page</strong></h2>




Only logged in users should be able to “purchase” meal packages by adding selected meal packages to their shopping cart.




From the meal package listing page, when a user clicks on a particular meal package, they should be navigated to the <strong>Meal Package Description page </strong>of the clicked meal package and from that page they can add the meal package to their shopping cart.




Sample of a Product Description Page Example:







The Meal Package Description page of any meal package should list the following:

<ol>

 <li>Meal Package Image</li>

 <li>Meal Package title</li>

 <li>Meal Package description</li>

 <li>Meal Package price</li>

 <li>No of meals within the package</li>

 <li>Add to order</li>

</ol>




When the user clicks the “<strong>Add to order</strong>” button, the given package will be added to the user’s shopping Cart.







<h2><strong>Shopping Cart Module</strong></h2>




The customer’s dashboard should have a link to the logged-in user shopping cart. This page must display all the meal packages that were added to the shopping cart and how much of each package was added for the given user. Also, the page should have a “Place your order” button.










See Example




When the “<strong>Place your order</strong>” button is pressed, your web application should “clean” your shopping cart, send an email to the logged in user’s email, indicating all the packages purchased and the quantity amount for each meal package purchased as well as the customer’s order total.