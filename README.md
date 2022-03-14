# IntroToProg-Python_Mod07

      Joel Quispe
      3/11/2022
      Foundations of Programming: Python
      Assignment 07 Overview
      
##        Using Error Handling and Pickling data 

In this assignment, python error handling and pickling were discussed. As well as opening files options. In Topic 1, I added Python handling webpages that reiterated the information from the online class videos. Also, I included screenshots of code that I wrote and executed to show ‘try/except’ error handling and pickling module. 

###     Topic 1. Find Python Exception Handling webpages

[exception handling webpage1](https://www.tutorialspoint.com/python/python_exceptions.htm)
- The reason I liked this webpage is because it lists a lot of common exceptions used. Instead of listing all of them which can be overwhelming to look at or search. It also lists examples and explanations.

[youtube video of exception handling](https://www.youtube.com/watch?v=NIWwJbo-9_8)
- This web video is helpful, because it is small ~10min and explains the exception. 


###     Topic 1. Find pickling webpages

[youtube of pickling basics](https://www.youtube.com/watch?v=z455OFnPjsI)
- This video is short and goes into the very basics of pickling files.

[Tutorial webpage of pickling examples](https://www.tutorialspoint.com/python-pickling)
-	I like this webpage, because it has examples of pickling and how to use the pickling module. 


### Topic 3. 
Python code to make binary file: 
```python
import pickle

sample_file_dict= {'Id':"John",'floor':"first floor", 'room':"B1"} #sample information in dictionary data
pickled_file = open("sample_dict_file.dat", 'wb') # This makes a new .dat file , binary file
pickle.dump(sample_file_dict,pickled_file) # The dump command writes all the data to the 'sample_dict_file.dat file that was opened
pickled_file.close() # The file is closed
```

![binary file read by wordpad](https://user-images.githubusercontent.com/100054021/158120171-f5076e52-ea17-4066-8db9-8451631ebc26.png)

binary file read by wordpad


### Topic 4
Python code to make exception:
```python
import pickle

sample_file_dict= {'Id':"John",'floor':"first floor", 'room':"B1"} #sample information in dictionary data
pickled_file = open("sample_dict_file.dat", 'wb') # This makes a new .dat file , binary file
pickle.dump(sample_file_dict,pickled_file) # The dump command writes all the data to the 'sample_dict_file.dat file that was opened
pickled_file.close() # The file is closed

'''To convert the binary file back to a dictionary data and print'''
pickled_file = open("sample_dict_file.dat", "rb") # This will load up the binary file
unpickled_file = pickle.load(pickled_file) # This converts the binary to a dictionary data
print (unpickled_file) # This prints the 'unpickled' data from


# Example of Exception error handling
# This will use the exception of wrong file used to open file
# File used is the one from pickle example, sample_file_dict.txt
try:
    file_name=str(input("enter name of file: ")) #This requests the file name
    Dic_File= open(file_name,"r") #This will open file
    for row in Dic_File: # reads out each row
        print (row) # print the correct file in binary format.
except FileNotFoundError as e:      #I used the specific exception of file not found
    print(file_name + "\tfile not correct")     #prints the value entered and description of error
    
```

![image_of cmd line output](https://github.com/jdquispe01/IntroToProg-Python_Mod07/blob/main/cmd_file_exception1.JPG)

Image of exception with code above 
The next image is with correct file name. 
![image with correect file name](https://github.com/jdquispe01/IntroToProg-Python_Mod07/blob/main/cmd_file_exception2.JPG)


### Summary
This assignment went over the importance of error handling and how it is best used to allow users to understand errors that can be made by the ‘end-users’. This is very useful when the code is tested by someone who is not familiar with the code or python. The pickling module was also explained in how to convert data into binary format for easier handling and copying from computer to another computer. The binary file is not human readable but can be easily converted back to its original version. 
Making modules from within the modules offered by the Python installation were explained in the videos and in the on-line web searches. 
