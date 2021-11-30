## User Requirements

### Software Interfaces
1. Apache Maven								
   - Maven									
   - Version 3.8.2									
   - This system must use Maven which is a POM based project management tool. System will communicate its dependencies to Maven, which will be managed by the external software.
2. Spring Boot								
   - Version 2.5.5									
   - This system must use Spring Boot to run the application. System will communicate when it needs to build the application, and software will create that application during runtime.
3. Google Cloud Platform Datastore	
   - GCP Datastore								
   - This system must just use GCP Datastore for its database component. Communication occurs through either HTTPS or Google Cloud Interconnect & VPN. Data that will be transmitted by the system must be in the proper format of the table data structures in GCP Datastore.
4. AWS S3
   - We used an S3 bucket to upload images from our Spring Boot system.
   - Thymeleaf HTML views load images from the S3 bucket to display in-browser.

### User Interfaces
The main interface between the software product and the users will be a GUI, which will ultimately be a webpage with textboxes, checkboxes, buttons, display tables, and forms for users to fill out. The textboxes and checkboxes will be primarily for user inputs where users will specify the fields such as item title, cost, description, and category. In addition there will also be an image upload field, which will be optional. Buttons will be utilized for committing changes such as adding a new item, editing an existing item, or deleting an existing item. Additionally, the same UI elements will be used for the filter search portion of the project. The UI elements will have the same fields but different layout. As this is a web page, the main way that the user will physically communicate with the system will be through the standard keyboard and mouse setup.

### Product Functions
- GT Marketplace will enable its users to create new ite posts with the following fields: title, description, cost, category, and an optional image upload. Once created, these items will be able to be viewed by all users on the GT Marketplace home page.
- GT Marketplace will allow its users to view all of the item posts they made in a my posts tab on the application. In this my posts tab, the users will have the option and ability to edit or delete any of their existing posts. Once edited or deleted, the changes will be reflected on the home page and the my posts page.
- GT Marketplace will only allow Georgia Tech students to register and utilize the applications services. When registering a new user, the user must enter a valid GTID and Georgia Tech email for successful registration.
- GT Marketplace will have a filter search feature which will allow any user to search for specific items from all of the item posts. The filter options will include the following: item name, item cost, item category, item min and max cost.
- GT Marketplace will have a messages page that a user can use to send an email to another user. The messages page takes in a username and email message body, and then sends the email to the intended user.

### User Characteristics
- The intended users of this product are specifically Georgia Tech students, however the knowledge and expertise they must possess to operate the webpage will not be higher than that of general internet users. For convenience, the goal of the GT Marketplace UI design is to mimic that of existing marketplaces such as the Facebook Marketplace since general internet users would already know how to navigate in that environment. Moreover, the structure of the webpage is organized and well-labeled so that general internet users can understand what each component of the webpage does intuitively. 

### Assumptions and Dependencies
- One assumption is that users will be utilizing one of the later web browsers versions when running the web application. If they are not, of one of the dependencies is that if they are running a much older version such as Internet Explorer 1, the intricate frontend features such as an interactive map may not be compatible.
- Another assumption is that the developers have Java 8, or a later version installed to be able to run the undeployed version of the GT Marketplace as a Spring Boot application. If not, the web application will have to deployed to be hosted locally or through external services such as deployment through containers, or through Amazon Web Services or Azure. 
  - Thankfully, this concern was unwarranted as we were able to each develop locally. For the demos, we ended up hosting the project on an AWS Lightsail server.
  - Both local development and the demos are dependent on the GCP Datastore and AWS S3 bucket being operational. Otherwise, the application will fail to initialize.
- Apportioning of Requirements
    1. Evolution 0: Basic Project Functionality
    2. Evolution 1: GT Verification for Registration
    3. Evolution 2: Adding Image Upload Functionality
    4. Evolution 3: Adding Filter Search Feature
    5. Evolution 4: Edit/Delete Item Functionality
    6. Evolution 5: Email Functionality
    7. Evolution 6: Integration and Testing