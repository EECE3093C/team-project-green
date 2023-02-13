# Team Green - Plant Monitor

## Vision

At a high-level, our product is a soil sensor that collects data on moisture levels, compares that to a plant API and displays information on the computer about when the plant should be watered. Our product is designed for everyday people who wish to take care of their plants as well as farmers and botanists who need to keep plants healthy for business or research purposes. Our product solves the problem of needing to manually identify moisture levels and other areas of interest in order to get accurate identifications and notifications on plant health.

The field of plant monitoring systems is relatively unexplored in the consumer space, however, there are a few competitors such as the [WANFEI Plant Monitor](https://www.amazon.com/Wanfei-Intelligent-Bluetooth-Fertility-Temperature/dp/B07ZH7FQJ7). Our product is novel in the fact that it will utilize a single microcontroller board for entire areas rather than a one to one direct connection from plant to monitor. Additionally, ours will not be tied to a smartphone app and will have direct access to a federal database for more accurate information.

## Software Architecture

The system that we aim to build is very achievable using current technologies, as well as within the twelve week timeframe provided. One of the key pieces to our project is the soil sensor itself, which we believe the best option for us to be a [commonly-available capacitive soil moisture sensor](https://www.amazon.com/Gikfun-Capacitive-Corrosion-Resistant-Detection/dp/B07H3P1NRM), easily intigratable into an Arduino microcontroller. 

There are three major parts to our product's architecture: the soil sensor board, the cloud storage component, and the command-line driver program/user front-end. The board, constantly measuring information about the plants, will upload data to the cloud for long term storage and future analysis. The command-line driver and interface is what the user will use on their desktop computer in order to specific the "profile" of the plant they're cultivating (name, current season, etc.), and where data anaylsis tools will be avaiable for use on data that can be downloaded locally from the cloud.

The majority of the data that we will access/store is data that the soil sensor will take from the plants that it is currently servicing. We plan on storing this data in a cloud-based service so that multiple devices can have access to it. A portion of our project will include some code written in the [Arduino programming language](https://www.arduino.cc/reference/en/), as we are planning on going with the Arduino board architecture to power our soil sensor. The command-line driver and user interface section of the project will be written in C++. We plan to do research on which cloud-based service will fit our needs the best, however, we are leaning towards using [Google Firebase](https://firebase.google.com/products/firestore) in order to store our long term data points for future analysis.

## Challenges and Risks
The most serious challenge that we see in the development and delivery of this project on schedule is the fact that not many of us on the team have worked with different hardware architectures before, including the Arduino board that we plan on using to act as the soil sensor for our project. 

We plan to mitigate this by using our first development sprint to do extensive research into how the board works, what functions it can provide us, and how we can do basic in and out operations on it before continuing to progress with the project. We want to make sure that we fully understand the hardware that we're working with before moving forward in order to make development run smoothly.

A risk that we've identified in the project is the accuracy of the soil sensor that we're planning on using might be too low to be able to work on a commercial scale as planned. However, we plan to minimize this risk by opting to use a capacitive soil moisture module instead of a resisitve one, which, while slighly more expensive, can lead to more accurate readings and therefore more accurate data as a result.