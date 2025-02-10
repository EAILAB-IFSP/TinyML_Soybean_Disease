# TinyML_Soybean_Disease

Intelligent System For Identifying Leaf Diseases In Soybean Crop


The system allows the farmer to take photos from leafs in the soybean crop, register date, time, lat-long coordinates and diagnost result from inference performed by the microcontroller. All data is saved in a SD Card.

Later, when the farmer has computer and internet facilities, he can open Microsoft BI interface, analyse the results of the photos, diagnostics, where the photos were collected in a google earth satelite map, and access information and reports on how to mitigate the disease.

A convolutional neural network (CNN) model was developed on the Edge Impulse platform, achieving an accuracy of 87.7% in classifying five prevalent diseases in Brazil: Target Spot (mancha alvo in Portuguese), Asian Rust (ferrugem asiática in Portuguese), Frog Eye Leaf Spot (olho de rã in Portuguese), Potassium Deficiency (deficiência de potássio in Portuguese), and the Healthy (saudável in Portuguese) class. The Edge Impulse export the ML model as an Arduino library that can be built as part of the microcontroller code.

Edge Impulse is available at: https://edgeimpulse.com/. Below is the generic Edge Impulse process to create a ML model for edge devices.

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/Edge%20Impulse%20Flowchart.png)

To build the ML model by Edge Impulse, a dataset of images were used, from 2 souces:

1. Images collected in Tallassee, Alabama-USA in 2020 and 2021 available at https://datadryad.org/stash/dataset/doi:10.5061/dryad.41ns1rnj3, from the article available at: https://doi.org/10.1016/j.compag.2022.107449.
2. Images captured by EMBRAPA, available at https://www.redape.dados.embrapa.br/dataset.xhtml?persistentId=doi%3A10.48432%2FXA1OVL&fileTypeGroupFacet=%22Document%22&fileAccess=Public, from the article available at: https://doi.org/10.1016/j.biosystemseng.2016.03.012.

Figure below shows the Intelligent System For Identifying Leaf Diseases In Soybean Crop process flow.

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/Flowchart%20of%20Process.png)

Hardware: ESP32-CAM, SD-Card, GPS Receiver model GY-NEO6MV2, 0.96" OLED Display, Liter Energy Battery SD 303040, 3.7V/450mAh

Figure below shows the hardware connection.

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

The SD card can be removed from the hardware as in the figure below.

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/SD%20Card%20remotion.png)

The microcontroller generate the images in folders and also generate a sheet in .csv format, called "dados.csv". The files and folders are as the figure below.

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/SD%20Card%20folder%20and%20files%20created.png)

Later the farmer can analyse the results in a Microsoft BI specially designed for the Intelligent System For Identifying Leaf Diseases In Soybean Crop. Because the intention is to small brazilian farmers, all the screens are in Portuguese language.

Figure below shows the main BI homepage, called "Agro Vision"

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/BI%20Main%20Homepage.png)

With 2 buttons: "Dashboard" for reports and maps and "Cartilhas" (booklet) for disease information and how to mitigate it, from oficial brazilian agro research center, called EMBRAPA.

Clicking on Dashboard...

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/BI%20Dashboard%20page.png)

Also, a BI Analysis Report is generated, related to the disease with most incidence during the images collection in the farm.

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/Report.png)

Now, clicking on the "Cartilhas" button...

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/BI%20Cartilhas%20Page.png)

The farmer can access information about soy diseases that occur the most in Brazil. For example, by clicking in the "Mancha Alvo" button (Target Spot Disease), the following page is accessed, with a brief information about the disease. Also, there are 2 buttons below left. First related to indicated products to mitigate the disease. The second is more detailed information related to the disease by the brasilian agro research center EMBRAPA.

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/BI%20Cartilha%20Target%20Spot%20page.png)

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/BI%20Product%20Abacus%20for%20Target%20Spot.png)

The same process for the other diseases.

For Asian Rust (Ferugem Asiática in Portuguese)

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/BI%20Cartilha%20Asian%20Rust%20page.png)

For Potassioum Deficiency (Deficiência de Potássio in Portuguese)

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/BI%20Cartilha%20Potassioum%20Deficiency.png)

and for Frogeye (Olho de Rã in Portuguese)

![image](https://github.com/EAILAB-IFSP/TinyML_Soybean_Disease/blob/main/BI%20Cartilha%20Frogeye%20page.png)



