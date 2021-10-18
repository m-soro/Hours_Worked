# Time Log App
<img src='https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTBepozD0DfuxWa5mS21jkqMOzrlAdwegiBnw&usqp=CAU'>

>A [google colab notebook](https://github.com/m-soro/Hours_Worked/blob/main/Hours_WorkedV2.ipynb), that collects time logged in and logged out with a press of a button.  


𝐖𝐡𝐲?
For a few months, I was tracking my hours with an excel sheet, but it got tedious and a bit boring just entering data 🤷 I wanted something to automate this task and a coding project is fun! 👍

Plus, It gives me practice in python  💻 and I have something to work on if I ever wanted to refactor and tinker with my code down the road.

𝐇𝐨𝐰 𝐝𝐢𝐝 𝐈 𝐛𝐮𝐢𝐥𝐭 𝐭𝐡𝐢𝐬?
I started this project by reading and cleaning the data from my google sheets. Along the way I found some mistakes with my manual entries like wrong dates or day, this has to be fixed first. Then, I converted this data to a pandas DataFrame.

The challenging part is to create this entire logging app, where will I store it 🗄 ? How can I build a DataFrame that behaves just like excel? Like entering log in and log out in separate cells? I'm sure there was already solutions with this problem posted somewhere, but I wanted to create and come up with the solution myself.

My solution is to create a separate csv files 🗒 timein.csv and timeout.csv file, then concatenate these two to create a main DataFrame, if the length of timein and timeout logs are off, then I must have made a mistake in double logging or forgetting to log, a solution that I found was to have print statements that returns the number of logs.

Storage problem was solved using my google drive, I specified a path where I wanted my log to be saved and every entry is appended.

𝐖𝐡𝐚𝐭 𝐚𝐛𝐨𝐮𝐭 𝐥𝐨𝐠𝐠𝐢𝐧𝐠 𝐦𝐢𝐬𝐭𝐚𝐤𝐞𝐬?
This is where the challenging part started, My first solution was undo the last log. I did this by reading the file, find the last line of the file and 📝 re-write everything except the last line.

Another solution, is to replace the value in the DataFrame, using index. First, by finding 🔎 the log that needs editing, second, using the index to find which entry is to be edited then enter the edits manually. Then, re-write the original file.

**Libraries used**:
* pandas
* datetime
* pytz
* csv
* xcelwriter

**Features**:

* **Hours Analyses** - Average hours worked by week and day
* **Analyses Table** - Hours worked vs hour rate vs overtime rate
* **Back ups** - Auto saves into csv and excel file in google drive
* **Data Visualization** - Quickly see trends

**Functionalities**:

* log time or time out with just a click
* undo last log
* edit time in or time out
* number of records are returned after every log, to ensure accuracy


