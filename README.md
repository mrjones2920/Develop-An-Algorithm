# Develop An Algorithm

<h1>Introduction</h1>
An algorithm is a set of steps that can be used to solve a problem. Security analysts develop algorithms to provide the solutions that they need for their work. For example, an analyst may work with users who bring them devices. The analyst may need an algorithm that first checks if a user is approved to access the system and then checks if the device that they have brought is the one assigned to them.

In this lab, you'll develop an algorithm in Python that automates this process.

<h1>Scenario</h1>
In this lab, you're working as a security analyst and you're responsible for developing an algorithm that connects users to their assigned devices. You'll write code that indicates if a user is approved on the system and has brought their assigned device to the security team.

<h1>Task 1</h1>
You'll work with a list of approved usernames along with a list of the approved devices assigned to these users. The elements of the two lists are synchronized. In other words, the user at index 0 in approved_users uses the device at index 0 in approved_devices. Later, this will allow you to verify if the username and device ID entered by a user correspond to each other.

First, to explore how indices in lists work, run the following code cell as is and observe the output. Then, replace each 0 with another index and run the cell to observe what happens.

![image](https://github.com/user-attachments/assets/83ead49a-02e7-4ece-989b-57df89cafa14)

<h1>Question 1</h1>
What did you observe about the output when approved_users[0] is displayed and when approved_devices[0] is displayed? What happens when you replace each 0 with another index?

When approved_users[0] is displayed, the output is the first approved username from approved_users. When approved_devices[0] is displayed, the output is the first device ID from approved_devices. When you replace each 0 with another index, the output is the element at that index in approved_users, followed by the element at that index in approved_devices. For example, if you replace each 0 with 2, the output is the element at index 2 in approved_users, followed by the element at index 2 in approved_devices.

<h1>Task 2</h1>
There's a new employee joining the organization, and they need to be provided with a username and device ID. In the following code cell, you are given a username and device ID of this new user, stored in the variables new_user and new_device, respectively. Use the .append() method to add these variables to the approved_users and approved_devices respectively. Afterwards, display the approved_users and approved_devices variables to confirm the added information. Be sure to replace each ### YOUR CODE HERE ### with your own code before you run the following cell.

![image](https://github.com/user-attachments/assets/b99cefcc-ab1b-4f7f-9ab2-e9da1169b06a)

<h1>Question 2</h1>
After the new approved user is added, what did you observe about the output when approved_users is displayed and when approved_devices is displayed?

After the new approved user is added, their username is at the end of the approved_users and their device ID is at the end of the approved_devices.

<h1>Task 3</h1>
An employee has left the team and should no longer have access to the system. In the following code cell, you are given the username and device ID of the user to be removed, stored in the variables removed_user and removed_device respectively. Use the .remove() method to remove each of these elements from the corresponding list. Afterwards, display both the approved_users and the approved_devices variables to view the removed users. Run the code and observe the results. Be sure to replace each ### YOUR CODE HERE ### with your own code before you run the following cell.

![image](https://github.com/user-attachments/assets/8c74b4e3-824e-4258-b84a-05e4a4ac2736)

<h1>Question 3</h1>
After the user who left the team is removed, what did you observe about the output when approved_users is displayed and when approved_devices is displayed?

After the user who left the team is removed, their username is no longer part of the approved_users and their device ID is no longer part of the approved_devices.

<h1>Task 4</h1>
As part of verifying a user's identity in the system, you'll need to check if the user is one of the approved users. Write a conditional statement that verifies if a given username is an element of the list of approved usernames. If it is, display "The user ______ is approved to access the system.". Otherwise, display "The user ______ is not approved to access the system.". Be sure to replace each ### YOUR CODE HERE ### with your own code before you run the following cell.

![image](https://github.com/user-attachments/assets/92982069-5fee-4fbe-9a8c-1ee394279fb6)

<h1>Question 4</h1>
What message do you observe in the output when username is "sgilmore"?

When username is "sgilmore", the outputted message reads "The username sgilmore is approved to access the system." since "sgilmore" is an element of the approved_users.

<h1>Task 5</h1>
The next part of the algorithm uses the .index() method to find the index of username in the approved_list and store that index in a variable named ind.

When used on a list, the .index() method will return the position of the given value in the list.

Add a statement to display ind in the following code cell to explore the value it contains. Be sure to replace the ### YOUR CODE HERE ### with your own code before you run the following cell.

![image](https://github.com/user-attachments/assets/4536f885-0eaa-45df-a690-0d36b516c87c)

<h1>Question 5</h1>
What do you observe from the output when username is "sgilmore"?

When username is "sgilmore", the output is 2, which indicates that the index value of "sgilmore" is 2 in the approved_users. In other words, "sgilmore" is the third element in the approved_users. Indexing in Python starts at 0.

<h1>Task 6</h1>
This task will allow you to build your understanding of list operations for the algorithm that you'll eventually build. It will demonstrate how you can find an index in one list and then use this index to display connected information in another list. First, use the .index() method again to find the index of username in the approved_users and store that in a variable named ind. Then, connect ind to the approved_devices and display the device ID located at the index ind. Afterwards, run the cell to observe the result. Be sure to replace each ### YOUR CODE HERE ### with your own code before you run the following cell.

![image](https://github.com/user-attachments/assets/5c3db183-4d32-42e5-9124-2a20c664537d)

<h1>Question 6</h1>
What do you observe from the output when username is "sgilmore"?

When username is "sgilmore", the output is 4n482ts, which is the device ID that corresponds to "sgilmore". The third approved username in the approved_users is "sgilmore", and similarly the third device ID in the approved_devices is "4n482ts".

<h1>Task 7</h1>
Your next step in creating the algorithm is to determine if a username and device ID correspond. To do this, write a conditional that checks if the username is an element of the approved_devices and if the device_id stored at the same index as username matches the device_id entered. You'll use the logical operator and to connect the two conditions. When both conditions evaluate to True, display a message that the username is approved and another message that the user has their assigned device. Be sure to replace each ### YOUR CODE HERE ### with your own code before you run the following cell.

![image](https://github.com/user-attachments/assets/b75e7376-ccd0-49f2-afe3-5409f62317d0)

<h1>Question 7</h1>
What do you observe from the output when username is "sgilmore" and device_id is "4n482ts"?

When username is "sgilmore" and device_id is "4n482ts", the output consists of The username sgilmore is approved to access the system. on the first line and 4n482ts is the assigned device for sgilmore on the second line.

<h1>Task 8</h1>
It would also be helpful for users to receive messages when their username is not approved or their device ID is incorrect.

Add to the code by writing an elif statement. This elif statement should run when the username is part of the approved_users but the device_id doesn't match the corresponding device ID in the approved_devices. The statement should also display two messages conveying that information.

Be sure to replace each ### YOUR CODE HERE ### with your own code before you run the following cell.

(After you run the code once with a device_id of "4n482ts", you might want to explore what happens if you assign a different value to device_id.)

![image](https://github.com/user-attachments/assets/13aede05-6f98-4df7-be25-7c968698b340)

<h1>Question 8</h1>
What do you observe from the output when username is "sgilmore" and device_id is "4n482ts"?

When username is "sgilmore" and device_id is "4n482ts", the output consists of The user sgilmore is approved to access the system. on the first line and 4n482ts is the assigned device for sgilmore on the second line.

If username wasn't in the approved_devices list, the output would be a message that the user is not approved to access the system.

If username was in the approved_devices list but device_id didn't correspond with username, the output would be a message that the user is approved to access the system but the device ID is not assigned to them.

<h1>Task 9</h1>
In this task, you'll complete your algorithm by developing a function that uses some of the code you've written in earlier tasks. This will automate the login process.

There are multiple ways to use conditionals to automate the login process. In the following code, a nested conditional is used to achieve the goals of the algorithm. There is a conditional statement inside of another conditional statement. The outer conditional handles the case when the username is approved and the case when username is not approved. The inner conditional, which is placed inside the first if statement, handles the case when the username is approved and the device_id is correct, as well as the case when the username is approved and the device_id is incorrect.

To complete this task, you must define a function named login that takes in two parameters, username and device_id. Afterwards, call the function and pass in different username and device ID combinations to experiment and observe the function's behavior. Be sure to replace the ### YOUR CODE HERE ### with your own code before you run the following cell.

![image](https://github.com/user-attachments/assets/25b3d028-6f1b-4aac-a931-e34fc2aed56f)

![image](https://github.com/user-attachments/assets/c9250db9-3e61-4772-8734-c9ce2323982a)

<h1>Question 9</h1>
After Python enters the inner conditional, what happens when the device_id is correct, and what happens when the device_id is incorrect?

The following happens after Python enters the inner conditional:

When the device_id is correct, the inner if condition evaluates to True, and a message that the device ID is assigned to the user is displayed.

When the device_id is incorrect, the inner if condition evaluates to False, Python enters the else case, and a message that the device ID is not the user's designed device is displayed.

<h1>Conclusion</h1>
What are your key takeaways from this lab?

- Indexing a list is similar to indexing a string. Index values start at 0.
- The .append() method helps you add new elements to the end of lists.
- The .remove() method helps you remove elements from lists.
- The .index() method can be used on different types of sequences. They can be used not only with strings, but also with lists.
- With a list, the .index() method allows you to identify the position where a specified element is located in that list.
- If two lists contain information that correspond to each other in a specific order, you can use indices to pair elements from the lists together.
- Functions can be used to develop algorithms. When defining a function, you must specify the parameters it takes in and the actions it should execute.
