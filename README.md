This contains the code used in the development of a frequnecy monitoring device:

**Zero Corossing Detects**- prints the correct frequency out on serial 

**Internet time protocols**- connects to WiFi, synchronises time, prints on serial

**OLED_NTP**- connects to wifi, synchronises time, prints data and time on OLED with dummy value of frequency 

**Upload average freuqnecy_NTP_OLED**- uses imterrupts to find frequnecy, connects to wifi, samples 200 frequnecy data points, finds average of those, uploads ave rage frequnecy to ThingSpeak, displays average frequency (with date and time frequency calculated) on OLED

**Concurrency in software**-  uses mutex and semaphors in a priority based concurrent code, task 1 calculates frequency, task 2 prints frequncy on new line in serial. 

**bulk upload with dummy variables**- upoloads data in bulk to thing speak using dummy variables

**Frequency_bulk_upload**- frequency is calculated and uploaded in bulk to thingspeak




References to 
