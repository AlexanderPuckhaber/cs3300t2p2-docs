## Test Strategy

### Testing Plan
We planned to write unit tests first to make sure every function works as expected. However, we ended up not doing that.
Instead, we used some code snippets to help us initialize models for testing, and conducted extensive manual testing of both the frontend and backend.

#### Technology
We used Shell commands to create, query, and delete Users and InventoryItems.

#### Manual Tests
Below are some of the manual test performed:
- Registration 
  - Checked if email field of registration page ended in "@gatech.edu"
  - Checked if GTID field of registration page started with "903" and has 9 digits
- Adding/Deleting/Editing Post Functionality
  - Added single title field to determine if inventoryItem was posted into the repository and displayed on the Home Page and the My Post Page
  - Performed editing and deleting on items while printing the full inventory repository is printed to the console on each action
- Filter Search
  - Each addition of inventoryItem field was tested and sorted on respective characteristics to see if the correct data was read from the object
- Email Functionality
  - Hard coded default email recipient to ensure proper delivery of email
  - Changed hard coded recipient to be th einput of text box entry
