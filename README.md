In this project, you are expected to write a program that calculates and keeps the tiredness of a rectangular 
field as a 2D int array (tirednessMap) given the information about which parts of the field has been planted in the 
previous years.  
The program will read the name of the file as a string which holds the planting input. The file will contain the following 
information: First the horizontal size of the rectangular field (sizeX) and the vertical size of the rectangular field (sizeY) 
will be given as int values. Then, a planting information will be given for each previous year as an information block. 
The information block will start with the year information (currentYear) and how many plantings have been made 
during that year (plantingCount), both as int values. Next, plantingCount many planting information will be given as 4 
int tuples: startXCoord, startYCoord, endXCoord, and endYCoord representing this smaller rectangular area has been 
planted in this year. 
This currentYear – plantingCount and that many plantingCount information blocks will keep continuing for each 
subsequent year until the currentYear’s value becomes 2017 which will be the last information block. 
Example input file: 
10 8 
2015 2 
0 0 5 5 
7 0 8 2 
2016 1 
0 0 5 5  
2017 2 
0 0 3 3 
7 0 8 2 
 
Each information will be given IN A SINGLE LINE within the file as seen in the example above. 
Using this information, your program will calculate the tiredness of each part of the 2D rectangular field as follows:  
• Each cell in the 2D int array will represent the tiredness of that part of the field. 
• The tiredness of each part starts at “0”. 
• The tiredness of each part increases by 1 every year the field has been planted. 
• The tiredness of each part decreases by 1 every year the field has NOT been planted to a minimum of 0. 
Example output tiredness map for the input given above: 
3 3 3 3 1 1 0 1 1 0 
3 3 3 3 1 1 0 1 1 0 
3 3 3 3 1 1 0 1 1 0 
3 3 3 3 1 1 0 0 0 0 
1 1 1 1 1 1 0 0 0 0 
1 1 1 1 1 1 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
Input:  
• The horizontal size of the field 
• The vertical size of the field 
• Yearly information block: 
o Starting with year information and number of plantings in that year 
o Then the top left and bottom right coordinates of each planting in that year 
Output: 
• The tiredness map of the whole field as a 2D int array 
NOTE: The coordinates of the top left corner part of the map is 0,0 and the maximum size of the field is 40, 40 
NOTE: No plantings given for the same year can overlap with one another. 
NOTE: You MUST use absolute address for the input file and put the file in the folder where your executable is. 
HINT: You should start with a 2D array where the value of EACH cell is 0. 
HINT: While calculating the map for the next year, using a temporary second 2D array is STRONGLY 
SUGGESTED (e.g., tirednessMap, newTirednessMap). 
Sample Input/Outputs: 


Input
fieldInfo1.txt 5 5 

File Contents (filename should be the 
same as in the input) 
2016 2 
0 0 2 2 
1 3 4 4 
2017 2 
1 1 3 3 
3 0 4 0 

Output
0 0 0 1 1  
0 2 2 1 0 
0 2 2 1 0 
0 2 2 2 0 
0 0 0 0 0 

Input
fieldInfo2.txt 10 10 

File Contents (filename should be the 
same as in the input) 
2014 3 
2 2 2 7 
5 4 8 7 
8 1 9 3 
2015 3 
2 2 2 7 
5 4 8 7 
8 1 9 3  
2016 4 
0 0 2 2 
3 8 6 9 
5 4 8 5 
8 1 9 3 
2017 2 
8 1 9 3 
9 8 9 9 

Output
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 4 4 
0 0 2 0 0 0 0 0 4 4 
0 0 0 0 0 0 0 0 4 4 
0 0 0 0 0 2 2 2 2 0 
0 0 0 0 0 2 2 2 2 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 0 1 
0 0 0 0 0 0 0 0 0 1 

Input
fieldInfo3.txt

File Contents (filename should be the 
same as in the input) 
5 5 
2014 1 
0 0 2 2 
2015 1 
0 0 2 2 
2016 0 
2017 0 

Output
0 0 0 0 0 
0 0 0 0 0 
0 0 0 0 0 
0 0 0 0 0 
0 0 0 0 0
