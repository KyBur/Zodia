# Zodia

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
Zodia is a dating application that pays special attention to zodiac signs

### App Evaluation
[Evaluation of your app across the following attributes]
- **Category:** Dating/Lifestyle
- **Mobile:** This application will be developed for mobile devices only
- **Story:** Matches individuals who are in the same area, highlighting their zodiac sign, personality, and interests. If two people match, then they can proceed to message eachother within the app.
- **Market:** Dating applications attract millions of users, with mobile dating apps being the largest source of users in this industry. Zodia is the first dating app to focus on the theme of zodiac signs.
- **Habit:** A fun app for those who use dating apps and/or are interested in zodiac signs
- **Scope:** This app focuses on location-based match making where users can choose who they are interested in, and message those with mutual feelings. Users can create their own profile with their pictures, interests, zodiac sign, and more. 

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

* User can login or create accounts with their cell phone number.
* User can manage their profile description and photos.
* User can browse profiles of other users and message them if they match.
* User can send messages to matched users
* Settings page for notifications, account information updating, etc
* User can log out of the app

**Optional Nice-to-have Stories**

* User can attach spotify music interests, instagram posts, etc
* Monetization option for users to get extra matches and features
* User can toggle dark mode
* gifs and photo sharing in messages

### 2. Screen Archetypes

* Register Screen
   * User creates account and fills out information
   * User verifies phone number
* Login Screen
   * User signs in with phone number and password
   * If user forgets their password, they can reset link sent to email
* Profile Screen
    * User can upload photos
    * User can fill in their interests, description, zodiac sign, etc
    * User can choose dating preferences
* Match Screen
    * User can show they are interested in other individuals
    * User can match with other users
    * User can report innapropriate profiles
* Instant Message Screen
    * Users can send messages to other users

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Personal Profile
* User feed
* Message Feed

**Flow Navigation** (Screen to Screen)

* Login -> User Feed
* Register -> Verification & Preferences
* Verification & Preferences -> Create Profile
* Create Profile -> User Feed
* Tab Bar -> User Feed
* Tab Bar -> Settings
* Tab Bar -> Messages

## Wireframes

<img src="https://i.imgur.com/G5OEnhN.jpg" width=600>

## Schema 
### Models
#### Profile

   | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | userID        | String   | unique id for user |
   | name          | String   | name of user |
   | images        | File     | images for users profile |
   | bio           | String   | user description |
   | location      | String   | description of user's city |
   | tags          | String   | tags for user relevancy |
   | zodiacSign    | String   | zodiac sign name |
   | interactions  | List   | List of userIDs that user has already intereacted with |
   | likes         | List   | List of userIDs that user has chosen to match with |

### Networking
#### List of network requests by screen
   - User Feed Screen
      - (Read/GET) Query all profiles in user's area
      - (Create/POST) Add users to interactions list
      - (Create/POST) Add users to likes list

   - Create Direct Message Screen
      - (Create/POST) Create a new conversation with a matched user
   - Profile Screen
      - (Read/GET) Query logged in user object
      - (Update/PUT) Update user profile photos

