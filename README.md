# ERP Panthera Calendar Project

## Overview
This repository showcases the work I completed during my internship at Softher. The project focused on developing a novel calendar-based representation for [ERP Panthera](https://www.panthera.it/) grids using Angular. It aimed to improve data visualization and accessibility for ERP users.

## Demo
A live demo of the project is not available yet.

## Technologies Used
- Angular
- TypeScript
- HTML
- CSS
- Java

## Project Objectives
The primary objective of my internship was to create a new representation of Panthera's ERP grids in the form of a calendar. This calendar would offer a more comprehensive and practical view when handling date-related operations. Users would have the flexibility to switch between the traditional grid view and the new calendar view based on their specific requirements.

## Features
It's crucial to note that the calendar needed to support all entities within Panthera that possess at least one date field. Furthermore, each entity is unique, making it necessary to find a generalized solution.

### Original Grid View

![image](https://github.com/medtaher123/ERP-Panthera-Calendar-Project/assets/56443200/7ab8f586-c50c-4584-8105-95ec027552c0)


### Calendar Views
I leveraged Angular's [CalendarComponent](https://mattlewis-github.com/angular-calendar/#/kitchen-sink) and tailored it to Panthera's style and our specific needs. The result is as follows: The calendar offers three primary views: Month View, Week View, and Day View.

#### Month View

  ![image](https://github.com/medtaher123/ERP-Panthera-Calendar-Project/assets/56443200/1d2df965-a54e-4d9c-9c0a-4c7391dba055)


#### Week View

![image](https://github.com/medtaher123/ERP-Panthera-Calendar-Project/assets/56443200/a7214ba0-1013-4303-a938-b322fb7974c3)


#### Day View

![image](https://github.com/medtaher123/ERP-Panthera-Calendar-Project/assets/56443200/2ca82e72-f08e-4025-8905-71c91cba3f64)




All three views facilitate event manipulation through drag and drop. A single click on an item opens an event editing page, and a tooltip displays event details.

![image](https://github.com/medtaher123/ERP-Panthera-Calendar-Project/assets/56443200/cf53a1d2-cc4a-4595-93ca-1dbde05ac9d8)


### Data Transformation
The transformation from the grid to the calendar works as follows: Each row in the grid is represented by an event in the calendar.
- A column of type String (or int) represents the event's title.
- A column of type Date or Timestamp, or two columns (one Date and one Time) as needed, represents the event's date.
- A column of type Enum specifies the color of the event in various views. These colors are consistent with those in the original grid. 

The choice of columns is customizable by the end user, each user has their own settings.


### Filtered Grids and Copy Functionality
At the bottom of the page, another grid appears upon clicking on a day displaying items for the activated date. This allows for the simultaneous copying of one or more items to a specific date in the calendar.

![image](https://github.com/medtaher123/ERP-Panthera-Calendar-Project/assets/56443200/362e868f-eec8-473f-a23d-fd16efeb76ce)


This grid also enables the copying of one or more items and allows for navigation to another month before pasting, a feature not possible with drag and drop alone.  

### Mobile Version
A simplified mobile version is also available (the style was not updated to the last version). For the active day, users can switch between a view containing a list of events and a grid.

  <img src="https://github.com/medtaher123/ERP-Panthera-Calendar-Project/assets/56443200/b23e8f13-6a04-4db0-aad6-1da2c40bb4be" width="35%"/>
  <img src="https://github.com/medtaher123/ERP-Panthera-Calendar-Project/assets/56443200/452254c5-33db-47bf-a123-3ae81e5e5ad8)" width="35%" /> 



### Dual View
I also developed additional versions that can simplify data manipulation by displaying two views simultaneously, enabling drag and drop between distant dates.

![image](https://github.com/medtaher123/ERP-Panthera-Calendar-Project/assets/56443200/de44c30d-e1da-48a4-9c67-5f6d4debfae4)
![image](https://github.com/medtaher123/ERP-Panthera-Calendar-Project/assets/56443200/c3b5603c-2066-4505-887f-ab8960fb457d)
![image](https://github.com/medtaher123/ERP-Panthera-Calendar-Project/assets/56443200/184f8a0a-3344-4552-9c43-c89bdeb632ec)
![image](https://github.com/medtaher123/ERP-Panthera-Calendar-Project/assets/56443200/cec4f1df-bcfe-43fb-a087-19be687f5666)



