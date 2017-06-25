# rattlesnake
A python application that does noise cancellation


## Motive
*Following soon*


## Explanation
This python tool can do *Active Noise Cancellation (ANC)* respectively *Active Noise Reduction (ANR)*.
It reads in a stream of audio, either live or from a pre-recorded file and calculates an inverted signal for every byte
of the data stream utilizing an XOR operation.    
After the execution is finished the program calculates a median of the difference levels which reflects
the results of the algorithm. It also plots a graph with the results and displays it afterwards.    
    
*More details soon to follow*


## Installation
Clone the repo and install the requirements via pip:    
`pip install -r requirements.txt`


## Usage
Run the python script from your terminal and specify the mode you want to use:    
`python3 start.py --mode nth_iteration`

Argument        | Description
--------        | -----------
--live (-l)     | This is the 'live-mode' which records audio and inverts it on-the-fly.
--file (-f)     | This is the more basic 'file-mode' which expects a wave audio file (.wav) as a second argument. It then plays back the original file as well as the inverted audio to effectively cancel it out.
--playback (-p) | This is the 'playback-mode' that does exactly what one would expect. It can be used to test an existing file.
nth_iteration   | This argument is required and needs to be a number. It specifies on which nth iterations data is saved for calculating and plotting the results. The lower the value, the more precise the result.

Both modes are self-adjusting themselves during execution.


## License
[MIT](LICENSE)
