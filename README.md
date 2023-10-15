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

<img width="960" alt="image" src="https://github.com/medtaher123/angularPantheraPresentation/assets/56443200/db48a5ab-509b-4e38-9280-c499c723a267">

### Calendar Views
I leveraged Angular's [CalendarComponent](https://mattlewis-github.com/angular-calendar/#/kitchen-sink) and tailored it to Panthera's style and our specific needs. The result is as follows: The calendar offers three primary views: Month View, Week View, and Day View.

#### Month View

  <img width="959" alt="image" src="https://github.com/medtaher123/angularPantheraPresentation/assets/56443200/02975b50-7b79-4899-8ec7-70e8e3c95a77">

#### Week View

<img width="959" alt="image" src="https://github.com/medtaher123/angularPantheraPresentation/assets/56443200/7fe5caa2-6018-4268-b46c-e1a921dd1a51">

#### Day View

<img width="960" alt="image" src="https://github.com/medtaher123/angularPantheraPresentation/assets/56443200/fd27eef1-6b2b-452f-ae25-2baf482b327e">



All three views facilitate event manipulation through drag and drop. A single click on an item opens an event editing page, and a tooltip displays event details.

<img width="809" alt="image" src="https://github.com/medtaher123/angularPantheraPresentation/assets/56443200/8457b4c5-f21b-4cca-9f4e-1ddc444710ca">

### Data Transformation
The transformation from the grid to the calendar works as follows: Each row in the grid is represented by an event in the calendar.
- A column of type String (or int) represents the event's title.
- A column of type Date or Timestamp, or two columns (one Date and one Time) as needed, represents the event's date.
- A column of type Enum specifies the color of the event in various views. These colors are consistent with those in the original grid. 

The choice of columns is customizable by the end user, each user has their own settings.


### Filtered Grids and Copy Functionality
At the bottom of the page, you'll find the original grid filtered for not planned items (with NULL dates). This allows for the simultaneous copying of one or more items to a specific date in the calendar.

<img width="954" alt="image" src="https://github.com/medtaher123/angularPantheraPresentation/assets/56443200/357bfecf-d859-4765-98ca-4a8b51947098">

Another grid appears upon clicking, displaying items for the activated date:

<img width="960" alt="image" src="https://github.com/medtaher123/angularPantheraPresentation/assets/56443200/0d5cd5e9-561f-46d7-8b98-d54d092c85fa">

This grid also enables the copying of one or more items and allows for navigation to another month before pasting, a feature not possible with drag and drop alone.  

### Mobile Version
A simplified mobile version is also available. For the active day, users can switch between a view containing a list of events and a grid.

<img width="167" alt="image" src="https://github.com/medtaher123/angularPantheraPresentation/assets/56443200/7406a07a-7552-4e59-87b4-15e6a22b9e70">
<img width="165" alt="image" src="https://github.com/medtaher123/angularPantheraPresentation/assets/56443200/b7a418d2-5a9f-4017-b68c-a7e23bf4dfb7">
<img width="170" alt="image" src="https://github.com/medtaher123/angularPantheraPresentation/assets/56443200/8421624e-c906-4d37-96b7-8e844bce4edc">
<img width="163" alt="image" src="https://github.com/medtaher123/angularPantheraPresentation/assets/56443200/ce0812c1-0c1b-42d8-a166-1d323f8b6948">

### Dual View
I also developed additional versions that can simplify data manipulation by displaying two views simultaneously, enabling drag and drop between distant dates.

<img width="804" alt="image" src="https://github.com/medtaher123/angularPantheraPresentation/assets/56443200/52dc3851-1bc8-4d7d-b4e4-4759704afe96">
<img width="587" alt="image" src="https://github.com/medtaher123/angularPantheraPresentation/assets/56443200/2e3ffac4-dce3-4acf-97a1-36541f20c488">
<img width="584" alt="image" src="https://github.com/medtaher123/angularPantheraPresentation/assets/56443200/925c4338-bb30-4ba1-a3cb-80d2e7694ec7">
<img width="586" alt="image" src="https://github.com/medtaher123/angularPantheraPresentation/assets/56443200/c995f32c-e2c9-4270-b990-f1aadfc7586a">


