# Team Green - Plant Monitor

## Vision

At a high-level, our product is a soil sensor that collects data on moisture levels, compares that to a plant API and displays information on the computer about when the plant should be watered. Our product is designed for everyday people who wish to take care of their plants as well as farmers and botanists who need to keep plants healthy for business or research purposes. Our product solves the problem of needing to manually identify moisture levels and other areas of interest in order to get accurate identifications and notifications on plant health.

The field of plant monitoring systems is relatively unexplored in the consumer space, however, there are a few competitors such as the WANFEI Plant Monitor. Our product is novel in the fact that it will utilize a single microcontroller board for entire areas rather than a one to one direct connection from plant to monitor. Additionally, ours will not be tied to a smartphone app and will have direct access to a federal database for more accurate information.

## Software Architecture

The system that we aim to build is very achievable using current technologies, as well as within the twelve week timeframe provided. One of the key pieces to our project is the soil sensor itself, which we believe the best option for us to be a commonly-available capacitive soil moisture sensor, easily intigratable into an Arduino microcontroller. 

There are three major parts to our product's architecture: the soil sensor board, the cloud storage component, and the command-line driver program/user front-end. The board, constantly measuring information about the plants, will upload data to the cloud for long term storage and future analysis. The command-line driver and interface is what the user will use on their desktop computer in order to specific the "profile" of the plant they're cultivating (name, current season, etc.), and where data anaylsis tools will be avaiable for use on data that can be downloaded locally from the cloud.

The majority of the data that we will access/store is data that the soil sensor will take from the plants that it is currently servicing. We plan on storing this data in a cloud-based service so that multiple devices can have access to it. A portion of our project will include some code written in the Arduino programming language, as we are planning on going with the Arduino board architecture to power our soil sensor. The command-line driver and user interface section of the project will be written in C++. We plan to do research on which cloud-based service will fit our needs the best, however, we are leaning towards using Google Firebase in order to store our long term data points for future analysis.

## Challenges and Risks

What is the single most serious challenge you see in developing the product on schedule?
How will you minimize or mitigate the risk?
