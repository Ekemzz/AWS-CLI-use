# AWS-CLI-use

PRE REQUISITE
AWS configuration steps. The CLI is configured for the aws account user with priviledge to create IAM users and other IAM functionalities.

In the 3 images below, An IAM USER nina-admin with IAM permissions was created and the access key and secret keys were generated.
<img width="939" height="420" alt="image" src="https://github.com/user-attachments/assets/0c377d22-e962-4434-880c-5223112bc3bb" />
<img width="938" height="403" alt="image" src="https://github.com/user-attachments/assets/c7258338-16b9-44c5-b69f-d4ca14d0df4e" />
<img width="951" height="437" alt="image" src="https://github.com/user-attachments/assets/1b49f069-6091-4978-bf78-b5502e2aad0a" />
<img width="940" height="437" alt="image" src="https://github.com/user-attachments/assets/1bf074aa-bbfe-4cf5-af00-0615ef0e5bd5" />

In the image below, the CLI was configured for aws using the access key ID, secret access key, region name and output format.
<img width="799" height="455" alt="image" src="https://github.com/user-attachments/assets/7157396e-bc93-413a-a8f7-263938419085" />




SCRIPT
✅ What the script Does
The script tests IAM functionality by:

Defining an array of IAM usernames (e.g. 5 users).

Looping through each name in the array.

For each user:

Attempts to create the IAM user using the AWS CLI.

Checks the result using $? (the command's exit status).

Prints a success or error message based on whether the user was created successfully or already exists.

A control flow of the script is shown below.

1. This image below capture the create_iam_users function. The for-loop utilises user in an array of IAM_USER_NAMES.

 <img width="881" height="425" alt="image" src="https://github.com/user-attachments/assets/9a4c1add-1cbc-42e1-8851-e5d389c91109" />

2. the image below captures the create_admin_group function. the if-else loop checks for the admin group in the account, and when not found it creates an admin group otherwise, it outputs "Admin group already exist".
 <img width="797" height="455" alt="image" src="https://github.com/user-attachments/assets/92cb65ca-fa9c-4392-b4d8-6cb1eab2f6df" />
 3. The  image below captures the add_users_to_admin_group function. the if-else loop was used to control the addition of each user to the admin group.The if-else loop was used to control the commands to either add users or abort with an output "Failed to add user to admin group"

 <img width="800" height="454" alt="image" src="https://github.com/user-attachments/assets/200ec34c-ec36-492b-8297-c1f1852e18a3" />

4. the image below  has the main function which ensures first that the cli is configured for aws before calling out the previously setup functions
 <img width="536" height="320" alt="image" src="https://github.com/user-attachments/assets/48d7ba24-5341-46fc-b3c9-fb36e43e0516" />


TERMINAL demostration
1. the 1st image describes the aws configure command and shows tha the cli has been configured. the aws-iam-manager.sh file is edited with the functions earlier explained. the mode was changed to executable.
<img width="855" height="477" alt="image" src="https://github.com/user-attachments/assets/6395ec2a-78ed-446d-99b0-05ff96087c1e" />

2. the script is ran on the second image and IAM users were entered. tom jerry matt cynthia sofia. all were created.
<img width="800" height="451" alt="image" src="https://github.com/user-attachments/assets/88d9dba1-0ad8-4390-af2e-03e4b06950c0" />

3.the admin group was created with the admin permissions policy attached. and the users were added to the group in this image.
<img width="799" height="452" alt="image" src="https://github.com/user-attachments/assets/760f6c15-2009-46b4-a27c-bd3c04008c0a" />






CONSOLE 
1. this shows the console for confirmation of the users created and the group belonged.
<img width="951" height="455" alt="image" src="https://github.com/user-attachments/assets/3d29ec8e-ca6b-4c1e-aa8b-e42343a02455" />
