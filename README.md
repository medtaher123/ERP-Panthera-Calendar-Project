# ERP Panthera Calendar Project

## Overview
This repository showcases the work I completed during my internship at Softher. The project focused on developing a novel calendar-based representation for ERP Panthera grids using Angular. It aimed to improve data visualization and accessibility for ERP users.

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
[Insert image of the old grid view]

### Calendar Views
I leveraged Angular's CalendarComponent and tailored it to Panthera's style and our specific needs. The result is as follows: The calendar offers three primary views: Month View, Week View, and Day View.

#### Month View
[Insert image of the month view]

#### Week View
[Insert image of the week view]

#### Day View
[Insert image of the day view]

All three views facilitate event manipulation through drag and drop. A single click on an item opens an event editing page, and a tooltip displays event details.
[Insert image of event manipulation]

### Data Transformation
The transformation from the grid to the calendar works as follows: Each row in the grid is represented by an event in the calendar.
- A column of type String (or int) represents the event's title.
- A column of type Date or Timestamp, or two columns (one Date and one Time) as needed, represents the event's date.
- A column of type Enum specifies the color of the event in various views. These colors are consistent with those in the original grid. 
The choice of columns is customizable by the end user, each user has their own settings.
[Insert images of data transformation]

### Filtered Grids and Copy Functionality
At the bottom of the page, you'll find the original grid filtered for not planned items (with NULL dates). This allows for the simultaneous copying of one or more items to a specific date in the calendar.
[Insert image of null grid]
Another grid appears upon clicking, displaying items for the activated date:
[Insert images of day grid]
This grid also enables the copying of one or more items and allows for navigation to another month before pasting, a feature not possible with drag and drop alone.  

### Mobile Version
A simplified mobile version is also available. For the active day, users can switch between a view containing a list of events and a grid.
[Insert images of the mobile version]

### Dual View
I also developed additional versions that can simplify data manipulation by displaying two views simultaneously, enabling drag and drop between distant dates.
[Insert images of dual view]


