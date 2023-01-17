# Hypothetical / ToDoMVC Tests

## Hypothetical Tests

| Automate | Reason | Don’t Automate | Reason |
| --- | --- | --- | --- |
| An addition function handles adding a positive integer to a negative integer | Given the simplicity of the task, it’s easy to test a lot of different integer combinations. | The "happy path" through the product which the CTO plans to demo in an hour is working as expected | Time to write up an automated test would take too long and therefore would be quicker to manually verify the demo is working as expected. |
| A program returns the first 1000 digits of pi correctly | Since the answer is a constant with several digits that never changes, this is a prime candidate for automation. | A workaround for some functionality is effective, knowing it's to be rewritten and replaced with something proper in two weeks time | Given that the functionality is going to be rewritten, there would be no point implementing automation at this time. |
| A website renders appropriately in Safari, Chrome, Firefox, Edge, Vivaldi and Brave | Due to time restraints of manually testing. (Caveat - may need human verification for particular visual elements) | An old, deprecated (and soon to be removed) bit of functionality still works, when a newer method for that functionality already exists | Would be a waste of time since the old code is soon to be irrelevant. |
| A website's dark/light theme can be applied and changes the site | This is an easy check. Also, screenshots can be taken to store and checked by people later. |  |  |
| The website's background colour is pure white (i.e. in hex #FFFFFF) not off-white/etc. | This is an easy check to automate. |  |  |
| A website's colour contrast is appropriate for users with different types of colour blindness | This can be checked through simple automation but may need human visual confirmation. | A website's colour contrast is appropriate for users with different types of colour blindness | This can be checked through simple automation but may need human visual confirmation. |
| The system fails gracefully when put under extreme load, such as having an excessive number of users in parallel | To simulate multiple users, automation would be a very efficient way of carrying out the task. |  |  |
| The Copyright symbol and version number are printed in the About dialog of each daily build of the product | This is a daily routine check which can easily be automated and checked with asserts. |  |  |
| A mobile phone displays a helpful number of WiFi signal bars as the phone moves nearer to/further from the router | This check can be done by checking the strength with asserts. |  |  |
| The system is still responsive under a normal/expected load of users using it at the same time | Load of users (possible mocking) could be injected to test responsiveness. |  |  |
|  |  | The accompanying manual pages for the newly added feature accurately describe how to use | Intricate reviewing of text needs human verification (since it is read by humans) |

## ToDoMVC Tests

| Automate Now | Automate Later | Don’t Automate | Reason | Test Type |
| --- | --- | --- | --- | --- |
| Can't add an item with an empty value |  |  | Simple Unit Test | Unit Test |
| Can add a value with a single character |  |  | Simple Unit Test | Unit Test |
| Check that every single accented character and symbol is supported |  |  | Simple Unit Test | Unit Test |
|  | Check that every single emoji character is supported |  | Simple Unit test with a lower priority. | Unit Test |
| Double clicking an item enables editing of ToDo item. |  |  | Simple Unit test with essential functionality. | Unit Test |
| If you click Escape during edit, it should cancel the modification |  |  | Simple Unit test with essential functionality. | Unit Test |
| A ToDo item can be ticked-off (it will appear with a line through it) |  |  | Simple Unit test with essential functionality. | Unit Test |
| A completed ToDo item can be unticked again |  |  | Simple Unit test. | Unit Test |
|  | A ToDo item can be reordered by dragging it up or down in the list |  | Once enhanced feature is introduced, look into automating. | Unit Test |
| Delete an incomplete ToDo item |  |  | Simple Unit test | Unit Test |
| Delete a completed ToDo item
 |  |  | Simple Unit test | Unit Test |
|  |  | Clicking the down arrow symbol next to the "What needs to be done?" box will 
toggle all items to Completed or Not Completed | Feature advised for alteration from arrow to checkbox.  | Unit Test |