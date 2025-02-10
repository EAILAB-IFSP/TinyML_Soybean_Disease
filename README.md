# TinyML_Soybean_Disease

Intelligent System For Identifying Leaf Diseases In Soybean Crop


The system allows the farmer to take photos from leafs in the soybean crop, register date, time, lat-long coordinates and diagnost result from inference performed by the microcontroller. All data is saved in a SD Card.

Later, when the farmer has computer and internet facilities, he can open Microsoft BI interface, analyse the results of the photos, diagnostics, where the photos were collected in a google earth satelite map, and access information and reports on how to mitigate the disease.

A convolutional neural network (CNN) model was developed on the Edge Impulse platform, achieving an accuracy of 87.7% in classifying five prevalent diseases in Brazil: Target Spot, Asian Rust, Brown Spot, Frog Eye Leaf Spot, Potassium Deficiency, and the Healthy class. The Edge Impulse export the ML model as an Arduino library that can be built as part of the microcontroller code.

Figure below shows the Intelligent System For Identifying Leaf Diseases In Soybean Crop process flow.

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/Flowchart%20of%20Process.png)

Hardware: ESP32-CAM, SD-Card, GPS Receiver model GY-NEO6MV2, 0.96" OLED Display, Liter Energy Battery SD 303040, 3.7V/450mAh

Figure below shows the hardware connection

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/Circuit_of_Hardware.png)

The code is in the file "Source Code.pdf", available in the repository in the link: https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/Source%20Code.pdf

Libraries from Edge Impulse fot the Intelligent System For Identifying Leaf Diseases In Soybean Crop

#include <Soja2024_v1_inferencing.h> // Edge Impulse ML Inferencing System
#include "edge-impulse-sdk/dsp/image/image.hpp"

A case is designed to accommodate the hardware and allow easy use in the field by the farmer. Figure below shows the case and the hardware inside.

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/Prototype%20Case%20in%203D%20Printer.jpg)

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/Prototype_Assembled.png)

Figure below shows the hardware collecting samples of leaves, with date/time/coordinates and diagnostic.

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/Collecting%20Samples.png)

Lter the farmer can analyse the results in a Microsoft BI specially designed for the Intelligent System For Identifying Leaf Diseases In Soybean Crop. Because the intention is to small brazilian farmers, all the screens are in Portuguese language.

Figure below shows the main BI homepage, called "Agro Vision"

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/BI%20Main%20Homepage.png)

With 2 buttons: "Dashboard" for reports and maps and "Cartilhas" (booklet) for disease information and how to mitigate it, from oficial brazilian agro research center, called EMBRAPA.

Clicking on Dashboard...

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/BI%20Dashboard%20page.png)
