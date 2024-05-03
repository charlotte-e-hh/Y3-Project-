The **'Testing'** folder contains the raw results from the tests conducted 

 **analysis code for accuracy** - MATLAB code used for data processing and creating figures to understand the data
 
 **comparioson with literature circuit file**- conatins 2 folders of scope images 1 for literature and the other for my circuit and an Excel sheet with data from the comparison between the circuit in [35] and my device
 
 **device vs scope frequency test**- data from testing the integrated device against scope frequency monitoring 

 **Filter testing folder**- contains data from filter testing both transformers (10VA and 0.35VA) and the simulink model used 

 **frequency_firmwave folder**-contains data from a static frequency being tested on the micrcontroller only (the name of each file is the frequency that was tested)
 


The'**Firmware'** folder contains the code used in the development of a frequnecy monitoring device:

**Zero Corossing Detects**- prints the correct frequency out on serial 

**Internet time protocols**- connects to WiFi, synchronises time, prints on serial

**OLED_NTP**- connects to wifi, synchronises time, prints data and time on OLED with dummy value of frequency 

**Upload average freuqnecy_NTP_OLED**- uses imterrupts to find frequnecy, connects to wifi, samples 200 frequnecy data points, finds average of those, uploads ave rage frequnecy to ThingSpeak, displays average frequency (with date and time frequency calculated) on OLED

**Concurrency in software**-  uses mutex and semaphors in a priority based concurrent code, task 1 calculates frequency, task 2 prints frequncy on new line in serial. 

**bulk upload with dummy variables**- upoloads data in bulk to thing speak using dummy variables

**Frequency_bulk_upload**- frequency is calculated and uploaded in bulk to thingspeak

**MATLAB_unpacking code**- the code used to unpack timestamped data sent to thingspeak

**Integrated code**- final integrated code combining, frequency detection, timestamping, OLED display, Bulk upload

References in the code will be indicated where appropriate: 

code  uses the Json Buffer format from mathwork documentation (makers of ThingSpeak) https://uk.mathworks.com/help/thingspeak/continuously-collect-data-and-bulk-update-a-thingspeak-channel-using-an-arduino-mkr1000-board-or-an-esp8266-board.html accessed 02/05/2024 which was then adapted for my variables 

code uses mathworks documentation for single upload to ThingSpeak https://uk.mathworks.com/help/thingspeak/write-data.html accessed 02/05/2024

code uses Arduino Libraries for the OLED https://www.arduino.cc/reference/en/libraries/oled-ssd1306-sh1106/ accessed 02/05/2024 which was then adapted for my varaibles 

code adapted from the arduino libraties https://github.com/arduino-libraries/NTPClient accessed 02/05/2024 was used for NTP
