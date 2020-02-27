# jsonnote
 A simple utility for working with JSON files.  
 
 Contains a small class jsonnote with the following attributes:
  

#### *Properties:* ####


   *filename* - name of the file without the extension (extention '.json' will be added automatically).

   *location* - location of the file. Once set, the file can be found and read from or write into.

   *contents* - JSON contents of the class instance.<br>  



#### *Methods:* ####

   *full_path()*

   *file_exists()*

   *is_empty()*      - returns True/False depending on whether the contents of the class instance are empty

   *get_from_file()* - reads contents from the JSON file

   *save_to_file()*  - saves contents in the JSON  file

   *clear()*         - empties the contents

   *destroy()*       - empties the contents and erases the file from the disc

   *reset()*         - empties the contents, destroys the file and sets 'filename' and 'location' to 'None'<br>



 #### Example of use: ####

 \>>> from jsonnote import jsonnote

\>>> x=jsonnote()

\>>> x.filename = 'temp'


\>>> x.location

\>>> x.location = '.'

\>>> x.full_path()

'./temp.json'

\>>> x.contents = {'fruits': ['apple', 'pear', 'orange'], 'veggies': ['potato', 'cucumber'], 'dairy': 'milk'}

\>>> x.mustsave=True

\>>> x.save_to_file()

 \>>> y=jsonnote()

\>>> y.filename = 'temp'

\>>> y.location='.'

\>>> y.file_exists()

True

\>>> y.contents

{'fruits': ['apple', 'pear', 'orange'], 'veggies': ['potato', 'cucumber'], 'dairy': 'milk'}

\>>> y.contents['fruits'][1]

'pear'


\>>> y.mustdelete=True # *False by default; if False the file is not deleted

\>>> y.destroy()

\>>> y.file_exists()

False

\>>> y.contents

{}
