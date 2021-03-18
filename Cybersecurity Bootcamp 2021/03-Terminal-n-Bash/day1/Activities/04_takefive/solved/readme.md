## Solution Guide: Take Five and Practice the Command Line

- First, navigate into the `Cybersecurity-Lesson-Plans/03-Terminal/student/take_5` folder on your VM (virtual machine). To do so, run the following commands:
      
  - `cd Cybersecurity-Lesson-Plans/03-Terminal/student/`
  - `cd take_5`

- Create a folder called `Internal_Investigation`:
    
  - `mkdir Internal_Investigation_Employee_A`
    
-  Confirm the folder was created:
    - `ls`
          
- Navigate into `Internal_Investigation`:

  - `cd Internal_Investigation_Employee_A`

- From within the `Internal_Investigation_Employee_A` folder, print the working directory to confirm you are in the correct location:
    
  - `pwd`
            
   This should display: 
  ```
   Cybersecurity-Lesson-Plans/03-Terminal/student/Internal_Investigation_Employee_A/
  ```
    
- Create three files inside the `Internal_Investigation_Employee_A` folder: `email_evidence`, `log_evidence`, `web_evidence`:

  - `touch email_evidence log_evidence web_evidence`
           
    We created three files with one command by putting a space between each of the file names. (You can also create them one at a time.)
    
- Delete the file called `web_evidence`:
   - `rm  web_evidence`
           
- Display (list) all the files created:
  - `ls`
            
- The two files that display are: 
  ```
  email_evidence 
  log_evidence
   ```
            
- Lastly, clear the terminal window:
   - `clear`
--- 
© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
