# Language-Model-RNN
Character Level Language Model with Recurrent Neural Network  
The data, which is persian news, is in this link : https://drive.google.com/file/d/1vtIG0NgHNPKv1yuE9aqrqVcmfGIICKNj/view  
and we just use the "text" column.  

class DataPreprocessor:  

clean : deleting characters that are not main characters, replace numbers with "N" , add "s" to beginning of sentences and "e" to end of them.  

count_chars : returns a dictionary of characters and their frequencies, the number of unique characters and the number of all characters.  

tokenize : returns 2 dictinaries char2index, which maps each character to an index, and index2char, which maps each index to a character.  

char_to_index : gets a string and returns the number of each character in the string.  

index_to_char : gets numbers and returns the corresponding string.  

char2index.txt : characters and their corresponding number.  
index2char.txt : numbers and their corresponding character.  

class define_model : 
<img width="353" alt="image" src="https://user-images.githubusercontent.com/97177956/203593154-e3ddbddb-ec58-44ad-b450-c7848a8fdcdf.png">
