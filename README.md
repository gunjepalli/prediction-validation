# prediction-validation
This task is implemented in Java. The run commands are specified in the run.sh file. The input and output files are passed as command line arguments along with the folder name.
avac ./src/PredictionValidation.java
java -classpath ./src PredictionValidation ./input/actual.txt  ./input/predicted.txt ./input/window.txt ./output/comparision.txt

Approach:

HashMaps<Integer,HourValues> are used to store sum of error values and their count for each hour.The output values are stored as the members of a class with start hour, end hour and the avg error.

Input files are read  and  the values are stored in arraylists.

sum of errors are caluclated and their count for each hour, to directly find the average based on window size using the
values, to reduce computation

Average of hours in the window are calculated using the sum and n (count) values stored by hour

Class HourValues is created  which is used to store sum and count values for each hour

All these operations are performed in different methods for modularity.

Data processing is done to handle the '|' operator in between the values.
