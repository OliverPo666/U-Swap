# U-Swap 

Design Document

Team member:  Oliver Lu   Juan Lopez Rosado

## Introduction  

U-Swap is an app that will offer an innovative yet user friendly experience, to incoming and outgoing students, who need a convenient solution to sell, purchase or auction items. xxx will allow students to purchase furniture, daily necessities, and electronic products from other students. U-Swap will include a simple and secure email verification method, a list of items from the University, a filtering system for specific items, and an option to auction products. 


## Storyboard

[Storyboard](https://projects.invisionapp.com/prototype/Plant-Diary-ck0bict0n005bqh01aaeu8tuu/play/c6560121)

![MyPlantDiaryFirstScreen](https://user-images.githubusercontent.com/2224876/82159850-58f52f80-985f-11ea-8260-b8391f7ae87e.png)

# Requirements

## Requirement 100: Search for Plants

### Scenario  

As a user interested in plants, I want to be able to search plants based on any part of the name: genus, species, cultivar, or common name.

### Dependencies  

Plant search data are available and accessible.

### Assumptions

Scientific names are stated in Latin.  

Common names are stated in English.

### Example  

1.1
**Given** a feed of plant data is available  
**When** I search for “Redbud”  
**Then** I should receive at least one result with these attributes:   
Genus: Cercis  
Species: canadensis  
Common: Eastern Redbud   
1.2  
**Given** a feed of plant data is available  
**When** I search for “Quercus”  
**Then** I should receive at least one result with these attributes:   
Genus: Quercus  
Species: robur  
Common: English Oak  
And I should receive at least one result with these attributes:  
Genus: Quercus  
Species: alba  
Common: White Oak  

1.3  
**Given** a feed of plant data is available  
**When** I search for “sklujapouetllkjsda;u”  
**Then** I should receive zero results (an empty list)  


## Requirement 101: Save Specimen

### Scenario

As a user interested in plants, I want to be able to enter and save details of a specimen: date planted, photos, and locations, so that I can view a history of this plant.  

### Dependencies
Plant search data are available and accessible.  
The device has a camera, and the user has granted access to the camera.  
The device has GPS capabilities, and the user has granted location access.  

## Assumptions  
Scientific names are stated in Latin.  
Common names are stated in English.  
Examples  
1.1  
**Given** a feed of plant data is available  
**Given** GPS details are available  
**When** 
-	Select the plant Asimina triloba  
-	Add notes: “planted by Brandan Jones”  
**Then**  when I navigate to the Specimen History view, I should see at least one Asimina triloba specimen with the notes, “planted by Brandan Jones”  
2.1  
**Given** a feed of plant data is available  
**Given** GPS details are available  
**When**   
-	Select the plant Malus domestica ‘Fuji’  
-	Take a photo of a Fuji apple seedling  
**Then** when I navigate to the Specimen History view, I should see at least one Malus domestica ‘Fuji’ specimen with the a photo of a Fuji apple seedling.  

# Class Diagram


![ClassDiagram](https://user-images.githubusercontent.com/2224876/82159966-05371600-9860-11ea-83dc-f13f4a7e2921.png)


## Class Diagram Description

**MainActivity**:  The first screen the user sees.  This will have a list of specimens, and an option to enter a new specimen.
**SpecimenDetailsActivity**:  A screen that shows details of a specimen.
**RetrofitInstance**: Boostrap class required for Retrofit.
**Plant**: Noun class that represents a plant.
**Specimen**: Noun class that represents a specimen.
**IPlantDAO**: Interface for Retrofit to find and parse Plant JSON.
**ISpecimenDAO**: Interface for Room to persist Specimen data.

# Scrum Roles

DevOps/Product Owner/Scrum Master: Brandan Jones  
Frontend Developer: Brandan Jones  
Integration Developer: Brandan Jones  

# Weekly Meeting

Sunday at 7 PM.  Use this WebEx:

Meeting Information
Meeting link:
https://ucincinnati.webex.com/ucincinnati/j.php?MTID=m4eae59003bb943cc093fcd3f287864db
Meeting number:
616 881 859
