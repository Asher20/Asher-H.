Project 2

The objective of the second project was to take in a station ID string and comppare it to other station ID's
and perform certain calulations on in such as finding the Ascii values.

The PosAvg class is the class that was used to get the first few lines of output. THe contructor takes in an input from the
driver which was the string "OKCE" which would be used throughout the class to campare the other station ID"s too.
Then it read in the lines from the Mesonet.txt file and added all of the station ID's from that file to an array list 
named inputFile. The first line of the output wanted to know what the index of the input string "OKCE" in the 
Mesonet.txt file. To get this value i used the inputFile.indexOf(inputId) in the indexOfStation method which 
returns the index of the input ID in the inputFile ArrayList. The next line of output wanted the names of the stations
at the index one above and below and also two above and below the input ID. To acomplish this i used
inputFile.get(x - 1), inputFile.get(x + 1), inputFile.get(x - 2), inputFile.get(x + 2)) where x was inputFile.indexOf(inputId);
and formatted it to output correctly. What inputFile.get(x + n) does is get the is get the name of the entry in the inputFile
at x + n.

The next three lines of the output had to do with gitting the Ascii values of the input station ID and this was done
in the MesoInherit class. I started by reading in the station ID "OKCE" and calculating the Ascii value of each letter.
By reading in each letter of the string and casting them to an int you end up returning a number which is the ascii valye
of that particular letter. So i read in each letter of the string "OKCE" and cast them to and int and added them all together
and divided them by 4 to get the average of the ascii values. Since the ascii calculation returned a double I rounded the average up 
a number and down a number using math.ceil() and math.floor(). For the next part of the output we needed to cinvert the average
we found in the last part back into a letter. I did this by casting the average value back to a char.

For the final lines of the output I used the letterAvg class. We were supposed to find the stations that have the same starting letter
as the average we had caluclated before. I started by adding all the stations who had the same ascii average as the averge of the input ID 
into a ArrayList. I then returned the names of the stations and the sum of all of the stations in the required format.