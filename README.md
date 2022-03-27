# Factory 

#### By _**Karl Starkweather**_

#### _An application for managers to track machines and engineers in a factory._

## Technologies Used

* C#
* .NET 5.0
* dotnet
* MySql/Workbench

## Description

This application allows managers to track machines and engineers in a factory. It includes the following features:
* Adding an engineer to the system.
* Viewing all engineers.
* Selecting an engineer to see their details.
* Adding a machine to the system.
* Viewing all machines.
* Selecting a machine to see its details.
* Assigning more than one engineer to a machine.
* viewing all engineers licensed to work on a machine.
* Assigning more than one machine to an engineer.
* viewing all machines an engineer is licensed to work on.

## Database Structure

![Database Structure Image](/wwwroot/img/DatabaseImage.jpg)

## Setup/Installation Requirements
* Clone the software from the GitHub repository
    - Open the terminal on your local machine and navigate to where you want to clone the project
    - Enter following command: <code> git clone https://github.com/KarlStarkweather/Factory.git </code>
* Setup/Import the data files
    - Download and install: MySql Community
    - Download and install: MySql Workbench
    - Determine if the MySql server is running locally by <code> mysql -uroot -p[The password you set up] </code> into the command line:
    - Open MySql Workbench. 
    - Once open select the Administration tab. 
    - Next select Data Import/Restore. This opens up the Data Import window with the Import from Disk tab open. 
    - Select the radio button for Import from Self-Contained File. 
    - Click the button with the three dots (if on windows) or two dots (if on mac) at the end of the path field. This will open a window to search for the sql dump file on your local disk. 
    - Navigate to the root directory of the cloned project
    - Select karl_starkweather.sql and click the open button. 
    - Next, press the New... button. This will open a window where you can choose the name of the imported schema. 
    - Choose a name appropriate to the project, (e.g. /Factory/) and click Okay. We'll need this name later when setting up the project to work with this schema. 
    - If on a mac, click the Start Import button. If on a windows machine, switch to the Import Progress tab on the Data Import page. Click the Import button. Finally, re-click on the Schemas tab. Right-click in the Schemas window, and select Refresh All. The imported schema should now be listed.
    
* Make sure to have dotnet-ef installed too.<br>
    - Enter <code> dotnet-ef --version </code> in the terminal if you are not sure whether you have it
    - If not installed, then enter:
        - <code> dotnet add package Microsoft.EntityFrameworkCore -v 5.0.0 </code>
        - <code> dotnet add package Pomelo.EntityFrameworkCore.MySql -v 5.0.0-alpha.2 </code>

* Open the project in VScode or your terminal/IDE of choice.
* Create a <code>appsettings.json</code> file in the root directory of the project folder. And add the following code replacing anything in square brackets with the information it represents specific to the project database:
```
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Port=3306;database=[DATABASE-NAME-HERE];uid=[USER-ID-HERE];pwd=[YOUR-PASSWORD-HERE];"
  }
}

```

* Now using your IDE navigate into the Factory/ folder and use the command <code>dotnet run</code> to launch the program. 
* The site should be available at the server address you used in the <code>appsettings.json</code> folder.


## Known Bugs

* _No known bugs_

## Contact Me

Let me know if you run into any issues or have questions, ideas or concerns:  
stark13@usa.net

## License

_MIT_

Copyright (c) February 2022 Karl Starkweather.
[MIT License](https://opensource.org/licenses/MIT)