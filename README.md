# Enhanced ANPR for Algerian plates
Algerian automatic vehicle number plate recognition with data extraction using Python's openCV and easyOCR without any Machine Learning, with a custom algorithm that enhances and corrects the values detected for low-quality images.

The **main idea** is to find the plate, crop it, zoom it and apply easyOCR methods ( reader.recognize() & reader.readtext() ) to read the digits and then send the 2 results to the algorithm to process them, fix common errors and output the most accurate plate number to finally extract information about the car.

## Examples:
![image](https://github.com/Azed1ne/Enhanced-ANPR-for-Algerian-plates/assets/123888749/79e50e15-de28-4088-90e6-4818e5bed227)


![template2](https://github.com/Azed1ne/Enhanced-ANPR-for-Algerian-plates/assets/123888749/5c4598d9-98af-4890-8dba-8dfcbf1bb233)

## Algerian registration plates facts:
+ Being composed solely of numbers, they are one of the few vehicle registration plates which can accurately be referred to as '**number plates**'.
+ The registration mark takes the form of three groups of digits separated by a space.
- The **first group** of numbers comprises 5 or 6 digits that make up the vehicle's actual registration/serial number.
* The **second group** of numbers is always composed of 3 digits, the first one indicating the class of the vehicle in accordance with the following list:
  1. Private Vehicles.
  2. Trucks.
  3. Vans (Camionettes).
  4. Buses.
  5. Tractor units.
  6. Other Tractors.
  7. Special vehicles.
  8. Trailers.
  9. Motorcycles.
- The other 2 digits represent the year in which the vehicle was manufactured, for ex: 99 = 1999, 06 = 2006 ..etc.
- If the second ( middle ) group contains "00" it means the car is newly purchased and has a temporary plate. 
- The **third group** of numbers contains 2 digits representing the wilaya (city) or province where the vehicle was first registered ( from 01 to 58 ).
- 
**Example:**

![image](https://github.com/Azed1ne/Enhanced-ANPR-for-Algerian-plates/assets/123888749/6a931948-eccf-44ba-92ba-4fd2b3802195)

More info can be found [here](https://en.m.wikipedia.org/wiki/Vehicle_registration_plates_of_Algeria) or [here](https://www.autobip.com/ar/actualite_auto/%D9%85%D9%88%D8%A7%D8%B5%D9%81%D8%A7%D8%AA_%D8%AC%D8%AF%D9%8A%D8%AF%D8%A9_%D9%84%D9%84%D9%88%D8%AD%D8%A7%D8%AA_%D8%AA%D8%B1%D9%82%D9%8A%D9%85_%D8%A7%D9%84%D9%85%D8%B1%D9%83%D8%A8%D8%A7%D8%AA_%D9%81%D9%8A_%D8%A7%D9%84%D8%AC%D8%B2%D8%A7%D8%A6%D8%B1/18660).

## Requirements and limitations:
- The image needs to be captured with a decent quality ( since we'll be zooming on the plate only ).
- It's made to detect only 1 plate in a picture.
- The plate needs to be a rectangle ( the logic for custom plates with two lines is very different ).
- The plate shouldn't be tilted very much, it's preferable to have it completely horizontal.

## About the dataset:
Most of the images are from this [repo](https://github.com/mouadb0101/License_Plates_of_Algeria_Dataset) and I've added some other public car images found on the internet.

The dataset folder contains 2 subfolders:
* **'yes/'**: contains images of cars that the script can detect their information.
* **'no/'**: on the other hand, the cases where it failed to detect the license plate.

Project idea inspiration from this [video](https://youtu.be/NApYP_5wlKY?si=x1vARYNGgxFETIij).







