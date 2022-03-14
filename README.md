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

![binary file read by wordpad]()
