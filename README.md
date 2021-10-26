Nextercise - README Template
===

# APP_NAME_HERE

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
Nextercise is an app that allows users to get recommendations on new exercises they should try. Users can also save the exercises to a list and search for exercises in the database.

### App Evaluation
- **Category:**
    - Fitness/ Exercise
- **Mobile:**
    - App would be mainly mobile as the user could exercise on the go and by following the exercise instructions from their phone screen
- **Story:**
    - Recommends new exercises for the user to try out, hopefully this feature will be more tailored towards individual users' wants and needs, but initially it would be generalized
- **Market:**
    - Any level of people who exercise, targeted towards all levels as exercises will be categorized by difficulty(hopefully)
- **Habit:**
    - Would follow the users exercise routine, being used more frequently by people who are frequently physically active
- **Scope:**
    - Would start with simple exercise searching and evolve hopefully into an AI that can analyze user's profiles and generate recommendations based on a given criterion. 

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

* 1. User can Login
* 2. Users can search for exercises
* 3. Users can save a list of favorite exercises
* 4. Users can see instructions on how to perform the exercises(Hopefully images will be included as well)
* 5. Users are recommended new exercises
* 6. Users can view previously saved lists/ exercises
* 7. Users can Logout
* 8. Users can create an account

**Optional Nice-to-have Stories**

* 1. Users are recommended new exercises based on previouisly saved exercises
* 2. Users are not recommended duplicate exercises
* 3. Users are recommended exercises based on user-provided search criteria
* 4. Users can view videos showcasing how to perform the exercise.

### 2. Screen Archetypes

* Login screen
    * Adresses required story #1. Users can either create an account or input existing credentials to access a pre-existing account.
* User's Home screen
   * Adresses Required stories #6 and #7 and the settings to address nice-to have story #3. Users can view exercises and saved exercise lists. This screen will provide users the ability to change their account settings and how they want to receive exercise recommendations if that story is added.
* Exercise Search Screen
   * Adresses required stories #2 and #3. Users can search exercises by category and name, this screen will feature a search bar and display a list of exercises with an image and description of the exercise.
* App Home Screen
    * Adresses required story #5, and nice to have stories #1, #2, and #3. The app home screen will have the recommended next exercise displayed. generally the plan for navigation between the different screens is a bottom navigation bar that is visible on all screens except the Login screen.
* Individual Exercise Screen
    * Adress required stories #3 and #4, and nice-to-have story #4. User can view a description of the exercise as well as images and videos if these features are implemented. There will be an add button to add the exercise to the users' favorites and then the option to add it to a more specific list. 
* Account Creation
    * Addresses required story #8. This will allow users top create an account.

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* App Home Screen
* Exercise Search Screen
* User Home Screen

**Flow Navigation** (Screen to Screen)

* Forced Login
   * User Logs in -> App Home Screen
* App Home Screen
   * User taps the recommended exercise -> the exercise's Individual Exercise Screen
   
   * User taps the User profile button -> User Home Screen
* Exercise Search Screen
    * User types in work-out name -> User taps the search button -> Matching exercises are displayed -> User taps an exercise -> Individual Exercise Screen
    * User taps the User profile button -> User Home Screen
    * User taps the App Home button -> App Home Screen
* User Home Screen 
    * User types in new account details -> User presses change account info button -> User's info is updated
    * User changes how exercises are recommended -> User presses confirm button -> The criteria for recommending user exercises is updated
    * User taps one of the lists of saved exercises -> User see's all the exercises saved to the selected list.
    * User taps the Exercise Search button -> Exercise Search Screen
    * User taps the App Home button -> App Home Screen
## Wireframes
* Hand-Sketched Wireframes
    * Login, User Home, Exercise Search, and User Home Screen Wireframes
![Login, User Home, Exercise Search, and User Home Screen Wireframes](https://i.imgur.com/BX6z0d6.jpg)
    * Individual Exercise, and Account Creation Screen Wireframes
![Individual Exercise, and Account Creation Screen Wireframes](https://i.imgur.com/PJBVJTb.jpg)
Individual Exercise, and Account Creation Screen Wireframes
    

### [BONUS] Digital Wireframes & Mockups
#### Create Account Digital Wireframe
![Create Account Screen Digital Wireframe](https://i.imgur.com/2ATnxj0.png)
#### Login Screen Digital Wireframe
![Login Screen Digital Wireframe](https://i.imgur.com/ELOzelk.png)
#### App Home Screen Digital Wireframe
![App Home Screen Digital Wireframe](https://i.imgur.com/89DUI0k.png)
#### Exercise Search Screen Digital Wireframe
![Exercise Search Screen Digital Wireframe](https://i.imgur.com/lA46r4B.png)
#### Account Settings Screen Digital Wireframe
![Account Settings Screen Digital Wireframe](https://i.imgur.com/IVMQ4fM.png)
#### Individual Exercise Sceen Digital Wireframe
![Individual Exercise Sceen Digital Wireframe](https://i.imgur.com/vLDQ1Vu.png)

### [BONUS] Interactive Prototype

## Schema 
[This section will be completed in Unit 9]
### Models
[Add table of models]
| Property | Type | Description |
| exerciseId | String | unique id for the exercise object |
| image | File | image of the exercise being performed |
| videoLink | String | link to video of someone performing the exercise |
| category | String | the area the area focuses on |
| user | Pointer to User | user that saves the exercise
| exerciseList | List of Exercises | list of exercises created by the user, likely have a user id atached to each list |
| exercise | New | Specialized type that contains the id, image, video, and category associated with an exercise |
### Networking
- [Add list of network requests by screen ]
- * Home Recommendation Screen
-   * (Update/Put) Update new exercise on home screen for user to try
- * Exercise Search Screen
-   * (GET/ Update) Search and retrieve exercise objects from user parameters, update screen with new results.
- * Profile Screen
-   * (Create/ Post) Create new lists to store exercises.
-   * (Update/ PUT) Edit account credentials.
- [Create basic snippets for each Parse network request]
- [OPTIONAL: List endpoints if using existing API such as Yelp]
