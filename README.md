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

class train_char_LSTM :  

x_y : converting data to baches.  

train_char_LSTM_function : for training the model. Optimizer : Adam. Loss function : CrossEntropyLoss.  

class LanguageModel :  

get_next_states_and_output : gets a character and current hidden state and cell state, and returns output and next hidden state and cell state. 

convert_prefix_to_hiddens : gets a string and with the help of "get_next_states_and_output" function returns output and next hidden state and cell state.  

get_probs : gets a string and returns the probability of each character comes after the string.  

get_next_char : gets a string and returns the most probable character that comes after the string.  

generate_text : gets a string and t, and complete the sentence until it gets to end of the sentence "e", or the number of characters reach to t.  

get_overall_prob : gets a string and returns the probability of occurrence of the string in our language model.  

evaluate_per : gets sentences and for each of them generates the next characters according to first 25 characters, and then returns the "perplexity" of each sentence.  

evaluate_cer : like the "evaluate_per" function, except it returns the "character error rate" of each sentence.  

We used 200 first sentences of the test data for evaluation.
