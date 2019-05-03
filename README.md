# Command Prompt Tricks And Techniques.

> Pinting Command

### Syntax: __echo__ _your message_

```bat
echo Hi Command Prompt

echo I am programming Geek
```

> Tip: You can execute two different command In one line using & (and) Operator.


### Syntax: _command_1_ __&__ _command_2_

```bat
mkdir my_new_directory & copy *.txt my_new_directory
```

> Display Directories in the current directory

### Syntax: __dir__ 
```bat
dir     

dir /S
```

> Search For Any File

### Syntax: dir file_name_to_search

```bat
dir Hello.txt

dir /S Hello.txt

dir /S *.java

dir /S *batch*
```

> Search Every Hidden File Save On Any Location On Disk

### Syntax: __dir__ __*/S*__ __*/AH*__ [file_name_optional]

```bat
dir /S /AH

dir /S /AH *.exe
```

---

> Displaying File Content on Console

Syntax: __type__ _file_name_

```bat
type example.txt
```

> ### Tip: You can use __| more__ to take pause when screen overflows. 

```bat
type example.txt | more

dir /S | more
```

> Tip: Storing the sonsole output in a file.

```bat
echo "This is the text which will printed on console" > echo_file.txt

dir /S > drive.txt
```

> Tip2: Appending the output to the Existing File.
```bat
echo "This is the Initial Text" > file.txt
rem >> operator will append the file.
echo "This is another Statement" >> file.txt
```

> See the File Structure In Tree Structure

Syntax: tree [/A /T]
```bat
tree /A

tree /A > tree.txt
```

> Get the Battery Report of the Laptop

```bat
powercfg /batteryreport
```

---


> Open Window Expored Form where you are in command Prompt

```bat
rem . represents self
start .

rem .. represent partent
start ..
```

> Tip: Hold the controll key and use left or right arrow in order to jump word by word in cmd

#### Ctrl + left_arrow

#### Ctrl _ right_arrow


> Print the Current Date or Time

```cmd
date /T

time /T
```

> Getting all the available drives letters using cmd

```cmd
wmic logicaldisk get name
```

> Tip: Nevigate directly to other directory with out knowing the path.

Just use back slash and tab in order to autocomplete the directories namm

```bat
rem press tab to auto complete.
cd C:\\ press_tab
```


> ### Check weather you are logically connected to other device or not

syntax: __ping__ _other_device_ip_

```bat
ping 127.0.0.1

ping www.google.com
```

> ### Get the IP address of any website

syntax: __nslookup__ _website_name_

```bat
nslookup www.facebook.com
```

> ### Trace the Route of the device that you are connected with

syntax: __tracert__ _other_device_address_

```bat
tracert 127.0.0.1

tracert www.google.com
```

---


> ### Get All the Sytem Related Info

```bat
systeminfo
```


> ### Combine Two different file records to single file.

```bat
type "first_file.scv" > "combined.csv"  &   "second_file.scv" >> "combined.csv"
```


> ### Tip: If you want second command should only be run if the first command runs successfully

Syntax: _first_command_ __&&__ _second_command_

```bat
mkdir "new_folder" && copy "old_file.txt" "new_folder"
```

> ### Find something inside the file

syntax: __find__ _"string_to_find"_ _"file_name.txt"_

```bat
find "main" "JavaProgram.java"
```


> ### Tip: Use pipeline operator for special use of find command

syntax: command | "text_to_find"

```bat
ipconfig | find "Ipv4"
```
